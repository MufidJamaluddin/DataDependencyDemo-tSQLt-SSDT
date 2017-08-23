# DataDependencyDemo-tSQLt-SSDT

A Visual Studio SSDT (SQL Server Data Tools) database unit testing demo using tSQLt to show why data depedency should be prevented while writing a good database unit test.

[comment]: <> ![Screenshot](https://github.com/haroonashraf/BestBooksTDD-SSDT/BestBooksTDD-SSDT-screenshot.png)

## Install

(1) Download the solution and Open in Visual Studio (2015).

(2) Change the connection strings and point them to your local SQL instance.

(3) Compile Solution to see if all works well.

(4) Debug Solution (F5) to run (already written) automated tests followed by deploying changes to debug databases.

(5) Goto Post Deployment script of BestCars_Tests_Dependcy database project and uncomment the following code to see how test fails after just adding one more record when it has data dependency :

/*
-- Step 2 (Uncomment the statement below to run both first and second test which is going to fail due to data dependency)
EXEC tsqlt.RunTestClass @TestClassName = N'MainTests' -- nvarchar(max)
*/


## FAQ

What to do if my automated tSQLt unit tests do not run when I debug my solution?  

Please make sure that you have selected "Multiple startup projects" under Startup Project Properties in Solution settings [comment]: <> ![Screenshot] (https://github.com/haroonashraf/BestBooksTDD-SSDT/BestBooksTDD-SSDT-setup.png)

## Contributing

If you'd like to contribute to this Project, please feel free to let me know.

## License

[MIT License](./LICENSE)