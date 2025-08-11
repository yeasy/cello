# Lesson 2: Server

By the end of this lesson, you'll be able to set up a *Hyperledger Cello* server on your computer.

## Dashboard
First, we'll need a dashboard for our server, which is the UI for us.
To do that, we have to build its image first by running:

```bash
make dashboard
```

The image will be tagged as `hyperledger/cello-dashboard:latest`.

This step can take a while because it builds the `node_module` via `yarn install`.

## Database
We'll directly use the official PostgreSQL image as our database, so there is no need to build another one.

## API Engine
Next, we'll build the center of our *Hyperledger Cello* server, which is the *api engine*.

```bash
make api-engine
```

The image will be tagged as `hyperledger/cello-api-engine:latest`.

This step can take a while because it has to install all the dependencies needed for the engine.

## Start the Server

Finally, we can start the server by:

```bash
make server
```

## Conclusion
That's it! You have successfully run a *Hyperledger Cello* server on your computer.

In the next lesson, we'll talk about how you can run an agent for it.

See you then!

## P.S. The "Quickstart" Way
Alternatively, you can run
```bash
make local
```

to set up a *Hyperledger Cello* server and agent as quick as possible.

However, in order to give you a deeper understanding of how everything works, 
we instead walked through the entire setup step-by-step in this lesson above.
