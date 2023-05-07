# CS 131 Spring 2023 - Project Test Cases

Hi 👋 !! This repo contains open-source test cases for the [CS 131 - Spring 2023](https://ucla-cs-131.github.io/spring-23/)'s course-long project: making an interpreter. This should be used in conjunction with the [Project Autograder](https://github.com/UCLA-CS-131/spring-23-autograder). See more 🔎 for setting up the local autograder.

## Usage

Within your `spring-23-autograder`, copy any specific `*.brewin`, `*.exp` and `*.in` files of interest to the appropriate folder: `v1/tests/` or `v1/fails/` (or other version). Ensure you copy all relevant files to the correct version of the project.

Then in `tester.py`, insert the name of your test case in the `generate_test_suite_v1()` function. Place them appropriately to test for correctness or incorrectness.

```python
def generate_test_suite_v1():
    """wrapper for generate_test_suite for v1"""
    return __generate_test_suite(
        1,
        # insert all CORRECTNESS test cases here
        ["test_case_pass_1", "test_case_pass_2", "test_case_pass_3"],
        # insert all INCORRECTNESS test cases here
        ["test_case_fail_1", "test_case_fail_2", "test_case_fail_3"],
    )
```

## Testing

Place a **working implementation**  of your `interpreterv1.py`/`interpreterv2.py`/`interpreterv3.py` that implements the `Interpreter` class in the same directory as `tester.py`.

```sh
$ python3 tester.py 1 # 1 signifies the version of the project
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

Feel free to submit any pull request to this repo 😊. Please make sure your test cases are instructively named like `test_pass_param_between_objects.brewin` AND are tested for accuracy on [Barista](https://barista.fly.dev/). For future project, I am thinking of sorting test cases by implementation categories so that the file structure should look something like

```bash
├── v1
│   ├── fails
│   │   ├── incompatible-types
│   │   │   ├── test_incompatible_type_1.brewin
│   │   │   ├── test_incompatible_type_1.exp
│   │   │   ├── test_incompat_operands_1.brewin
│   │   │   ├── test_incompat_operands_1.exp
│   │   ├── invalid-expression
│   │   │   ├── test_duplicate_field.brewin
│   │   │   ├── test_duplicate_field.exp
│   │   │   ├── test_duplicate_class.brewin
│   │   │   ├── test_duplicate_class.exp
...
│   ├── tests
│   │   ├── instantiating-objects
│   │   │   ├── instantiating-objects_1.brewin
│   │   │   ├── instantiating-objects_1.exp
│   │   ├── call-stack
│   │   │   ├── test_return_call_1.brewin
│   │   │   ├── instantiating-test_return_call_1.exp
...
├── v2
│   ├── fails
│   ├── tests
...
```
