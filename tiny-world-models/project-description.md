This is a learning project to learn world models in the style of André Karpathy, which is project-oriented, vertically deep, and learning fundamentals as you go as needed.

Create a 2D universe: bouncing balls, walls, gravity, friction, collisions, maybe controllable paddles or a small agent. Render it to pixels. Then build models that learn the world from pixels and compare them.

The repo should answer one central question:

What kind of learned representation is best for predicting and planning in a simple physical world?

You then implement several models vertically:

1. Pixel predictor baseline
   CNN encoder-decoder or small video transformer predicts future frames directly.
2. VAE latent dynamics model
   Encode frame → latent vector → predict next latent → decode future frames. This gives you the Ha & Schmidhuber intuition.
3. JEPA-style latent predictor
   Encode context frames, predict future target embeddings, avoid pixel reconstruction. This connects directly to LeCun/V-JEPA.
4. Object-centric model
   Use slots or explicit detected objects. Predict object states and interactions. This connects to Slot Attention and C-SWM.
5. Planner on top
   Give the agent a goal, use the learned model to search possible action sequences, and execute the best one in the real simulator.

This is the best project because it is small enough to finish, but deep enough to teach the whole field: representation learning, latent spaces, video prediction, dynamics, object decomposition, planning, uncertainty, and long-horizon failure.
