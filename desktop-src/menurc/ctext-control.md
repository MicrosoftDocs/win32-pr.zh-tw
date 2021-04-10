---
title: CTEXT 控制項
description: 定義中央文字控制項。
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- CTEXT 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092688"
---
# <a name="ctext-control"></a><span data-ttu-id="62722-104">CTEXT 控制項</span><span class="sxs-lookup"><span data-stu-id="62722-104">CTEXT control</span></span>

<span data-ttu-id="62722-105">定義中央文字控制項。</span><span class="sxs-lookup"><span data-stu-id="62722-105">Defines a centered-text control.</span></span> <span data-ttu-id="62722-106">控制項是一個簡單的矩形，可顯示以矩形為中心的指定文字。</span><span class="sxs-lookup"><span data-stu-id="62722-106">The control is a simple rectangle displaying the given text centered in the rectangle.</span></span> <span data-ttu-id="62722-107">文字會在顯示之前格式化。</span><span class="sxs-lookup"><span data-stu-id="62722-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="62722-108">延伸超過行尾的單字會自動換行到下一行的開頭。</span><span class="sxs-lookup"><span data-stu-id="62722-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="62722-109">長度超過控制項寬度的文字會被截斷。</span><span class="sxs-lookup"><span data-stu-id="62722-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="62722-110">[**LTEXT**](ltext-control.md)語句只能用在 rep 語句中，可定義控制項的文字、識別碼、維度和屬性。</span><span class="sxs-lookup"><span data-stu-id="62722-110">The [**LTEXT**](ltext-control.md) statement, which can be used only in a rep statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="62722-111"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="62722-111"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="62722-112">要置於控制項矩形區域中的文字。</span><span class="sxs-lookup"><span data-stu-id="62722-112">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="62722-113"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="62722-113"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="62722-114">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="62722-114">Control styles.</span></span> <span data-ttu-id="62722-115">這個值可以是下列樣式的任意組合： **SS \_ CENTER**、 **WS \_ TABSTOP** 和 **WS \_ GROUP**。</span><span class="sxs-lookup"><span data-stu-id="62722-115">This value can be any combination of the following styles: **SS\_CENTER**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="62722-116">如果您未指定樣式，則預設樣式為 `SS_CENTER | WS_GROUP` 。</span><span class="sxs-lookup"><span data-stu-id="62722-116">If you do not specify a style, the default style is `SS_CENTER | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="62722-117">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="62722-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="62722-118">範例</span><span class="sxs-lookup"><span data-stu-id="62722-118">Examples</span></span>

<span data-ttu-id="62722-119">此範例會定義標示為 Filename 的中央文字控制項：</span><span class="sxs-lookup"><span data-stu-id="62722-119">This example defines a centered-text control that is labeled Filename:</span></span>

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a><span data-ttu-id="62722-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62722-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62722-121">**控制**</span><span class="sxs-lookup"><span data-stu-id="62722-121">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="62722-122">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="62722-122">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="62722-123">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="62722-123">**LTEXT**</span></span>](ltext-control.md)
</dt> <dt>

[<span data-ttu-id="62722-124">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="62722-124">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 