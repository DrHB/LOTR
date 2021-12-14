| Task                 | LR                                                                                                                                                                                          | Schedular                                    | Optimzer                    | Regulizer                      | Paper                                   |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|-----------------------------|--------------------------------|-----------------------------------------|
| GPT2                 | max `1.5e-4`,  min  `1e-5`                                                                                                                                                                  | `3K` iterration `warmup`, `297k` `cosine` decay      | `Adam`                        | wd = `0.01`                      | https://arxiv.org/pdf/1909.08053v4.pdf  | 
| BERT                 | max `1.0e-4`,  min  `1e-5`                                                                                                                                                                  | `10k` iteration `warmup`, 2 million `linear` decay | `Adam`                        | wd = `0.01`                    | https://arxiv.org/pdf/1909.08053v4.pdf  |  
| OmniNet              | max `8e−4`                                                                                                                                                                                 | `10k` iteration `warmup`, `linear` decay           | `Adam` (β1 = `0.9`, β2 = `0.999`) |                                | https://arxiv.org/pdf/2103.01075v1.pdf  | 
| Mask2Former          | max `0.0001` A learning rate multiplier of `0.1` is applied to the backbone and we decay the learning rate at `0.9` and `0.95` fractions of the total number of training steps by a factor of 10. |                                              | `AdamW`                       | wd = `0.1`                       | https://arxiv.org/pdf/2112.01527v2.pdf  |  
| CoAtNet              | max - `1e-3` min `1e-5`                                                                                                                                                                       | `10k` step `warmup`, `cosine` decay                | `AdamW`                       | wd = `0.05`, gradinet_clip = `1.0` | https://arxiv.org/pdf/2106.04803v2.pdf  |  
| CoAtNet - FineTuning | max-`5e-5`                                                                                                                                                                                  | None                                         | `AdamW`                       | wd = `1e-8` gradinet_clip = `1.0`  | https://arxiv.org/pdf/2106.04803v2.pdf  |  
