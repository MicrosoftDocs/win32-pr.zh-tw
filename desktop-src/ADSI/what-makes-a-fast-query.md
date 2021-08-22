---
title: 什麼可進行快速查詢
description: 本主題列出查詢目錄時要使用的慣用程式設計方法。
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- 什麼是讓 Fast Query ADSI
- 查詢 ADSI，如何進行快速查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134d391c728d543c407ee770081e2ced96afbba86d205462e814d89f74e82a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589838"
---
# <a name="what-makes-a-fast-query"></a>什麼是快速查詢？

執行查詢時，請考慮下列效能增強概念：

-   可能的話，請只篩選索引屬性。 使用您預期會產生最少點擊次數的索引屬性。 如需 Windows 的索引屬性的詳細資訊和完整清單，請參閱[Active Directory 架構](/windows/desktop/ADSchema/active-directory-schema)。
-   搜尋 **objectCategory** 而非 **Objectclass** ，因為 **objectClass** 不是索引屬性。
-   請留意參考。 如果您的屬性列為 GC 已複寫，請考慮搜尋通用類別目錄。
-   避免搜尋字串中間和結尾的文字。 例如，"cn = \* hille \* " 或 "cn = \* larouse"。
-   假設子樹搜尋將傳回大型結果集。 執行子樹搜尋時，請使用分頁。 如此一來，伺服器就能夠以區塊來串流大型結果集，以減少伺服器端記憶體資源。 這可有效地將網路使用量壓平合併，並減少透過網路傳送極大區塊資料的需求。
-   適當地界定搜尋範圍，如此就不需要取得超過的範圍。
-   對多個屬性執行複雜的搜尋，因為它比執行多個搜尋的效能低。 針對讀取兩個屬性的物件進行一項搜尋，會比對相同物件的兩個搜尋更有效率，每個都傳回一個屬性。
-   若要讀取具有大量值的屬性，請使用範圍限制將搜尋大小降到最低，讓您一次可以讀取數千個成員。 如需有關指定屬性範圍限制的詳細資訊，請參閱 [屬性範圍](attribute-range-retrieval.md)抓取。
-   系結至物件，以保存會話其餘部分的系結控制碼。 請勿系結和解除系結每個呼叫。 如果您使用的是 ADO 或 OLE DB，請勿建立許多連線物件。
-   讀取 rootDSE 一次，並記住其內容以供會話的其餘部分之用。

 

 