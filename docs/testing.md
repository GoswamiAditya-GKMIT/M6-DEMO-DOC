# Testing

We have implemented a robust testing strategy with over **120+ automated tests** ensuring the reliability and stability of the TaskVault Backend.

## Coverage
Our testing covers:

- **User Authentication & Management**: Registration, login, JWT handling, and user updates.
- **Task & Subtask Management**: CRUD operations, access controls, and multi-tenant isolation.
- **Organization & Subscription**: Organization creation, life cycle, and payment integration.
- **Serialization Validation and Model Testing**: Cover Serialization and model testing also.

## Tools Used
- **Pytest**: For unit and integration testing.
- **Pytest-Django**: Django-specific testing utilities.
- **Factory Boy**: Used for generating complex database models in an expressive and readable way.
- **Faker**: Integrated with Factory Boy to generate realistic dummy data (names, emails, dates).
- **Pytest-Cov**: Automated coverage reporting.
- **Locust**: For high-concurrency load testing.

## Methodology
- **Modular Test Structure**: Tests are organized by app and function (e.g., `tests/users/views/`, `tests/tasks/serializers/`). This modularity ensures the test suite is easy to navigate and scale.
- **Pytest Fixtures**: Shared setup and teardown logic is maintained in `conftest.py` and `fixtures.py` to minimize code duplication.
- **Mocking & Patching**: We use `pyytest-mock` library to isolate tests from external services like Razorpay and email relays, ensuring tests are deterministic and fast.

## Coverage Report

Then view directly:
- [HTML report](htmlcov/index.html)

<iframe src="../htmlcov/index.html" style="width:100%;height:800px;border:1px solid #ccc"></iframe>
