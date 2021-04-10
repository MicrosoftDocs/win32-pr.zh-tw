---
title: 使用 >idirectorysearch 指定其他搜尋選項
description: '>idirectorysearch 介面可讓您透過使用搜尋選項來進一步控制搜尋的執行方式。'
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 指定其他搜尋選項
- ADSI、搜尋、>idirectorysearch、其他搜尋選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931824"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a>使用 >idirectorysearch 指定其他搜尋選項

[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面可讓您透過使用搜尋選項來進一步控制搜尋的執行方式。 這些搜尋選項的設定方式是填入 [**ADS \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) 結構的陣列，然後呼叫 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 方法。 如需詳細資訊，請參閱下列主題：

-   [使用 SetSearchPreference 方法](using-the-setsearchpreference-method.md)
-   [使用 >idirectorysearch 進行同步和非同步搜尋](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [使用 >idirectorysearch 進行分頁](paging-with-idirectorysearch.md)
-   [使用 >idirectorysearch 的結果快取](result-caching-with-idirectorysearch.md)
-   [執行屬性範圍查詢](performing-an-attribute-scoped-query.md)
-   [使用 >idirectorysearch 排序搜尋結果](sorting-the-search-results-with-idirectorysearch.md)
-   [使用 >idirectorysearch 的參考追蹤](referral-chasing-with-idirectorysearch.md)
-   [使用 >idirectorysearch 的大小限制](size-limit-with-idirectorysearch.md)
-   [使用 >idirectorysearch 的伺服器時間限制](server-time-limit-with-idirectorysearch.md)
-   [使用 >idirectorysearch 的用戶端時間限制](client-time-limit-with-idirectorysearch.md)
-   [使用 >idirectorysearch 只傳回屬性名稱](returning-only-attribute-names-with-idirectorysearch.md)

 

 




