---
title: 'PGM_GETBUTTONSTATE 訊息 (Commctrl .h) '
description: 抓取頁面導航控制項中指定之按鈕的狀態。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetButtonState 宏。
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934715"
---
# <a name="pgm_getbuttonstate-message"></a><span data-ttu-id="fb5c9-105">PGM \_ GETBUTTONSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="fb5c9-105">PGM\_GETBUTTONSTATE message</span></span>

<span data-ttu-id="fb5c9-106">抓取頁面導航控制項中指定之按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-106">Retrieves the state of the specified button in a pager control.</span></span> <span data-ttu-id="fb5c9-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) 宏。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-107">You can send this message explicitly or use the [**Pager\_GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb5c9-108">參數</span><span class="sxs-lookup"><span data-stu-id="fb5c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb5c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb5c9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fb5c9-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fb5c9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb5c9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb5c9-112">指出要取得狀態的按鈕。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-112">Indicates which button to retrieve the state for.</span></span> <span data-ttu-id="fb5c9-113">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="fb5c9-113">This can be one of the following values:</span></span>



| <span data-ttu-id="fb5c9-114">值</span><span class="sxs-lookup"><span data-stu-id="fb5c9-114">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="fb5c9-115">意義</span><span class="sxs-lookup"><span data-stu-id="fb5c9-115">Meaning</span></span>                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <span data-ttu-id="fb5c9-116"><dt>**PGB \_ TOPORLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="fb5c9-116"><dt>**PGB\_TOPORLEFT**</dt></span></span> </dl>             | <span data-ttu-id="fb5c9-117">指出 [**pg \_ 垂直**](pager-control-styles.md) 呼機控制項中的頂端按鈕，或 [**pg \_ HORZ**](pager-control-styles.md) 頁面控制項中的左按鈕。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-117">Indicates the top button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the left button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <span data-ttu-id="fb5c9-118"><dt>**PGB \_ BOTTOMORRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="fb5c9-118"><dt>**PGB\_BOTTOMORRIGHT**</dt></span></span> </dl> | <span data-ttu-id="fb5c9-119">表示 [**pg \_ 垂直**](pager-control-styles.md) 呼機控制項中的底部按鈕，或 [**pg \_ HORZ**](pager-control-styles.md) 頁面控制項中的右方按鈕。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-119">Indicates the bottom button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the right button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb5c9-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb5c9-120">Return value</span></span>

<span data-ttu-id="fb5c9-121">傳回 *lParam* 中指定之按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-121">Returns the state of the button specified in *lParam*.</span></span> <span data-ttu-id="fb5c9-122">這會是下列其中一個或多個值 (如果傳回一個以上的值，則會使用位 OR) 來合併它們：</span><span class="sxs-lookup"><span data-stu-id="fb5c9-122">This will be one or more of the following values (if more then one value is returned they will be combined using a bitwise OR):</span></span>



| <span data-ttu-id="fb5c9-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fb5c9-123">Return code</span></span>                                                                                   | <span data-ttu-id="fb5c9-124">Description</span><span class="sxs-lookup"><span data-stu-id="fb5c9-124">Description</span></span>                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="fb5c9-125"><dt>**PGF \_ 不可見**</dt></span><span class="sxs-lookup"><span data-stu-id="fb5c9-125"><dt>**PGF\_INVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="fb5c9-126">看不到此按鈕。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-126">The button is not visible.</span></span> <br/>      |
| <dl> <span data-ttu-id="fb5c9-127"><dt>**PGF \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="fb5c9-127"><dt>**PGF\_NORMAL**</dt></span></span> </dl>    | <span data-ttu-id="fb5c9-128">按鈕處於正常狀態。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-128">The button is in normal state.</span></span> <br/>  |
| <dl> <span data-ttu-id="fb5c9-129"><dt>**PGF \_ 灰色**</dt></span><span class="sxs-lookup"><span data-stu-id="fb5c9-129"><dt>**PGF\_GRAYED**</dt></span></span> </dl>    | <span data-ttu-id="fb5c9-130">按鈕處於灰色狀態。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-130">The button is in grayed state.</span></span> <br/>  |
| <dl> <span data-ttu-id="fb5c9-131"><dt>**PGF \_ 按下**</dt></span><span class="sxs-lookup"><span data-stu-id="fb5c9-131"><dt>**PGF\_DEPRESSED**</dt></span></span> </dl> | <span data-ttu-id="fb5c9-132">按鈕處於按下狀態。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-132">The button is in pressed state.</span></span> <br/> |
| <dl> <span data-ttu-id="fb5c9-133"><dt>**PGF \_ 熱**</dt></span><span class="sxs-lookup"><span data-stu-id="fb5c9-133"><dt>**PGF\_HOT**</dt></span></span> </dl>       | <span data-ttu-id="fb5c9-134">按鈕處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="fb5c9-134">The button is in hot state.</span></span> <br/>     |



 

## <a name="requirements"></a><span data-ttu-id="fb5c9-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb5c9-135">Requirements</span></span>



| <span data-ttu-id="fb5c9-136">需求</span><span class="sxs-lookup"><span data-stu-id="fb5c9-136">Requirement</span></span> | <span data-ttu-id="fb5c9-137">值</span><span class="sxs-lookup"><span data-stu-id="fb5c9-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb5c9-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb5c9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fb5c9-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb5c9-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb5c9-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb5c9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fb5c9-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb5c9-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb5c9-142">標頭</span><span class="sxs-lookup"><span data-stu-id="fb5c9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb5c9-143"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb5c9-143"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





