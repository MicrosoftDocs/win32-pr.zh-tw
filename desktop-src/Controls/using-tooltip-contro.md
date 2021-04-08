---
title: 使用工具提示控制項
description: 本章節包含的範例會示範如何建立不同類型的工具提示。
ms.assetid: 4486b406-a069-4250-b7ab-671d895b79f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fd4a0cef452be3f9700f8466959043ac8d30b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672883"
---
# <a name="using-tooltip-controls"></a><span data-ttu-id="61f7b-103">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="61f7b-103">Using Tooltip Controls</span></span>

<span data-ttu-id="61f7b-104">本章節包含的範例會示範如何建立不同類型的工具提示。</span><span class="sxs-lookup"><span data-stu-id="61f7b-104">This section contains examples that demonstrate how to create different types of tooltips.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61f7b-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="61f7b-105">In this section</span></span>



| <span data-ttu-id="61f7b-106">主題</span><span class="sxs-lookup"><span data-stu-id="61f7b-106">Topic</span></span>                                                                                                    | <span data-ttu-id="61f7b-107">描述</span><span class="sxs-lookup"><span data-stu-id="61f7b-107">Description</span></span>                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61f7b-108">如何建立控制項的工具提示</span><span class="sxs-lookup"><span data-stu-id="61f7b-108">How to Create a Tooltip for a Control</span></span>](create-a-tooltip-for-a-control.md)<br/>                   | <span data-ttu-id="61f7b-109">下列範例函數會建立工具提示，並將其與資源識別碼傳入的控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="61f7b-109">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span> <br/>                                                                                                                                                  |
| [<span data-ttu-id="61f7b-110">如何建立矩形區域的工具提示</span><span class="sxs-lookup"><span data-stu-id="61f7b-110">How to Create a Tooltip for a Rectangular Area</span></span>](create-a-tooltip-for-a-rectangular-area.md)<br/> | <span data-ttu-id="61f7b-111">下列範例示範如何建立視窗整個工作區的標準工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="61f7b-111">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span> <br/>                                                                                                                                                       |
| [<span data-ttu-id="61f7b-112">如何執行追蹤工具提示</span><span class="sxs-lookup"><span data-stu-id="61f7b-112">How to Implement Tracking Tooltips</span></span>](implement-tracking-tooltips.md)<br/>                         | <span data-ttu-id="61f7b-113">追蹤工具提示會保持可見，直到應用程式明確關閉為止，並且可以動態地變更螢幕上的位置。</span><span class="sxs-lookup"><span data-stu-id="61f7b-113">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="61f7b-114">[版本 4.70](common-control-versions.md)和更新版本的通用控制項都支援它們。</span><span class="sxs-lookup"><span data-stu-id="61f7b-114">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <br/>                         |
| [<span data-ttu-id="61f7b-115">如何執行多行工具提示</span><span class="sxs-lookup"><span data-stu-id="61f7b-115">How to Implement Multiline Tooltips</span></span>](implement-multiline-tooltips.md)<br/>                       | <span data-ttu-id="61f7b-116">多行工具提示允許文字顯示在一行以上。</span><span class="sxs-lookup"><span data-stu-id="61f7b-116">Multiline tooltips allow text to be displayed on more than one line.</span></span> <br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="61f7b-117">如何執行氣球工具提示</span><span class="sxs-lookup"><span data-stu-id="61f7b-117">How to Implement Balloon Tooltips</span></span>](implement-balloon-tooltips.md)<br/>                           | <span data-ttu-id="61f7b-118">氣球工具提示類似于標準工具提示，但會顯示在卡通樣式的「球標」中，並以主幹指向工具。</span><span class="sxs-lookup"><span data-stu-id="61f7b-118">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="61f7b-119">氣球工具提示可以是單行或多行。</span><span class="sxs-lookup"><span data-stu-id="61f7b-119">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="61f7b-120">它們的建立和處理方式與標準工具提示的方式大致相同。</span><span class="sxs-lookup"><span data-stu-id="61f7b-120">They are created and handled in much the same way as standard tooltips.</span></span> <br/> |
| [<span data-ttu-id="61f7b-121">如何執行狀態列圖示的工具提示</span><span class="sxs-lookup"><span data-stu-id="61f7b-121">How to Implement Tooltips for Status Bar Icons</span></span>](implement-tooltips-for-status-bar-icons.md)<br/> | <span data-ttu-id="61f7b-122">顯示狀態列圖示之解釋性訊息的不造成干擾方式是執行工具提示。</span><span class="sxs-lookup"><span data-stu-id="61f7b-122">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="61f7b-123">按一下時，工具提示就會消失，但是您也可以指定超時值。</span><span class="sxs-lookup"><span data-stu-id="61f7b-123">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span> <br/>                                                                                |
| [<span data-ttu-id="61f7b-124">如何執行 In-Place 工具提示</span><span class="sxs-lookup"><span data-stu-id="61f7b-124">How to Implement In-Place Tooltips</span></span>](implement-in-place-tooltips.md)<br/>                         | <span data-ttu-id="61f7b-125">就地工具提示是用來顯示已裁剪之物件的文字字串。</span><span class="sxs-lookup"><span data-stu-id="61f7b-125">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="61f7b-126">如需圖例，請參閱 [關於工具提示控制項](tooltip-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="61f7b-126">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span> <br/>                                                                                                      |



 

 

 





