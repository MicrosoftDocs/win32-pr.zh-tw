---
description: 本節說明 Windows Shell 登錄處理函式。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。
title: Shell 登錄處理函式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7bd7204ada31db6791d3cb78d1a11087d19eae45f0cacbfdf6ae6e032ae66a04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676497"
---
# <a name="shell-registry-handling-functions"></a>Shell 登錄處理函式

本節說明 Windows Shell 登錄處理函式。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。

## <a name="in-this-section"></a>本節內容



| 主題                                                             | 描述                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | 傳回 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 物件的指標。<br/>                                                                                         |
| [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | 根據檔案的副檔名抓取檔案的認知型別。<br/>                                                                                                                |
| [**AssocIsDangerous**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | 判斷檔案類型是否視為潛在的安全性風險。<br/>                                                                                                  |
| [**AssocQueryKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | 搜尋並從登錄中取出與檔案或通訊協定關聯相關的金鑰。<br/>                                                                            |
| [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | 搜尋並從登錄中抓取檔案或通訊協定關聯的字串。<br/>                                                                              |
| [**AssocQueryStringByKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | 從登錄中的指定索引鍵開始搜尋和抓取檔案關聯相關的字串。<br/>                                                            |
| [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | 將來源子機碼的子機碼和值以遞迴方式複製到目的地金鑰。 [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) 不會複製金鑰的安全性屬性。<br/> |
| [**SHDeleteEmptyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | 刪除空的索引鍵。<br/>                                                                                                                                                    |
| [**SHDeleteKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | 刪除子機碼及其所有子代。 此函式會從登錄中移除機碼和所有索引鍵的值。<br/>                                                      |
| [**SHDeleteValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | 從指定的登錄機碼刪除命名值。<br/>                                                                                                                   |
| [**SHEnumKeyEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | 列舉指定的開啟登錄機碼的子機碼。<br/>                                                                                                               |
| [**SHEnumValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | 列舉指定之開啟登錄機碼的值。<br/>                                                                                                                |
| [**SHGetAssocKeys**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | 捕獲與 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 物件相關聯的類別子機碼陣列。<br/>                                                          |
| [**SHGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | 抓取登錄值。<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | 開啟登錄值，並提供可用於讀取或寫入值的資料流程。 此函數會取代 [**SHOpenRegStream**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama)。<br/>   |
| [**SHQueryInfoKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | 抓取所指定登錄機碼的相關資訊。<br/>                                                                                                                    |
| [**SHQueryValueEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | 開啟登錄機碼，並針對特定的值查詢它。<br/>                                                                                                                |
| [**SHRegCloseUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | 關閉使用者特定子樹中使用者特定登錄子機碼的控制碼 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 。<br/>                                             |
| [**SHRegCreateUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | 在使用者特定的子樹中建立或開啟登錄子機碼 (HKEY \_ CURRENT \_ USER 或 HKEY \_ LOCAL \_ MACHINE) 。<br/>                                                             |
| [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | 在使用者特定的子樹中刪除空的登錄子機碼 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 。<br/>                                                               |
| [**SHRegDeleteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | 刪除使用者特定子樹中的登錄子機碼值 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 。<br/>                                                                |
| [**SHRegDuplicateHKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | 複製登錄機碼的 HKEY 控制碼。<br/>                                                                                                                                 |
| [**SHRegEnumUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | 列舉使用者特定子樹中登錄子機碼的子機碼 (HKEY \_ CURRENT \_ USER 或 HKEY \_ LOCAL \_ MACHINE) 。<br/>                                                    |
| [**SHRegEnumUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | 列舉使用者特定子樹中指定之登錄子機碼的值 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 。<br/>                                         |
| [**SHRegGetBoolUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | 從使用者指定的子樹中的登錄子機碼中抓取布林值 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 。<br/>                                               |
| [**SHRegGetIntW**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | 從登錄讀取數值字串值，並將它轉換成整數。<br/>                                                                                            |
| [**SHRegGetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | 從登錄抓取檔案路徑，視需要展開環境變數。<br/>                                                                                      |
| [**SHRegGetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | 從使用者特定子樹中的登錄子機碼抓取值 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 。<br/>                                                       |
| [**SHRegOpenUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | 在使用者特定的子樹中開啟登錄子機碼 (HKEY \_ CURRENT \_ USER 或 HKEY \_ LOCAL \_ MACHINE) 。<br/>                                                                        |
| [**SHRegQueryInfoUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | 在使用者特定的子樹中，抓取指定的登錄子機碼 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 的相關資訊。<br/>                                        |
| [**SHRegQueryUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | 在使用者特定子樹中，抓取與開啟的登錄子機碼相關聯之指定名稱的類型和資料 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 。<br/>       |
| [**SHRegSetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | 取得檔案路徑、將資料夾名稱取代為環境字串，並將產生的字串放在登錄中。<br/>                                                      |
| [**SHRegSetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | 在使用者特定的子樹中設定登錄子機碼值， (HKEY \_ CURRENT \_ USER 或 HKEY \_ LOCAL \_ MACHINE) 。<br/>                                                                   |
| [**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | 設定登錄值。<br/> 使用 [**RegSetValue**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) 的位置。<br/>                                                                                  |
| [**SHRegWriteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | 將值寫入至使用者特定子樹中的登錄子機碼 (HKEY \_ 目前 \_ 使用者或 HKEY \_ 本機 \_ 電腦) 。<br/>                                                            |
| [**SHSetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | 設定登錄機碼的值。<br/>                                                                                                                                        |



 

 

 
