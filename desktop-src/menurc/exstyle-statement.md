---
title: EXSTYLE 語句
description: 定義對話方塊的延伸視窗樣式。 在資源定義中，EXSTYLE 語句會在資源定義主體開頭之前加上選擇性的語句。
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- EXSTYLE 語句功能表和其他資源
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463044"
---
# <a name="exstyle-statement"></a><span data-ttu-id="67b9e-105">EXSTYLE 語句</span><span class="sxs-lookup"><span data-stu-id="67b9e-105">EXSTYLE statement</span></span>

<span data-ttu-id="67b9e-106">定義對話方塊的延伸視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="67b9e-106">Defines extended window styles for a dialog box.</span></span> <span data-ttu-id="67b9e-107">在資源定義中， **EXSTYLE** 語句會在資源定義主體開頭之前加上選擇性的語句。</span><span class="sxs-lookup"><span data-stu-id="67b9e-107">In a resource definition, the **EXSTYLE** statement is placed with the optional statements before the beginning of the body of the resource definition.</span></span>

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span data-ttu-id="67b9e-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*擴充樣式*</span><span class="sxs-lookup"><span data-stu-id="67b9e-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="67b9e-109">對話方塊或控制項的擴充視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="67b9e-109">Extended window style for the dialog box or control.</span></span> <span data-ttu-id="67b9e-110">如需延伸視窗樣式的清單，請參閱 [**擴充的視窗樣式**](/windows/desktop/winmsg/extended-window-styles)。</span><span class="sxs-lookup"><span data-stu-id="67b9e-110">For a list of extended window styles, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67b9e-111">備註</span><span class="sxs-lookup"><span data-stu-id="67b9e-111">Remarks</span></span>

<span data-ttu-id="67b9e-112">對於控制項，擴充樣式是在控制項資源定義語句的 *style* 選項之後指定。</span><span class="sxs-lookup"><span data-stu-id="67b9e-112">For controls, extended styles are specified after the *style* option in the control resource-definition statement.</span></span> <span data-ttu-id="67b9e-113">如需詳細資訊，請參閱個別控制項的資源定義語句。</span><span class="sxs-lookup"><span data-stu-id="67b9e-113">For more information, see the resource-definition statement for the individual control.</span></span>

## <a name="see-also"></a><span data-ttu-id="67b9e-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67b9e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b9e-115">**加速器**</span><span class="sxs-lookup"><span data-stu-id="67b9e-115">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="67b9e-116">**控制**</span><span class="sxs-lookup"><span data-stu-id="67b9e-116">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="67b9e-117">**對話 框**</span><span class="sxs-lookup"><span data-stu-id="67b9e-117">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="67b9e-118">**功能表**</span><span class="sxs-lookup"><span data-stu-id="67b9e-118">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="67b9e-119">**彈出**</span><span class="sxs-lookup"><span data-stu-id="67b9e-119">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="67b9e-120">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="67b9e-120">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="67b9e-121">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="67b9e-121">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="67b9e-122">使用者定義的資源</span><span class="sxs-lookup"><span data-stu-id="67b9e-122">User-Defined Resource</span></span>](user-defined-resource.md)
</dt> </dl>

 

 