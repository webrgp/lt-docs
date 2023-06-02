# Integrated Web Solutions for Language Together

## Introduction

Dative, Inc. has been privileged to work with Language Together on a series of interconnected projects aimed at enhancing their digital presence and providing innovative language learning solutions. This documentation provides a comprehensive overview of these projects, detailing the objectives, technologies used, challenges encountered, and solutions implemented.

### Overview of Dative's Collaboration with Language Together

Language Together is a platform dedicated to making language learning achievable for children. They utilize a unique method called the Spot Color Immersion Method® to teach vocabulary, phrases, and cultural lingo through 10-reader sets.

Dative, Inc. is a web development company that specializes in creating and managing websites that are easy to use and deliver results. Our collaboration with Language Together involved three main projects: the Language Together Website Migration, the Language Together Flashcard App, and the langt.co URL Shortener.

These projects were not only significant in their individual capacities but also as a collective effort to enhance Language Together's digital presence and user experience. Our collaboration was marked by a shared vision for innovative, user-friendly solutions that would make language learning more accessible and enjoyable for children.

### Interrelationship Between the Projects

The three projects were tightly coupled, each one supporting and enhancing the others.

- The Language Together Website Migration involved moving their existing website to a new server and performing updates. This migration laid the groundwork for the other projects, providing a stable and updated platform from which to launch the Flashcard App and the URL Shortener.
- The Language Together Flashcard App was a new product offering from Language Together. The website's CMS was modified to support this app, allowing customers to navigate flashcards online and listen to audio files.
- The langt.co URL Shortener was added to support both the Flashcard App and the website. It helped Language Together create short, manageable URLs for their marketing efforts, improving user experience and tracking capabilities.

In the following sections, we will delve into each project in more detail, exploring the goals, technologies used, infrastructure and architecture, roles and responsibilities, project roadmap, challenges and solutions, and ongoing maintenance and updates.

## 1. Language Together Website Migration

### 1.1 Project Overview

The Language Together Website Migration was the first project we embarked on with Language Together. The primary goal was to provide continued support for their existing website and overcome their inability to update the website due to server and development limitations.

We were able to migrate their existing Craft CMS website from Bluehost to a server better suited to run Craft, and perform some minor updates to the website. This migration was crucial as it laid the groundwork for the subsequent projects.

### 1.2 Goals and Objectives

The main objective of the project was to enhance the performance and reliability of the Language Together website. This involved:

- Migrating the website to a new server that is better suited to run Craft CMS.
- Overcoming server and development limitations that were preventing updates to the website.
- Performing minor updates to the website after the migration.

### 1.3 Technologies Used

The project utilized the following technologies:

- Craft CMS 2.9.2
- PHP 7.4.11
- MySQL 5.7.32
- Nginx 1.18.0

The server hosting Language Together's website was provisioned and managed using Laravel Forge. It was set up on a Digital Ocean Droplet located in Region New York 1, with an IP address of 157.230.179.54. The server is running a LEMP stack on Ubuntu 20.04 (LTS) x64 as the operating system, and had 1 GB of Memory, 1 Intel CPU, and a 25 GB SSD as its hardware configuration. In terms of bandwidth, it has 1 TB Transfer per month.

### 1.4 Infrastructure and Architecture (with Diagram)

The infrastructure and architecture of the project involved a LEMP stack on a Digital Ocean Droplet. The server was provisioned and managed using Laravel Forge. The website was built using Craft CMS, which was hosted on the server.

### 1.5 Role and Responsibilities

As the primary developer for this project, Dative was responsible for:

- DevOps: Setting up and managing the server on Digital Ocean using Laravel Forge.
- Backend Development: Migrating the website and overcoming server and development limitations.
- Frontend Development: Performing minor updates to the website after the migration.
- Project Management: Coordinating the project and communicating with the client.

### 1.6 Project Roadmap

The project was divided into several stages:

- Initial Consultation: Understanding the client's needs and planning the migration.
- Setting Up the Server: Provisioning and managing the server using Laravel Forge.
- Migrating the Website: Transferring the website to the new server and overcoming server and development limitations.
- Testing / QA: Ensuring the website functions correctly on the new server.
- Finalizing Migration: Making the necessary DNS changes to point the domain to the new server.

### 1.7 Challenges and Solutions (with Context)

The main challenge was that the original Craft CMS website wasn't version controlled. We had to manually download the files and database from Bluehost, and then upload them to the new server. We also had to manually update the Craft CMS version to 2.9.2 as well as update the plugins.

The other challenge was that the website was using a custom plugin to manage the various content sections, instead of either built-in Craft CMS features or popular plugins. This made it difficult to migrate the content to the new server.

We overcame these challenges by creating a staging server to test the migration process, and then documenting the process so that we could repeat it on the production server.

Due to the lack on database migrations in Craft CMS 2, we've opt to update the update the production server directly using SSH instead of deploying changes using CI/CD.

### 1.8 Ongoing Maintenance and Updates

