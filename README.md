
GoLimiter is a Go library designed to control the number of concurrently executing goroutines. This library provides a straightforward way to create a goroutine pool that limits the number of goroutines running at the same time, effectively managing resource use and preventing overload.

## Features

- Create a goroutine pool with a customizable concurrency limit.
- Easy-to-use API for submitting tasks.
- Ability to dynamically adjust the capacity of the goroutine pool.

## Installation

To start using GoLimiter, you need to install it into your Go project. You can do this with the following Go command:

```bash
go get github.com/Yewenyu/GoLimiter
```

Ensure that your Go version is at least 1.11, as GoLimiter uses modules for dependency management.

## Usage

Here is how you can use GoLimiter to manage concurrency in your Go applications:

1. **Import the package**:

   ```go
   import "github.com/Yewenyu/GoLimiter"
   ```

2. **Create a new goroutine pool**:

   ```go
   pool := golimiter.NewGoroutinePool[int](10, func(task int) {
       fmt.Println("Handling task", task)
   })
   ```

   This creates a new pool that can handle up to 10 tasks concurrently.

3. **Submit tasks to the pool**:

   ```go
   for i := 0; i < 50; i++ {
       pool.SubmitTask(i)
   }
   ```

   This submits 50 tasks to the pool, which are processed concurrently by up to 10 goroutines.



## Contributing

Contributions are welcome! If you would like to improve the GoLimiter library, please feel free to fork the repository, make your changes, and submit a pull request.

## License

GoLimiter is released under the MIT License. See the LICENSE file in the repository for more details.
```

This README provides a clear overview of what `GoLimiter` is, how to install it, how to use it in a Go project, and how to contribute to its development. It’s structured to be helpful to users at different levels of familiarity with Go and open source projects. You can now add this README to the root of your project to provide guidance for other developers.