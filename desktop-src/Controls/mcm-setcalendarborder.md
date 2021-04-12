---
title: 'MCM_SETCALENDARBORDER 訊息 (Commctrl .h) '
description: 設定框線的大小（以圖元為單位）。 您可以使用 MonthCal SetCalendarBorder 宏明確地傳送此訊息 \_ 。
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465248"
---
# <a name="mcm_setcalendarborder-message"></a><span data-ttu-id="127cf-105">MCM \_ SETCALENDARBORDER 訊息</span><span class="sxs-lookup"><span data-stu-id="127cf-105">MCM\_SETCALENDARBORDER message</span></span>

<span data-ttu-id="127cf-106">設定框線的大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="127cf-106">Sets the size of the border, in pixels.</span></span> <span data-ttu-id="127cf-107">您可以使用 [**MonthCal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="127cf-107">You can send this message explicitly or by using the [**MonthCal\_SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="127cf-108">參數</span><span class="sxs-lookup"><span data-stu-id="127cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="127cf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="127cf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="127cf-110">若 **為 TRUE**，則會將框線大小設定為 *lParam* 指定的圖元數。</span><span class="sxs-lookup"><span data-stu-id="127cf-110">If **TRUE**, then the border size is set to the number of pixels that *lParam* specifies.</span></span> <span data-ttu-id="127cf-111">如果 **為 FALSE**，則會將框線大小重設為主題所指定的預設值，如果未使用主題則為零。</span><span class="sxs-lookup"><span data-stu-id="127cf-111">If **FALSE**, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.</span></span>

</dd> <dt>

<span data-ttu-id="127cf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="127cf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="127cf-113">框線大小的圖元數。</span><span class="sxs-lookup"><span data-stu-id="127cf-113">Number of pixels of the border size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="127cf-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="127cf-114">Return value</span></span>

<span data-ttu-id="127cf-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="127cf-115">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="127cf-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="127cf-116">Requirements</span></span>



| <span data-ttu-id="127cf-117">需求</span><span class="sxs-lookup"><span data-stu-id="127cf-117">Requirement</span></span> | <span data-ttu-id="127cf-118">值</span><span class="sxs-lookup"><span data-stu-id="127cf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="127cf-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="127cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="127cf-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="127cf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="127cf-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="127cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="127cf-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="127cf-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="127cf-123">標頭</span><span class="sxs-lookup"><span data-stu-id="127cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="127cf-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="127cf-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





