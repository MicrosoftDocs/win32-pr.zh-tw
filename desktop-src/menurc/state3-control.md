---
title: STATE3 控制項
description: 定義三個狀態的核取方塊控制項。 控制項與核取方塊相同，不同之處在于它有三個已核取、未選取和停用的狀態 (灰色) 。
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- STATE3 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678287"
---
# <a name="state3-control"></a><span data-ttu-id="efaa8-105">STATE3 控制項</span><span class="sxs-lookup"><span data-stu-id="efaa8-105">STATE3 control</span></span>

<span data-ttu-id="efaa8-106">定義三個狀態的核取方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="efaa8-106">Defines a three-state check box control.</span></span> <span data-ttu-id="efaa8-107">控制項與 [**核取方塊**](checkbox-control.md)相同，不同之處在于它有三種狀態： [已選取]、[未選取] 和 [已停用] (灰色) 。</span><span class="sxs-lookup"><span data-stu-id="efaa8-107">The control is identical to a [**CHECKBOX**](checkbox-control.md), except that it has three states: checked, unchecked, and disabled (grayed).</span></span>

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="efaa8-108"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="efaa8-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="efaa8-109">要在控制項右邊顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="efaa8-109">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="efaa8-110"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="efaa8-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="efaa8-111">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="efaa8-111">Control styles.</span></span> <span data-ttu-id="efaa8-112">這個值可以是 button 類別樣式 **BS \_ 3STATE** 和 **ws \_ TABSTOP** 和 **ws \_ GROUP** 樣式的組合。</span><span class="sxs-lookup"><span data-stu-id="efaa8-112">This value can be a combination of the button class style **BS\_3STATE** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="efaa8-113">如果您未指定樣式，則預設樣式為 `BS_3STATE | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="efaa8-113">If you do not specify a style, the default style is `BS_3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="efaa8-114">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="efaa8-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="efaa8-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="efaa8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efaa8-116">**AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="efaa8-116">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="efaa8-117">核取方塊</span><span class="sxs-lookup"><span data-stu-id="efaa8-117">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="efaa8-118">**相應**</span><span class="sxs-lookup"><span data-stu-id="efaa8-118">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="efaa8-119">**控制**</span><span class="sxs-lookup"><span data-stu-id="efaa8-119">**CONTROL**</span></span>](control-control.md)
</dt> </dl>

 

 




