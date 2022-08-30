# Next.js + Builder.io Edge Personalization Demo

This is a fork of [Next.js Commerce](https://github.com/vercel/commerce) with [Builder.io](https://www.builder.io) integrated and using [Edge Middleware](https://vercel.com/docs/concepts/functions/edge-middleware) to personalize pages with great performance.

## Get Started

### Run Locally

After you clone this repo, from the project root:

#### Run the dev server

```bash
yarn # run this command in root folder of the mono repo
yarn dev
```

#### Connect Builder.io

To connect [Builder.io](https://www.builder.io), create a [free account](https://www.builder.io/signup), from your account settings copy your Public API Key and paste it into [site/config/builder.ts](site/config/builder.ts#L6:L6)

<img src="https://cdn.builder.io/api/v1/image/assets%2F1c3b72c36b194b318c40d99ec0a3bf75%2Fafd38ce9af0b4f25988759f8c5936fe5" alt="Screenshot of copying your API key">

#### Set your Preview URL

Next, head to [builder.io/models](https://builder.io/models) and choose the `page` model and enter `http://localhost:3000` as the [preview URL](https://www.builder.io/c/docs/guides/preview-url), and then hit `save` at the top right of the page.

<img src="https://cdn.builder.io/api/v1/image/assets%2F1c3b72c36b194b318c40d99ec0a3bf75%2Fb3bd5b2015e3450985cc69910e368c9d" alt="Screenshot of adding your Preivew URL in Builder.io">

#### Create a page

Now, go to [builder.io/content](https://builder.io/content) and choose the `+ new` button, choose `page`, and drag and drop to create a page on your Next.js site with your React components!

<img src="https://cdn.builder.io/api/v1/image/assets%2F1c3b72c36b194b318c40d99ec0a3bf75%2F4c04f8deda7d4f9d89868323d18d5310" alt="Image of creating a page and editing visually">

> :warning: **If you are having trouble connecting**: be sure you are running your dev server on `http://localhost:3000` by running `yarn dev` from this project root like shown [above](#run-the-dev-server)

### Deploy to Vercel

To get your site live, you can [deploy it to Vercel](https://nextjs.org/learn/basics/deploying-nextjs-app/deploy). Be sure to use the following configuration:

**Framework preset**: Next.js
**Build command**: `cd .. && yarn build`

<img alt="Screenshot of the Vercel configuration" src="https://cdn.builder.io/api/v1/image/assets%2F1c3b72c36b194b318c40d99ec0a3bf75%2F2513e3f0ac804cc2b313a6e6e87876ba">

Once you deploy to vercel, you can update your Preview URL to use the live URL so now others on your team can create content on your new site with Builder.io.

E.g. if your site is now live at `https://my-site.vercel.app`, you can go back to [builder.io/models](https://builder.io/models), choose the `page` model, and update your Preview URL to `https://my-site.vercel.app` and save.

<img alt="Screenshot of updating your Preview URL" src="https://cdn.builder.io/api/v1/image/assets%2F1c3b72c36b194b318c40d99ec0a3bf75%2F09ab3eadebe5453883f77e60c97a9eba">
