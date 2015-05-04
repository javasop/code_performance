## Benchmark

* Used to measure and report time used to execute Ruby code
* part of Standard Library (must be required)
* set a variable to run code a certain number of times (x = 1_000_000)


#### Benchmark.bm
```ruby
Benchmark.bm do |performance|
  performance.report('thing1') { 
    # your code here
  }

  performance.report('thing2') { 
    # your code here
  }
  ...
end
```


#### Benchmark.bmbm
The times may vary dramatically between running Benchmark.bm. In an attempt to standardize benchmark times,
Benchmark.bmbm runs a "rehearsal", then runs GC.start, then runs the real thing.

```ruby
Benchmark.bmbm do |performance|
  performance.report('thing1') { 
    # your code here
  }

  performance.report('thing2') { 
    # your code here
  }
  ...
end
```


#### Output
* Real time is the amount of time that a stopwatch or clock would measure between the start and end of process. 
* User time is the time spent on running code that the user typed.
* System time is the time spent on running system instructions.
* Total time is User + System time.


#### Benchmark Exercises
* Loops
* Combining Strings
* Array Methods
* Destructive vs. Non-Destructive Methods
* Variable assignment
* Accessing data with attr_reader vs. instance variable
* Reading data from file vs. reading data from memory
* Conditional vs. Rescue