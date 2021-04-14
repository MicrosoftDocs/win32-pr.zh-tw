---
title: 'COMBOBOX 控制項 (功能表和其他資源) '
description: 定義 (下拉式方塊的下拉式方塊控制項) 。
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- COMBOBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375100"
---
# <a name="combobox-control"></a><span data-ttu-id="1f909-104">COMBOBOX 控制項</span><span class="sxs-lookup"><span data-stu-id="1f909-104">COMBOBOX control</span></span>

<span data-ttu-id="1f909-105">定義 (下拉式方塊的下拉式方塊控制項) 。</span><span class="sxs-lookup"><span data-stu-id="1f909-105">Defines a combination box control (a combo box).</span></span> <span data-ttu-id="1f909-106">下拉式方塊是由靜態文字方塊或與清單方塊結合的編輯方塊所組成。</span><span class="sxs-lookup"><span data-stu-id="1f909-106">A combo box consists of either a static text box or an edit box combined with a list box.</span></span> <span data-ttu-id="1f909-107">清單方塊可以隨時顯示，或由使用者向下提取。</span><span class="sxs-lookup"><span data-stu-id="1f909-107">The list box can be displayed at all times or pulled down by the user.</span></span> <span data-ttu-id="1f909-108">如果下拉式方塊包含 [靜態] 文字方塊，文字方塊的清單方塊部分中的任何) ，文字方塊一律會顯示選取 (。</span><span class="sxs-lookup"><span data-stu-id="1f909-108">If the combo box contains a static text box, the text box always displays the selection (if any) in the list box portion of the combo box.</span></span> <span data-ttu-id="1f909-109">如果它使用編輯方塊，使用者可以輸入所需的選取專案;如果任何符合使用者在編輯方塊中輸入的) ，清單方塊會反白顯示第一個專案 (。</span><span class="sxs-lookup"><span data-stu-id="1f909-109">If it uses an edit box, the user can type in the desired selection; the list box highlights the first item (if any) that matches what the user has entered in the edit box.</span></span> <span data-ttu-id="1f909-110">然後，使用者可以選取清單方塊中反白顯示的專案來完成選擇。</span><span class="sxs-lookup"><span data-stu-id="1f909-110">The user can then select the item highlighted in the list box to complete the choice.</span></span> <span data-ttu-id="1f909-111">此外，下拉式方塊也可以是主控描繪，也可以是固定或可變高度。</span><span class="sxs-lookup"><span data-stu-id="1f909-111">In addition, the combo box can be owner-drawn and of fixed or variable height.</span></span>

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="1f909-112"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="1f909-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="1f909-113">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="1f909-113">Control styles.</span></span> <span data-ttu-id="1f909-114">這個值可以是 COMBOBOX 類別樣式和下列任何樣式的組合： **WS \_ TABSTOP**、 **ws \_ GROUP**、 **ws \_ VSCROLL** 和 **ws \_ DISABLED**。</span><span class="sxs-lookup"><span data-stu-id="1f909-114">This value can be a combination of the COMBOBOX class styles and any of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="1f909-115">如果您未指定樣式，則預設樣式為 `CBS_SIMPLE | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="1f909-115">If you do not specify a style, the default style is `CBS_SIMPLE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="1f909-116">*Height* 參數適用于下拉式方塊的高度，且下拉式清單完全展開。</span><span class="sxs-lookup"><span data-stu-id="1f909-116">The *height* parameter applies to the height of a combo box with a drop-down list fully expanded.</span></span>

<span data-ttu-id="1f909-117">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="1f909-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1f909-118">範例</span><span class="sxs-lookup"><span data-stu-id="1f909-118">Examples</span></span>

<span data-ttu-id="1f909-119">這個範例會定義具有垂直捲動條的下拉式方塊控制項：</span><span class="sxs-lookup"><span data-stu-id="1f909-119">This example defines a combo-box control with a vertical scroll bar:</span></span>

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a><span data-ttu-id="1f909-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f909-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f909-121">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="1f909-121">Combo Boxes</span></span>](../controls/about-combo-boxes.md)
</dt> </dl>

 

 