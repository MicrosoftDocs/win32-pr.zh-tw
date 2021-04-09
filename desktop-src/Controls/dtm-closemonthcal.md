---
title: 'DTM_CLOSEMONTHCAL 訊息 (Commctrl .h) '
description: 關閉 (DTP) 控制項的日期和時間選擇器。 請明確地傳送此訊息，或使用 DateTime \_ CloseMonthCal 宏。
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024674"
---
# <a name="dtm_closemonthcal-message"></a><span data-ttu-id="b298f-105">DTM \_ CLOSEMONTHCAL 訊息</span><span class="sxs-lookup"><span data-stu-id="b298f-105">DTM\_CLOSEMONTHCAL message</span></span>

<span data-ttu-id="b298f-106">關閉 (DTP) 控制項的日期和時間選擇器。</span><span class="sxs-lookup"><span data-stu-id="b298f-106">Closes a date and time picker (DTP) control.</span></span> <span data-ttu-id="b298f-107">請明確地傳送此訊息，或使用 [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) 宏。</span><span class="sxs-lookup"><span data-stu-id="b298f-107">Send this message explicitly or by using the [**DateTime\_CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b298f-108">參數</span><span class="sxs-lookup"><span data-stu-id="b298f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b298f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b298f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b298f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b298f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b298f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b298f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b298f-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b298f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b298f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b298f-113">Return value</span></span>

<span data-ttu-id="b298f-114">傳回零。</span><span class="sxs-lookup"><span data-stu-id="b298f-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b298f-115">備註</span><span class="sxs-lookup"><span data-stu-id="b298f-115">Remarks</span></span>

<span data-ttu-id="b298f-116">終結控制項，並傳送控制項正在關閉的 [DTN \_ 特寫](dtn-closeup.md) 通知，而不是控制項開啟 (下拉式清單，如同在控制項的父系) 的 [DTN \_ 下拉式](dtn-dropdown.md) 通知中一樣。</span><span class="sxs-lookup"><span data-stu-id="b298f-116">Destroys the control and sends a [DTN\_CLOSEUP](dtn-closeup.md) notification that the control is closing as opposed to the control is opening (dropping-down as in the [DTN\_DROPDOWN](dtn-dropdown.md) notification) to the control's parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b298f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b298f-117">Requirements</span></span>



| <span data-ttu-id="b298f-118">需求</span><span class="sxs-lookup"><span data-stu-id="b298f-118">Requirement</span></span> | <span data-ttu-id="b298f-119">值</span><span class="sxs-lookup"><span data-stu-id="b298f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b298f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b298f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b298f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b298f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b298f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b298f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b298f-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b298f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b298f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b298f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b298f-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b298f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b298f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b298f-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b298f-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="b298f-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b298f-128">DTN \_ 下拉式清單</span><span class="sxs-lookup"><span data-stu-id="b298f-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="b298f-129">DTN \_ 特寫</span><span class="sxs-lookup"><span data-stu-id="b298f-129">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> </dl>

 

 





