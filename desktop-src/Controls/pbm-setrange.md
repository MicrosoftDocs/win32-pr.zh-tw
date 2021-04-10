---
title: 'PBM_SETRANGE 訊息 (Commctrl .h) '
description: 設定進度列的最小值和最大值，並重新繪製橫條以反映新的範圍。
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843928"
---
# <a name="pbm_setrange-message"></a><span data-ttu-id="6c1db-104">PBM \_ SETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="6c1db-104">PBM\_SETRANGE message</span></span>

<span data-ttu-id="6c1db-105">設定進度列的最小值和最大值，並重新繪製橫條以反映新的範圍。</span><span class="sxs-lookup"><span data-stu-id="6c1db-105">Sets the minimum and maximum values for a progress bar and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c1db-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c1db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c1db-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c1db-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c1db-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6c1db-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6c1db-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c1db-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c1db-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定最小範圍值，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定最大範圍值。</span><span class="sxs-lookup"><span data-stu-id="6c1db-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum range value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum range value.</span></span> <span data-ttu-id="6c1db-111">最小範圍值不得為負數。</span><span class="sxs-lookup"><span data-stu-id="6c1db-111">The minimum range value must not be negative.</span></span> <span data-ttu-id="6c1db-112">根據預設，最小值為零。</span><span class="sxs-lookup"><span data-stu-id="6c1db-112">By default, the minimum value is zero.</span></span> <span data-ttu-id="6c1db-113">最大範圍值必須大於最小範圍值。</span><span class="sxs-lookup"><span data-stu-id="6c1db-113">The maximum range value must be greater than the minimum range value.</span></span> <span data-ttu-id="6c1db-114">根據預設，最大範圍值為100。</span><span class="sxs-lookup"><span data-stu-id="6c1db-114">By default, the maximum range value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c1db-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c1db-115">Return value</span></span>

<span data-ttu-id="6c1db-116">如果成功，則傳回先前的範圍值，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="6c1db-116">Returns the previous range values if successful, or zero otherwise.</span></span> <span data-ttu-id="6c1db-117">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定先前的最小值，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定先前的最大值。</span><span class="sxs-lookup"><span data-stu-id="6c1db-117">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the previous minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the previous maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c1db-118">備註</span><span class="sxs-lookup"><span data-stu-id="6c1db-118">Remarks</span></span>

<span data-ttu-id="6c1db-119">如果您未設定範圍值，系統會將最小值設定為0，並將最大值設定為100。</span><span class="sxs-lookup"><span data-stu-id="6c1db-119">If you do not set the range values, the system sets the minimum value to 0 and the maximum value to 100.</span></span> <span data-ttu-id="6c1db-120">因為此訊息以16位不帶正負號的整數表示範圍，所以可以從0延伸至65535。</span><span class="sxs-lookup"><span data-stu-id="6c1db-120">Because this message expresses the range as a 16-bit unsigned integer, it can extend from 0 to 65,535.</span></span> <span data-ttu-id="6c1db-121">範圍中的最小值可介於0到65535之間。</span><span class="sxs-lookup"><span data-stu-id="6c1db-121">The minimum value in the range can be from 0 to 65,535.</span></span> <span data-ttu-id="6c1db-122">同樣地，最大值可以是從0到65535。</span><span class="sxs-lookup"><span data-stu-id="6c1db-122">Likewise, the maximum value can be from 0 to 65,535.</span></span>

<span data-ttu-id="6c1db-123">若要設定較大的範圍，請呼叫 [**PBM \_ SETRANGE32**](pbm-setrange32.md)。</span><span class="sxs-lookup"><span data-stu-id="6c1db-123">To set a larger range, call [**PBM\_SETRANGE32**](pbm-setrange32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1db-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c1db-124">Requirements</span></span>



| <span data-ttu-id="6c1db-125">需求</span><span class="sxs-lookup"><span data-stu-id="6c1db-125">Requirement</span></span> | <span data-ttu-id="6c1db-126">值</span><span class="sxs-lookup"><span data-stu-id="6c1db-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1db-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c1db-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6c1db-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c1db-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c1db-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c1db-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6c1db-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c1db-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c1db-131">標頭</span><span class="sxs-lookup"><span data-stu-id="6c1db-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c1db-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c1db-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c1db-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c1db-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c1db-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="6c1db-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c1db-135">**PBM \_ GETRANGE**</span><span class="sxs-lookup"><span data-stu-id="6c1db-135">**PBM\_GETRANGE**</span></span>](pbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="6c1db-136">**PBM \_ SETRANGE32**</span><span class="sxs-lookup"><span data-stu-id="6c1db-136">**PBM\_SETRANGE32**</span></span>](pbm-setrange32.md)
</dt> </dl>

 

