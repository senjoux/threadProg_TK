# threadProg_TK

## 1.1 Call method in different thread : Normal Java way

```java
Future<Void> createSummary = Executors.newSingleThreadExecutor().submit(new Callable<Void>(){
	@Override
	public Void call() throws Exception {
		addSummary(nextBean, userDetails); // this method will be executed in another thread
		return null;
	}}); addSummary(some params ...){
	// logic ... etc }
```


## 1.2 Call method in different thread : Z2 way 

```java
try {
WorkUnit.work(new Callable<Void>() {
	@Override
	public Void call() throws Exception {
		addSummary(nextBean, userDetails);
		return null;
	}
	});
} catch (Exception e) {
	// TODO Auto-generated catch block
	e.printStackTrace();
}
```
