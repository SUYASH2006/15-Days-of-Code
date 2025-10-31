day 1
   <img width="2874" height="1343" alt="image" src="https://github.com/user-attachments/assets/5d5f8947-4659-4209-8a8e-e1daded73fa7" />

day 2
   <img width="2879" height="1339" alt="image" src="https://github.com/user-attachments/assets/491768d5-a62a-48d6-812d-9a4e43673874" />
   
class Solution {
public:
    int largestRectangleArea(vector<int>& heights) 
    {
        int n=heights.size();
        vector <int> prev,next;
        stack<int>s;
        s.push(-1);
        stack<int>st;
        st.push(-1);
        for(int i=0;i<n;i++)
        {
            while(s.top()!=-1 && heights[s.top()]>=heights[i])
            {
                s.pop();
            }
            prev.push_back(s.top());
            s.push(i);
        }
        for(int i=n-1;i>=0;i--)
        {
            while(st.top()!=-1 && heights[st.top()]>=heights[i])
            {
                st.pop();
            }
            next.push_back(st.top());
            st.push(i);
        }
        reverse(next.begin(),next.end());
        int area=-1;
        for(int i=0;i<n;i++)
        {
            if(next[i]==-1) next[i]=n;
            int a=heights[i]*(next[i]-prev[i]-1);
            area=max(area,a);
        }
        return area;
    }
};


DAY 3
   <img width="2879" height="1347" alt="image" src="https://github.com/user-attachments/assets/587ec407-0d6b-40aa-838a-048b941a826f" />

DAY 4
   <img width="2876" height="1337" alt="image" src="https://github.com/user-attachments/assets/ca9489dc-350d-4d30-8d55-de906a22c811" />
DAY 5

DAY 6

DAY 7

DAY 8
   <img width="2879" height="1344" alt="image" src="https://github.com/user-attachments/assets/0caa9fca-e219-4527-acbb-1d3d5c5cd48e" />
DAY 9
   <img width="2879" height="1349" alt="image" src="https://github.com/user-attachments/assets/f2de482e-ac6c-4353-8267-270c81dddaae" />
DAY 10
   <img width="2879" height="1339" alt="image" src="https://github.com/user-attachments/assets/cad597a9-5965-4781-8bd9-41968d0aaf86" />
DAY 11
   <img width="2877" height="1354" alt="image" src="https://github.com/user-attachments/assets/082541f1-e819-421a-97a1-e4a4a01729e8" />
DAY 12
   
DAY 13
   <img width="2879" height="1332" alt="image" src="https://github.com/user-attachments/assets/92741fc5-3729-4588-8429-1c61b72e153e" />

DAY 14 
   I WAS TRAVELLING.
DAY 15
   I WAS TRAVELLING.








