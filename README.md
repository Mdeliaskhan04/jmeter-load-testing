# jmeter-load-testing

# Parabank User Registration Load Testing with CI/CD

This project performs **load testing** on the user registration feature of the [Parabank demo app](https://parabank.parasoft.com/parabank/index.htm) using **Apache JMeter**. The tests run automatically on every push or pull request via **GitHub Actions CI/CD**, generating and uploading HTML reports as artifacts.

## Project Structure
.
├── Test Plan.jmx # JMeter test plan for user registration
├── .github/workflows/jmeter.yml # GitHub Actions workflow for CI/CD
├── report/ # Generated HTML report (artifact)
├── results.jtl # JMeter results file
└── README.md # Project documentation

## How It Works

- On push or pull request to `main` branch:
  - Java and JMeter are set up
  - JMeter runs the `Test Plan.jmx` in non-GUI mode
  - HTML report is generated in `report/`
  - Report uploaded as GitHub Actions artifact for download

## Technologies Used

- Apache JMeter  
- GitHub Actions  
- Java 11  
- Ubuntu Runner  

## Usage

1. **Clone the repo:**

git clone https://github.com/Mdeliaskhan04/jmeter-load-testing.git
cd your-repo

Run tests locally (optional):

jmeter -n -t "Test Plan.jmx" -l results.jtl -e -o report

View reports:

After workflow runs, download reports from the Actions > Artifacts tab on GitHub.

#Contact

Feel free to open an issue or contact me for questions or improvements.

If you want, I can customize the GitHub repo URL and other details for you — just sh
