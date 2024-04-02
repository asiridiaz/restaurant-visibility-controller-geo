# Geo based merchant visibility controller for food delivery service

## Overview

This project involved the development of a PHP script for a leading food delivery service in Sri Lanka, specifically designed to manage the dequeueing of food orders within a specified radius around certain locations. The script was developed as a freelancing job and is showcased here to demonstrate the capabilities and technical skills involved in the project.

## Objective

The primary objective of this project was to implement a system that could dynamically control the visibility of food delivery services based on the current demand and surge in orders. This was achieved by assigning control limits to different areas (geo) and adjusting these visibility radius limits based on the number of surging orders in each area. The system also included functionality to manage the visibility of merchants based on these control limits.

## Technologies Used

- **PHP**: The script was written in PHP, utilizing the MySQLi extension for database interactions.
- **MySQL**: The database used for storing and retrieving data related to food orders and merchant visibility.
- **Kafka**: For real-time event publishing and handling, ensuring that changes in merchant visibility are communicated efficiently.
- **Chat**: For sending automated messages and updates to a designated Slack/GoogleChat/Teams group, providing real-time insights into the system's operations.

## Key Features

1. **Dynamic Control Limits**: The script dynamically assigns control limits to different areas based on the surge in orders. This ensures that areas with high demand have their limits adjusted accordingly, while areas with low demand have their limits reduced.

2. **Merchant Visibility Management**: The system manages the visibility of merchants based on the assigned visibility radius limits. Merchants within the visibility radius limits are made visible, while those outside are hidden.

3. **Event Publishing**: Utilizes Kafka for real-time event publishing. This ensures that changes in merchant visibility are communicated efficiently and in real-time.

4. **Chat Integration**: Sends automated messages and updates to a designated Slack/GoogleChat/Teams groups, providing real-time insights into the system's operations.

## Implementation Details

### Database Interactions

The script interacts with two MySQL databases: one for food-related data  and another for the ride-hailing service's data. It performs various SQL queries to fetch and update data related to food orders, merchant visibility, and control limits.

### Control Limit Assignment

The script assigns control limits to different areas based on the surge in orders. It uses SQL queries to fetch the unique geo IDs with surging restaurant counts and assigns control limits based on the number of surging orders in each area.

### Merchant Visibility Management

The script manages the visibility of merchants based on the assigned control limits. It fetches the list of merchants within each geo and updates their visibility status based on the control limits.

### Event Publishing

The script uses Kafka for real-time event publishing. It prepares and publishes events related to merchant visibility changes, ensuring that these changes are communicated efficiently and in real-time.

### Chat Integration

The script sends automated messages and updates to a designated Slack/GoogleChat/Teams groups. These messages provide real-time insights into the system's operations, including the number of merchants controlled and released, and the current control limits for each area.

## Conclusion

This project demonstrates a comprehensive approach to managing the visibility of food delivery services based on current demand. By dynamically adjusting control limits and managing merchant visibility, the system ensures efficient order processing and delivery. The use of Kafka for real-time event publishing and Slack/GoogleChat/Teams for automated updates showcases the project's capability to integrate with modern technologies for efficient communication and real-time insights.

## Future Enhancements

- **Scalability**: The system can be enhanced to handle larger volumes of data and more complex scenarios.
- **User Interface**: Developing a user-friendly interface for managing control limits and monitoring merchant visibility.
- **Performance Optimization**: Optimizing the script for better performance, especially in handling large datasets.
