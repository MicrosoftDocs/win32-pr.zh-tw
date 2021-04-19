---
title: '流覽常數 (Oleacc .h) '
description: 本主題說明 oleacc 中定義的常數值，指出當用戶端使用 IAccessible accNavigate 在相同容器內的某個使用者介面專案之間流覽時，所觀察到的空間 (向上、向下、左方和右邊) 或邏輯 (第一個子系、最後一個、下一個和先前的) 方向。
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983015"
---
# <a name="navigation-constants"></a><span data-ttu-id="53ed5-103">導覽常數</span><span class="sxs-lookup"><span data-stu-id="53ed5-103">Navigation Constants</span></span>

<span data-ttu-id="53ed5-104">本主題說明在 oleacc 中定義的常數值，指出 *空間* (向上、向下、向左和向右) 或 *邏輯* (第一個子系、最後一個、下一個，以及當用戶端使用 [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 從某個使用者介面專案流覽至相同容器內的另一個使用者介面專案時所觀察到的) 方向。</span><span class="sxs-lookup"><span data-stu-id="53ed5-104">This topic describes the constant values, defined in oleacc.h, that indicate the *spatial* (up, down, left, and right) or *logical* (first child, last, next, and previous) direction observed when clients use [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to navigate from one user interface element to another within the same container.</span></span> <span data-ttu-id="53ed5-105">如需詳細資訊，請參閱 [物件導覽屬性和方法](object-navigation-properties-and-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="53ed5-105">For more information, see [Object Navigation Properties and Methods](object-navigation-properties-and-methods.md).</span></span>

<span data-ttu-id="53ed5-106">Microsoft Active Accessibility 的導覽常數如下所示：</span><span class="sxs-lookup"><span data-stu-id="53ed5-106">The Microsoft Active Accessibility navigation constants are as follows:</span></span>



| <span data-ttu-id="53ed5-107">常數</span><span class="sxs-lookup"><span data-stu-id="53ed5-107">Constant</span></span>                                                                                                                                                                  | <span data-ttu-id="53ed5-108">描述</span><span class="sxs-lookup"><span data-stu-id="53ed5-108">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <span data-ttu-id="53ed5-109"><dt>**\_向下 NAVDIR**</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-109"><dt>**NAVDIR\_DOWN**</dt></span></span> </dl>                   | <span data-ttu-id="53ed5-110">流覽至位於起始物件下方的同級物件。</span><span class="sxs-lookup"><span data-stu-id="53ed5-110">Navigate to the sibling object that is located below the starting object.</span></span><br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <span data-ttu-id="53ed5-111"><dt>**NAVDIR \_ FIRSTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-111"><dt>**NAVDIR\_FIRSTCHILD**</dt></span></span> </dl> | <span data-ttu-id="53ed5-112">流覽至這個物件的第一個子系。</span><span class="sxs-lookup"><span data-stu-id="53ed5-112">Navigate to the first child of this object.</span></span> <span data-ttu-id="53ed5-113">使用這個旗標時， *varStart* 參數的 **lVal** 成員必須是 CHILDID \_ SELF。</span><span class="sxs-lookup"><span data-stu-id="53ed5-113">When this flag is used, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <span data-ttu-id="53ed5-114"><dt>**NAVDIR \_ LASTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-114"><dt>**NAVDIR\_LASTCHILD**</dt></span></span> </dl>    | <span data-ttu-id="53ed5-115">流覽至這個物件的最後一個子系。</span><span class="sxs-lookup"><span data-stu-id="53ed5-115">Navigate to the last child of this object.</span></span> <span data-ttu-id="53ed5-116">使用這個旗標時， *varStart* 參數的 **lVal** 成員必須是 CHILDID \_ SELF。</span><span class="sxs-lookup"><span data-stu-id="53ed5-116">When using this flag, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <span data-ttu-id="53ed5-117"><dt>**\_左 NAVDIR**</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-117"><dt>**NAVDIR\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="53ed5-118">流覽至位於起始物件左邊的同級物件。</span><span class="sxs-lookup"><span data-stu-id="53ed5-118">Navigate to the sibling object located to the left of the starting object.</span></span><br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <span data-ttu-id="53ed5-119"><dt>**NAVDIR \_ 下一步**</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-119"><dt>**NAVDIR\_NEXT**</dt></span></span> </dl>                   | <span data-ttu-id="53ed5-120">流覽至下一個邏輯物件;一般而言，它是起始物件的同級。</span><span class="sxs-lookup"><span data-stu-id="53ed5-120">Navigate to the next logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <span data-ttu-id="53ed5-121"><dt>**NAVDIR \_ 上一步**</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-121"><dt>**NAVDIR\_PREVIOUS**</dt></span></span> </dl>       | <span data-ttu-id="53ed5-122">流覽至先前的邏輯物件;一般而言，它是起始物件的同級。</span><span class="sxs-lookup"><span data-stu-id="53ed5-122">Navigate to the previous logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <span data-ttu-id="53ed5-123"><dt>**NAVDIR \_ RIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-123"><dt>**NAVDIR\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="53ed5-124">流覽至位於起始物件右邊的同級物件。</span><span class="sxs-lookup"><span data-stu-id="53ed5-124">Navigate to the sibling object that is located to the right of the starting object.</span></span><br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <span data-ttu-id="53ed5-125"><dt>**\_向上 NAVDIR**</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-125"><dt>**NAVDIR\_UP**</dt></span></span> </dl>                         | <span data-ttu-id="53ed5-126">流覽至位於起始物件上方的同級物件。</span><span class="sxs-lookup"><span data-stu-id="53ed5-126">Navigate to the sibling object that is located above the starting object.</span></span><br/>                                                                  |



## <a name="requirements"></a><span data-ttu-id="53ed5-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="53ed5-127">Requirements</span></span>



| <span data-ttu-id="53ed5-128">需求</span><span class="sxs-lookup"><span data-stu-id="53ed5-128">Requirement</span></span> | <span data-ttu-id="53ed5-129">值</span><span class="sxs-lookup"><span data-stu-id="53ed5-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53ed5-130">標頭</span><span class="sxs-lookup"><span data-stu-id="53ed5-130">Header</span></span><br/> | <dl> <span data-ttu-id="53ed5-131"><dt>Oleacc。h</dt></span><span class="sxs-lookup"><span data-stu-id="53ed5-131"><dt>Oleacc.h</dt></span></span> </dl> |



 

 





