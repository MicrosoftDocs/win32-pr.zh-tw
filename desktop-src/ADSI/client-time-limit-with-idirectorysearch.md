---
title: 使用 >idirectorysearch 的用戶端時間限制
description: 用戶端可能會強制服務器的時間限制，以傳回結果集。 當伺服器無法在指定的期間內回應查詢時，用戶端可能會放棄搜尋，稍後再試一次。
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch 的用戶端時間限制
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、用戶端時間限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1798094a980c41de2e1902533415839020cfd690384f0e56a37bff918d4ecc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692507"
---
# <a name="client-time-limit-with-idirectorysearch"></a>使用 >idirectorysearch 的用戶端時間限制

用戶端可能會強制服務器的時間限制，以傳回結果集。 當伺服器無法在指定的期間內回應查詢時，用戶端可能會放棄搜尋，稍後再試一次。

當用戶端要求非同步搜尋時，用戶端時間限制喜好設定會很有用。 在非同步搜尋中，用戶端會提出要求，然後在等候伺服器傳回結果時，繼續執行其他工作。 伺服器可能會離線，而不會通知用戶端。 在此情況下，用戶端將不會通知伺服器是否仍在處理查詢，或是該查詢已不存在。 用戶端時間限制喜好設定可讓用戶端控制像這樣的情況。

用戶端時間限制的預設值為 [無限制]。 若要設定用戶端時間限制，請 **將 ads \_ SEARCHPREF \_ TIMEOUT** 搜尋選項設定為 **ADSTYPE \_ 整數** 值，其中包含傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中的用戶端時間限制（以秒為單位）。 用戶端時間限制為0表示沒有時間限制。

下列程式碼範例顯示如何設定用戶端時間限制。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




