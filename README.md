include <iostream.h> #include<conio.h>

#include<stdlib.h>

int con[10][10].1.1.k.n.stk(10).top.v.visit(10), visited(10) int main()

int m:

clrscr):

cout <<"Enter no of vertices:": n>>n;

cout<<"Enter no of edges:";

cin >> m

cout <<"\nEDGES \n":

forik=1; k<=m; k++)

cin >>i>>j: cost[i][j]=1;

cout <<"Enter initial vertex to traverse from:":

an >>v;

cout <<"DFS ORDER OF VISITED VERTICES":

cout << v<<":

visited[v]=1; k=1;

while(k<n)

for(j=n; j>=1: j-)

if(cost(v)[j]!=0 && visited[i]!=18& visit[j]!=1)

visit[j]=1;

stk(top)=j;

top++:

1

v=stk[-top):

cout<<<<":

k++:

Visited(v)=1:

124

Visit(v)=0:

getch)

remum o# website






#include <iostream>
#include <vector>
#include <stack>

using namespace std;

void DFS(vector<vector<int>> &graph, int start, vector<bool> &visited) {
    stack<int> stk;
    stk.push(start);
    visited[start] = true;

    cout << "DFS ORDER OF VISITED VERTICES: ";

    while (!stk.empty()) {
        int v = stk.top();
        stk.pop();
        cout << v << " ";

        for (int i = graph[v].size() - 1; i >= 0; i--) {
            int adj = graph[v][i];
            if (!visited[adj]) {
                stk.push(adj);
                visited[adj] = true;
            }
        }
    }
}

int main() {
    int n, m;

    cout << "Enter the number of vertices: ";
    cin >> n;

    cout << "Enter the number of edges: ";
    cin >> m;

    vector<vector<int>> graph(n + 1);
    vector<bool> visited(n + 1, false);

    cout << "\nEDGES\n";
    for (int k = 0; k < m; k++) {
        int i, j;
        cin >> i >> j;
        graph[i].push_back(j);
        graph[j].push_back(i);  // Assuming it's an undirected graph
    }

    int start;
    cout << "Enter the initial vertex to traverse from: ";
    cin >> start;

    DFS(graph, start, visited);

    return 0;
}
