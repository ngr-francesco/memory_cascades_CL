# memory_cascades_CL
Using cascade model of memory consolidation for Continual Learning

This jupyter notebook contains a variation of the code used in the paper: [Continual Learning with Memory Cascades](https://openreview.net/pdf?id=E1xIZf0E7qr)
The idea is to use the Cascade Model for synaptic consolidation developed by Benna and Fusi in DNNs and hope that somehow the idea could translate well into continual learning problems.
This version is updated and corrected to account for some miscalculations that were used in that paper. 

The results don't look so good, and this method generally seems to not be immediately applicable
to continual learning for DNNs. The reasons I found for this problem is essentially this:
Using backprop, weight modifications are highly correlated and not uniformly distributed, 
this means that there is no real noise in the network that you have to dampen to keep your
memory signal as strong as possible. So what ends up happening is that instead of helping with 
memory consolidation through filtering of background noise, the system just tends to exhibit a 
larger resistance to learning and performance simply degrades over time. 
A more accurate report on these features is described in the report 'cascade-model-report' present in this repo.