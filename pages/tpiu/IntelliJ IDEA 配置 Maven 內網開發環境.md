# **簡介**

本文介紹了如何完成內網 Maven Repository 的設置，確保開發環境可在無網路的情況下正常運行。

# **前言**

在企業內網環境中，無法連接外網時，配置與下載 Maven 依賴是一項挑戰。為了解決此問題，本文說明如何將專案所需的 Maven Repository 傳輸至內網，並透過 IDE 設定離線開發環境，確保開發過程順利進行，即使沒有網路，也能完成 Maven 依賴管理、建置與編譯。

# **取得 Spring Boot 專案範本檔案**

前往 [Spring Initializr](https://start.spring.io/) 下載 Spring Boot 專案範本。

[![](https://remnote-user-data.s3.amazonaws.com/mWnhKwZgisY64bGjuWSyFdFHSOSU-X48szsFD8APUAmy6FK1Xp5rbcJ8qwhA7-tasMcEzMRtZ09v7ycUgySwZ8Uue_QYmKVgX58m11G5XScswb-TNhkQ6MX2KcJSrNIl.jpeg)](https://remnote-user-data.s3.amazonaws.com/mWnhKwZgisY64bGjuWSyFdFHSOSU-X48szsFD8APUAmy6FK1Xp5rbcJ8qwhA7-tasMcEzMRtZ09v7ycUgySwZ8Uue_QYmKVgX58m11G5XScswb-TNhkQ6MX2KcJSrNIl.jpeg)

將下載的壓縮檔解壓，獲取 Maven 專案結構。

[![](https://remnote-user-data.s3.amazonaws.com/V7y7bshVa5gkZ9q886V3m-nEpeIfcKFpCvSDOe-stx3dWB2SMflWitgXlWECjeua1EJPB7U8QU_fmoyMTJYIRsJeAZ3mtTtyHqfT5xFj71wjEd7bBKD3RJtnoKrwpegP.jpeg)](https://remnote-user-data.s3.amazonaws.com/V7y7bshVa5gkZ9q886V3m-nEpeIfcKFpCvSDOe-stx3dWB2SMflWitgXlWECjeua1EJPB7U8QU_fmoyMTJYIRsJeAZ3mtTtyHqfT5xFj71wjEd7bBKD3RJtnoKrwpegP.jpeg)

# **使用 IntelliJ IDEA 開啟專案**

開啟專案後，IntelliJ IDEA 會自動偵測到 Maven 專案，並啟用 Maven 工具面板供操作。

[![](https://remnote-user-data.s3.amazonaws.com/lmimkyS4nbpF0GOGrtovsuYKj9hnATncDXfto-yxVQjmLZR60eqYsZbdG0rbnlvcga_95G7m-4HkRee2FEpV2OT7pH7hl6qtPRFqV_g1JO1vxMXxRfxCA32hNGmRVkCy.jpeg)](https://remnote-user-data.s3.amazonaws.com/lmimkyS4nbpF0GOGrtovsuYKj9hnATncDXfto-yxVQjmLZR60eqYsZbdG0rbnlvcga_95G7m-4HkRee2FEpV2OT7pH7hl6qtPRFqV_g1JO1vxMXxRfxCA32hNGmRVkCy.jpeg)

進入 Settings > Build, Execution, Deployment > Maven，檢視預設的 Maven home 路徑指向 IDE 內建的 Maven。

[![](https://remnote-user-data.s3.amazonaws.com/khusC0O-gaFSuqg4DmiTLzkz0njB2FPo88pHOFA11UVV6u1Kq_VDLHpwyxuoNTjh4pQipRbFWZYmyauKO3wayrQL2MGiu-IPiIAQB6yF3wFHQQCroS0T-Y8PwR08LC2v.jpeg)](https://remnote-user-data.s3.amazonaws.com/khusC0O-gaFSuqg4DmiTLzkz0njB2FPo88pHOFA11UVV6u1Kq_VDLHpwyxuoNTjh4pQipRbFWZYmyauKO3wayrQL2MGiu-IPiIAQB6yF3wFHQQCroS0T-Y8PwR08LC2v.jpeg)

而 User settings 則預設指向本地的 .m2/settings.xml。

[![](https://remnote-user-data.s3.amazonaws.com/klYfvu2Nvl-BJhNZtEuR6iLo2odxE_bo2TfVb3yjuBR-Yu9dc6hd42KRBiaGYXPai1BsHOcvNydwdaKIF0qHwJr6mH3KP1aDGcA_iyBqpFIdPy89XSPuQ7p6vafhk4pG.jpeg)](https://remnote-user-data.s3.amazonaws.com/klYfvu2Nvl-BJhNZtEuR6iLo2odxE_bo2TfVb3yjuBR-Yu9dc6hd42KRBiaGYXPai1BsHOcvNydwdaKIF0qHwJr6mH3KP1aDGcA_iyBqpFIdPy89XSPuQ7p6vafhk4pG.jpeg)

本地 Maven 依賴的存放位置，預設位於 .m2/repository 資料夾中。

[![](https://remnote-user-data.s3.amazonaws.com/50DmsNRZkgOf-EDIjdxpJceUaYlGAVKbgZ5bBhQ26MyPGBuxpTbBzrJv9Bwib3hgWdlmWKcuMDfXf2SzEoZYdPoO_J6noIGnerxLmWxk3OE4uT5K-t1Udctp7TzC5nmq.jpeg)](https://remnote-user-data.s3.amazonaws.com/50DmsNRZkgOf-EDIjdxpJceUaYlGAVKbgZ5bBhQ26MyPGBuxpTbBzrJv9Bwib3hgWdlmWKcuMDfXf2SzEoZYdPoO_J6noIGnerxLmWxk3OE4uT5K-t1Udctp7TzC5nmq.jpeg)

專案下 .mvn/wrapper/maven-wrapper.properties有提供 maven 下載的連結可以取得 apache-maven-XXXX-bin.zip

[![](https://remnote-user-data.s3.amazonaws.com/vbtLkV8uIXmVZda-xXDf2uznCDTa4WoGX93UnHHy9hZLkTCLvnGMOOlrKZ8u08Y1e8BcPjrjTXdyk_CUBtiI_E0WRjiR1eEZugngE1mMqGXR2QwJvtrb-hS_-8VsTQYH.jpeg)](https://remnote-user-data.s3.amazonaws.com/vbtLkV8uIXmVZda-xXDf2uznCDTa4WoGX93UnHHy9hZLkTCLvnGMOOlrKZ8u08Y1e8BcPjrjTXdyk_CUBtiI_E0WRjiR1eEZugngE1mMqGXR2QwJvtrb-hS_-8VsTQYH.jpeg)

根據 Maven 官方連結進行手動下載。

[![](https://remnote-user-data.s3.amazonaws.com/TCebwjlVhvALVo5hQwoV2ZZOsfNSUeaa6Y70zGGvzW4l-sRMCvvPD0PVJGla-ZIj0uMrx9yUQJJQ52AJElLdFU8tOLYoNv-gEE1hQLS9tVWzc0apdvvPFNDcbxMSiLrI.jpeg)](https://remnote-user-data.s3.amazonaws.com/TCebwjlVhvALVo5hQwoV2ZZOsfNSUeaa6Y70zGGvzW4l-sRMCvvPD0PVJGla-ZIj0uMrx9yUQJJQ52AJElLdFU8tOLYoNv-gEE1hQLS9tVWzc0apdvvPFNDcbxMSiLrI.jpeg)

將下載的 Maven 壓縮檔解壓後，移至專案根目錄，並重新命名為 maven。

[![](https://remnote-user-data.s3.amazonaws.com/deW9119j4TlcD00yzCmG_i9hIxwOnLQ-gIhrfpqj13_5l5zmY5qAu6i7FgUWo_XSFCqbgRGAdKlRBbFJYZL4RUkpscqdgqyKfP0KRXAdxSweDLQQSXtK8eF7Zaz0ufR1.jpeg)](https://remnote-user-data.s3.amazonaws.com/deW9119j4TlcD00yzCmG_i9hIxwOnLQ-gIhrfpqj13_5l5zmY5qAu6i7FgUWo_XSFCqbgRGAdKlRBbFJYZL4RUkpscqdgqyKfP0KRXAdxSweDLQQSXtK8eF7Zaz0ufR1.jpeg)

[![](https://remnote-user-data.s3.amazonaws.com/QP5vqCNkTEKGlwxHhU52C_S0JFagDJHm49rNY8Ehq3KxXC6qgA9nftxhlua3RHtWAGSoGVPyZlg7txcGA6mS9u_rb4iXZrBImQLX1uD2saJe9EGA2amjWw75Xh6lacBC.jpeg)](https://remnote-user-data.s3.amazonaws.com/QP5vqCNkTEKGlwxHhU52C_S0JFagDJHm49rNY8Ehq3KxXC6qgA9nftxhlua3RHtWAGSoGVPyZlg7txcGA6mS9u_rb4iXZrBImQLX1uD2saJe9EGA2amjWw75Xh6lacBC.jpeg)

開啟 ./maven/conf/settings.xml，設定 localRepository 指向專案內的 repository 資料夾。

[![](https://remnote-user-data.s3.amazonaws.com/YD7rN6h2ZARG_JipY6rcx9cDGpv8KFTS9ZQx0q0b3SjqUpSJp8V_gFo3hGOcWi7fkTpQUV-WiUPdXUDO2TmU9ESEa0vIFlG5sttgXFHsN1KPBv-ahN3-MDur-5tM-EDe.jpeg)](https://remnote-user-data.s3.amazonaws.com/YD7rN6h2ZARG_JipY6rcx9cDGpv8KFTS9ZQx0q0b3SjqUpSJp8V_gFo3hGOcWi7fkTpQUV-WiUPdXUDO2TmU9ESEa0vIFlG5sttgXFHsN1KPBv-ahN3-MDur-5tM-EDe.jpeg)

將 IntelliJ IDEA 中的 Maven home path 更改為自訂的 maven 資料夾。

確認 Local Repository 已正確指向專案內的 repository。

[![](https://remnote-user-data.s3.amazonaws.com/f5zOAXhbw_S55V5-2oFSYc-kn9BkkV9R6c6kJehXhC0Zvh3Ezm7VSasglar_KiEgJNdfJmcRTms0isn1iLd5lU7fydfhGIGsrU05bCrKjdHdSiFLXH-gxtiOac1tQ61L.jpeg)](https://remnote-user-data.s3.amazonaws.com/f5zOAXhbw_S55V5-2oFSYc-kn9BkkV9R6c6kJehXhC0Zvh3Ezm7VSasglar_KiEgJNdfJmcRTms0isn1iLd5lU7fydfhGIGsrU05bCrKjdHdSiFLXH-gxtiOac1tQ61L.jpeg)

使用 IntelliJ IDEA 中的 Maven 面板執行 install。檢查專案中的 repository 資料夾，確認依賴已正確下載與安裝。

[![](https://remnote-user-data.s3.amazonaws.com/0W0ZjtXtZRvCRlhx31YJ58Csh5Q5Y2OeRMlXRP9GQrdNSgP7Eg8KNd4jxe1x4_oLKHyzv17uogAb1YUhgAjpdext7KsiDWRyQKC3WDszKeud83Q-iicrDmvHLuzNIxKO.jpeg)](https://remnote-user-data.s3.amazonaws.com/0W0ZjtXtZRvCRlhx31YJ58Csh5Q5Y2OeRMlXRP9GQrdNSgP7Eg8KNd4jxe1x4_oLKHyzv17uogAb1YUhgAjpdext7KsiDWRyQKC3WDszKeud83Q-iicrDmvHLuzNIxKO.jpeg)

完成上述配置後，開發環境即使無法連接外網，仍可正常運行，確保離線開發流程的穩定性與效率。

# **補充說明**

## **配置前的準備**

- 明確專案是否需要特殊的 Maven Plugin 或私有倉庫。

- 確認內網伺服器的存取權限，避免傳輸失敗。

- 安裝對應版本的 Maven，避免版本不匹配。

## **Maven 設定補充**

## **內網 Repository 的訪問測試**

- 在設定完成後，使用以下指令檢查內網 Maven Repository 是否可正常訪問：
    
    `mvn help:effective-settings`
    

- 檢視是否正確載入內網設定。

## **啟用離線模式的注意事項**

- 在離線模式下，確保專案中所有依賴都已經被完整下載，否則會導致構建錯誤。

# **常見問題排查**

- `.m2/settings.xml` 是否配置正確。

- 專案是否啟用了正確的 Maven Profile。

- 檢查 Maven 日誌，找出具體錯誤信息。

# **相關連結**

- [https://start.spring.io/](https://start.spring.io/)

- [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)

- [https://maven.apache.org/](https://maven.apache.org/)

- [https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/)

- [https://gist.github.com/wanyutang/33d9c27693612c33bb9df4732f5ae040](https://gist.github.com/wanyutang/33d9c27693612c33bb9df4732f5ae040)

# **延申閱讀**

- [https://medium.com/@openthedidi2004/maven筆記-二-settings-xml-fd788d7f11ed](https://medium.com/@openthedidi2004/maven%E7%AD%86%E8%A8%98-%E4%BA%8C-settings-xml-fd788d7f11ed)

- [Spring + Maven + IntelliJ 多環境 (Profile) 整合技巧](https://ithelp.ithome.com.tw/articles/10310206)