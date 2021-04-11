---
title: 選項按鈕控制項
description: 定義選項按鈕控制項。
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- 選項按鈕控制項功能表和其他資源
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023475"
---
# <a name="radiobutton-control"></a><span data-ttu-id="6a1a0-104">選項按鈕控制項</span><span class="sxs-lookup"><span data-stu-id="6a1a0-104">RADIOBUTTON control</span></span>

<span data-ttu-id="6a1a0-105">定義選項按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="6a1a0-105">Defines a radio-button control.</span></span> <span data-ttu-id="6a1a0-106">控制項是一個小圓圈，其旁邊會顯示指定的文字，通常會顯示在右邊。</span><span class="sxs-lookup"><span data-stu-id="6a1a0-106">The control is a small circle that has the given text displayed next to it, typically to its right.</span></span> <span data-ttu-id="6a1a0-107">控制項會在使用者選取按鈕時，反白顯示圓形並將訊息傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="6a1a0-107">The control highlights the circle and sends a message to its parent window when the user selects the button.</span></span> <span data-ttu-id="6a1a0-108">控制項會移除反白顯示，並在下一次選取按鈕時傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="6a1a0-108">The control removes the highlight and sends a message when the button is next selected.</span></span>

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="6a1a0-109"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="6a1a0-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="6a1a0-110">選項按鈕的樣式，可以是按鈕類別樣式和下列樣式的組合： **ws \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。</span><span class="sxs-lookup"><span data-stu-id="6a1a0-110">Styles for the radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="6a1a0-111">如果您未指定樣式，則預設樣式為 `BS_RADIOBUTTON | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="6a1a0-111">If you do not specify a style, the default style is `BS_RADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="6a1a0-112">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6a1a0-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6a1a0-113">範例</span><span class="sxs-lookup"><span data-stu-id="6a1a0-113">Examples</span></span>

<span data-ttu-id="6a1a0-114">下列範例示範如何使用 **選項按鈕** 語句：</span><span class="sxs-lookup"><span data-stu-id="6a1a0-114">The following example demonstrates the use of the **RADIOBUTTON** statement:</span></span>

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="6a1a0-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a1a0-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1a0-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="6a1a0-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="6a1a0-117">選項按鈕</span><span class="sxs-lookup"><span data-stu-id="6a1a0-117">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 