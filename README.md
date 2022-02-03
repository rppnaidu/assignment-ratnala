# Phani Padmanabha Naidu Ratnala

###### Bhimavaram

Bhimavaram is in the epicentre of the **Godavari delta region**. It is one of the principal trade centres of paddy in the state of Andhra Pradesh. Agriculture-based businesses like food processing, aqua culture, rice mills etc., are the chief sources of the town's revenue. It serves as a distribution centre as well as commercial centre to its hinterland. The town is the regional centre for higher education and is known for its **specialized health services**.It has many major Retail brand shops like KLM, DMart, Coastal city centre etc..,

---
### Ordered List
The distance between Vijayawada Airport to Abhiruchi restaurant is exactly 120kms.
1. After reaching the airport you can travel through either by road or railways.
2. The best way to reach abhiruchi is by road you can refer the directions in google maps and enjoy the travel as sceneries passby.
3. You can find abhiruchi restaurant in the middle of the town,mixed biryani is a must try dish.
4. Your favourite food destination abhiruchi is arrived.

---
### Unordered List
- Fastfood centers near one town police station.
- Bajji mixtures points are famous for their spice and taste.
- Ice creams and tiffins at mid nights with added chutneys.
- Chicken pakodi and salla punukulu near Subbaraidu temple.
- Sri Ramu sweets near sarovar petrol bunk.

[Link for AboutMe](https://github.com/rppnaidu/assignment-ratnala/blob/main/AboutMe.md)


---

Tables

---

Below table provides details about the sports and the price to play the game as a group and also determined locations.

| Game | Location | Price
| --- | --- | ---
| Cricket | Dharmasala | 22 $
| Hockey | Pune | 43 $
| Badminton | Hyderabad | 55 $

---

Pithy Quotes

---

> You can do anything, but not everything

- *David Allen*

> Science and everyday life cannot and should not be separated.

- *Rosalind Franklin*

---

Code Fencing

---

> A minimum spanning tree (MST) or minimum weight spanning tree is a subset of the edges of a connected, edge-weighted undirected graph that connects all the vertices together, without any cycles and with the minimum possible total edge weight.[1] That is, it is a spanning tree whose sum of edge weights is as small as possible.[2] More generally, any edge-weighted undirected graph (not necessarily connected) has a minimum spanning forest, which is a union of the minimum spanning trees for its connected components.

[Click on this for more](https://en.wikipedia.org/wiki/Minimum_spanning_tree)

Code for Minimum Spanning tree

~~~

int n;
vector<vector<int>> adj; // adjacency matrix of graph
const int INF = 1000000000; // weight INF means there is no edge

struct Edge {
    int w = INF, to = -1;
};

void prim() {
    int total_weight = 0;
    vector<bool> selected(n, false);
    vector<Edge> min_e(n);
    min_e[0].w = 0;

    for (int i=0; i<n; ++i) {
        int v = -1;
        for (int j = 0; j < n; ++j) {
            if (!selected[j] && (v == -1 || min_e[j].w < min_e[v].w))
                v = j;
        }

        if (min_e[v].w == INF) {
            cout << "No MST!" << endl;
            exit(0);
        }

        selected[v] = true;
        total_weight += min_e[v].w;
        if (min_e[v].to != -1)
            cout << v << " " << min_e[v].to << endl;

        for (int to = 0; to < n; ++to) {
            if (adj[v][to] < min_e[to].w)
                min_e[to] = {adj[v][to], v};
        }
    }

    cout << total_weight << endl;
}

~~~

[Click here for more on this](https://cp-algorithms.com/graph/mst_prim.html)


