---
title: 公開 Owner-Drawn 下拉式方塊專案
description: 應用程式開發人員不需要執行 IAccessible 來公開主控描繪下拉式方塊中具有樣式 CBS HASSTRINGS 的專案， \_ 因為 Microsoft Active Accessibility 會使用這個樣式來公開下拉式方塊中的專案。
ms.assetid: 9ff14b2f-ae09-4839-b281-fba46addaf5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364dccaf21927e2d0092fc744d501f47830c6eeb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106993731"
---
# <a name="exposing-owner-drawn-combo-box-items"></a>公開 Owner-Drawn 下拉式方塊專案

應用程式開發人員不需要執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 來公開主控描繪下拉式方塊中具有樣式 **CBS \_ HASSTRINGS** 的專案，因為 Microsoft Active Accessibility 會使用這個樣式來公開下拉式方塊中的專案。 具有 **CBS \_ HASSTRINGS** 樣式之主控描繪下拉式方塊中的專案會顯示為文字。 不過，此樣式也會與主控描繪的下拉式方塊搭配使用，而不會顯示文字，因此 Microsoft Active Accessibility 會公開下拉式方塊專案。

若要允許 Microsoft Active Accessibility 公開主控描繪下拉式方塊中未顯示文字的專案：

-   建立下拉式方塊時，請使用 **CBS \_ HASSTRINGS** 樣式。
-   建立名稱為的文字對應，或描述下拉式方塊中的每個專案。
-   將專案新增至主控描繪下拉式方塊時，請使用 CB \_ ADDSTRING 訊息來新增您想要 Microsoft Active Accessibility 公開的文字。 這段文字不會顯示，因此它不能是主控描繪資料的一部分。 使用 CB SETITEMDATA 訊息加入擁有者繪製的專案資料 \_ 。

使用上述方法時，請注意下列事項：

-   如果您使用 **CBS \_ 排序** 樣式，則會使用提供的字串，而不是使用 [WM \_ COMPAREITEM](../controls/wm-compareitem.md) 回呼程式來排序下拉式方塊。
-   使用樣式 **CBS \_ OWNERDRAWVARIABLE** 建立的主控描繪變數下拉式方塊時，請使用全域變數或其他機制來追蹤 [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct)的 **itemData** 成員何時有效。 全域變數是必要的，因為系統會在加入字串之後，但在附加專案資料之前立即傳送 [WM \_ MEASUREITEM](../controls/wm-measureitem.md) 訊息，此時 **itemData** 成員將無效。
-   若要在具有 **CBS \_ HASSTRINGS** 樣式的下拉式方塊中變更專案的字串，請使用 [cb \_ DELETESTRING](../controls/cb-deletestring.md) 訊息刪除該專案，然後使用 [cb \_ ADDSTRING](../controls/cb-addstring.md) 訊息來加入新的字串。

 

 