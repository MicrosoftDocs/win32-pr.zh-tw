---
title: 'MCM_GETRANGE 訊息 (Commctrl .h) '
description: 抓取月曆控制項設定的最小和最大允許日期。 您可以使用 MonthCal GetRange 宏明確地傳送此訊息 \_ 。
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844287"
---
# <a name="mcm_getrange-message"></a><span data-ttu-id="18225-105">MCM \_ GETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="18225-105">MCM\_GETRANGE message</span></span>

<span data-ttu-id="18225-106">抓取月曆控制項設定的最小和最大允許日期。</span><span class="sxs-lookup"><span data-stu-id="18225-106">Retrieves the minimum and maximum allowable dates set for a month calendar control.</span></span> <span data-ttu-id="18225-107">您可以使用 [**MonthCal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="18225-107">You can send this message explicitly or by using the [**MonthCal\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="18225-108">參數</span><span class="sxs-lookup"><span data-stu-id="18225-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18225-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18225-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="18225-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="18225-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="18225-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18225-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="18225-112">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標，會接收日期限制資訊。</span><span class="sxs-lookup"><span data-stu-id="18225-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the date limit information.</span></span> <span data-ttu-id="18225-113">最小限制設定為 *lprgSysTimeArray* \[ 0 \] ，而 *lprgSysTimeArray* 1 則會 \[ 收到上限 \] 。</span><span class="sxs-lookup"><span data-stu-id="18225-113">The minimum limit is set in *lprgSysTimeArray*\[0\], and *lprgSysTimeArray*\[1\] receives the maximum limit.</span></span> <span data-ttu-id="18225-114">如果任一個元素設定為全部零，則不會針對月曆控制項設定對應的限制。</span><span class="sxs-lookup"><span data-stu-id="18225-114">If either element is set to all zeros, then no corresponding limit is set for the month calendar control.</span></span> <span data-ttu-id="18225-115">此參數必須是有效的位址，而且不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18225-115">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18225-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="18225-116">Return value</span></span>

<span data-ttu-id="18225-117">傳回可為零的 **DWORD** (沒有設定任何限制) 或下列值的組合，這些值會指定限制資訊：</span><span class="sxs-lookup"><span data-stu-id="18225-117">Returns a **DWORD** that can be zero (no limits are set) or a combination of the following values that specify limit information:</span></span>



| <span data-ttu-id="18225-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="18225-118">Return code</span></span>                                                                              | <span data-ttu-id="18225-119">Description</span><span class="sxs-lookup"><span data-stu-id="18225-119">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18225-120"><dt>**GDTR \_ MAX**</dt></span><span class="sxs-lookup"><span data-stu-id="18225-120"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="18225-121">為控制項設定了上限，*lprgSysTimeArray* \[0 \] 有效，且包含適用的日期資訊。</span><span class="sxs-lookup"><span data-stu-id="18225-121">A maximum limit is set for the control; *lprgSysTimeArray*\[0\] is valid and contains the applicable date information.</span></span> <br/> |
| <dl> <span data-ttu-id="18225-122"><dt>**GDTR \_ 分鐘**</dt></span><span class="sxs-lookup"><span data-stu-id="18225-122"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="18225-123">針對控制項設定的最小限制為;*lprgSysTimeArray* \[1 \] 是有效的，而且包含適用的日期資訊。</span><span class="sxs-lookup"><span data-stu-id="18225-123">A minimum limit is set for the control; *lprgSysTimeArray*\[1\] is valid and contains the applicable date information.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="18225-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="18225-124">Requirements</span></span>



| <span data-ttu-id="18225-125">需求</span><span class="sxs-lookup"><span data-stu-id="18225-125">Requirement</span></span> | <span data-ttu-id="18225-126">值</span><span class="sxs-lookup"><span data-stu-id="18225-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18225-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18225-127">Minimum supported client</span></span><br/> | <span data-ttu-id="18225-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18225-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18225-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18225-129">Minimum supported server</span></span><br/> | <span data-ttu-id="18225-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18225-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18225-131">標頭</span><span class="sxs-lookup"><span data-stu-id="18225-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="18225-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="18225-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18225-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18225-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18225-134">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="18225-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

