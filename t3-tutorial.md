https://api.planetscale.com/internal/user

{"id":"507kivka87mw","type":"CurrentUser","display_name":"Gustavo Dias","name":"Gustavo Dias","email":"gustav.almd@gmail.com","unconfirmed_email":null,"avatar_url":"https://app.planetscale.com/gravatar-fallback.png","created_at":"2023-04-06T09:19:14.488Z","updated_at":"2023-04-06T09:19:22.518Z","flags":{"data_imports":"full","deployment_revert_beta":"full","safe_migrations":"full","user_self_delete":"full"},"two_factor_auth_required":false,"two_factor_auth_configured":false,"session_expires_at":null,"session_refresh_url":null,"email_verified":false,"staff":false,"oauth":true,"sso":false,"managed":true,"directory_managed":false,"authenticated_cli":false,"tos":true,"read_only":false,"has_oauth_tokens":false}

___

### Connecting Prisma to [PlanetScale](https://planetscale.com/docs/tutorials/prisma-quickstart)

![[Pasted image 20230406123835.png]]

![[Pasted image 20230406123944.png]]

![[Pasted image 20230406124202.png]]

Visualize 
```bash
npx prisma studio
```

You need to sync the DB with what we have in our schema, create models (provide the format for data).
This tells Prisma to take the current state of things in your schema and set them into the DB:

```bash
npx prisma db push
```

```bash
npx prisma studio 
```

To pick the changes to commit:
```bash
git add -p
```

![[Pasted image 20230406133704.png]]


![[Pasted image 20230406133815.png]]

11:57
___
### [Clerk](https://clerk.com/)

```bash
npm install @clerk/nextjs
```

##### Get api Keys:
https://dashboard.clerk.com/apps/app_2OH4qrPPaamSWamGVBvjMBZlj1T/instances/ins_2OH4qw94hFb8aQChHaBAXzl2Op3/api-keys

![[Pasted image 20230411121834.png]]

Vercel:

### [<ClerkProvider />](https://clerk.com/docs/nextjs/configure-clerkprovider)

Wrappi9ng your app with the core provider means that every component in your app has access to  your authentication.

![[Pasted image 20230411122803.png]]


### [Middleware](https://clerk.com/docs/nextjs/middleware)

Allows you to have auth in every server request by embedding the auth state inside the request itself.
![[Pasted image 20230411125423.png]]