# RFM

Customers segmentation by:
  - **recency**
  - **frequency**
  - **monetary**
 
 Used 111 to 444 scores.
 
 Segmenting customers into:
   - champions
   - loyal customers
   - new customers
   - promising
   - need attention
   - about to sleep
   - at risk
   - can't lose them
   - hibernating
   - lost.
 
  *CASE WHEN (r_score = 4 AND f_score = 4 AND m_score = 4) <br>
    THEN 'Champions' <br>
    --Customers who bought most recently, most often and spend the most        
    WHEN rfm_score IN ('334', '342', '343', '344', '433', '434', '443') <br>
    THEN 'Loyal Customers' <br>
       --Customers who bought most frequently and recently        
    WHEN rfm_score IN ('332','333','341','412','413','414','431','432','441','442','421','422','423','424')<br>
    THEN 'Potential to Loyal'        
    WHEN rfm_score IN ('411')<br>
    THEN 'New Customers' <br>
    WHEN rfm_score IN ('311','312','313','331')<br>
    THEN 'Promising'<br>
    WHEN rfm_score IN ('212','213','214','231','232','233','241','314','321','322','323','324')<br>
    THEN 'Need Attention' <br>
      -- haven't bought for a while and made only one or few orders          
    WHEN rfm_score IN ('211')<br>
    THEN 'About to sleep' <br>
      --Customers who didn't buy for a while and were not very active before        
    WHEN rfm_score IN ('112','113','114','131','132','133','142','124','123','122','121','224','223','222','221')<br>
    THEN 'At risk'       
    WHEN rfm_score IN ('134','143','144','234','242','243','244')<br>
    THEN 'Cant lose them'<br>
    WHEN  rfm_score IN ('141')<br>
    THEN 'Hibernating'   
    WHEN  rfm_score IN ('111')<br>
    THEN 'Lost'<br>*
    
Data visualized using Google Looker Studio. 
Buuble chart is showing customer recency (X-axis), frequency (Y-axis) and monetary (bubble size).
    

![rfm1](https://user-images.githubusercontent.com/117217908/231402744-ef907e0a-1464-4c55-8c42-ac29275e8f4e.JPG)

