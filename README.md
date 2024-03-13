# Web-App-DevOps-Project

An application allows users to efficiently manage and track orders for a potential business. 

Providing an intuitive user interface for viewing existing orders, and the addition of new orders. 

## Technology Stack

<p align="left"> <a href="https://azure.microsoft.com/en-in/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/microsoft_azure/microsoft_azure-icon.svg" alt="azure" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://flask.palletsprojects.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/pocoo_flask/pocoo_flask-icon.svg" alt="flask" width="40" height="40"/> </a> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://kubernetes.io" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/kubernetes/kubernetes-icon.svg" alt="kubernetes" width="40" height="40"/> </a> <a href="https://www.microsoft.com/en-us/sql-server" target="_blank" rel="noreferrer"> <img src="https://www.svgrepo.com/show/303229/microsoft-sql-server-logo.svg" alt="mssql" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>

- **Backend:** Flask is used to build the backend of the application, handling routing, data processing, and interactions with the database.

- **Frontend:** The user interface is designed using HTML, CSS, and JavaScript to ensure a smooth and intuitive user experience.

- **Database:** The application employs an Azure SQL Database as its database system to store order-related data.

  
## The Scenario 
![Swiftwave Logistics Logo](https://github.com/WayneRose-95/Web-App-DevOps-Project/assets/89411656/534a5e9e-7fca-4dfa-8e57-d2f869402828)

Swiftwave Logistics is a fictional logistics company with over 200+ locations worldwide, specialising in drop shipping. 

Currently, the business has implemented a new Web Application to track new orders from customers. 

This new system has faced many challenges in its implementation

### Challenges 

- The development team work on seperate operating systems: Windows, Mac and Linux. Environments for said operating systems must be configured seperately, and managed for each operating system.
- Changes to code are manually deployed to production via a rigourous process, which is prone to human error. Leading to longer deployment times.
- The business development infrastructure is rigid due to a lack of Infrastucture as Code (IaC) to deploy cloud resources. 

## The Solution

![UML Diagram of Architecture](https://github.com/WayneRose-95/Web-App-DevOps-Project/assets/89411656/1fdfa6f7-1baa-4ac0-8f48-be29011104e3)

The solution is to create an end-to-end CI/CD DevOps Pipeline hosted on Azure; featuring some of the latest technologies in DevOps.  

The environment is built using Terraform. An infrastructure as code (IaC) framework for provisoning the cloud infrastructure used to host the web application. 
Terraform allows for cross-platform portability, automation and ease of use when provisioning cloud services. 

To allow for cross-OS compatibility with the web-app, Docker is used to containerise applications, allowing for developers of different operating systems to run the web application. 

The containerised applications are deployed to the Azure Kubernetes Services (AKS) cluster, which acts as a repository for managing containerised applications. 

Utilizing the Azure DevOps service, release pipelines are orchestrated to automate the building and pushing of docker containers to the AKS cluster, allowing for flexible and seamless transititions between development and deployment of code changes. 

## Getting Started

### Prerequisites

For the application to succesfully run, you need to install the following packages:

- flask (version 2.2.2)
- pyodbc (version 4.0.39)
- SQLAlchemy (version 2.0.21)
- werkzeug (version 2.2.3)

### Usage

To run the application, you simply need to run the `app.py` script in this repository. Once the application starts you should be able to access it locally at `http://127.0.0.1:5000`. Here you will be meet with the following two pages:

1. **Order List Page:** Navigate to the "Order List" page to view all existing orders. Use the pagination controls to navigate between pages.

2. **Add New Order Page:** Click on the "Add New Order" tab to access the order form. Complete all required fields and ensure that your entries meet the specified criteria.
## Features

- **Order List:** View a comprehensive list of orders including details like date UUID, user ID, card number, store code, product code, product quantity, order date, and shipping date.
  
![Screenshot 2023-08-31 at 15 48 48](https://github.com/maya-a-iuga/Web-App-DevOps-Project/assets/104773240/3a3bae88-9224-4755-bf62-567beb7bf692)

- **Pagination:** Easily navigate through multiple pages of orders using the built-in pagination feature.
  
![Screenshot 2023-08-31 at 15 49 08](https://github.com/maya-a-iuga/Web-App-DevOps-Project/assets/104773240/d92a045d-b568-4695-b2b9-986874b4ed5a)

- **Add New Order:** Fill out a user-friendly form to add new orders to the system with necessary information.
  
![Screenshot 2023-08-31 at 15 49 26](https://github.com/maya-a-iuga/Web-App-DevOps-Project/assets/104773240/83236d79-6212-4fc3-afa3-3cee88354b1a)

- **Data Validation:** Ensure data accuracy and completeness with required fields, date restrictions, and card number validation.

## Contributors 

- [Maya Iuga](https://github.com/maya-a-iuga)
- [Wayne Rose](https://github.com/WayneRose-95)


## License

This project is licensed under the MIT License. For more details, refer to the [LICENSE](LICENSE) file.
