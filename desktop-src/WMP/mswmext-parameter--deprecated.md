---
title: " (已淘汰的 MSWMExt 參數) "
description: " (已淘汰的 MSWMExt 參數) "
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Windows媒體中繼檔，MSWMExt 參數
- 中繼檔，MSWMExt 參數
- MSWMExt 參數
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ec80530f95d4429769758488e5a2b24b0268c57255248c7685a0d00125aa130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574595"
---
# <a name="mswmext-parameter-deprecated"></a> (已淘汰的 MSWMExt 參數) 

*MSWMExt* 參數會向用戶端程式指出參考檔案的格式。

**語法**


```XML

URL?MSWMExt=.
ext
```



**範例程式碼**


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a>備註

用戶端程式有時會使用副檔名或 MIME 類型來判斷是否要將媒體檔案轉譯為數據流、在完整下載之後轉譯檔案，或拒絕轉譯檔案。 如果用戶端程式無法判斷如何根據副檔名或 MIME 類型來處理媒體檔案，它可以藉由檢查 *MSWMExt* 參數來判斷如何處理檔案。 例如，用戶端可以將檔案視為具有等於 *MSWMExt* 參數值的副檔名。 如需有關 MIME 類型與 [副檔名的詳細](file-name-extensions.md)資訊，請參閱副檔名。 如需 *MSWMExt* 參數的詳細資訊，請參閱 Microsoft 知識庫中的文章 [236895](https://support.microsoft.com/kb/236895) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**舊版 Windows 媒體中繼檔 (已淘汰)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