We are currently performing ongoing maintenance and updates on the website and the server. This includes regular updates to the Craft CMS and server software, as well as monitoring the server's performance and resolving any issues that arise.

Here's a diagram that illustrates the infrastructure and architecture of the Language Together Website Migration project:

![Language Together Website Migration Infrastructure and Architecture](./images/lt-website-migration-infrastructure-and-architecture.svg)

### 1.9 Craft CMS Configuration

The Language Together website is built on Craft CMS, a flexible and powerful content management system. Here's an overview of the website's configuration:

#### 1.9.1 Craft CMS Version

The website is running on Craft CMS version 2.9.2. This version was chosen for its stability and compatibility with the website's existing plugins and content model. The client opted to not upgrade to Craft 3, and later to not upgrade to Craft 4 (the latest major version), due to the extensive changes required and potential impact on the website's functionality.

#### 1.9.2 Plugins

The website uses a number of plugins to extend the functionality of Craft CMS. These include:

- [Asset Rev](https://github.com/clubstudioltd/craft-asset-rev/tree/v5)
- [Element API](https://github.com/craftcms/element-api/tree/v1)
- [Formerly](https://github.com/enigmadigital/Formerly)
- [Linkit](https://github.com/fruitstudios/linkit)
- Menus (No longer available)
- Redactor Plugins (No longer available)
- [Retour](https://github.com/nystudio107/retour/tree/master)
- [SEOmatic](https://github.com/nystudio107/seomatic/)
- [SafeCraft](https://github.com/quebecstudio/safecraft)
- [Super Table](https://github.com/verbb/super-table/tree/craft-2)
- [Task Manager](https://github.com/boboldehampsink/taskmanager)
- Teacher Site Plugins (No longer available)
- XML Sitemap (No longer available)
- [User Creator](https://github.com/sjelfull/Craft-UserCreator)
- Zip Assets (No longer available)

#### 1.9.3 Content Model

The content model of the website is structured around various sections. These sections include:

- Home (Single): Showcases featured products, and testimonials, providing an engaging introduction to the site.
- About (Single): Presents comprehensive information about Language Together, detailing the company's history, mission, and values.
- Awards (Single): Highlights the accolades and recognition Language Together has received, underscoring its credibility and success.
- Contact (Single): Features a contact form, enabling visitors to easily get in touch with Language Together (Formerly).
- Method (Single): Explains Language Together's unique teaching method, offering insight into its pedagogical approach.
- Research (Single): Recommends valuable articles and books, serving as a resource for those interested in language learning research.
- Teachers (Single): Provides information about Language Together's offerings for teachers, detailing the benefits and features of its products.
- General Pages (Channel): Includes essential pages such as the privacy policy and terms of use, ensuring transparency and trust.
- Listen (Structure): Hosts language audio sets pages, where users can play and listen to audio files.
- Shop (Structure): Displays product pages, providing detailed information about Language Together's products and facilitating online purchases.

Each section is equipped with a unique set of fields, including text fields, rich text fields, and image fields, to facilitate content management and presentation.

To support the Flashcard App, we've integrated two new sections:

- Flashcard Themes (Channel): This section hosts flashcard themes, complete with cards, images, and audio files.
- Flashcard Sets (Channel): Features flashcard language and level sets, each linked to corresponding flashcard themes, offering a structured way to manage language sets.

#### 1.9.4 Assets

The website has several configured asset locations, each serving a specific type of content:

- Photos: This location stores images used across the website, such as those used in blog posts, product pages, and general site content.
- Products: This location is dedicated to images of Language Together's products, providing clear visuals for the Shop section.
- Audio: This location hosts audio files for the Listen and Flashcard Themes sections, offering users aural language learning content.
- Illustrations: This location stores illustrations used across the website, adding a visual element to the language learning experience.
- PDFs: This location contains PDF files, such as downloadable resources and guides.
- Guides: This location is specifically for guide-related assets, providing resources for users to better understand and use Language Together's products.
- Flashcard Assets: This location stores assets specifically for the Flashcard App, including images and audio files associated with flashcard themes and sets.

Each asset location is configured to ensure easy management and optimal performance of the website.

## 2. Language Together Flashcard App

### 2.1 Project Overview

### 2.2 Goals and Objectives

### 2.3 Technologies Used

### 2.4 Infrastructure and Architecture (with Diagram)

### 2.5 Role and Responsibilities

### 2.6 Project Roadmap

### 2.7 Challenges and Solutions (with Context)

### 2.8 Ongoing Maintenance and Updates

## 3. langt.co (URL Shortener)

### 3.1 Project Overview

### 3.2 Goals and Objectives

### 3.3 Technologies Used

### 3.4 Infrastructure and Architecture (with Diagram)

### 3.5 Role and Responsibilities

### 3.6 Project Roadmap

### 3.7 Challenges and Solutions (with Context)

### 3.8 Ongoing Maintenance and Updates

## Conclusion

### Summary of Achievements

### Future Prospects
