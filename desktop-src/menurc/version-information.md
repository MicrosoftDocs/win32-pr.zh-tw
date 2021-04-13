---
title: 版本資訊
description: 本節討論版本資訊資源。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- 資源，版本資訊
- 版本資訊
- 版本編號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e43de27f18f89a5f240242b63ade057f57ec92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300943"
---
# <a name="version-information"></a>版本資訊

版本資訊可讓應用程式更輕鬆地安裝檔案，並讓安裝程式分析目前已安裝的檔案。 版本資訊資源包含檔案的版本號碼、其預定的作業系統，以及原始檔案的名稱。

### <a name="in-this-section"></a>本節內容



| Name                                                               | 描述                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [關於版本資訊](about-version-information.md)         | 討論版本資訊功能。<br/>            |
| [使用版本資訊](using-version-information.md)         | 討論如何使用版本資訊函數。<br/> |
| [版本資訊參考](version-information-reference.md) | 包含 API 參考。<br/>                             |



 

### <a name="version-information-functions"></a>版本資訊函式



| Name                                                         | 描述                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | 抓取指定檔案的版本資訊。 <br/>                                                                                                                                                                                                                                                                                                     |
| [**GetFileVersionInfoEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | 抓取指定檔案的版本資訊。<br/>                                                                                                                                                                                                                                                                                                      |
| [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | 判斷作業系統是否可以取出指定檔案的版本資訊。 如果有可用的版本資訊， [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) 會傳回該資訊的大小（以位元組為單位）。 <br/>                                                                                                             |
| [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | 判斷作業系統是否可以取出指定檔案的版本資訊。 如果有可用的版本資訊， [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) 會傳回該資訊的大小（以位元組為單位）。<br/>                                                                                                          |
| [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | 根據檔案是否在系統中找到另一個版本，決定要安裝檔案的位置。 [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)在指定的緩衝區中傳回的值會在後續的 [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)函數呼叫中使用。 <br/>                                                                          |
| [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | 根據 [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) 函式所傳回的資訊，安裝指定的檔案。 [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) 會在必要時解壓縮檔案，並檢查是否有錯誤，例如檔案是否過期。 <br/>                                                                                   |
| [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | 抓取與所指定二進位 Microsoft 語言識別項相關聯之語言的描述字串。<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | 從指定的版本資訊資源中，抓取指定的版本資訊。 若要取出適當的資源，在呼叫 [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)之前，您必須先呼叫 [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) 函式，然後再呼叫 [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) 函式。 <br/> |



 

### <a name="version-information-structures"></a>版本資訊結構



| Name                                          | 描述                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**字串**](string-str.md)                  | 描述檔案版本資源中的資料組織。 它包含的字串會描述檔案的特定層面，例如檔案的版本、其著作權聲明或其商標。<br/>                |
| [**StringFileInfo**](stringfileinfo.md)      | 描述檔案版本資源中的資料組織。 它包含可以針對特定語言和字碼頁顯示的版本資訊。<br/>                                                           |
| [**StringTable**](stringtable.md)            | 描述檔案版本資源中的資料組織。 它包含 **子** 系成員所指定之字串的語言和字碼頁格式資訊。 字碼頁是一組已排序的字元集。<br/> |
| [**無 功**](var-str.md)                        | 描述檔案版本資源中的資料組織。 它通常會包含應用程式或 DLL 版本所支援的語言和字碼頁識別碼組清單。<br/>                             |
| [**VarFileInfo**](varfileinfo.md)            | 描述檔案版本資源中的資料組織。 它包含不相依于特定語言和字碼頁組合的版本資訊。<br/>                                                        |
| [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | 包含檔案的版本資訊。 這項資訊與語言和字碼頁無關。 <br/>                                                                                                                   |
| [**VS \_ VERSIONINFO**](vs-versioninfo.md)     | 描述檔案版本資源中的資料組織。 它是包含所有其他檔案版本資訊結構的根結構。<br/>                                                                    |



 

 

 





