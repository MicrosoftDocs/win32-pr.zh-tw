---
title: Proxy 物件的設計考慮
description: Proxy 和可存取的物件設計取決於伺服器 UI 元素的設計。 無論設計為何，UI 專案都必須在終結之前通知 proxy 物件，讓 proxy 物件適當地處理來自用戶端的呼叫。
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021036"
---
# <a name="design-considerations-for-proxy-objects"></a><span data-ttu-id="e682d-104">Proxy 物件的設計考慮</span><span class="sxs-lookup"><span data-stu-id="e682d-104">Design Considerations for Proxy Objects</span></span>

<span data-ttu-id="e682d-105">Proxy 和可存取的物件設計取決於伺服器 UI 元素的設計。</span><span class="sxs-lookup"><span data-stu-id="e682d-105">Proxy and accessible object design depends on the design of the server UI elements.</span></span> <span data-ttu-id="e682d-106">無論設計為何，UI 專案都必須在終結之前通知 proxy 物件，讓 proxy 物件適當地處理來自用戶端的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e682d-106">Regardless of the design, a UI element must notify its proxy object right before it is destroyed so that the proxy object handles calls from clients appropriately.</span></span>

<span data-ttu-id="e682d-107">下列清單描述兩種設計可能性：</span><span class="sxs-lookup"><span data-stu-id="e682d-107">The following list describes two design possibilities:</span></span>

-   <span data-ttu-id="e682d-108">將實 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的程式碼放在與執行使用者介面專案的程式碼相同的模組中，如果使用者介面程式碼容易擴充。</span><span class="sxs-lookup"><span data-stu-id="e682d-108">Place the code that implements the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface in the same module as the code that implements the user interface element if the user interface code is easily extensible.</span></span> <span data-ttu-id="e682d-109">在此情況下，proxy 的意義是「輕量」，因為它所做的只是監視可存取物件的存留期、將呼叫轉送到可存取的物件，然後傳回結果。</span><span class="sxs-lookup"><span data-stu-id="e682d-109">In this case, the proxy is "lightweight" in the sense that all it does is monitor the life span of the accessible object, forward calls to the accessible object, and return the results.</span></span>
-   <span data-ttu-id="e682d-110">將實 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 的程式碼放在與執行 proxy 物件的程式碼相同的模組中。</span><span class="sxs-lookup"><span data-stu-id="e682d-110">Place the code that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in the same module as the code that implements the proxy object.</span></span> <span data-ttu-id="e682d-111">在此情況下，可存取的物件會使用內建函式來取得 UI 元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e682d-111">In this case, the accessible object uses internal functions to obtain information about the UI element.</span></span>

## <a name="trackbar-controls"></a><span data-ttu-id="e682d-112">[請] 控制項</span><span class="sxs-lookup"><span data-stu-id="e682d-112">Trackbar Controls</span></span>

<span data-ttu-id="e682d-113">當您在執行資料類型控制時，請使用 **\_ 反向** 的 [資料類型] 的 [tb] 來提供更有意義</span><span class="sxs-lookup"><span data-stu-id="e682d-113">When implementing trackbar controls, use the trackbar style **TBS\_REVERSED** to provide more meaningful information.</span></span> <span data-ttu-id="e682d-114">此樣式會反轉 [**IAccessible：： get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)所使用的小數位數。</span><span class="sxs-lookup"><span data-stu-id="e682d-114">This style reverses the scale used by [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="e682d-115">針對沒有此樣式的垂直 trackbars， [**IAccessible：： get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 會在 [頁首] 捲軸位於控制項頂端時傳回零 (0) 。當您將 thumb 朝底部滑動時，這些值就會增加。</span><span class="sxs-lookup"><span data-stu-id="e682d-115">For vertical trackbars without this style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns zero (0) when the trackbar thumb is at the top of the control; the values increase as you slide the thumb toward the bottom.</span></span> <span data-ttu-id="e682d-116">使用 **tb \_ 反轉** 樣式時， **IAccessible：： get \_ accValue** 會傳回 100 (100) 當頁首位於頂端時; 當您將頁首移往底部時，會降低數位。</span><span class="sxs-lookup"><span data-stu-id="e682d-116">With the **TBS\_REVERSED** style, **IAccessible::get\_accValue** returns one hundred (100) when the trackbar thumb is at the top; the numbers decrease as you move the trackbar thumb toward the bottom.</span></span>

<span data-ttu-id="e682d-117">若為不含此樣式的水準 trackbars，當捲軸捲動方塊位於控制項的左邊時，會傳回零 (0) ;當您將 [對齊] 捲軸移至右側時，這些值就會增加。</span><span class="sxs-lookup"><span data-stu-id="e682d-117">For horizontal trackbars without this style, zero (0) is returned when the trackbar thumb is at the left end of the control; the values increase as you move the trackbar thumb to the right.</span></span> <span data-ttu-id="e682d-118">使用 **tb \_ 反轉** 樣式時， [**IAccessible：： get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 會在 [資料列] 捲軸位於左邊時，傳回 100 (100) ; 當您將 [資料列] 捲軸向右移動時，這些值就會降低。</span><span class="sxs-lookup"><span data-stu-id="e682d-118">With the **TBS\_REVERSED** style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns one hundred (100) when the trackbar thumb is at the left; the values decrease as you move the trackbar thumb to the right.</span></span>

 

 




