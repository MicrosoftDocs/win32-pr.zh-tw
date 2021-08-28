---
title: 使用 >idirectorysearch 進行同步和非同步搜尋
description: 當您使用 >idirectorysearch 介面執行搜尋時，>idirectorysearch ExecuteSearch 方法不會將搜尋要求傳送至伺服器。
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 進行同步和非同步搜尋
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、同步和非同步搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3891351bc7ebb9872938f3022f5397100e0be74ca6cd2d86d21a2535f010cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690195"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>使用 >idirectorysearch 進行同步和非同步搜尋

當您使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面執行搜尋時， [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 方法不會將搜尋要求傳送至伺服器。 這個方法只會儲存搜尋參數。 當您呼叫 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) 或 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)時，會實際傳送搜尋要求。

針對 Active Directory 搜尋，同步與非同步之間的主要差異在於傳回結果的第一個資料列，也就是當第一個 [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) 或 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 呼叫傳回時。

在同步搜尋中，如果未啟用分頁功能，當伺服器已經建立並將整個結果集傳回給用戶端時，就會傳回第一個資料列。 如果啟用分頁，則傳回結果集的第一個頁面時，就會傳回第一個資料列。

在非同步搜尋中，如果未啟用分頁功能，當伺服器已經建立結果集的第一個資料列時，就會傳回第一個資料列。 如果啟用分頁，則傳回結果集的第一個頁面時，就會傳回第一個資料列。

預設搜尋類型為同步。 若要指定非同步搜尋，請在傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中，設定 **\_ SEARCHPREF \_ 非同步** 搜尋選項 **ADSTYPE \_ 布林** 值為 **TRUE** 的 ads。 下列程式碼範例會顯示這項作業。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




