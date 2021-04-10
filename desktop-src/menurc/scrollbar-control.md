---
title: 捲軸控制項
description: 定義捲軸控制項。
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- 捲軸控制項功能表和其他資源
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092729"
---
# <a name="scrollbar-control"></a><span data-ttu-id="cb697-104">捲軸控制項</span><span class="sxs-lookup"><span data-stu-id="cb697-104">SCROLLBAR control</span></span>

<span data-ttu-id="cb697-105">定義捲軸控制項。</span><span class="sxs-lookup"><span data-stu-id="cb697-105">Defines a scroll-bar control.</span></span> <span data-ttu-id="cb697-106">控制項是包含捲動方塊的矩形，而且兩端都有方向箭號。</span><span class="sxs-lookup"><span data-stu-id="cb697-106">The control is a rectangle that contains a scroll box and has direction arrows at both ends.</span></span> <span data-ttu-id="cb697-107">每當使用者按一下控制項中的滑鼠時，捲軸控制項就會將通知訊息傳送到其父系。</span><span class="sxs-lookup"><span data-stu-id="cb697-107">The scroll-bar control sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="cb697-108">父代負責更新捲動方塊的位置。</span><span class="sxs-lookup"><span data-stu-id="cb697-108">The parent is responsible for updating the scroll-box position.</span></span> <span data-ttu-id="cb697-109">捲軸控制項可放置在視窗中的任何位置，並在需要時用來提供滾動輸入。</span><span class="sxs-lookup"><span data-stu-id="cb697-109">Scroll-bar controls can be positioned anywhere in a window and used whenever needed to provide scrolling input.</span></span>

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="cb697-110"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="cb697-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="cb697-111">下列樣式的零或組合： **ws \_ TABSTOP**、 **ws \_ GROUP** 和 **WS \_ 已停用**。</span><span class="sxs-lookup"><span data-stu-id="cb697-111">Zero or a combination of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="cb697-112">除了這些樣式之外， *style* 參數可以包含捲軸類別樣式的 (或無) 的組合。</span><span class="sxs-lookup"><span data-stu-id="cb697-112">In addition to these styles, the *style* parameter may contain a combination (or none) of the SCROLLBAR-class styles.</span></span>

<span data-ttu-id="cb697-113">如果您未指定樣式，則預設樣式為 **SBS \_ HORZ**。</span><span class="sxs-lookup"><span data-stu-id="cb697-113">If you do not specify a style, the default style is **SBS\_HORZ**.</span></span>

</dd> </dl>

<span data-ttu-id="cb697-114">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="cb697-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span> <span data-ttu-id="cb697-115">請注意，您不能指定這個控制項的文字。</span><span class="sxs-lookup"><span data-stu-id="cb697-115">Note that you cannot specify text for this control.</span></span>

## <a name="examples"></a><span data-ttu-id="cb697-116">範例</span><span class="sxs-lookup"><span data-stu-id="cb697-116">Examples</span></span>

<span data-ttu-id="cb697-117">下列範例示範如何使用 **捲軸** 語句：</span><span class="sxs-lookup"><span data-stu-id="cb697-117">The following example demonstrates the use of the **SCROLLBAR** statement:</span></span>

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a><span data-ttu-id="cb697-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb697-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb697-119">捲軸</span><span class="sxs-lookup"><span data-stu-id="cb697-119">Scroll Bars</span></span>](../controls/about-scroll-bars.md)
</dt> </dl>

 

 