---
title: 使用 >idirectorysearch 的結果快取
description: ADS SEARCHPREF 快取 \_ \_ 結果喜好設定會快取 \_ 用戶端上的結果集。
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 的結果快取
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、結果快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4febc2f02e03759861978e062ee972d8e90df27b996c8161d6163e764fefe9a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838854"
---
# <a name="result-caching-with-idirectorysearch"></a>使用 >idirectorysearch 的結果快取

**ADS SEARCHPREF 快取 \_ \_ \_ 結果** 喜好設定會快取用戶端上的結果集。 結果快取可讓應用程式保留抓取的結果集，並再次流覽抓取過的資料列。 它也會啟用資料指標支援，其中 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 和 [**>idirectorysearch：： GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) 方法可以用來向上和向下移動結果集。

預設會停用結果快取。 如果下列任何一個條件成立，則應該啟用結果快取：

-   如果相同的結果集必須列舉多次，而不在伺服器上再次執行搜尋。
-   如果執行搜尋需要耗用大量資源的伺服器 (慢速連線、大型結果集或複雜查詢) 。
-   如果需要資料指標支援。

如果您的應用程式必須減少在用戶端快取大型結果集的記憶體需求，請關閉快取。

結果快取會增加用戶端的記憶體需求，因此，如果這是問題，則應該停用結果快取。

若要啟用結果快取，請在傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中，設定 SEARCHPREF 快取 **\_ \_ \_ 結果** 搜尋選項 **ADSTYPE \_ 布林** 值為 **TRUE** 的 ads。

下列程式碼範例顯示如何啟用結果快取。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




