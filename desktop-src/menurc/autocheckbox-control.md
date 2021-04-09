---
title: AUTOCHECKBOX 控制項
description: 定義自動核取方塊控制項。
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- AUTOCHECKBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681922"
---
# <a name="autocheckbox-control"></a><span data-ttu-id="e697d-104">AUTOCHECKBOX 控制項</span><span class="sxs-lookup"><span data-stu-id="e697d-104">AUTOCHECKBOX control</span></span>

<span data-ttu-id="e697d-105">定義自動核取方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="e697d-105">Defines an automatic check box control.</span></span> <span data-ttu-id="e697d-106">控制項是一個小型矩形 (核取方塊) ，其旁邊會顯示指定的文字 (通常是右邊) 。</span><span class="sxs-lookup"><span data-stu-id="e697d-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="e697d-107">當使用者選擇控制項時，控制項會反白顯示矩形，並將訊息傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="e697d-107">When the user chooses the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="e697d-108">**AUTOCHECKBOX** 語句只能用在 [**DIALOG**](dialog-resource.md)或 [**DIALOGEX**](dialogex-resource.md)語句的主體中。</span><span class="sxs-lookup"><span data-stu-id="e697d-108">The **AUTOCHECKBOX** statement can only be used in the body of a [**DIALOG**](dialog-resource.md) or [**DIALOGEX**](dialogex-resource.md) statement.</span></span>

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="e697d-109"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="e697d-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="e697d-110">控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="e697d-110">Styles of the control.</span></span> <span data-ttu-id="e697d-111">這個值可以是 button 類別樣式 **BS \_ AUTOCHECKBOX** 和 **ws \_ TABSTOP** 和 **ws \_ GROUP** 樣式的組合。</span><span class="sxs-lookup"><span data-stu-id="e697d-111">This value can be a combination of the button class style **BS\_AUTOCHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="e697d-112">如果您未指定樣式，則預設樣式為 `BS_AUTOCHECKBOX | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="e697d-112">If you do not specify a style, the default style is `BS_AUTOCHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="e697d-113">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="e697d-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e697d-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e697d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e697d-115">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="e697d-115">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="e697d-116">按鈕樣式</span><span class="sxs-lookup"><span data-stu-id="e697d-116">Button Styles</span></span>](../controls/button-styles.md)
</dt> <dt>

[<span data-ttu-id="e697d-117">**相應**</span><span class="sxs-lookup"><span data-stu-id="e697d-117">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="e697d-118">**控制**</span><span class="sxs-lookup"><span data-stu-id="e697d-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="e697d-119">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="e697d-119">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 