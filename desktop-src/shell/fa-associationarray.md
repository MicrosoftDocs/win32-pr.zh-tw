---
description: 關聯陣列是登錄位置的排序清單，可用來儲存專案類型的相關資訊，包括處理常式、動詞和其他屬性，例如類型的圖示和顯示名稱。
title: 關聯陣列
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112772"
---
# <a name="association-arrays"></a>關聯陣列

關聯陣列是登錄位置的排序清單，可用來儲存專案類型的相關資訊，包括處理常式、動詞和其他屬性，例如類型的圖示和顯示名稱。 Shell 會使用關聯陣列來查詢一組預先定義的登錄位置，其中可能包含 Shell 專案的相關資訊。

本主題的組織方式如下：

-   [關於關聯陣列](#about-association-arrays)
-   [查詢關聯陣列](#querying-association-arrays)
-   [使用特定 Shell 資料來源的關聯陣列](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [Shell 資料來源關聯陣列](#shell-data-source-association-arrays)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="about-association-arrays"></a>關於關聯陣列

關聯陣列是登錄位置的排序清單，其中包含專案類型的相關資訊，包括處理常式、動詞和其他屬性，例如類型的圖示和顯示名稱。 此專案類型的相關資訊可以在明確的不同層級進行註冊。 例如，您可以註冊只會顯示特定檔案類型的動詞 (例如 .jpg) ，或所有具有相同 system.string 的專案 (例如，system.string = picture) ，或所有專案的所有專案。

Shell 會使用關聯陣列來查詢一組預先定義的登錄位置，其中可能包含專案的相關資訊。 您可以使用關聯陣列 Api，從登錄子機碼中取出包含所要求資訊的單一值，而該值來自陣列中提供它的第一個專案。 例如，預設圖示值會以這種方式抓取。 關聯陣列也可以用來抓取儲存在登錄子機碼中的一組值。 例如，動詞清單是根據在所有子機碼下註冊的動詞來建立。

在 Shell 查詢一組預先定義的登錄位置以取得 Shell 專案的相關資訊之後，它會將登錄位置從最特定的位置排列到最一般的陣列中。

因為關聯陣列是已排序的清單，所以會為應用程式開發人員提供一個機制，將資訊加入至將針對特定類型的專案傳回的登錄中。 同樣地，當這些專案在更一般的位置註冊時，關聯陣列可讓應用程式開發人員將資訊新增至特定專案群組的登錄中。 此邏輯會通知您有關登錄中最適當位置的決定，以儲存 Shell 專案的相關資訊。

在預設的 Windows 系統上，.jpg 檔案具有下列關聯陣列：

-   **HKEY \_類別 \_ 根** \\ **jpgfile**
-   **HKEY \_類別 \_ 根目錄** \\ **SystemFileAssociations** \\ **.jpg**
-   **HKEY \_類別 \_ 根** \\ **映射**
-   **HKEY \_類別 \_ 根目錄** \\ * *\** _
-   _ *HKEY \_ 類別 \_ 根 **\\** AllFilesystemObjects**

如需註冊關聯陣列的詳細資訊，請參閱 [應用程式註冊](app-registration.md)。

## <a name="querying-association-arrays"></a>查詢關聯陣列

有 Shell Api 可從某個範圍的登錄子機碼取得資訊，從最特定的登錄子機碼到所有登錄子機碼的資訊超集合。

關聯陣列最常見的用法是查詢 Shell 從陣列中具有所要求資訊的最特定元素傳回的單一值。 下列程式碼範例示範如何執行這項作業。


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



下列 Api 可用來查詢關聯陣列，或是用來建立可查詢的關聯陣列 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 物件：

-   Windows Vista) 之前的 [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (
-   [**AssocCreateForClasses**](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a>使用特定 Shell 資料來源的關聯陣列

每個 Shell 資料來源都會定義其專案的關聯陣列。 定義關聯陣列通常是專案類型的函式。 Shell 資料來源實作者應定義並記載關聯陣列，讓應用程式能夠擴充這些類型的行為，例如註冊動詞或其他資訊。 應用程式可以根據將資料加入至關聯陣列子機碼（例如新增專案的動詞）來擴充專案的行為。

檔案系統資料來源會根據下列登錄子機碼和特殊 Progid 來建立檔案的關聯陣列：

-   如果檔案具有已註冊的 ProgID，則會使用 **HKEY \_ 類別的 \_ 根目錄** \\ *ProgID* 。 否則會使用 **HKEY \_ 類別 \_ 根** \\ **未知**。
-   副檔名是在 **HKEY \_ 類別 \_ 根** \\ **SystemFileAssociations** \\ *. fileExtension* 子機碼下註冊。
-   下表顯示特殊的 Progid。 

    | 特殊 progID                                    | Description                   |
    |---------------------------------------------------|-------------------------------|
    | **HKEY \_類別 \_ 根目錄** \\ * *\** _                   | 所有檔案 (非資料夾)        |
    | _ *HKEY \_ 類別 \_ 根 **\\** AllFilesystemObjects** | 檔案和檔系統資料夾 |
    | **HKEY \_類別 \_ 根目錄** \\             | 檔系統資料夾           |
    | **HKEY \_類別 \_ 根** \\ **資料夾**               | Shell 容器              |

    

     

### <a name="shell-data-source-association-arrays"></a>Shell 資料來源關聯陣列

下列清單表示某些 Shell 資料存放區關聯陣列，可用於本主題中所述的用途：

-   **HKEY \_類別 \_ 根目錄** \\ * *\** _
-   _ *HKEY \_ 類別 \_ 根 **\\** AllFilesystemObjects**
-   **HKEY \_類別 \_ 根目錄** \\ **Kind.Doc>ument**
-   **HKEY \_類別 \_ 根** \\ **結果**
-   **HKEY \_類別 \_ 根目錄** \\ **SystemFileAssociations** \\ **.docx**
-   **HKEY \_類別 \_ 根目錄** \\ **Word.Doc>ument 12**

可以用於 DBFolder (Shell 資料存放區（代表搜尋結果中的專案）和查詢型視圖) 的 shell 資料來源關聯陣列如下所示：

-   磁碟機
-   網路
-   RegItems
-   範例：
    -   ContentView
    -   動詞

其他常見的關聯陣列包括資料夾和印表機。

## <a name="additional-resources"></a>其他資源

-   若要建立 Shell 資料存放區，請參閱 [執行基本資料夾物件介面](nse-implement.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式註冊](app-registration.md)
</dt> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[檔案關聯的運作方式](fa-how-work.md)
</dt> <dt>

[依檔案類型或種類的內容視圖](prophand-content-view.md)
</dt> <dt>

[檔案類型驗證器](file-type-verifier.md)
</dt> <dt>

[檔案類型處理常式](fa-file-extensions.md)
</dt> <dt>

[程式設計識別碼](fa-progids.md)
</dt> <dt>

[認知類型](fa-perceivedtypes.md)
</dt> </dl>

 

 
