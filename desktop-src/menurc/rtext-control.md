---
title: RTEXT 控制項
description: 定義靠右對齊的文字控制項。
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- RTEXT 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463133"
---
# <a name="rtext-control"></a><span data-ttu-id="14251-104">RTEXT 控制項</span><span class="sxs-lookup"><span data-stu-id="14251-104">RTEXT control</span></span>

<span data-ttu-id="14251-105">定義靠右對齊的文字控制項。</span><span class="sxs-lookup"><span data-stu-id="14251-105">Defines a right-aligned text control.</span></span> <span data-ttu-id="14251-106">控制項是一個簡單的矩形，可在矩形中顯示指定的文字（靠右對齊）。</span><span class="sxs-lookup"><span data-stu-id="14251-106">The control is a simple rectangle displaying the given text right-aligned in the rectangle.</span></span> <span data-ttu-id="14251-107">文字會在顯示之前格式化。</span><span class="sxs-lookup"><span data-stu-id="14251-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="14251-108">延伸超過行尾的單字會自動換行到下一行的開頭。</span><span class="sxs-lookup"><span data-stu-id="14251-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="14251-109">長度超過控制項寬度的文字會被截斷。</span><span class="sxs-lookup"><span data-stu-id="14251-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="14251-110">**RTEXT** 語句只能用在 [**DIALOGEX**](dialogex-resource.md)語句中，可定義控制項的文字、識別碼、維度和屬性。</span><span class="sxs-lookup"><span data-stu-id="14251-110">The **RTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="14251-111"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="14251-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="14251-112">文字控制項的樣式，可以是下列各項的任意組合： **WS \_ TABSTOP** 和 **WS \_ GROUP**。</span><span class="sxs-lookup"><span data-stu-id="14251-112">Styles for the text control, which can be any combination of the following: **WS\_TABSTOP** and **WS\_GROUP**.</span></span>

<span data-ttu-id="14251-113">如果您未指定樣式，則預設樣式為 `SS_RIGHT | WS_GROUP` 。</span><span class="sxs-lookup"><span data-stu-id="14251-113">If you do not specify a style, the default style is `SS_RIGHT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="14251-114">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="14251-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="14251-115">範例</span><span class="sxs-lookup"><span data-stu-id="14251-115">Examples</span></span>

<span data-ttu-id="14251-116">下列範例示範如何使用 **RTEXT** 語句：</span><span class="sxs-lookup"><span data-stu-id="14251-116">The following example demonstrates the use of the **RTEXT** statement:</span></span>

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="14251-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14251-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14251-118">**控制**</span><span class="sxs-lookup"><span data-stu-id="14251-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="14251-119">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="14251-119">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="14251-120">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="14251-120">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="14251-121">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="14251-121">**LTEXT**</span></span>](ltext-control.md)
</dt> </dl>

 

 