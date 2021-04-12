---
title: 'HDM_CLEARFILTER 訊息 (Commctrl .h) '
description: 清除指定標題控制項的篩選。 您可以明確地傳送此訊息，或使用標頭 \_ ClearFilter 宏。
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- HDM_CLEARFILTER message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104490"
---
# <a name="hdm_clearfilter-message"></a><span data-ttu-id="609ff-105">HDM \_ CLEARFILTER 訊息</span><span class="sxs-lookup"><span data-stu-id="609ff-105">HDM\_CLEARFILTER message</span></span>

<span data-ttu-id="609ff-106">清除指定標題控制項的篩選。</span><span class="sxs-lookup"><span data-stu-id="609ff-106">Clears the filter for a given header control.</span></span> <span data-ttu-id="609ff-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) 宏。</span><span class="sxs-lookup"><span data-stu-id="609ff-107">You can send this message explicitly or use the [**Header\_ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="609ff-108">參數</span><span class="sxs-lookup"><span data-stu-id="609ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="609ff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="609ff-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="609ff-110">指出要清除之篩選準則的資料行值。</span><span class="sxs-lookup"><span data-stu-id="609ff-110">A column value indicating which filter to clear.</span></span>

</dd> <dt>

<span data-ttu-id="609ff-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="609ff-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="609ff-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="609ff-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="609ff-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="609ff-113">Return value</span></span>

<span data-ttu-id="609ff-114">傳回整數。</span><span class="sxs-lookup"><span data-stu-id="609ff-114">Returns an integer.</span></span> <span data-ttu-id="609ff-115">**LRESULT** 會轉換為整數，表示 **TRUE** (1) 或 **FALSE** (0) 。</span><span class="sxs-lookup"><span data-stu-id="609ff-115">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="remarks"></a><span data-ttu-id="609ff-116">備註</span><span class="sxs-lookup"><span data-stu-id="609ff-116">Remarks</span></span>

<span data-ttu-id="609ff-117">如果將資料行值指定為-1，則會清除所有篩選，而 [HDN \_ FILTERCHANGE](hdn-filterchange.md) 通知只會傳送一次。</span><span class="sxs-lookup"><span data-stu-id="609ff-117">If the column value is specified as -1, all the filters are cleared, and the [HDN\_FILTERCHANGE](hdn-filterchange.md) notification is sent only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="609ff-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="609ff-118">Requirements</span></span>



| <span data-ttu-id="609ff-119">需求</span><span class="sxs-lookup"><span data-stu-id="609ff-119">Requirement</span></span> | <span data-ttu-id="609ff-120">值</span><span class="sxs-lookup"><span data-stu-id="609ff-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="609ff-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="609ff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="609ff-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="609ff-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="609ff-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="609ff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="609ff-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="609ff-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="609ff-125">標頭</span><span class="sxs-lookup"><span data-stu-id="609ff-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="609ff-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="609ff-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="609ff-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="609ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="609ff-128">**標頭 \_ ClearAllFilters**</span><span class="sxs-lookup"><span data-stu-id="609ff-128">**Header\_ClearAllFilters**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





