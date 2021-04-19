---
title: DEFPUSHBUTTON 控制項
description: 定義預設的按鈕控制項。
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- DEFPUSHBUTTON 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965625"
---
# <a name="defpushbutton-control"></a><span data-ttu-id="7c244-104">DEFPUSHBUTTON 控制項</span><span class="sxs-lookup"><span data-stu-id="7c244-104">DEFPUSHBUTTON control</span></span>

<span data-ttu-id="7c244-105">定義預設的按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="7c244-105">Defines a default push-button control.</span></span> <span data-ttu-id="7c244-106">控制項是具有粗體外框的小矩形，代表使用者的預設回應。</span><span class="sxs-lookup"><span data-stu-id="7c244-106">The control is a small rectangle with a bold outline that represents the default response for the user.</span></span> <span data-ttu-id="7c244-107">指定的文字會顯示在按鈕內。</span><span class="sxs-lookup"><span data-stu-id="7c244-107">The given text is displayed inside the button.</span></span> <span data-ttu-id="7c244-108">控制項會在使用者按一下按鈕時，以一般方式反白顯示按鈕，並將訊息傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="7c244-108">The control highlights the button in the usual way when the user clicks the mouse in it and sends a message to its parent window.</span></span>

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="7c244-109"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="7c244-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="7c244-110">要置於控制項矩形區域中的文字。</span><span class="sxs-lookup"><span data-stu-id="7c244-110">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="7c244-111"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="7c244-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="7c244-112">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="7c244-112">Control styles.</span></span> <span data-ttu-id="7c244-113">這個值可以是下列樣式的組合： **BS \_ DEFPUSHBUTTON**、 **WS \_ TABSTOP**、 **ws \_ GROUP** 和 **ws \_ DISABLED**。</span><span class="sxs-lookup"><span data-stu-id="7c244-113">This value can be a combination of the following styles: **BS\_DEFPUSHBUTTON**, **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="7c244-114">如果您未指定樣式，則預設樣式為 `BS_DEFPUSHBUTTON | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="7c244-114">If you do not specify a style, the default style is `BS_DEFPUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="7c244-115">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="7c244-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7c244-116">範例</span><span class="sxs-lookup"><span data-stu-id="7c244-116">Examples</span></span>

<span data-ttu-id="7c244-117">這個範例會定義一個標示為 [取消] 的預設按鈕控制項：</span><span class="sxs-lookup"><span data-stu-id="7c244-117">This example defines a default push-button control that is labeled Cancel:</span></span>

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a><span data-ttu-id="7c244-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c244-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c244-119">推播按鈕</span><span class="sxs-lookup"><span data-stu-id="7c244-119">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="7c244-120">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="7c244-120">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> <dt>

[<span data-ttu-id="7c244-121">**RADIOBUTTON**</span><span class="sxs-lookup"><span data-stu-id="7c244-121">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




