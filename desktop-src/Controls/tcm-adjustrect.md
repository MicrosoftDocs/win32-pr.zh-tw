---
title: 'TCM_ADJUSTRECT 訊息 (Commctrl .h) '
description: 在指定視窗矩形的情況下，計算索引標籤控制項的顯示區域，或計算對應至指定之顯示區域的視窗矩形。 您可以使用 TabCtrl AdjustRect 宏明確地傳送此訊息 \_ 。
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969204"
---
# <a name="tcm_adjustrect-message"></a><span data-ttu-id="b2a82-105">TCM \_ ADJUSTRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="b2a82-105">TCM\_ADJUSTRECT message</span></span>

<span data-ttu-id="b2a82-106">在指定視窗矩形的情況下，計算索引標籤控制項的顯示區域，或計算對應至指定之顯示區域的視窗矩形。</span><span class="sxs-lookup"><span data-stu-id="b2a82-106">Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area.</span></span> <span data-ttu-id="b2a82-107">您可以使用 [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b2a82-107">You can send this message explicitly or by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2a82-108">參數</span><span class="sxs-lookup"><span data-stu-id="b2a82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2a82-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2a82-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2a82-110">要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="b2a82-110">Operation to perform.</span></span> <span data-ttu-id="b2a82-111">如果此參數為 **TRUE**， *lParam* 會指定一個顯示矩形，並接收對應的視窗矩形。</span><span class="sxs-lookup"><span data-stu-id="b2a82-111">If this parameter is **TRUE**, *lParam* specifies a display rectangle and receives the corresponding window rectangle.</span></span> <span data-ttu-id="b2a82-112">如果此參數為 **FALSE**，則 *lParam* 會指定視窗矩形，並接收對應的顯示區域。</span><span class="sxs-lookup"><span data-stu-id="b2a82-112">If this parameter is **FALSE**, *lParam* specifies a window rectangle and receives the corresponding display area.</span></span>

</dd> <dt>

<span data-ttu-id="b2a82-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2a82-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2a82-114">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，該結構會指定指定的矩形，並接收匯出的矩形。</span><span class="sxs-lookup"><span data-stu-id="b2a82-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the given rectangle and receives the calculated rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2a82-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2a82-115">Return value</span></span>

<span data-ttu-id="b2a82-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b2a82-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2a82-117">備註</span><span class="sxs-lookup"><span data-stu-id="b2a82-117">Remarks</span></span>

<span data-ttu-id="b2a82-118">此訊息只適用于位於頂端的索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="b2a82-118">This message applies only to tab controls that are at the top.</span></span> <span data-ttu-id="b2a82-119">它並不適用于側邊或底部的索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="b2a82-119">It does not apply to tab controls that are on the sides or bottom.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a82-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2a82-120">Requirements</span></span>



| <span data-ttu-id="b2a82-121">需求</span><span class="sxs-lookup"><span data-stu-id="b2a82-121">Requirement</span></span> | <span data-ttu-id="b2a82-122">值</span><span class="sxs-lookup"><span data-stu-id="b2a82-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a82-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2a82-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b2a82-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2a82-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2a82-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2a82-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b2a82-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2a82-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2a82-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b2a82-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2a82-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2a82-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

