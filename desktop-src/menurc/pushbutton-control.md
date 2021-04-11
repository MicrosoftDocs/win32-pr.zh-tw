---
title: '將控制項按鈕 (功能表和其他資源) '
description: 定義按鈕控制項。 控制項是包含指定文字的圓角矩形。 文字是在控制項的中央。 每當使用者選擇控制項時，控制項會將訊息傳送到其父系。
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- 按鈕控制功能表和其他資源
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315130"
---
# <a name="pushbutton-control"></a><span data-ttu-id="9ea33-107">按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="9ea33-107">PUSHBUTTON control</span></span>

<span data-ttu-id="9ea33-108">定義按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="9ea33-108">Defines a push-button control.</span></span> <span data-ttu-id="9ea33-109">控制項是包含指定文字的圓角矩形。</span><span class="sxs-lookup"><span data-stu-id="9ea33-109">The control is a round-cornered rectangle containing the given text.</span></span> <span data-ttu-id="9ea33-110">文字是在控制項的中央。</span><span class="sxs-lookup"><span data-stu-id="9ea33-110">The text is centered in the control.</span></span> <span data-ttu-id="9ea33-111">每當使用者選擇控制項時，控制項會將訊息傳送到其父系。</span><span class="sxs-lookup"><span data-stu-id="9ea33-111">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="9ea33-112"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="9ea33-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="9ea33-113">按鍵的樣式，可以是 **BS \_ 按鈕** 樣式和下列樣式的組合： **WS \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。</span><span class="sxs-lookup"><span data-stu-id="9ea33-113">Styles for the pushbutton, which can be a combination of the **BS\_PUSHBUTTON** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="9ea33-114">如果您未指定樣式，則預設樣式為 `BS_PUSHBUTTON | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="9ea33-114">If you do not specify a style, the default style is `BS_PUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="9ea33-115">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="9ea33-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9ea33-116">範例</span><span class="sxs-lookup"><span data-stu-id="9ea33-116">Examples</span></span>

<span data-ttu-id="9ea33-117">下列範例示範如何使用 **按鈕** 語句：</span><span class="sxs-lookup"><span data-stu-id="9ea33-117">The following example demonstrates the use of the **PUSHBUTTON** statement:</span></span>

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a><span data-ttu-id="9ea33-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ea33-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea33-119">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="9ea33-119">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="9ea33-120">推播按鈕</span><span class="sxs-lookup"><span data-stu-id="9ea33-120">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 