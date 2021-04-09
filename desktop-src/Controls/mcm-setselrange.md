---
title: 'MCM_SETSELRANGE 訊息 (Commctrl .h) '
description: 將月曆控制項的選取範圍設定為指定的日期範圍。 您可以使用 MonthCal SetSelRange 宏明確地傳送此訊息 \_ 。
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- MCM_SETSELRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024657"
---
# <a name="mcm_setselrange-message"></a><span data-ttu-id="e674b-105">MCM \_ SETSELRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="e674b-105">MCM\_SETSELRANGE message</span></span>

<span data-ttu-id="e674b-106">將月曆控制項的選取範圍設定為指定的日期範圍。</span><span class="sxs-lookup"><span data-stu-id="e674b-106">Sets the selection for a month calendar control to a given date range.</span></span> <span data-ttu-id="e674b-107">您可以使用 [**MonthCal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e674b-107">You can send this message explicitly or by using the [**MonthCal\_SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e674b-108">參數</span><span class="sxs-lookup"><span data-stu-id="e674b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e674b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e674b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e674b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e674b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e674b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e674b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e674b-112">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標，其中包含代表選取限制的日期資訊。</span><span class="sxs-lookup"><span data-stu-id="e674b-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain date information representing the selection limits.</span></span> <span data-ttu-id="e674b-113">第一個選取的日期必須指定于 *lpSysTimeArray* \[ 0 \] ，而且必須在 *lpSysTimeArray* 1 中指定最後選取的日期 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="e674b-113">The first selected date must be specified in *lpSysTimeArray*\[0\], and the last selected date must be specified in *lpSysTimeArray*\[1\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e674b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e674b-114">Return value</span></span>

<span data-ttu-id="e674b-115">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="e674b-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="e674b-116">如果套用到不使用 [**MCS \_ 多重選**](month-calendar-control-styles.md) 樣式的月曆控制項，此訊息將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e674b-116">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e674b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e674b-117">Requirements</span></span>



| <span data-ttu-id="e674b-118">需求</span><span class="sxs-lookup"><span data-stu-id="e674b-118">Requirement</span></span> | <span data-ttu-id="e674b-119">值</span><span class="sxs-lookup"><span data-stu-id="e674b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e674b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e674b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e674b-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e674b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e674b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e674b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e674b-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e674b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e674b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e674b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e674b-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e674b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e674b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e674b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e674b-127">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="e674b-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

