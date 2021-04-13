---
title: 公開 Owner-Drawn 清單方塊專案
description: 應用程式開發人員不需要執行 IAccessible 來公開主控描繪清單方塊中具有樣式磅 HASSTRINGS 的專案， \_ 因為 Microsoft Active Accessibility 會使用此樣式來公開清單方塊中的專案。
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbb72285f55796a285cd6e1a8838a629218659b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376237"
---
# <a name="exposing-owner-drawn-list-box-items"></a><span data-ttu-id="86929-103">公開 Owner-Drawn 清單方塊專案</span><span class="sxs-lookup"><span data-stu-id="86929-103">Exposing Owner-Drawn List Box Items</span></span>

<span data-ttu-id="86929-104">應用程式開發人員不需要執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 來公開主控描繪清單方塊中具有樣式 **磅 \_ HASSTRINGS** 的專案，因為 Microsoft Active Accessibility 會使用此樣式來公開清單方塊中的專案。</span><span class="sxs-lookup"><span data-stu-id="86929-104">Application developers do not need to implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) to expose the items in an owner-drawn list box that has the style **LBS\_HASSTRINGS** because Microsoft Active Accessibility exposes the items in list boxes with this style.</span></span> <span data-ttu-id="86929-105">具有 **磅 \_ HASSTRINGS** 樣式的主控描繪清單方塊中的專案會顯示為文字。</span><span class="sxs-lookup"><span data-stu-id="86929-105">The items in an owner-drawn list box with the **LBS\_HASSTRINGS** style are displayed as text.</span></span> <span data-ttu-id="86929-106">不過，此樣式也會與主控描繪清單方塊搭配使用，而不會顯示文字，以便 Microsoft Active Accessibility 公開清單方塊專案。</span><span class="sxs-lookup"><span data-stu-id="86929-106">However, this style is also used with owner-drawn list boxes that do not display text so that the list box items are exposed by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="86929-107">若要允許 Microsoft Active Accessibility 公開主控描繪清單方塊中未顯示文字的專案：</span><span class="sxs-lookup"><span data-stu-id="86929-107">To allow Microsoft Active Accessibility to expose the items in an owner-drawn list box that does not display text:</span></span>

-   <span data-ttu-id="86929-108">建立清單方塊時，請使用 **磅 \_ HASSTRINGS** 樣式。</span><span class="sxs-lookup"><span data-stu-id="86929-108">Use the **LBS\_HASSTRINGS** style when creating the list box.</span></span>
-   <span data-ttu-id="86929-109">建立名稱或描述清單方塊中每個專案的文字對應專案。</span><span class="sxs-lookup"><span data-stu-id="86929-109">Create a textual counterpart that names or describes each item in the list box.</span></span>
-   <span data-ttu-id="86929-110">將專案新增至主控描繪清單方塊時，請使用 [LB \_ ADDSTRING](../controls/lb-addstring.md) 訊息來新增您想要 Microsoft Active Accessibility 公開的文字。</span><span class="sxs-lookup"><span data-stu-id="86929-110">When adding items to the owner-drawn list box, use the [LB\_ADDSTRING](../controls/lb-addstring.md) message to add the text that you want Microsoft Active Accessibility to expose.</span></span> <span data-ttu-id="86929-111">這段文字不會顯示，因此它不是擁有者繪製資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="86929-111">This text is not displayed, so it is not part of the owner-drawn data.</span></span> <span data-ttu-id="86929-112">使用 [LB \_ SETITEMDATA](../controls/lb-setitemdata.md) 訊息加入擁有者繪製的專案資料。</span><span class="sxs-lookup"><span data-stu-id="86929-112">Add the owner-drawn item data using the [LB\_SETITEMDATA](../controls/lb-setitemdata.md) message.</span></span>

<span data-ttu-id="86929-113">使用上述方法時，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="86929-113">When using the above method, note the following:</span></span>

-   <span data-ttu-id="86929-114">如果您使用 **磅 \_ 排序** 樣式，清單方塊會使用提供的字串而非 [WM \_ COMPAREITEM](../controls/wm-compareitem.md) 回呼程式來排序。</span><span class="sxs-lookup"><span data-stu-id="86929-114">If you use the **LBS\_SORT** style, the list box is sorted using the supplied strings and not the [WM\_COMPAREITEM](../controls/wm-compareitem.md) callback procedure.</span></span>
-   <span data-ttu-id="86929-115">使用以樣式 **磅 \_ OWNERDRAWVARIABLE** 建立的主控描繪變數清單方塊時，請使用全域變數或其他機制來追蹤 [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct)的 **itemData 成員** 何時有效。</span><span class="sxs-lookup"><span data-stu-id="86929-115">With owner-drawn variable list boxes created with the style **LBS\_OWNERDRAWVARIABLE**, use a global variable or some other mechanism to keep track of when the **itemData member** of the [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct) is valid.</span></span> <span data-ttu-id="86929-116">全域變數是必要的，因為系統會在加入字串之後，但在附加專案資料之前立即傳送 [WM \_ MEASUREITEM](../controls/wm-measureitem.md) 訊息，此時 **itemData** 成員將無效。</span><span class="sxs-lookup"><span data-stu-id="86929-116">The global variable is needed because the system sends the [WM\_MEASUREITEM](../controls/wm-measureitem.md) message as soon as the string is added but before the item data is attached, and at this point the **itemData** member is not valid.</span></span>
-   <span data-ttu-id="86929-117">若要在清單方塊中以 **磅 \_ HASSTRINGS** 樣式變更專案的字串，請刪除具有 [lb \_ DELETESTRING](../controls/lb-deletestring.md) 訊息的專案，然後新增具有 lb \_ ADDSTRING 訊息的字串。</span><span class="sxs-lookup"><span data-stu-id="86929-117">To change the string for an item in a list box with the **LBS\_HASSTRINGS** style, delete the item with the [LB\_DELETESTRING](../controls/lb-deletestring.md) message and add the new string with the LB\_ADDSTRING message.</span></span>

 

 