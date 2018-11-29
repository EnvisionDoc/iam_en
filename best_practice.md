# Centralizing authorization by grouping users

You can segregate user groups according to their different job responsibilities within your organization and grant minimum access to users that are just sufficient for them to perform their jobs.

We recommend to create a user group for each identified user role to control access collectively instead of authorizing users individually.

The following are the typical roles in EnOS and the suggested minimum permissions for your reference.

### Edge developer

**Major duties**: Develop edge software and edge configuration center in order to manage the edge gateway.

**Recommended permissions**:
The following services are the minimum required permissions for this role:
- Model
- Edge Gateway
- Device Provisioning

### IoT Engineer

**Major duties**:
- Set up and debug device connections, including creating products and devices, and testing the communication among the devices in the EnOS console.
- On-site installation, including installing the edge gateway devices and connecting the cables between edge gateways and devices.

**Recommended permissions**:
The following services are the minimum required permissions for this role:
- Edge Gateway
- Device Provisioning

### Assets manager

**Major job duties**: Create the asset hierarchy and manage assets based on the business case scanarios. Optionally, might create user accounts for internal and external users, for example, IoT engineer, and manage authorization for the users to do their job around EnOS.

**Recommended permissions**:
The following services are the minimum required permissions for this role:
- Asset Management
- IAM (only when the asset manager is also responsible for user management)

### Application developer

**Major duties**: Develop applications based on the APIs and SDKs provided by EnOS to fulfill the business needs.

**Recommended permissions**:
The following services are the minimum required permissions for this role:
- Application Management
- EnOS APIs
- SDK Center
- Asset Alert


### Data developer and analyst


**Major duties**: missioned with data-driven business analysis, their responsibilities are to:
- Based on the data storage and computing capabilities, use the scheduling workflows to perform data extration, transformation, and loading (ETL).
- Develop data structure and algorithm
- Perform data analysis and data mining
- Design BI reports based on business KPIs to assist business decisions

**Recommended permissions**:
The following services are the minimum required permissions for this role:
- Data IDE
- Data Integration
- Task Monitor
- Data Explorer
- Metadata Management
- BI&Report