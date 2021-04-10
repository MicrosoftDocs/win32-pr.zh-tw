---
title: 'TBM_SETPOS 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的目前邏輯位置。
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935123"
---
# <a name="tbm_setpos-message"></a><span data-ttu-id="702e5-104">TBM \_ SETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="702e5-104">TBM\_SETPOS message</span></span>

<span data-ttu-id="702e5-105">設定捲軸中滑杆的目前邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="702e5-105">Sets the current logical position of the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="702e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="702e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="702e5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="702e5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="702e5-108">重繪旗標。</span><span class="sxs-lookup"><span data-stu-id="702e5-108">Redraw flag.</span></span> <span data-ttu-id="702e5-109">如果此參數為 **TRUE**，則訊息會使用 *lParam* 所指定位置的滑杆來重新繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="702e5-109">If this parameter is **TRUE**, the message redraws the control with the slider at the position given by *lParam*.</span></span> <span data-ttu-id="702e5-110">如果此參數為 **FALSE**，則訊息不會在新位置重繪滑杆。</span><span class="sxs-lookup"><span data-stu-id="702e5-110">If this parameter is **FALSE**, the message does not redraw the slider at the new position.</span></span> <span data-ttu-id="702e5-111">請注意，無論 *wParam* 參數為何，訊息都會將滑杆位置 (的值設定為 [**TBM \_ GETPOS**](tbm-getpos.md)訊息所傳回) 。</span><span class="sxs-lookup"><span data-stu-id="702e5-111">Note that the message sets the value of the slider position (as returned by the [**TBM\_GETPOS**](tbm-getpos.md) message) regardless of the *wParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="702e5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="702e5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="702e5-113">滑杆的新邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="702e5-113">New logical position of the slider.</span></span> <span data-ttu-id="702e5-114">有效的邏輯位置是在最小至最大滑杆位置的最小值範圍中的整數值。</span><span class="sxs-lookup"><span data-stu-id="702e5-114">Valid logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span> <span data-ttu-id="702e5-115">如果這個值超出控制項的最大和最小範圍，則會將位置設定為最大值或最小值。</span><span class="sxs-lookup"><span data-stu-id="702e5-115">If this value is outside the control's maximum and minimum range, the position is set to the maximum or minimum value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="702e5-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="702e5-116">Return value</span></span>

<span data-ttu-id="702e5-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="702e5-117">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="702e5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="702e5-118">Requirements</span></span>



| <span data-ttu-id="702e5-119">需求</span><span class="sxs-lookup"><span data-stu-id="702e5-119">Requirement</span></span> | <span data-ttu-id="702e5-120">值</span><span class="sxs-lookup"><span data-stu-id="702e5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="702e5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="702e5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="702e5-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="702e5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="702e5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="702e5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="702e5-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="702e5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="702e5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="702e5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="702e5-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="702e5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





