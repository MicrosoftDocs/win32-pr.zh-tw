---
title: '分組控制項 (功能表和其他資源) '
description: 定義群組框控制項。 控制項是將其他控制項群組在一起的矩形。 控制項的分組方式是在其周圍繪製框線，並在左上角顯示指定的文字。
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- 分組控制功能表和其他資源
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104022787"
---
# <a name="groupbox-control"></a><span data-ttu-id="df7aa-106">分組控制項</span><span class="sxs-lookup"><span data-stu-id="df7aa-106">GROUPBOX control</span></span>

<span data-ttu-id="df7aa-107">定義群組框控制項。</span><span class="sxs-lookup"><span data-stu-id="df7aa-107">Defines a group box control.</span></span> <span data-ttu-id="df7aa-108">控制項是將其他控制項群組在一起的矩形。</span><span class="sxs-lookup"><span data-stu-id="df7aa-108">The control is a rectangle that groups other controls together.</span></span> <span data-ttu-id="df7aa-109">控制項的分組方式是在其周圍繪製框線，並在左上角顯示指定的文字。</span><span class="sxs-lookup"><span data-stu-id="df7aa-109">The controls are grouped by drawing a border around them and displaying the given text in the upper-left corner.</span></span>

<span data-ttu-id="df7aa-110">您只能在 [**DIALOGEX**](dialogex-resource.md)語句中使用的 **分組** 符號語句，會定義控制項視窗的文字、識別碼、維度和屬性。</span><span class="sxs-lookup"><span data-stu-id="df7aa-110">The **GROUPBOX** statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="df7aa-111"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="df7aa-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="df7aa-112">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="df7aa-112">Control styles.</span></span> <span data-ttu-id="df7aa-113">這個值可以是 button 類別樣式 **BS \_ 分組** 程式和 **ws \_ TABSTOP** 和 **ws \_ DISABLED** 樣式的組合。</span><span class="sxs-lookup"><span data-stu-id="df7aa-113">This value can be a combination of the button class style **BS\_GROUPBOX** and the **WS\_TABSTOP** and **WS\_DISABLED** styles.</span></span>

<span data-ttu-id="df7aa-114">如果您未指定樣式，則預設樣式為 **BS \_ 分組**。</span><span class="sxs-lookup"><span data-stu-id="df7aa-114">If you do not specify a style, the default style is **BS\_GROUPBOX**.</span></span>

</dd> </dl>

<span data-ttu-id="df7aa-115">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="df7aa-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df7aa-116">備註</span><span class="sxs-lookup"><span data-stu-id="df7aa-116">Remarks</span></span>

<span data-ttu-id="df7aa-117">當樣式包含 **WS \_ TABSTOP** 或文字指定快速鍵時，請將焦點移至群組內的第一個控制項，或按下快速鍵。</span><span class="sxs-lookup"><span data-stu-id="df7aa-117">When the style contains **WS\_TABSTOP** or the text specifies an accelerator, tabbing or pressing the accelerator key moves the focus to the first control within the group.</span></span>

## <a name="examples"></a><span data-ttu-id="df7aa-118">範例</span><span class="sxs-lookup"><span data-stu-id="df7aa-118">Examples</span></span>

<span data-ttu-id="df7aa-119">這個範例會定義一個標示為 [選項] 的群組方塊控制項：</span><span class="sxs-lookup"><span data-stu-id="df7aa-119">This example defines a group-box control that is labeled Options:</span></span>

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="df7aa-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df7aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df7aa-121">群組方塊</span><span class="sxs-lookup"><span data-stu-id="df7aa-121">Group Boxes</span></span>](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




