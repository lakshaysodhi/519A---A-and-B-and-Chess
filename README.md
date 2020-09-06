# 519A---A-and-B-and-Chess
#include <bits/stdc++.h>
using namespace std;

int main() {
    int white=0,black=0;
    vector<string> chess(8);
    for(int i=0;i<8;i++){
        cin>>chess[i];
    }

    unordered_map<char,int> weight;
    weight['Q']=9;
    weight['q']=9;
    weight['R']=5;
    weight['r']=5;
    weight['B']=3;
    weight['b']=3;
    weight['N']=3;
    weight['n']=3;
    weight['P']=1;
    weight['p']=1;
    weight['K']=0;
    weight['k']=0;
    for(int i=0;i<8;i++){
        for(int j=0;j<chess[i].size();j++){
            if(chess[i][j]!='.'){
                if(chess[i][j]<=90){
                    white+=weight[chess[i][j]];
                }else {
                    black+=weight[chess[i][j]];
                }

            }
        }
    }
    if(white>black) cout<<"White";
    else if(black>white) cout<<"Black";
    else cout<<"Draw";
}

