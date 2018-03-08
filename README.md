#include <bits/stdc++.h>

using namespace std;

int main()
{

    
    int n,p,sum=0;
    int arr[1005];
    int t;
    cin>>t;
    while(t--)
    {
        bool check=false;
        cin>>n>>p;
        for(int i=0; i<p; i++)
        {
            cin>>arr[i];
        }
        for(int j=0; j<(1<<p); j++)
        {
            sum=0;
            for(int k=0; k<p; k++)
            {
                 if(j&(1<<k))
                sum+=arr[k];
            }
       if(sum==n)
            check=true;
        }

        if(check)
            cout<<"YES"<<endl;
        else
            cout<<"NO"<<endl;
    }
    return 0;
}
