# DIS-reco-paper

This contains the code used to train the Deep Neural Networks (DNNs) described in [NIMA 1025 (2022) 166164](https://doi.org/10.1016/j.nima.2021.166164), [arXiv:2110.05505](https://arxiv.org/abs/2110.05505).

The DNN is a regression network trained to predict the neutral-current deep inelastic scattering variables Q<sup>2</sup>, y, and x from detector level electron - proton scattering reconstruction variables in the event.  Inputs to the DNN are the scattered electron, the hadronic final state, and photons in the event that may be from QED radiation.  The learning target values of Q<sup>2</sup>, y, and x in the training samples are defined from the generated electrons, where for events with QED radiation, the generated beam electron after initial state radiation or the generated scattered electron before final state radiation is used to calculate the learning targets.  This approach allows the DNN to make optimal use of the available information in the event and largely mitigate the effects of QED radiation.  For more details, please see our [paper](https://arxiv.org/abs/2110.05505). 

Here are some brief descriptions of what you can find in this repository.

- **NN_athena_reg_v6a.ipynb** :  Jupyter Notebook for running the DNN training using the ATHENA fast simulation.
- **NN_h1_reg_v4c.ipynb** : Jupyter Notebook for running the DNN training using the H1 full simulation.
- **NN_h1_make_dnn_tree_v2.ipynb** : Jupyter Notebook example that reads in the DNN training results and creates a root TTree containing all of the input variables as well as the DNN outputs.

The input files for the training are [ROOT](https://root.cern) files containing a simple TTree that is imported into a Pandas data frame.

The training output for the results shown in the paper is in the **training_*** directories in this repository.
