---
title: 註冊服務
description: 若要將您的服務加入至 [Web 發佈嚮導] 或 [線上列印順序] wizard 中的提供者清單，您必須將適當的索引鍵和其值新增至 Windows 登錄中。
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- 註冊、服務
- Web 發佈嚮導，註冊
- 線上列印訂購嚮導，註冊
- 註冊，Web 發佈嚮導
- 註冊，線上列印訂購嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f5e3f43fe981558fcbf8573eb8768646f112f4816486159cc7c16d71e40e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608638"
---
# <a name="registering-a-service"></a>註冊服務

若要將您的服務加入至 [Web 發佈嚮導] 或 [線上列印順序] wizard 中的提供者清單，您必須將適當的索引鍵和其值新增至 Windows 登錄中。

## <a name="required-keys-and-values"></a>必要的索引鍵和值

若要將您的服務加入至 Web 發佈嚮導的提供者清單，請新增如下所示的索引鍵。

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

若要將您的服務新增至線上列印訂購嚮導的提供者清單，請新增如下所示的索引鍵。

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

每個值都是 REG SZ 型別的字串 \_ 。 提供其資料，如下表所述。 

| 值名稱     | 說明                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| >iconpath       | 圖示檔案的完整路徑，包括檔案名。                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | 在嚮導的 [提供者] 清單中，為您的服務顯示的名稱。                                                                                                                                                                                                                                                                                                                                                             |
| 描述    | 您服務的簡短描述。 此描述也會顯示在您的服務名稱正下方的 wizard 提供者清單中。                                                                                                                                                                                                                                                                                    |
| HREF           | 服務第一頁的 URL。                                                                                                                                                                                                                                                                                                                                                                                      |
| SupportedTypes | 您的服務所支援的檔案類型。 例如， *\*.jpg*。 只要指定特定檔案類型，您的服務就只會在選取這些檔案類型時出現。 如果選取了多個檔案類型，如果您的服務支援這些檔案類型的任何一種，則會出現您的服務。 如果您想要指定多個檔案類型，請在清單中以分號分隔它們。 例如， *\*.jpg; \*.bmp*。 |



 

以下是名為 "MyProvider" 之相片處理服務的完整範例。

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

呼叫服務的 URL 時，會將兩個值新增至 URL 的結尾，也就是 lcid 和 langid。 例如，上述範例的 URL 字串可能是 HTTPs： \/ /www.MyProvider.com/Intro.htm？ lcid = 1033&langid = 1033。 這些變數會用於語言和當地語系化資訊。

-   **lcid** 用來通知伺服器用戶端的國家/地區和語言設定。 它不會用來判斷用戶端 UI 的語言，而是用來判斷貨幣、日期和時間，以及其他特定區域資料的正確格式。
-   **langid** 用來通知伺服器用戶端的預設語言設定，讓它可以在 UI 中使用適當的語言。

 

 




