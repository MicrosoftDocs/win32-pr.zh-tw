---
title: '工具列按鈕狀態 (CommCtrl .h) '
description: 此區段會列出工具列按鈕可以有的狀態。
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998796"
---
# <a name="toolbar-button-states"></a><span data-ttu-id="1ea10-103">工具列按鈕狀態</span><span class="sxs-lookup"><span data-stu-id="1ea10-103">Toolbar Button States</span></span>

<span data-ttu-id="1ea10-104">此區段會列出工具列按鈕可以有的狀態。</span><span class="sxs-lookup"><span data-stu-id="1ea10-104">This section lists the states a toolbar button can have.</span></span>



| <span data-ttu-id="1ea10-105">常數</span><span class="sxs-lookup"><span data-stu-id="1ea10-105">Constant</span></span>                                                                                                                                                                              | <span data-ttu-id="1ea10-106">描述</span><span class="sxs-lookup"><span data-stu-id="1ea10-106">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <span data-ttu-id="1ea10-107"><dt>**TBSTATE \_ 已核取**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-107"><dt>**TBSTATE\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="1ea10-108">此按鈕具有 [**TBSTYLE \_ 檢查**](toolbar-control-and-button-styles.md) 樣式，且正在按一下。</span><span class="sxs-lookup"><span data-stu-id="1ea10-108">The button has the [**TBSTYLE\_CHECK**](toolbar-control-and-button-styles.md) style and is being clicked.</span></span><br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <span data-ttu-id="1ea10-109"><dt>**TBSTATE \_ 橢圓形**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-109"><dt>**TBSTATE\_ELLIPSES**</dt></span></span> </dl>                | <span data-ttu-id="1ea10-110">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="1ea10-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="1ea10-111">按鈕的文字會被剪下，並顯示省略號。</span><span class="sxs-lookup"><span data-stu-id="1ea10-111">The button's text is cut off and an ellipsis is displayed.</span></span><br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <span data-ttu-id="1ea10-112"><dt>**TBSTATE \_ 已啟用**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-112"><dt>**TBSTATE\_ENABLED**</dt></span></span> </dl>                   | <span data-ttu-id="1ea10-113">按鈕接受使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="1ea10-113">The button accepts user input.</span></span> <span data-ttu-id="1ea10-114">沒有此狀態的按鈕會呈現灰色。</span><span class="sxs-lookup"><span data-stu-id="1ea10-114">A button that does not have this state is grayed.</span></span><br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <span data-ttu-id="1ea10-115"><dt>**\_隱藏 TBSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-115"><dt>**TBSTATE\_HIDDEN**</dt></span></span> </dl>                      | <span data-ttu-id="1ea10-116">按鈕不會顯示，且無法接收使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="1ea10-116">The button is not visible and cannot receive user input.</span></span><br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <span data-ttu-id="1ea10-117"><dt>**TBSTATE \_ 不定**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-117"><dt>**TBSTATE\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="1ea10-118">按鈕會呈現灰色。</span><span class="sxs-lookup"><span data-stu-id="1ea10-118">The button is grayed.</span></span><br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <span data-ttu-id="1ea10-119"><dt>**TBSTATE \_ 標示**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-119"><dt>**TBSTATE\_MARKED**</dt></span></span> </dl>                      | <span data-ttu-id="1ea10-120">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="1ea10-120">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="1ea10-121">按鈕會標示為。</span><span class="sxs-lookup"><span data-stu-id="1ea10-121">The button is marked.</span></span> <span data-ttu-id="1ea10-122">標示專案的解讀取決於應用程式。</span><span class="sxs-lookup"><span data-stu-id="1ea10-122">The interpretation of a marked item is dependent upon the application.</span></span> <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <span data-ttu-id="1ea10-123"><dt>**已 \_ 按下 TBSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-123"><dt>**TBSTATE\_PRESSED**</dt></span></span> </dl>                   | <span data-ttu-id="1ea10-124">正在按一下按鈕。</span><span class="sxs-lookup"><span data-stu-id="1ea10-124">The button is being clicked.</span></span><br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <span data-ttu-id="1ea10-125"><dt>**TBSTATE \_ WRAP**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-125"><dt>**TBSTATE\_WRAP**</dt></span></span> </dl>                            | <span data-ttu-id="1ea10-126">按鈕後面接著分行符號。</span><span class="sxs-lookup"><span data-stu-id="1ea10-126">The button is followed by a line break.</span></span> <span data-ttu-id="1ea10-127">此按鈕也必須具有 TBSTATE \_ 啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="1ea10-127">The button must also have the TBSTATE\_ENABLED state.</span></span><br/>                                              |



## <a name="remarks"></a><span data-ttu-id="1ea10-128">備註</span><span class="sxs-lookup"><span data-stu-id="1ea10-128">Remarks</span></span>

<span data-ttu-id="1ea10-129">工具列可能會有狀態的組合。</span><span class="sxs-lookup"><span data-stu-id="1ea10-129">A toolbar may have a combination of states.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ea10-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ea10-130">Requirements</span></span>



| <span data-ttu-id="1ea10-131">需求</span><span class="sxs-lookup"><span data-stu-id="1ea10-131">Requirement</span></span> | <span data-ttu-id="1ea10-132">值</span><span class="sxs-lookup"><span data-stu-id="1ea10-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea10-133">標頭</span><span class="sxs-lookup"><span data-stu-id="1ea10-133">Header</span></span><br/> | <dl> <span data-ttu-id="1ea10-134"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ea10-134"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





