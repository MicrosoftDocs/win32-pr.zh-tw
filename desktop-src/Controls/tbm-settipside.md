---
title: 'TBM_SETTIPSIDE 訊息 (Commctrl .h) '
description: 放置 [提示] 控制項所使用的工具提示控制項。 使用 [TBS \_ 工具提示] 樣式的 [顯示工具提示] 控制項。
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- TBM_SETTIPSIDE message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384262"
---
# <a name="tbm_settipside-message"></a><span data-ttu-id="b4d69-105">TBM \_ SETTIPSIDE 訊息</span><span class="sxs-lookup"><span data-stu-id="b4d69-105">TBM\_SETTIPSIDE message</span></span>

<span data-ttu-id="b4d69-106">放置 [提示] 控制項所使用的工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="b4d69-106">Positions a tooltip control used by a trackbar control.</span></span> <span data-ttu-id="b4d69-107">使用 [ [**TBS \_ 工具提示**](trackbar-control-styles.md) ] 樣式的 [顯示工具提示] 控制項。</span><span class="sxs-lookup"><span data-stu-id="b4d69-107">Trackbar controls that use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style display tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4d69-108">參數</span><span class="sxs-lookup"><span data-stu-id="b4d69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4d69-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4d69-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4d69-110">值，表示要顯示工具提示控制項的位置。</span><span class="sxs-lookup"><span data-stu-id="b4d69-110">Value representing the location at which to display the tooltip control.</span></span> <span data-ttu-id="b4d69-111">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="b4d69-111">This value can be one of the following:</span></span>



| <span data-ttu-id="b4d69-112">值</span><span class="sxs-lookup"><span data-stu-id="b4d69-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="b4d69-113">意義</span><span class="sxs-lookup"><span data-stu-id="b4d69-113">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <span data-ttu-id="b4d69-114"><dt>**TBTS \_ TOP**</dt></span><span class="sxs-lookup"><span data-stu-id="b4d69-114"><dt>**TBTS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="b4d69-115">工具提示控制項將定位在 [並排] 上方。</span><span class="sxs-lookup"><span data-stu-id="b4d69-115">The tooltip control will be positioned above the trackbar.</span></span> <span data-ttu-id="b4d69-116">此旗標用於水準 trackbars。</span><span class="sxs-lookup"><span data-stu-id="b4d69-116">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <span data-ttu-id="b4d69-117"><dt>**\_左 TBTS**</dt></span><span class="sxs-lookup"><span data-stu-id="b4d69-117"><dt>**TBTS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="b4d69-118">工具提示控制項將放置在 [並排] 的左邊。</span><span class="sxs-lookup"><span data-stu-id="b4d69-118">The tooltip control will be positioned to the left of the trackbar.</span></span> <span data-ttu-id="b4d69-119">此旗標用於垂直 trackbars。</span><span class="sxs-lookup"><span data-stu-id="b4d69-119">This flag is for use with vertical trackbars.</span></span><br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <span data-ttu-id="b4d69-120"><dt>**TBTS \_ 底部**</dt></span><span class="sxs-lookup"><span data-stu-id="b4d69-120"><dt>**TBTS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="b4d69-121">工具提示控制項將放置在 [並排] 下方。</span><span class="sxs-lookup"><span data-stu-id="b4d69-121">The tooltip control will be positioned below the trackbar.</span></span> <span data-ttu-id="b4d69-122">此旗標用於水準 trackbars。</span><span class="sxs-lookup"><span data-stu-id="b4d69-122">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <span data-ttu-id="b4d69-123"><dt>**TBTS \_ RIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="b4d69-123"><dt>**TBTS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="b4d69-124">工具提示控制項將放置在 [程式提示] 右邊。</span><span class="sxs-lookup"><span data-stu-id="b4d69-124">The tooltip control will be positioned to the right of the trackbar.</span></span> <span data-ttu-id="b4d69-125">此旗標用於垂直 trackbars。</span><span class="sxs-lookup"><span data-stu-id="b4d69-125">This flag is for use with vertical trackbars.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b4d69-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4d69-126">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b4d69-127">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b4d69-127">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4d69-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4d69-128">Return value</span></span>

<span data-ttu-id="b4d69-129">傳回值，這個值表示工具提示控制項先前的位置。</span><span class="sxs-lookup"><span data-stu-id="b4d69-129">Returns a value that represents the tooltip control's previous location.</span></span> <span data-ttu-id="b4d69-130">傳回值等於 *wParam* 的其中一個可能值。</span><span class="sxs-lookup"><span data-stu-id="b4d69-130">The return value equals one of the possible values for *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d69-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4d69-131">Requirements</span></span>



| <span data-ttu-id="b4d69-132">需求</span><span class="sxs-lookup"><span data-stu-id="b4d69-132">Requirement</span></span> | <span data-ttu-id="b4d69-133">值</span><span class="sxs-lookup"><span data-stu-id="b4d69-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4d69-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4d69-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d69-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4d69-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4d69-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4d69-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d69-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4d69-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4d69-138">標頭</span><span class="sxs-lookup"><span data-stu-id="b4d69-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4d69-139"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4d69-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





