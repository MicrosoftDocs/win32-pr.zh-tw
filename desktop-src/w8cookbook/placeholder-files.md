---
title: 預留位置檔案
description: 預留位置檔案
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8891fef6c7fc54a66c093507b1831ab7cc6525ea96d685d06cf6fa8d9ded1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452498"
---
# <a name="placeholder-files"></a>預留位置檔案

## <a name="platform"></a>平台

**用戶端-** Windows 8。1  
**伺服器-** Windows Server 2012 R2  

## <a name="description"></a>描述

預留位置檔案可讓使用者不論連線能力，都能查看和管理 Microsoft OneDrive 檔案。 預留位置檔案代表 OneDrive 命名空間，即使檔案不是在本機快取。 它們包含相片的檔案中繼資料和縮圖影像。

## <a name="manifestation"></a>表現

對於使用者和開發人員而言，預留位置檔案的外觀和行為幾乎與本機檔案相同。

如果您的應用程式使用 [一般檔案] 對話方塊來列舉檔案系統，則您的應用程式不會受到影響。 當使用者嘗試從 [一般/file] 對話方塊開啟檔案時，將會下載檔案內容，並將其傳遞至您的應用程式。

如果您的應用程式直接存取檔案系統，則您的應用程式可以使用下列指導方針來利用預留位置檔案。

## <a name="solution"></a>解決方案

-   根據屬性，根據慣例隱藏預留位置
-   使用重新分析標記識別項 IO 重新 \_ 分析 \_ 標記 \_ 檔案 \_ 預留位置來識別預留位置

使用 shell 資料模型來取得無縫行為：

-   使用 SHCreateItemFromParsingName () 建立 shell 專案
-   使用 IShellItem：： BindToHandler (BHID stream 來系結至資料流程 \_) 
-   屬性存取 (IShellItem2：： GetPropertyHandler) 的使用者屬性處理常式
-   使用者介面 thumbnailhandler 取得預留位置的縮圖影像
-   \*如果動詞透過 BindToHandler 系結至資料流程，請在您的動詞執行上指定 SupportedProtocols =


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




