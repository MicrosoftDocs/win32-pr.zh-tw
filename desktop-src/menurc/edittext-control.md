---
title: EDITTEXT 控制項
description: 定義屬於編輯類別的編輯控制項。
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- EDITTEXT 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682002"
---
# <a name="edittext-control"></a><span data-ttu-id="482d8-104">EDITTEXT 控制項</span><span class="sxs-lookup"><span data-stu-id="482d8-104">EDITTEXT control</span></span>

<span data-ttu-id="482d8-105">定義屬於編輯類別的編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="482d8-105">Defines an edit control belonging to the EDIT class.</span></span> <span data-ttu-id="482d8-106">它會建立一個矩形區域，讓使用者可以在其中輸入和編輯文字。</span><span class="sxs-lookup"><span data-stu-id="482d8-106">It creates a rectangular region in which the user can type and edit text.</span></span> <span data-ttu-id="482d8-107">當使用者按一下滑鼠時，控制項會顯示資料指標。</span><span class="sxs-lookup"><span data-stu-id="482d8-107">The control displays a cursor when the user clicks the mouse in it.</span></span> <span data-ttu-id="482d8-108">使用者接著可以使用鍵盤來輸入文字或編輯現有文字。</span><span class="sxs-lookup"><span data-stu-id="482d8-108">The user can then use the keyboard to enter text or edit the existing text.</span></span> <span data-ttu-id="482d8-109">編輯索引鍵包括倒退鍵和刪除鍵。</span><span class="sxs-lookup"><span data-stu-id="482d8-109">Editing keys include the BACKSPACE and DELETE keys.</span></span> <span data-ttu-id="482d8-110">使用者也可以使用滑鼠來選取要刪除的字元，或選取要插入新字元的位置。</span><span class="sxs-lookup"><span data-stu-id="482d8-110">The user can also use the mouse to select characters to be deleted or to select the place to insert new characters.</span></span>

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="482d8-111"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="482d8-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="482d8-112">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="482d8-112">Control styles.</span></span> <span data-ttu-id="482d8-113">這個值可以是編輯類別樣式和下列樣式的組合： **WS \_ TABSTOP**、 **ws \_ GROUP**、 **ws \_ VSCROLL**、 **ws \_ HSCROLL** 和 **ws \_ DISABLED**。</span><span class="sxs-lookup"><span data-stu-id="482d8-113">This value can be a combination of the edit class styles and the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, **WS\_HSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="482d8-114">如果您未指定樣式，則預設樣式為 `ES_LEFT | WS_BORDER | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="482d8-114">If you do not specify a style, the default style is `ES_LEFT | WS_BORDER | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="482d8-115">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="482d8-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="482d8-116">範例</span><span class="sxs-lookup"><span data-stu-id="482d8-116">Examples</span></span>

<span data-ttu-id="482d8-117">下列範例示範如何使用 **EDITTEXT** 語句：</span><span class="sxs-lookup"><span data-stu-id="482d8-117">The following example demonstrates the use of the **EDITTEXT** statement:</span></span>

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="482d8-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="482d8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="482d8-119">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="482d8-119">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> </dl>

 

 