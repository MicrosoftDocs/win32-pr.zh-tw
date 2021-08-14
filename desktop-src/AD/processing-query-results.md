---
title: 處理搜尋結果
description: 在第一次呼叫 >idirectorysearch GetFirstRow 或 >idirectorysearch GetNextRow 之後，可能 \_ 會傳回 s OK、s \_ ADS \_ NOMORE \_ ROWS 或 error 結果。
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- 處理搜尋結果廣告
- Active Directory、搜尋、處理搜尋結果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a3ba7d3dac59e5d887dc7897eb6722295842f08cb4167d5292aaace0d115c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185202"
---
# <a name="processing-the-search-results"></a>處理搜尋結果

在第一次呼叫 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) 或 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow)之後， **s \_ OK**、 **s \_ ADS \_ NOMORE 資料 \_ 列** 或傳回錯誤結果。

如果傳回值是的 **\_ ADS \_ NOMORE 資料 \_ 列**，則找不到符合篩選準則的物件。 如果傳回錯誤結果，查詢就會失敗。 在這兩種情況下，您都不需要處理結果中的資料列，因為沒有傳回任何資料列。

如果傳回 **S \_ OK** ，則已取出資料列。 您可以使用 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn)，依名稱剖析資料行。 名稱是資料行中屬性的 **lDAPDisplayName** 。 所有資料行的集合都是由 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) 方法的 pAttributeNames 參數所定義。 如果指定 **Null** ，則所有資料行的集合都是所有傳回之物件的所有屬性的聯集。 若要讀取為物件傳回的整組資料行，請使用 [**>idirectorysearch：： GetNextColumnName**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) 逐一查看每個資料行，並使用傳回的資料行名稱來呼叫 **>idirectorysearch：： GetColumn**。

[**>Idirectorysearch：： GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn)方法會傳回 [**ADS 搜尋 \_ 資料 \_ 行**](/windows/desktop/api/iads/ns-iads-ads_search_column)結構，其中包含屬性名稱、屬性類型、值的計數，以及包含值之 [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue)結構陣列的指標。 您可以對 **ADSVALUE** 結構執行迴圈，以讀取資料行所傳回之屬性的值。 您必須根據 **ADS \_ 搜尋資料 \_ 行** 結構的 **DwADsType** 成員所指定的 [**ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) ，讀取 **ADSVALUE** 結構的適當成員 (或 **ADSVALUE** 結構) 的 **dwType** 成員。 例如，如果 **dwADsType** 是 **ADSTYPE \_ 整數**，您會讀取每個 **ADSVALUE** 結構的 **整數** 成員。

如需詳細資訊和程式碼範例，請參閱 [搜尋使用者的範例程式碼](example-code-for-searching-for-users.md)。

 

 