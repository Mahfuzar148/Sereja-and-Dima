/*# Sereja-and-Dima
codeforces problem*/





Solution:





#include<bits/stdc++.h>
using namespace std;
int main()
{
    ios_base::sync_with_stdio(false);
    cin.tie(NULL);
    cout.tie(NULL);
    int n;
    cin>>n;
    vector<int>v;
    for(int i=0;i<n;i++)
    {
        int a;
        cin>>a;
        v.push_back(a);
    }
    int s=0,d=0,i=0;
    int l =0,f =0;
    while(v.size())
    {

             f = v.front();
             l = v.back();

            if(i%2==0)
            {

                if(f>=l)
                {
                    s = s + f;
                    v.erase(v.begin());
                }
                else
                {
                    s = s + l;
                    v.pop_back();
                }
                i++;
            }
            else
            {

                if(f>=l)
                {
                    d = d + f;
                    v.erase(v.begin());
                }
                else
                {
                    d = d + l;
                    v.pop_back();
                }
                i++;
            }

        }
    cout<<s<<"  "<<d<<endl;
}
