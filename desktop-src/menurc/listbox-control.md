---
title: 'LISTBOX 控制項 (功能表和其他資源) '
description: 定義用於對話方塊或視窗的常用控制項。 控制項是包含字串清單的矩形， (例如可供使用者選取的檔案名) 。
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- LISTBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092715"
---
# <a name="listbox-control"></a><span data-ttu-id="1a0f4-105">LISTBOX 控制項</span><span class="sxs-lookup"><span data-stu-id="1a0f4-105">LISTBOX control</span></span>

<span data-ttu-id="1a0f4-106">定義用於對話方塊或視窗的常用控制項。</span><span class="sxs-lookup"><span data-stu-id="1a0f4-106">Defines commonly used controls for a dialog box or window.</span></span> <span data-ttu-id="1a0f4-107">控制項是包含字串清單的矩形， (例如可供使用者選取的檔案名) 。</span><span class="sxs-lookup"><span data-stu-id="1a0f4-107">The control is a rectangle containing a list of strings (such as filenames) from which the user can select.</span></span>

<span data-ttu-id="1a0f4-108">**LISTBOX** 語句（只能用在 [**DIALOGEX**](dialogex-resource.md)或 **WINDOW** 語句中）會定義控制項視窗的識別碼、維度和屬性。</span><span class="sxs-lookup"><span data-stu-id="1a0f4-108">The **LISTBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) or **WINDOW** statement, defines the identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="1a0f4-109"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="1a0f4-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="1a0f4-110">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="1a0f4-110">Control styles.</span></span> <span data-ttu-id="1a0f4-111">這個值可以是清單方塊類別樣式和下列任何樣式的組合： **WS \_ BORDER** 和 **ws \_ VSCROLL**。</span><span class="sxs-lookup"><span data-stu-id="1a0f4-111">This value can be a combination of the list-box class styles and any of the following styles: **WS\_BORDER** and **WS\_VSCROLL**.</span></span>

<span data-ttu-id="1a0f4-112">如果您未指定樣式，則預設樣式為 `LBS_NOTIFY | WS_BORDER` 。</span><span class="sxs-lookup"><span data-stu-id="1a0f4-112">If you do not specify a style, the default style is `LBS_NOTIFY | WS_BORDER`.</span></span>

</dd> </dl>

<span data-ttu-id="1a0f4-113">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="1a0f4-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1a0f4-114">範例</span><span class="sxs-lookup"><span data-stu-id="1a0f4-114">Examples</span></span>

<span data-ttu-id="1a0f4-115">此範例會定義識別碼為101的清單方塊控制項：</span><span class="sxs-lookup"><span data-stu-id="1a0f4-115">This example defines a list-box control whose identifier is 101:</span></span>

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="1a0f4-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a0f4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a0f4-117">**組合**</span><span class="sxs-lookup"><span data-stu-id="1a0f4-117">**COMBOBOX**</span></span>](combobox-control.md)
</dt> <dt>

[<span data-ttu-id="1a0f4-118">清單方塊</span><span class="sxs-lookup"><span data-stu-id="1a0f4-118">List Boxes</span></span>](../controls/about-list-boxes.md)
</dt> </dl>

 

 