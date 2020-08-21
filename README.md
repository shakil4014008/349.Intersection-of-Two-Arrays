# 349.Intersection-of-Two-Arrays

```C#
     public int[] Intersection(int[] nums1, int[] nums2) {
        
         List<int> list = new List<int>();
            Hashtable hash = new Hashtable();
            for(int i=0; i<nums1.Length; i++)
            {
                if(!hash.ContainsKey(nums1[i]))
                    hash.Add(nums1[i],i );
            }
            for(int i=0; i<nums2.Length; i++)
            {
                if (hash.Contains(nums2[i]))
                {
                    list.Add(nums2[i]);
                    hash.Remove(nums2[i]);
                }
            }
            

            return list.ToArray(); 
    }
```

## Complexity Analysis

* Time Complexity: O(N)
* Space Complexity: O(N)
