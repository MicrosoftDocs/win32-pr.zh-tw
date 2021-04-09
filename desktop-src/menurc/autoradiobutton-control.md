---
title: AUTORADIOBUTTON 控制項
description: 定義自動選項按鈕控制項。 此控制項會自動與相同群組中的其他 AUTORADIOBUTTON 控制項執行互斥。 選擇按鈕時，應用程式會在按下 BN 時收到通知 \_ 。
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- AUTORADIOBUTTON 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678435"
---
# <a name="autoradiobutton-control"></a><span data-ttu-id="d5f72-106">AUTORADIOBUTTON 控制項</span><span class="sxs-lookup"><span data-stu-id="d5f72-106">AUTORADIOBUTTON control</span></span>

<span data-ttu-id="d5f72-107">定義自動選項按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="d5f72-107">Defines an automatic radio button control.</span></span> <span data-ttu-id="d5f72-108">此控制項會自動與相同群組中的其他 **AUTORADIOBUTTON** 控制項執行互斥。</span><span class="sxs-lookup"><span data-stu-id="d5f72-108">This control automatically performs mutual exclusion with the other **AUTORADIOBUTTON** controls in the same group.</span></span> <span data-ttu-id="d5f72-109">選擇按鈕時，應用程式會在按下 **BN 時 \_** 收到通知。</span><span class="sxs-lookup"><span data-stu-id="d5f72-109">When the button is chosen, the application is notified with **BN\_CLICKED**.</span></span>

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="d5f72-110"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="d5f72-110"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="d5f72-111">將顯示在選項按鈕旁的文字。</span><span class="sxs-lookup"><span data-stu-id="d5f72-111">Text that will appear next to the radio button.</span></span>

</dd> <dt>

<span data-ttu-id="d5f72-112"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="d5f72-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="d5f72-113">自動選項按鈕的樣式，可以是按鈕類別樣式和下列樣式的組合： **ws \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。</span><span class="sxs-lookup"><span data-stu-id="d5f72-113">Styles for the automatic radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="d5f72-114">如果您未指定樣式，則預設樣式為 `BS_AUTORADIOBUTTON | WS_TABSTOP` 。</span><span class="sxs-lookup"><span data-stu-id="d5f72-114">If you do not specify a style, the default style is `BS_AUTORADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="d5f72-115">如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d5f72-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d5f72-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5f72-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f72-117">**控制**</span><span class="sxs-lookup"><span data-stu-id="d5f72-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="d5f72-118">選項按鈕</span><span class="sxs-lookup"><span data-stu-id="d5f72-118">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[<span data-ttu-id="d5f72-119">**RADIOBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d5f72-119">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




