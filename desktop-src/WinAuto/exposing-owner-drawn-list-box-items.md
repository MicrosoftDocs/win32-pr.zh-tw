---
title: 公開 Owner-Drawn 清單方塊專案
description: 應用程式開發人員不需要執行 IAccessible 來公開主控描繪清單方塊中具有樣式磅 HASSTRINGS 的專案， \_ 因為 Microsoft Active Accessibility 會使用此樣式來公開清單方塊中的專案。
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fed68477680376373da6c16f59b3fb556b6a435f15f04daae8f3f1262829dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115271"
---
# <a name="exposing-owner-drawn-list-box-items"></a>公開 Owner-Drawn 清單方塊專案

應用程式開發人員不需要執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 來公開主控描繪清單方塊中具有樣式 **磅 \_ HASSTRINGS** 的專案，因為 Microsoft Active Accessibility 會使用此樣式來公開清單方塊中的專案。 具有 **磅 \_ HASSTRINGS** 樣式的主控描繪清單方塊中的專案會顯示為文字。 不過，此樣式也會與主控描繪清單方塊搭配使用，而不會顯示文字，以便 Microsoft Active Accessibility 公開清單方塊專案。

若要允許 Microsoft Active Accessibility 公開主控描繪清單方塊中未顯示文字的專案：

-   建立清單方塊時，請使用 **磅 \_ HASSTRINGS** 樣式。
-   建立名稱或描述清單方塊中每個專案的文字對應專案。
-   將專案新增至主控描繪清單方塊時，請使用 [LB \_ ADDSTRING](../controls/lb-addstring.md) 訊息來新增您想要 Microsoft Active Accessibility 公開的文字。 這段文字不會顯示，因此它不是擁有者繪製資料的一部分。 使用 [LB \_ SETITEMDATA](../controls/lb-setitemdata.md) 訊息加入擁有者繪製的專案資料。

使用上述方法時，請注意下列事項：

-   如果您使用 **磅 \_ 排序** 樣式，清單方塊會使用提供的字串而非 [WM \_ COMPAREITEM](../controls/wm-compareitem.md) 回呼程式來排序。
-   使用以樣式 **磅 \_ OWNERDRAWVARIABLE** 建立的主控描繪變數清單方塊時，請使用全域變數或其他機制來追蹤 [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct)的 **itemData 成員** 何時有效。 全域變數是必要的，因為系統會在加入字串之後，但在附加專案資料之前立即傳送 [WM \_ MEASUREITEM](../controls/wm-measureitem.md) 訊息，此時 **itemData** 成員將無效。
-   若要在清單方塊中以 **磅 \_ HASSTRINGS** 樣式變更專案的字串，請刪除具有 [lb \_ DELETESTRING](../controls/lb-deletestring.md) 訊息的專案，然後新增具有 lb \_ ADDSTRING 訊息的字串。

 

 