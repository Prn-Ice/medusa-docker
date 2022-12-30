# [Medusa Docker](https://github.com/medusajs/tutorial-template/blob/main/tutorial-link) tutorial codebase.

## Architecture

A medusa store is made up of the following components

- The headless backend
- The admin dashboard
- The storefront

![Medusa Architecture](https://res.cloudinary.com/dza7lstvk/image/upload/v1667999772/Medusa%20Docs/Diagrams/ZHvM2bu_td4rnx.png)
*Image showing medusa architecture, from [here](https://docs.medusajs.com/introduction/#architecture)*

### Headless Backend

This is the main component that holds all the logic and data of the store. Your admin dashboard and storefront interact with the backend to retrieve, create, and modify data through REST APIs.

The backend is a `nodejs` server. In the past, setting up the backend required cloning the base medusa backend from [here](https://github.com/medusajs/medusa-starter-default), installing all the necessary dependencies on your local system, and starting the server by running `medusa develop`.

However, using Docker can simplify this process. With Docker, you only need to update a few configuration files to work with the Docker setup, and you won't need to install any dependencies on your local system.

### Admin dashboard

The admin dashboard is a tool used by store operators to view, create, and modify data such as orders and products. It is built with `gatsbyjs` and can be accessed through a web browser.

Without Docker, setting up the admin dashboard requires cloning the code from [here](https://github.com/medusajs/admin) and installing all the necessary dependencies on your local system. To start the server, run `yarn start`.

### Storefront

Your customers use the Storefront to view products and make orders. Medusa provides two starter storefronts, one built with `gatsbyjs` and one built with `nextjs`. We will be using the `nextjs` storefront in this tutorial, I think it looks better.

The base storefront can be found [here](https://github.com/medusajs/nextjs-starter-medusa) and as you might have guessed we will also be automating starting this up with docker. 