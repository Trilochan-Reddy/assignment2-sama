# assignment2-sama
Assignment2
# Trilochan Reddy Sama
###### Manchi Baphe
This is a **unique and different place** for Buffet . We liked the food and it has a lot of varieties of food right for starters,  **maincourse** and even for deserts. There is a live kitchen that serves you special delicacy of the day tif you wish to eat.

---
# Direction to Manchi Baphe

Nearest airport to Manchi Baphe is RGIA
1. Come to the enterance and walk stright taking right from the enterance.
2. continue walking untill you reach Y-junction.
3. Take left and walk for 5 minutes.
4. then you will reach a building with name SAMA Nilayam
5. Opposite to that you will find Manchi Baphe

* Chicken Biryani
* Chicken Tikka
* prawns Biryani
* Apollo Fish
---

![link to aboutme.md](https://github.com/Trilochan-Reddy/assignment2-sama/blob/main/AboutMe.md)

---
# Recomended sports/Activities
Table below shows my recomended sports or activities to someone who are interested in sports.<br>In the 1st column i tells about sports,second column location and in third column amount one can buy personal things to play game

| Sports name | Location | Amount |
|:---         |:---      |:---    |
| Cricket      | cricket ground | 200$,ball,bat,gaurd |
| Basketball | basketball court | 150$,ball,gaurd |
| volley ball | volleyball court | 50$,teeshirt |
| Table tennis | TT board | 100$,ball,bat |
---

---
# pithy Quote
> It is during our darkest moments that we must focus to see the light.- *Aristotle*
>
> Whoever makes happy will make others happy too.- *Anne Frank*
---

---
# code fencing

>A matching in a Bipartite Graph is a set of the edges chosen in such a way that no two edges share an endpoint. A maximum matching is a matching of maximum size (maximum number of edges). In a maximum matching, if any edge is added to it, it is no longer a matching. There can be more than one maximum matchings for a given Bipartite Graph. 

<https://www.geeksforgeeks.org/maximum-bipartite-matching/>

```
int n, k;
vector<vector<int>> g;
vector<int> mt;
vector<bool> used;

bool try_kuhn(int v) {
    if (used[v])
        return false;
    used[v] = true;
    for (int to : g[v]) {
        if (mt[to] == -1 || try_kuhn(mt[to])) {
            mt[to] = v;
            return true;
        }
    }
    return false;
}

int main() {
    //... reading the graph ...

    mt.assign(k, -1);
    for (int v = 0; v < n; ++v) {
        used.assign(n, false);
        try_kuhn(v);
    }

    for (int i = 0; i < k; ++i)
        if (mt[i] != -1)
            printf("%d %d\n", mt[i] + 1, i + 1);
}
```
<https://cp-algorithms.com/graph/kuhn_maximum_bipartite_matching.html>
---

