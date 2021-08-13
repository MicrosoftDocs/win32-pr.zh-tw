---
title: 使用 >idirectorysearch 的參考追蹤
description: 參考是目錄伺服器在不包含查詢所要求之物件的足夠資料時，用來將用戶端導向至另一部伺服器的機制。
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 的參考追蹤
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、參考追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7fcc74103c5c09816976e9ff91c17ecca8578fcbf596b731df890a350e922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690687"
---
# <a name="referral-chasing-with-idirectorysearch"></a>使用 >idirectorysearch 的參考追蹤

參考是目錄伺服器在不包含查詢所要求之物件的足夠資料時，用來將用戶端導向至另一部伺服器的機制。

在一層或子樹搜尋中，只會針對已知、立即的從屬網域、架構或設定容器傳回參考;亦即，子域是直接下階。 如需詳細資訊，請參閱 [搜尋範圍](/windows/desktop/AD/search-scope)。

在目錄中，並非所有資料都可在單一伺服器上使用，而是分散在網路上的數部不同伺服器上。 如果伺服器共用其他伺服器可提供的資料，則可以在源伺服器上無法解析要求的查詢時，提供用戶端的參考。 例如，當用戶端要求伺服器 A 查詢使用者物件 (U) 時，可以建議用戶端在伺服器 B 上繼續搜尋（如果 U 不在上，但識別為 B）。用戶端可以選擇尋求參考。 用戶端可以讓用戶端不需要擁有每一部伺服器的功能，但用戶端必須指定伺服器應該執行的參照類型。

若要啟用或停用參考追蹤，請設定 **ads \_ SEARCHPREF 「 \_ \_ 追蹤參考**」搜尋選項，其 **ADSTYPE \_ 整數** 值包含其中一個廣告會在傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中 [**\_ \_ 追蹤參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)列舉值。

下列程式碼範例示範如何啟用「查看參考」。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



如需 Active Directory 中參考的詳細資訊，請參閱 [參考](/windows/desktop/AD/referrals)。

 

 