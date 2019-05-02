# Design Amazon Locker 

![Aamzon Locker](https://i.imgur.com/buqwcSo.jpg)

from [Everything you need to know about Amazon Locker](https://www.amazon.com/primeinsider/tips/amazon-locker-qa.html)

## Why?

amazon locker系统，实现一个算法帮助邮递员找到最优的available lockers来投递包裹(因为包裹有不同的尺寸，locker也有不同的尺寸，算法必须能够让尽可能多的package能够被投递到locker)



## What 

- Noun
	- **Locker**: `id`, `size`, `empty`
		- get, set  
	- **Package**: `id`, `size` 	
		- get, set 
	- **Map**: locker ~ package  
- Verb 
	- `search`: get next greater locker for the package 
	- `get`: return the locker id which stores my package   
	- `set`: put packages into lockers 

More:

- get the package and set the locker empty

## Code 

- [Design Amazon Locker](https://repl.it/@WillWang42/design-amazon-locker)

``` java
import java.util.ArrayList;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import java.util.concurrent.locks.Lock;


public class Main {

	public static void main(String[] args){
		Main solution = new Main();
		List<Locker> lockers = new ArrayList<>();
		lockers.add(new Locker(1, 3));
		lockers.add(new Locker(2, 5));
		lockers.add(new Locker(3, 1));
		lockers.add(new Locker(4, 4));
		lockers.add(new Locker(5, 2));

		List<Package> packages = new ArrayList<>();
		packages.add(new Package(1, 2));
		packages.add(new Package(2, 1));
		packages.add(new Package(3, 5));
		packages.add(new Package(4, 3));
		packages.add(new Package(5, 4));

		solution.setPackagesToLokcers(lockers, packages);
		System.out.println();
	}

	Map<Package, Locker> map;
	public Main() {
    map = new HashMap<>();
	}


	public void setPackagesToLokcers(List<Locker> lockers, List<Package> packages) {
		lockers.sort((a, b) -> (a.getSize() - b.getSize()));
		for (Package curPack : packages){
			Locker curLocker = searchFirstGreaterLocker(lockers, curPack);
			if (curLocker != null) {
				map.put(curPack, curLocker);
				curLocker.setLockerStatus(false);
				lockers.remove(curLocker);
			}
			else {
				throw new IllegalArgumentException("No Available Locker!");
			}
		}
    System.out.println(lockers);
    System.out.println(packages);

	}


	public Locker searchFirstGreaterLocker(List<Locker> lockers, Package curPack){
		int left = 0; int right = lockers.size() - 1;
		while (left + 1 < right){
			int mid = left + (right - left) / 2;
			if (lockers.get(mid).getSize() == curPack.getSize()){
				return lockers.get(mid);
			}
			else if (lockers.get(mid).getSize() > curPack.getSize()){
				right = mid - 1;
			}
			else {
				left = mid + 1;
			}
		}

		if (lockers.get(left).getSize() >= curPack.getSize()){
			return lockers.get(left);
		}
		else if(lockers.get(right).getSize() >= curPack.getSize()){
			return lockers.get(right);
		}
		else {
			return null;
		}

	}

	public Locker getPackagePosition(Package myPackage) {
		if (map.containsKey(myPackage.getId())) {
			return map.get(myPackage.getId());
		}
		return null;

	}

	static class Locker {
		private int id;
		private int size;
		private boolean empty = true;

		public Locker(int id, int size) {
			this.id = id;
			this.size = size;
		}

		public void setId(int id){
			this.id = id;
		}

		public int getId() {
			return id;
		}

		public void setSize(int size){
			this.size = size;
		}

		public int getSize() {
			return size;
		}

		public void setLockerStatus(boolean empty){
			this.empty = empty;
		}

		public boolean isEmpty() {
			return empty;
		}
	}

	static class Package {
		private int id;
		private int size;

		public Package(int id, int size){
			this.id = id;
			this.size = size;
		}

		public void setId(int id){
			this.id = id;
		}

		public int getId() {
			return id;
		}

		public void setSize(int size){
			this.size = size;
		}

		public int getSize() {
			return size;
		}
	}
}
```

## More 

- [Amazon Interview Question for Software Engineers](https://www.careercup.com/question?id=5694206820483072)
- [Amazon Interview Question for SDE-2s](https://www.careercup.com/question?id=5719952523788288)