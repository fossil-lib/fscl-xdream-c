# XDream XTest - *C*

**XDream: An AI-Enhanced Test Library**

*XDream* is a cutting-edge test library developed by Fossil Logic, designed to streamline and enhance the testing process for modern software development. Combining the power of artificial intelligence, multi-threaded execution, rich assertion capabilities, behavior-driven development (BDD), test-driven development (TDD), and a command-line interface (CLI), *XDream* empowers developers to achieve unparalleled efficiency and reliability in their testing workflows.

**Key Features:**

1. **AI Integration:** *XDream* leverages artificial intelligence to intelligently analyze test results, predict potential issues, and provide actionable insights to developers. By continuously learning from test outcomes, it assists in identifying patterns and optimizing testing strategies for enhanced productivity.

2. **Threaded Execution:** With multi-threaded execution support, *XDream* enables parallel testing of multiple scenarios, drastically reducing test execution time. This feature ensures efficient utilization of system resources and faster feedback loops, enhancing the overall testing process.

3. **Rich Assertions:** *XDream* offers a comprehensive suite of assertion functionalities, allowing developers to express complex testing scenarios with ease. Whether it's comparing values, verifying data integrity, or validating system behavior, *XDream* provides a wide range of assertion options to suit diverse testing needs.

4. **Behavior-Driven Development (BDD):** *XDream* promotes collaborative testing practices through BDD, enabling stakeholders to define test cases in a human-readable format. By facilitating clear communication between developers, testers, and other project stakeholders, *XDream* fosters alignment and ensures that tests accurately reflect desired system behavior.

5. **Test-Driven Development (TDD):** With built-in support for TDD methodologies, *XDream* encourages developers to write tests before implementing code, promoting a rigorous and iterative development approach. By writing tests upfront, developers can clarify requirements, identify edge cases, and maintain high code quality throughout the development lifecycle.

6. **Command-Line Interface (CLI):** *XDream* offers a user-friendly CLI interface, allowing developers to interact with the test framework seamlessly from the command line. From running individual test suites to generating detailed test reports, developers can perform various testing tasks efficiently using simple CLI commands.

**Benefits:**

- *XDream* streamlines the testing process, enabling faster feedback cycles and accelerated development workflows.
- By leveraging AI-driven insights, developers can identify potential issues early and proactively address them, minimizing risks and improving software quality.
- The threaded execution feature optimizes resource utilization and reduces overall test execution time, enabling faster time-to-market for software products.
- With support for BDD and TDD methodologies, *XDream* promotes collaboration, clarity, and code quality across development teams.
- The intuitive CLI interface makes it easy for developers to interact with the test framework, facilitating seamless integration into existing development environments.

In summary, *XDream* represents the next generation of test frameworks, combining advanced technologies and best practices to revolutionize software testing and ensure the delivery of high-quality, robust software solutions.

## Who is This For?

This guide is designed for developers of all skill levels who want to use the Meson build system for their projects. It assumes basic familiarity with command-line interfaces and project organization.

## Prerequisites

Before getting started, make sure you have the following installed:

- **Meson Build System**: This project relies on Meson. If you don't have Meson installed, visit the official [Meson website](https://mesonbuild.com/Getting-meson.html) for installation instructions.

## Setting up Meson Build

1. **Install Meson**:
   - Follow the installation instructions on the [Meson website](https://mesonbuild.com/Getting-meson.html) for your operating system.

## Setting up, Compiling, Installing, and Running the Project

1. **Create a Wrap File**:

Create a directory named subprojects in the root directory, next create a file named `tscl-xdream-c.wrap` in the `subprojects` directory of your project with the following content:

   ```ini
   [wrap-git]
   url = https://github.com/fossil-lib/fscl-xdream-c.git
   revision = main
   
   [provide]
   fscl-xdream-c = fscl_xdream_c_dep
   ```

**Integrate Dependency**:
   ```meson
   project('my_project', 'c')

   exe = executable('my_project', 'my_project.c',
       dependencies : dependency('fscl-xdream-c')) # add this line

   test('basic', exe)
   ```

## Including the Demo and Running Tests

To run tests, you can use the following options when configuring the build:

- **Running Tests**: Add `-Dwith_test=enabled` when configuring the build.

Example:

```bash
meson setup builddir -Dwith_test=enabled
```

## Contributing and Support

If you're interested in contributing to this project, encounter any issues, have questions, or would like to provide feedback, don't hesitate to open an issue or visit the [Fossil Logic Docs](https://fossillogic.com/the-docs) for more information.


---

Thank you for choosing this project with the Meson build system. Happy coding and building amazing projects!
