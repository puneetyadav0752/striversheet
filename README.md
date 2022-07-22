class Solution {
public:
    void rotate(vector<vector<int>>& matrix) {
        
        // approach 1---brute force approach
        // int n =matrix.size();
        // vector<vector<int>>rotated(n, vector<vector<int>>(n,0));
        // for(int i=0; i<n; i++)
        // {
        //     for(int j=0; j<n; j++)
        //     {
        //         rotated[j][n-i-1]=matrix[i][j];
        //     }
        // }
        // return rotated;
        
        int n = matrix.size();
        for(int i=0; i<n; i++)
        {
            for(int j=0; j<i; j++)
            {
                swap(matrix[i][j], matrix[j][i]);
            }
        }
        
        for(int i=0; i<n; i++){
            reverse(matrix[i].begin(), matrix[i].end());
        }
        
    }
};
