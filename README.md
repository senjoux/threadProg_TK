# threadProg_TK



				Future<Void> createSummary = Executors.newSingleThreadExecutor().submit(new Callable<Void>(){

					@Override
					public Void call() throws Exception {
						addSummary(nextBean, userDetails); // this will be executed in another thread
						return null;
					}});
          
          
          
          
          
          addSummary(some params ...){
            // logic ... etc
          
          }
