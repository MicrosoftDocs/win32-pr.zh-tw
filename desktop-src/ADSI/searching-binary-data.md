---
title: 搜尋二進位資料
description: 雖然 ADSI 搜尋功能只支援搜尋字串資料，但是您可以搜尋二進位資料。
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- 搜尋二進位資料 ADSI
- 二進位資料 ADSI
- 二進位資料 ADSI，搜尋二進位資料
- ADSI ADSI，範例程式碼 C/c + +，搜尋二進位資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0973ff7a769d68abf85e6557fef2e1d434ba3ff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020791"
---
# <a name="searching-binary-data"></a>搜尋二進位資料

雖然 ADSI 搜尋功能只支援搜尋字串資料，但是您可以搜尋二進位資料。 若要這樣做，請使用 [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) 函式，將二進位資料轉換成可與搜尋方法搭配使用的字串。 搜尋 GUID 或 SID 時，搜尋二進位資料在搜尋 GUID 或 SID 時特別有用，因為這些資料類型會儲存為二進位資料。

使用 [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) 函式時，必須使用 [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) 函數來釋放配置的記憶體。

下列 c + + 程式碼範例顯示如何建立查詢字串，以搜尋具有特定 **objectGUID** 值的物件。


```C++
LPWSTR pwszGuid = NULL;
LPWSTR pwszFormat = L"(objectGUID=%s)";
LPWSTR pwszSearch = NULL;
hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
if(FAILED(hr))
{
    goto cleanup;
}

pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
if(NULL == pwszSearch)
{
    goto cleanup;
}
    
swprintf_s(pwszSearch, pwszFormat, pwszGuid);

// Use pwszSearch to perform a query for the object.

cleanup:    
if(pwszGuid)
{
    FreeADsMem(pwszGuid);
}
if(pwszSearch)
{
    delete pwszSearch;
}

```



 

 




