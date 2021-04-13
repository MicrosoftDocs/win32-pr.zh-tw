---
title: STYLE 語句
description: 定義對話方塊的視窗樣式。 視窗樣式會指定方塊是快顯視窗或子視窗。
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- 樣式語句功能表和其他資源
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375193"
---
# <a name="style-statement"></a><span data-ttu-id="bb6e8-105">STYLE 語句</span><span class="sxs-lookup"><span data-stu-id="bb6e8-105">STYLE statement</span></span>

<span data-ttu-id="bb6e8-106">定義對話方塊的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="bb6e8-106">Defines the window style of the dialog box.</span></span> <span data-ttu-id="bb6e8-107">視窗樣式會指定方塊是快顯視窗或子視窗。</span><span class="sxs-lookup"><span data-stu-id="bb6e8-107">The window style specifies whether the box is a pop-up or a child window.</span></span>

``` syntax
STYLE style
```

<dl> <dt>

<span data-ttu-id="bb6e8-108"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="bb6e8-108"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="bb6e8-109">視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="bb6e8-109">The window style.</span></span> <span data-ttu-id="bb6e8-110">這個參數可以是整數值，也可以是視窗樣式值的組合 (例如 **ws \_ 標題** 和 **WS \_ SYSMENU**) 和對話方塊樣式值 (例如 **DS \_ CENTER**) 。</span><span class="sxs-lookup"><span data-stu-id="bb6e8-110">This parameter can be an integer value or a combination of window style values (such as **WS\_CAPTION** and **WS\_SYSMENU**) and dialog box style values (such as **DS\_CENTER**).</span></span>

</dd> </dl>

<span data-ttu-id="bb6e8-111">如需視窗樣式的清單，請參閱 [視窗樣式](/windows/desktop/winmsg/window-styles)。</span><span class="sxs-lookup"><span data-stu-id="bb6e8-111">For a list of window styles, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span> <span data-ttu-id="bb6e8-112">如需對話方塊樣式的清單，請參閱 [對話方塊範本樣式](../dlgbox/about-dialog-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="bb6e8-112">For a list of dialog box styles, see [Dialog Box Template Styles](../dlgbox/about-dialog-boxes.md).</span></span> <span data-ttu-id="bb6e8-113">如果您使用視窗或對話方塊的樣式值，就必須包含 Windows .h。</span><span class="sxs-lookup"><span data-stu-id="bb6e8-113">If you use the window or dialog box style values, you must include Windows.h.</span></span>

 

 