# NBA-Player-Clustering 
This project uses unsupervised learning to group NBA players into meaningful archetypes based on advanced stats. Instead of assigning labels manually, the data reveals natural roles that highlight contributions beyond the box score.

Goal
Cluster NBA players into three intuitive roles:
Floor Spacers — perimeter shooters who stretch defenses
Interior Enforcers — bigs who dominate rebounding and shot-blocking
Star Playmakers — high-impact players driving team offense

Methods
We compared multiple unsupervised clustering approaches on PCA-reduced stats:
KMeans + PCA: Baseline method. Best separation at k=2, silhouette ≈ 0.27.
Agglomerative + PCA: Best method. Strongest separation at k=3, silhouette ≈ 0.29. Produced clear, basketball-relevant clusters.
DBSCAN: Tested with min_samples=10, but returned negative silhouette, meaning no meaningful structure.

Results
Cluster 0 – Floor Spacers (n=205): High 3P attempt rates, weaker PER/WS. Examples: Bennedict Mathurin, Andrew Nembhard, Immanuel Quickley.
Cluster 1 – Interior Enforcers (n=40): Elite rebounders and rim protectors. Examples: Jaren Jackson Jr., Jakob Poeltl, Bobby Portis.
Cluster 2 – Star Playmakers (n=26): Elite BPM/VORP players. Examples: Devin Booker, Kawhi Leonard, Anthony Edwards.
👉 Agglomerative Clustering (k=3) was the best-performing model, producing the clearest roles compared to KMeans.

Limitations
Based only on one season — injuries, trades, or coaching can shift roles.
800-minute cutoff and outlier removal are subjective.
PCA simplifies data, which may hide nuances.

Next Steps
Compare across multiple seasons to test role stability.
Add richer features (tracking data, lineup impact, contracts).
Try Gaussian Mixtures or HDBSCAN for more flexible clusters.
Build a dashboard so users can search players and see archetypes.
