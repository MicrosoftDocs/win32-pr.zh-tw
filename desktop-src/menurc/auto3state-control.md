---
title: AUTO3STATE 控制項
description: 會定義三個自動狀態的核取方塊。
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- AUTO3STATE 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092690"
---
# <a name="auto3state-control"></a><span data-ttu-id="3eab2-104">AUTO3STATE 控制項</span><span class="sxs-lookup"><span data-stu-id="3eab2-104">AUTO3STATE control</span></span>

<span data-ttu-id="3eab2-105">會定義三個自動狀態的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="3eab2-105">Defines an automatic three-state check box.</span></span> <span data-ttu-id="3eab2-106">控制項是一個開啟方塊，其中指定的文字位於方塊右邊。</span><span class="sxs-lookup"><span data-stu-id="3eab2-106">The control is an open box with the given text positioned to the right of the box.</span></span> <span data-ttu-id="3eab2-107">選擇時，方塊會自動在三個狀態之間前進：已核取、未選取和停用的 (灰色) 。</span><span class="sxs-lookup"><span data-stu-id="3eab2-107">When chosen, the box automatically advances between three states: checked, unchecked, and disabled (grayed).</span></span> <span data-ttu-id="3eab2-108">每當使用者選擇控制項時，控制項會將訊息傳送到其父系。</span><span class="sxs-lookup"><span data-stu-id="3eab2-108">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="3eab2-109"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="3eab2-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="3eab2-110">控制項的樣式，可以是 **BS \_ AUTO3STATE** 樣式和下列樣式的組合： **ws \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。</span><span class="sxs-lookup"><span data-stu-id="3eab2-110">Styles for the control, which can be a combination of the **BS\_AUTO3STATE** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="3eab2-111">如果您未指定樣式，則預設樣式為 `BS_AUTO3STATE | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="3eab2-111">If you do not specify a style, the default style is `BS_AUTO3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="3eab2-112">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="3eab2-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3eab2-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3eab2-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eab2-114">**AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="3eab2-114">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="3eab2-115">核取方塊</span><span class="sxs-lookup"><span data-stu-id="3eab2-115">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="3eab2-116">**相應**</span><span class="sxs-lookup"><span data-stu-id="3eab2-116">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="3eab2-117">**控制**</span><span class="sxs-lookup"><span data-stu-id="3eab2-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="3eab2-118">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="3eab2-118">**STATE3**</span></span>](state3-control.md)
</dt> <dt>

[<span data-ttu-id="3eab2-119">視窗樣式</span><span class="sxs-lookup"><span data-stu-id="3eab2-119">Window Styles</span></span>](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 