---
title: LTEXT 控制項
description: 定義靠左對齊的文字控制項。
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- LTEXT 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969901"
---
# <a name="ltext-control"></a><span data-ttu-id="08572-104">LTEXT 控制項</span><span class="sxs-lookup"><span data-stu-id="08572-104">LTEXT control</span></span>

<span data-ttu-id="08572-105">定義靠左對齊的文字控制項。</span><span class="sxs-lookup"><span data-stu-id="08572-105">Defines a left-aligned text control.</span></span> <span data-ttu-id="08572-106">控制項是一個簡單的矩形，可顯示矩形中靠左對齊的指定文字。</span><span class="sxs-lookup"><span data-stu-id="08572-106">The control is a simple rectangle displaying the given text left-aligned in the rectangle.</span></span> <span data-ttu-id="08572-107">文字會在顯示之前格式化。</span><span class="sxs-lookup"><span data-stu-id="08572-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="08572-108">延伸超過行尾的單字會自動換行到下一行的開頭。</span><span class="sxs-lookup"><span data-stu-id="08572-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="08572-109">長度超過控制項寬度的文字會被截斷。</span><span class="sxs-lookup"><span data-stu-id="08572-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="08572-110">**LTEXT** 語句只能用在 [**DIALOGEX**](dialogex-resource.md)語句中，可定義控制項的文字、識別碼、維度和屬性。</span><span class="sxs-lookup"><span data-stu-id="08572-110">The **LTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="08572-111"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="08572-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="08572-112">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="08572-112">Control styles.</span></span> <span data-ttu-id="08572-113">這個值可以是 **BS \_ 選項按鈕** 樣式和下列樣式的任意組合： **SS \_ LEFT**、 **WS \_ TABSTOP** 和 **WS \_ GROUP**。</span><span class="sxs-lookup"><span data-stu-id="08572-113">This value can be any combination of the **BS\_RADIOBUTTON** style and the following styles: **SS\_LEFT**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="08572-114">如果您未指定樣式，則預設樣式為 `SS_LEFT | WS_GROUP` 。</span><span class="sxs-lookup"><span data-stu-id="08572-114">If you do not specify a style, the default style is `SS_LEFT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="08572-115">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="08572-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08572-116">範例</span><span class="sxs-lookup"><span data-stu-id="08572-116">Examples</span></span>

<span data-ttu-id="08572-117">這個範例會定義一個靠左對齊的文字控制項，其標示為 Filename：</span><span class="sxs-lookup"><span data-stu-id="08572-117">This example defines a left-aligned text control that is labeled Filename:</span></span>

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="08572-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08572-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08572-119">**控制**</span><span class="sxs-lookup"><span data-stu-id="08572-119">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="08572-120">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="08572-120">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="08572-121">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="08572-121">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="08572-122">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="08572-122">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 