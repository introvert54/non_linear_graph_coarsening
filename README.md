# non_linear_graph_coarsening
Worked under our professor to improve upon the work done by him in his research paper, "Featured Graph Coarsening with Similarity Guarantees".
1) Incorporated train-validation-testing split of the dataset to be able to perform testing on benchmark datasets like Cora and Citeseer.
Used masking approach for splitting the graph dataset. why? -> because this makes sure that edges/links between nodes of different splits are maintained. This means that an edge between a node belonging to train set and other node belonging to test set will not be ignored during computations.
2) Added non-linearity in the graph coarsening process to improve accuracy.
For simplicity, i will refer to CXtilde as Y.
So earlier, the code was minimizing the frobenius norm of X-Y.
Now, ReLU activation is introduced here and instead it minimizes the frobenius norm of X-ReLU(Y).
To achieve this optimization, the derivative term of this norm was updated as required.
As a result, the accuracy improved by 5-7% on benchamrk datasets like Cora and Citeseer.
3) Performed hyperparameter-tuning using grid search to find out the hyperparameters that resulted in the best results.
