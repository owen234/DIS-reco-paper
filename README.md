# DIS-reco-paper

This contains the code used to train the Deep Neural Networks (DNNs) described in [arXiv:2110.05505](https://arxiv.org/abs/2110.05505).

The DNN is a regression network trained to predict the neutral-current deep inelastic scattering variables Q<sup>2</sup>, y, and x from detector level electron - proton scattering reconstruction variables in the event.  Inputs to the DNN are the scattered electron, the hadronic final state, and photons in the event that may be from QED radiation.  The learning target values of Q<sup>2</sup>, y, and x in the training samples are defined from the generated electron information.  For events with QED radiation, the generated beam electron after initial state radiation or the generated scattered electron before final state radiation is used to calculate the learning targets.  This approach allows the DNN to make optimal use of the available information in the event and largely mitigate the effects of QED radiation. 
