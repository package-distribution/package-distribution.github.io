## Package Distribution
Package distriution is an high level system allow the organizations to share the packages at organization level.

### High level system design:
  ![High level](/img/highlevel_design.png)

### User Interactions
only authorized users are able to access the page.
  1) organizational users view the published packages.
  2) Download the packages into their machines.
  3) provide the necessary feedback for individual packages.

  ![User Flow](/img/user_flow.png)
  
### Admin Interactons
Admin is responsible for setting the organizational accounts and providing the necessary rights to the organization users.
  1) Create a sepearate S3 and set the policy to allow only organization specific access.
  2) configuring the signed url times.
  
  ![Admin Flow](/img/admin_flow.png)