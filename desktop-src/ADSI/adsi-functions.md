---
title: ADSI 函數
description: Active Directory 服務介面會將下列 helper 函式公開給未使用 Automation 的用戶端。
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI、reference、函數
- 函數 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7245069ca427cbf6b1e4548749636a2c8448c2d4b9853bb27f7fa273f4a19a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180612"
---
# <a name="adsi-functions"></a>ADSI 函數

Active Directory 服務介面會將下列 helper 函式公開給未使用 Automation 的用戶端。



| 函式                                           | 描述                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | 建立指定 ADSI 容器物件的枚舉器物件。                              |
| [**ADsBuildVarArrayInt**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | 從 **DWORD** s 陣列建立 variant 陣列。                                                |
| [**ADsBuildVarArrayStr**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | 從 Unicode 字串的陣列建立變體陣列。                                           |
| [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | 將二進位資料的 blob 轉換成適合搜尋篩選的格式。                         |
| [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | 使用從指定的列舉值物件取出的元素，填入 variant 陣列。            |
| [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | 釋放 [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)先前建立的枚舉器物件。 |
| [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | 抓取呼叫執行緒的最後一個錯誤碼值。                                         |
| [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | 使用目前的認證系結至 ADSI 物件。                                             |
| [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | 使用指定的認證系結至 ADSI 物件                                                |
| [**ADsSetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | 設定呼叫執行緒的錯誤碼值。                                                   |
| [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | 配置記憶體區塊。                                                                       |
| [**AllocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | 配置指定字串的記憶體。                                                               |
| [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | 釋放 [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)所配置的記憶體。                                  |
| [**FreeADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | 釋放為指定字串配置的記憶體。                                                   |
| [**ReallocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | 將現有的記憶體內容指派給新建立的記憶體位置。                            |
| [**ReallocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | 以新的字串取代現有的字串。                                                        |



 

下列 ADSI 函數已淘汰。



| 函式                                                  | 描述 |
|-----------------------------------------------------------|-------------|
| [**AdsFreeAllErrorRecords**](obsolete-adsi-functions.md) | 已過時。   |
| [**AdsDecodeBinaryData**](obsolete-adsi-functions.md)    | 已過時。   |
| [**PropVariantToAdsType**](obsolete-adsi-functions.md)   | 已過時。   |
| [**AdsTypeToPropVariant**](obsolete-adsi-functions.md)   | 已過時。   |
| [**AdsFreeAdsValues**](obsolete-adsi-functions.md)       | 已過時。   |
| [**InitAdsMem**](obsolete-adsi-functions.md)             | 已過時。   |
| [**AssertAdsmemLeaks**](obsolete-adsi-functions.md)      | 已過時。   |
| [**DumpMemorytracker**](obsolete-adsi-functions.md)      | 已過時。   |



 

 

 




