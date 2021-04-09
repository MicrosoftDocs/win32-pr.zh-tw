---
title: 'DTM_GETMONTHCAL 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器的 (DTP) 子月曆控制項的控制碼。 您可以明確地傳送此訊息，或使用 DateTime \_ GetMonthCal 宏。
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- DTM_GETMONTHCAL message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934739"
---
# <a name="dtm_getmonthcal-message"></a><span data-ttu-id="596f6-105">DTM \_ GETMONTHCAL 訊息</span><span class="sxs-lookup"><span data-stu-id="596f6-105">DTM\_GETMONTHCAL message</span></span>

<span data-ttu-id="596f6-106">取得日期和時間選擇器的 (DTP) 子月曆控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="596f6-106">Gets the handle to a date and time picker's (DTP) child month calendar control.</span></span> <span data-ttu-id="596f6-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) 宏。</span><span class="sxs-lookup"><span data-stu-id="596f6-107">You can send this message explicitly or use the [**DateTime\_GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="596f6-108">參數</span><span class="sxs-lookup"><span data-stu-id="596f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="596f6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="596f6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="596f6-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="596f6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="596f6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="596f6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="596f6-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="596f6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="596f6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="596f6-113">Return value</span></span>

<span data-ttu-id="596f6-114">如果成功，則會將控制碼傳回給 DTP 控制項的子月曆控制項，否則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="596f6-114">Returns the handle to a DTP control's child month calendar control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="596f6-115">備註</span><span class="sxs-lookup"><span data-stu-id="596f6-115">Remarks</span></span>

<span data-ttu-id="596f6-116">當使用者按一下下拉式箭號 ([DTN \_ ](dtn-dropdown.md) 下拉式通知) 時，會建立一個子月曆控制項。</span><span class="sxs-lookup"><span data-stu-id="596f6-116">DTP controls create a child month calendar control when the user clicks the drop-down arrow ([DTN\_DROPDOWN](dtn-dropdown.md) notification).</span></span> <span data-ttu-id="596f6-117">當月曆不再需要時，它會被終結 (在) 上傳送 [DTN 的 \_ 特寫](dtn-closeup.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="596f6-117">When the month calendar is no longer needed, it is destroyed (a [DTN\_CLOSEUP](dtn-closeup.md) notification is sent on destruction).</span></span> <span data-ttu-id="596f6-118">因此，您的應用程式不得依賴 DTP 控制項之子月份行事曆的靜態控制碼。</span><span class="sxs-lookup"><span data-stu-id="596f6-118">So your application must not rely on a static handle to the DTP control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="596f6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="596f6-119">Requirements</span></span>



| <span data-ttu-id="596f6-120">需求</span><span class="sxs-lookup"><span data-stu-id="596f6-120">Requirement</span></span> | <span data-ttu-id="596f6-121">值</span><span class="sxs-lookup"><span data-stu-id="596f6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="596f6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="596f6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="596f6-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="596f6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="596f6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="596f6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="596f6-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="596f6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="596f6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="596f6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="596f6-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="596f6-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="596f6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="596f6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="596f6-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="596f6-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="596f6-130">DTN \_ 特寫</span><span class="sxs-lookup"><span data-stu-id="596f6-130">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="596f6-131">DTN \_ 下拉式清單</span><span class="sxs-lookup"><span data-stu-id="596f6-131">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> </dl>

 

 





