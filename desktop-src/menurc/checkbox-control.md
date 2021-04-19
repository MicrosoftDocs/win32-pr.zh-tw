---
title: 'CHECKBOX 控制項 (資源編譯器) '
description: 定義核取方塊控制項。
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- CHECKBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965838"
---
# <a name="checkbox-control"></a><span data-ttu-id="0cec2-104">CHECKBOX 控制項</span><span class="sxs-lookup"><span data-stu-id="0cec2-104">CHECKBOX control</span></span>

<span data-ttu-id="0cec2-105">定義核取方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="0cec2-105">Defines a check box control.</span></span> <span data-ttu-id="0cec2-106">控制項是一個小型矩形 (核取方塊) ，其旁邊會顯示指定的文字 (通常是右邊) 。</span><span class="sxs-lookup"><span data-stu-id="0cec2-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="0cec2-107">當使用者選取控制項時，控制項會反白顯示矩形，並將訊息傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="0cec2-107">When the user selects the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="0cec2-108">**CHECKBOX** 語句（只能在 [**DIALOGEX**](dialogex-resource.md)語句中使用）會定義控制項的文字、識別碼、維度和屬性。</span><span class="sxs-lookup"><span data-stu-id="0cec2-108">The **CHECKBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0cec2-109"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="0cec2-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="0cec2-110">要在控制項右邊顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="0cec2-110">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0cec2-111"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="0cec2-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0cec2-112">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="0cec2-112">Control styles.</span></span> <span data-ttu-id="0cec2-113">這個值可以是按鈕類別樣式 **BS \_ 核取方塊** 和 **ws \_ TABSTOP** 和 **ws \_ GROUP** 樣式的組合。</span><span class="sxs-lookup"><span data-stu-id="0cec2-113">This value can be a combination of the button class style **BS\_CHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="0cec2-114">如果您未指定樣式，則預設樣式為 `BS_CHECKBOX | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="0cec2-114">If you do not specify a style, the default style is `BS_CHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="0cec2-115">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="0cec2-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0cec2-116">範例</span><span class="sxs-lookup"><span data-stu-id="0cec2-116">Examples</span></span>

<span data-ttu-id="0cec2-117">這個範例會定義標記為斜體的核取方塊控制項：</span><span class="sxs-lookup"><span data-stu-id="0cec2-117">This example defines a check-box control that is labeled Italic:</span></span>

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="0cec2-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cec2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cec2-119">**AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="0cec2-119">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="0cec2-120">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="0cec2-120">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="0cec2-121">核取方塊</span><span class="sxs-lookup"><span data-stu-id="0cec2-121">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="0cec2-122">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="0cec2-122">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="0cec2-123">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="0cec2-123">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 