# **簡介**

- 本文將以流程圖 mermaid 語法為例，介紹如何使用 **Mermaid Live Editor**、**Notion** 和 **Diagrams.net (Draw.io)**，將 Mermaid 語法匯出為圖片，輕鬆應用於各種工作場景。

# **前言**

- 在處理流程設計時，Mermaid 語法是一種快速、輕量級的解決方案，可以用簡單的代碼生成高效的圖表。

- 將圖表轉換為圖片檔案是應用於報告、簡報和團隊協作的重要一環。

- 以下文章內容將說明如何用三種工具完成 Mermaid 語法的圖表匯出，並選擇最適合的解決方案。

# 示**範流程圖 mermaid 語法**

```mermaid
flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car] 
```

# **匯出方案與操作步驟**

## **使用官網 Mermaid Live Editor**

- **打開工具**
    - 網址：[Online FlowChart & Diagrams Editor - Mermaid Live Editor](https://mermaid.live/?isPin=false)

- **輸入語法**
    - 在編輯器的左側文本框中粘貼上述語法。

- **預覽與匯出**
    
    - 語法輸入後，右側會即時顯示圖表預覽。
    
    - 點擊右上角的「Download」按鈕，選擇以下格式進行匯出：
        - **支援匯出格式**：PNG、SVG。

- [![](https://remnote-user-data.s3.amazonaws.com/2zKbRbUCi4HLJElgAxgqOy42pEIwvMI9PodUt-E8pEA-13B1ICGh_lcOyE3Jm614Uh1l6VXHsaALcQfj3mebxW4NMtdnOlFxkfjDyN7vD454Ayjw7K9DPqLbcBCpZa9p.png)](https://remnote-user-data.s3.amazonaws.com/2zKbRbUCi4HLJElgAxgqOy42pEIwvMI9PodUt-E8pEA-13B1ICGh_lcOyE3Jm614Uh1l6VXHsaALcQfj3mebxW4NMtdnOlFxkfjDyN7vD454Ayjw7K9DPqLbcBCpZa9p.png)
    

## **在 Notion 中嵌入 Mermaid 語法**

- 可先閱讀 [使用 Notion 和 Mermaid 語法生成流程圖](https://www.tpisoftware.com/tpu/articleDetails/3126?isPin=false)來熟悉基本操作。

- 本文將說明如何將現有 Mermaid 語法嵌入 Notion 並匯出成圖檔。

- **新增 Code Block**
    
    - 在 Notion 中輸入 ，選擇「Code Block」。
        
        /code
        
        - [![](https://remnote-user-data.s3.amazonaws.com/NMF8nflo6xiy5lUb5bvBVUWgvliUiIQAcYGPvIZ9w2uCVesgajFIh5ZPigXTAZTQtq6esTZ1CSV4mBHJglO0Sk7OXnLAQiLGFpzqIg_TkwL2qyPa2Z7OROiuGBfzQNRq.png)](https://remnote-user-data.s3.amazonaws.com/NMF8nflo6xiy5lUb5bvBVUWgvliUiIQAcYGPvIZ9w2uCVesgajFIh5ZPigXTAZTQtq6esTZ1CSV4mBHJglO0Sk7OXnLAQiLGFpzqIg_TkwL2qyPa2Z7OROiuGBfzQNRq.png)
            
    
    - 設定語言為 mermaid

- **輸入語法**
    
    - 將 Mermaid 語法粘貼到 Code Block 中。
    
    - Notion 會自動渲染生成流程圖。
        - [![](https://remnote-user-data.s3.amazonaws.com/Z1noWln4IpEOre7Rtks_aPJoHFSA8kXZOz7i8ESo5g5RKyb3KjJfbS0CTR-jZmd_YKc7ibY1zMGjput9ImQmB1uCe_kbtxONadOuRQPWilRlGZv2JKC-cxOA8kdB1R3y.jpeg)](https://remnote-user-data.s3.amazonaws.com/Z1noWln4IpEOre7Rtks_aPJoHFSA8kXZOz7i8ESo5g5RKyb3KjJfbS0CTR-jZmd_YKc7ibY1zMGjput9ImQmB1uCe_kbtxONadOuRQPWilRlGZv2JKC-cxOA8kdB1R3y.jpeg)
            

- **匯出圖片**
    - Notion 暫無直接匯出流程圖為圖片的功能，可採用以下方法：
        
        - 使用**截圖工具**保存為圖片。
        
        - 或分享 Notion 頁面以供他人查看。

- **支援匯出格式**
    - **間接匯出格式**：PNG（通過截圖保存）。

- **補充：匯出整頁文件**
    
    - 雖然無法直接將 Mermaid 流程圖匯出為圖片，但 Notion 支援以下文件格式：
        
        - PDF
        
        - HTML
        
        - Markdown
    
    - 將 Markdown 上傳至 Git 倉庫後，可使用 GitHub Editor 檢視流程圖。
        
        - [![](https://remnote-user-data.s3.amazonaws.com/J6qDy1jY-CIfPUbjqWkZ90RNt_2uCH34uMH9EKgzAsA8PbQhAX_47fCtgpVGca6JCB4bbQWjjRXwLJIHNebfE-zrYJbHG8lMitNTrgJUO4Omhte52JYJF-w5ZNwbKShu.png)](https://remnote-user-data.s3.amazonaws.com/J6qDy1jY-CIfPUbjqWkZ90RNt_2uCH34uMH9EKgzAsA8PbQhAX_47fCtgpVGca6JCB4bbQWjjRXwLJIHNebfE-zrYJbHG8lMitNTrgJUO4Omhte52JYJF-w5ZNwbKShu.png)
            
        
        - [![](https://remnote-user-data.s3.amazonaws.com/MEWLTseuIRVY4aD_QtbVe3nwnDkAk-WAlakC5dCOlJ2WGFp-sIhNsLI19sXxGCxY54lCB-Q0E8u3Lbbc2mwmo6rrltV7DvVAy07ts_v_FvZYXIsJTOH-GKSlTx-PfWLW.png)](https://remnote-user-data.s3.amazonaws.com/MEWLTseuIRVY4aD_QtbVe3nwnDkAk-WAlakC5dCOlJ2WGFp-sIhNsLI19sXxGCxY54lCB-Q0E8u3Lbbc2mwmo6rrltV7DvVAy07ts_v_FvZYXIsJTOH-GKSlTx-PfWLW.png)
            
    
    - **建議**：使用 Mermaid 語法保存原始碼更方便進行版本控制與變更對比，比僅保存圖片更有優勢。

## **匯入 Diagrams.net (Draw.io)**

- 參考 [Blog - Use Mermaid syntax to create diagrams](https://www.drawio.com/blog/mermaid-diagrams?isPin=false) 的說明了解如何將 Mermaid 語法匯入 draw.io

- **打開工具**
    - 網址：[Flowchart Maker & Online Diagram Software](https://app.diagrams.net/?isPin=false)

- **匯入語法**
    
    - 點擊「Advanced > Mermaid」，在彈出的窗口中貼上 Mermaid語法，點擊「Insert」。
    
    - 系統會渲染出流程圖。
        
        - [![](https://remnote-user-data.s3.amazonaws.com/QPsb7zQNataOJxpohgwUirutuXEiia77tpOg_6fW7IRG82gj1geOnVyLNpqlqZK8rGfoX0GDZMIf3nrb8mK3cbozJq7YJbgMg8JYHECihVTRNcpnDs1rbGEnQrdE4kbw.jpeg)](https://remnote-user-data.s3.amazonaws.com/QPsb7zQNataOJxpohgwUirutuXEiia77tpOg_6fW7IRG82gj1geOnVyLNpqlqZK8rGfoX0GDZMIf3nrb8mK3cbozJq7YJbgMg8JYHECihVTRNcpnDs1rbGEnQrdE4kbw.jpeg)
            
        
        - [![](https://remnote-user-data.s3.amazonaws.com/5Ssnl4a9xAs_FnC4fsN64k-0wpq8pCjTy_Qhrh1KvCcPt7u_-ryOsZRKd7W3qp_ahKchYiy3mMGFsgdfrQbi1p83n3gIB_R3CODgvjn8_Ugq9H7i_LimM1hOriKzSQPz.jpeg)](https://remnote-user-data.s3.amazonaws.com/5Ssnl4a9xAs_FnC4fsN64k-0wpq8pCjTy_Qhrh1KvCcPt7u_-ryOsZRKd7W3qp_ahKchYiy3mMGFsgdfrQbi1p83n3gIB_R3CODgvjn8_Ugq9H7i_LimM1hOriKzSQPz.jpeg)
            

- **調整與匯出**
    
    - 可使用 Draw.io 提供的工具調整字體、顏色和佈局。
    
    - 點擊「 Menu > Exprot as」，選擇以下格式進行匯出：
        - **支援匯出格式**：PNG、JPEG、SVG、PDF、XML。
    
    - [![](https://remnote-user-data.s3.amazonaws.com/raqrr35UMQWZZvQIg58GJOm4lYM9VUk1odTtMpJRPmzffA9KAtHnZWwYAUoEnx2stCy64O4rrZLEj1D-qZf0Vg0cYACt0DvKFw7S3QC81IYLuqWjiZUle-Y_7UNwfutY.jpeg)](https://remnote-user-data.s3.amazonaws.com/raqrr35UMQWZZvQIg58GJOm4lYM9VUk1odTtMpJRPmzffA9KAtHnZWwYAUoEnx2stCy64O4rrZLEj1D-qZf0Vg0cYACt0DvKFw7S3QC81IYLuqWjiZUle-Y_7UNwfutY.jpeg)
        

## **各方案匯出格式對比**

- **Mermaid Live Editor**
    
    - 支援格式: PNG, SVG
    
    - 操作難易度: 簡單
    
    - 適用場合: 快速生成與下載小型圖表

- **Notion**
    
    - 支援格式: PNG（截圖）
    
    - 匯出文件格式: PDF, HTML, Markdown
    
    - 操作難易度: 簡單
    
    - 適用場合: 團隊筆記與共享文檔

- **Diagrams.net (Draw.io)**
    
    - 支援格式: PNG, SVG, PDF
    
    - 操作難易度: 中等
    
    - 適用場合: 調整樣式與匯出多格式圖表

## **總結**

- **快速匯出圖檔**：使用 **Mermaid Live Editor** 是最簡單的選擇。

- **嵌入日常筆記**：**Notion** 適合進行團隊協作與筆記管理，但需要手動截圖匯出圖片。

- **匯出整頁文章**：**Notion** 匯出 Mermaid 語法保存原始碼更方便進行版本控制與變更對比

- **專業調整與多格式輸出**：**Diagrams.net** 提供更多樣化的匯出格式和設計靈活性，適合更複雜的需求。

- 希望這些說明可以協助使用 Mermaid 語法匯出成高品質圖片，靈活應用於不同場景！

## 相關連結

- [Online FlowChart & Diagrams Editor - Mermaid Live Editor](https://mermaid.live/?isPin=false)

- [Blog - Use Mermaid syntax to create diagrams](https://www.drawio.com/blog/mermaid-diagrams?isPin=false)

## 參考來源

- [https://gist.github.com/wanyutang/1c320dfc4bc6419d2ab968b80e812ee4?isPin=false](https://gist.github.com/wanyutang/1c320dfc4bc6419d2ab968b80e812ee4?isPin=false)

- [Mermaid 語法匯出圖檔格式操作說明 - Mermaid Live Editor, Notion, Draw IO](https://www.notion.so/Mermaid-Mermaid-Live-Editor-Notion-Draw-IO-14e76e7a7e838047b54bc6a6a4bf28c7?pvs=21)

## 延申閱讀

- [https://www.tpisoftware.com/tpu/articleDetails/3126?isPin=false](https://www.tpisoftware.com/tpu/articleDetails/3126?isPin=false)