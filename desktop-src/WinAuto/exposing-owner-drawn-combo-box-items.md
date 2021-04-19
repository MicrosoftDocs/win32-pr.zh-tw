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
# <a name="exposing-owner-drawn-combo-box-items"></a><span data-ttu-id="3c986-103">公開 Owner-Drawn 下拉式方塊專案</span><span class="sxs-lookup"><span data-stu-id="3c986-103">Exposing Owner-Drawn Combo Box Items</span></span>

<span data-ttu-id="3c986-104">應用程式開發人員不需要執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 來公開主控描繪下拉式方塊中具有樣式 **CBS \_ HASSTRINGS** 的專案，因為 Microsoft Active Accessibility 會使用這個樣式來公開下拉式方塊中的專案。</span><span class="sxs-lookup"><span data-stu-id="3c986-104">Application developers do not need to implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) to expose the items in an owner-drawn combo box that has the style **CBS\_HASSTRINGS** because Microsoft Active Accessibility exposes the items in combo boxes with this style.</span></span> <span data-ttu-id="3c986-105">具有 **CBS \_ HASSTRINGS** 樣式之主控描繪下拉式方塊中的專案會顯示為文字。</span><span class="sxs-lookup"><span data-stu-id="3c986-105">The items in an owner-drawn combo box with the **CBS\_HASSTRINGS** style are displayed as text.</span></span> <span data-ttu-id="3c986-106">不過，此樣式也會與主控描繪的下拉式方塊搭配使用，而不會顯示文字，因此 Microsoft Active Accessibility 會公開下拉式方塊專案。</span><span class="sxs-lookup"><span data-stu-id="3c986-106">However, this style is also used with owner-drawn combo boxes that do not display text so that the combo box items are exposed by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="3c986-107">若要允許 Microsoft Active Accessibility 公開主控描繪下拉式方塊中未顯示文字的專案：</span><span class="sxs-lookup"><span data-stu-id="3c986-107">To allow Microsoft Active Accessibility to expose the items in an owner-drawn combo box that does not display text:</span></span>

-   <span data-ttu-id="3c986-108">建立下拉式方塊時，請使用 **CBS \_ HASSTRINGS** 樣式。</span><span class="sxs-lookup"><span data-stu-id="3c986-108">Use the **CBS\_HASSTRINGS** style when creating the combo box.</span></span>
-   <span data-ttu-id="3c986-109">建立名稱為的文字對應，或描述下拉式方塊中的每個專案。</span><span class="sxs-lookup"><span data-stu-id="3c986-109">Create a textual counterpart that names or describes each item in the combo box.</span></span>
-   <span data-ttu-id="3c986-110">將專案新增至主控描繪下拉式方塊時，請使用 CB \_ ADDSTRING 訊息來新增您想要 Microsoft Active Accessibility 公開的文字。</span><span class="sxs-lookup"><span data-stu-id="3c986-110">When adding items to the owner-drawn combo box, use the CB\_ADDSTRING message to add the text that you want Microsoft Active Accessibility to expose.</span></span> <span data-ttu-id="3c986-111">這段文字不會顯示，因此它不能是主控描繪資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="3c986-111">This text is not displayed, so it must not be part of the owner-drawn data.</span></span> <span data-ttu-id="3c986-112">使用 CB SETITEMDATA 訊息加入擁有者繪製的專案資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3c986-112">Add the owner-drawn item data using the CB\_SETITEMDATA message.</span></span>

<span data-ttu-id="3c986-113">使用上述方法時，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="3c986-113">When using the above method, note the following:</span></span>

-   <span data-ttu-id="3c986-114">如果您使用 **CBS \_ 排序** 樣式，則會使用提供的字串，而不是使用 [WM \_ COMPAREITEM](../controls/wm-compareitem.md) 回呼程式來排序下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="3c986-114">If you use the **CBS\_SORT** style, the combo box is sorted using the supplied strings and not the [WM\_COMPAREITEM](../controls/wm-compareitem.md) callback procedure.</span></span>
-   <span data-ttu-id="3c986-115">使用樣式 **CBS \_ OWNERDRAWVARIABLE** 建立的主控描繪變數下拉式方塊時，請使用全域變數或其他機制來追蹤 [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct)的 **itemData** 成員何時有效。</span><span class="sxs-lookup"><span data-stu-id="3c986-115">With owner-drawn variable combo boxes created with the style **CBS\_OWNERDRAWVARIABLE**, use a global variable or some other mechanism to keep track of when the **itemData** member of the [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct) is valid.</span></span> <span data-ttu-id="3c986-116">全域變數是必要的，因為系統會在加入字串之後，但在附加專案資料之前立即傳送 [WM \_ MEASUREITEM](../controls/wm-measureitem.md) 訊息，此時 **itemData** 成員將無效。</span><span class="sxs-lookup"><span data-stu-id="3c986-116">The global variable is required because the system sends the [WM\_MEASUREITEM](../controls/wm-measureitem.md) message as soon as the string is added but before the item data is attached, and at this point the **itemData** member is not valid.</span></span>
-   <span data-ttu-id="3c986-117">若要在具有 **CBS \_ HASSTRINGS** 樣式的下拉式方塊中變更專案的字串，請使用 [cb \_ DELETESTRING](../controls/cb-deletestring.md) 訊息刪除該專案，然後使用 [cb \_ ADDSTRING](../controls/cb-addstring.md) 訊息來加入新的字串。</span><span class="sxs-lookup"><span data-stu-id="3c986-117">To change the string for an item in a combo box with the **CBS\_HASSTRINGS** style, delete the item with the [CB\_DELETESTRING](../controls/cb-deletestring.md) message and add the new string with the [CB\_ADDSTRING](../controls/cb-addstring.md) message.</span></span>

 

 