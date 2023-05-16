# CS 131 Spring 2023 - Project Test Cases

Hi 👋 !! This repo contains open-source test cases for the [CS 131 - Spring 2023](https://ucla-cs-131.github.io/spring-23/)'s course-long project: making an interpreter. This should be used in conjunction with the [Project Autograder](https://github.com/UCLA-CS-131/spring-23-autograder). See more 🔎 for setting up the local autograder.

## Usage

After cloning the `spring-23-tests` repository, copy any specific `*.brewin`, `*.exp` and `*.in` files of interest to the appropriate folder: `v1/tests/` or `v1/fails/` (or other version). Ensure you copy all relevant files to the correct version of the project.

## Testing

Complete a **working implementation**  of your interpreter in the respective file `interpreterv1.py`/`interpreterv2.py`/`interpreterv3.py`. Then run the following command:

```sh
$ python3 tester.py 2 # 2 signifies the version of the project
Running 5 tests...
Running v1/tests/test_inputi.brewin...  PASSED
Running v1/tests/test_recursion1.brewin...  PASSED
Running v1/tests/test_set_field.brewin...  PASSED
Running v1/fails/test_if.brewin...  PASSED
Running v1/fails/test_incompat_operands1.brewin...  PASSED
5/5 tests passed.
Total Score:    100.00%
```

The output of this command is **identical to what is visible on Gradescope pre-due date**, and they are the same cases that display on every submission.

## Contributions

Feel free to submit any pull request to this repo 😊. Please make sure your test cases are instructively named like `test_pass_param_between_objects.brewin` AND are tested for accuracy on [Barista](https://barista.fly.dev/). Let me know if there are any inconsistencies with my test cases !!
