---
title: 'DTM_SETRANGE 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以明確地傳送此訊息，或使用 DateTime \_ SetRange 宏。
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- DTM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686172"
---
# <a name="dtm_setrange-message"></a><span data-ttu-id="0696e-105">DTM \_ SETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="0696e-105">DTM\_SETRANGE message</span></span>

<span data-ttu-id="0696e-106">設定日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。</span><span class="sxs-lookup"><span data-stu-id="0696e-106">Sets the minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="0696e-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) 宏。</span><span class="sxs-lookup"><span data-stu-id="0696e-107">You can send this message explicitly or use the [**DateTime\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0696e-108">參數</span><span class="sxs-lookup"><span data-stu-id="0696e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0696e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0696e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0696e-110">值，指定有效的範圍值。</span><span class="sxs-lookup"><span data-stu-id="0696e-110">A value specifying which range values are valid.</span></span> <span data-ttu-id="0696e-111">這個參數可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="0696e-111">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="0696e-112">值</span><span class="sxs-lookup"><span data-stu-id="0696e-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="0696e-113">意義</span><span class="sxs-lookup"><span data-stu-id="0696e-113">Meaning</span></span>                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="0696e-114"><dt>**GDTR \_ 分鐘**</dt></span><span class="sxs-lookup"><span data-stu-id="0696e-114"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="0696e-115">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構陣列中的第一個元素是有效的，而且將用來設定允許的最小系統時間。</span><span class="sxs-lookup"><span data-stu-id="0696e-115">The first element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the minimum allowable system time.</span></span><br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="0696e-116"><dt>**GDTR \_ MAX**</dt></span><span class="sxs-lookup"><span data-stu-id="0696e-116"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="0696e-117">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構陣列中的第二個元素是有效的，而且將用來設定允許的最大系統時間。</span><span class="sxs-lookup"><span data-stu-id="0696e-117">The second element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the maximum allowable system time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0696e-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0696e-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0696e-119">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="0696e-119">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span> <span data-ttu-id="0696e-120">**SYSTEMTIME** 陣列的第一個元素包含允許的最小時間。</span><span class="sxs-lookup"><span data-stu-id="0696e-120">The first element of the **SYSTEMTIME** array contains the minimum allowable time.</span></span> <span data-ttu-id="0696e-121">**SYSTEMTIME** 陣列的第二個元素包含允許的最大時間。</span><span class="sxs-lookup"><span data-stu-id="0696e-121">The second element of the **SYSTEMTIME** array contains the maximum allowable time.</span></span> <span data-ttu-id="0696e-122">不需要填滿未在 *wParam* 參數中指定的陣列元素。</span><span class="sxs-lookup"><span data-stu-id="0696e-122">It is not necessary to fill an array element that is not specified in the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0696e-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="0696e-123">Return value</span></span>

<span data-ttu-id="0696e-124">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="0696e-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0696e-125">備註</span><span class="sxs-lookup"><span data-stu-id="0696e-125">Remarks</span></span>

<span data-ttu-id="0696e-126">日期和時間選擇器只會顯示落在指定範圍內的日期/時間，防止使用者選取超出範圍的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0696e-126">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="0696e-127">如果 [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) 訊息指定超出範圍的日期和時間，它將會失敗。</span><span class="sxs-lookup"><span data-stu-id="0696e-127">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="0696e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0696e-128">Requirements</span></span>



| <span data-ttu-id="0696e-129">需求</span><span class="sxs-lookup"><span data-stu-id="0696e-129">Requirement</span></span> | <span data-ttu-id="0696e-130">值</span><span class="sxs-lookup"><span data-stu-id="0696e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0696e-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0696e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0696e-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0696e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0696e-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0696e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0696e-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0696e-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0696e-135">標頭</span><span class="sxs-lookup"><span data-stu-id="0696e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0696e-136"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0696e-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

