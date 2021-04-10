---
title: 'TTM_TRACKACTI加值稅E 訊息 (Commctrl .h) '
description: 啟用或停用追蹤工具提示。
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- TTM_TRACKACTI加值稅E message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934622"
---
# <a name="ttm_trackactivate-message"></a><span data-ttu-id="d31fa-104">TTM \_ TRACKACTI加值稅E 訊息</span><span class="sxs-lookup"><span data-stu-id="d31fa-104">TTM\_TRACKACTIVATE message</span></span>

<span data-ttu-id="d31fa-105">啟用或停用追蹤工具提示。</span><span class="sxs-lookup"><span data-stu-id="d31fa-105">Activates or deactivates a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="d31fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="d31fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d31fa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d31fa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d31fa-108">值，指定是否要啟用或停用追蹤。</span><span class="sxs-lookup"><span data-stu-id="d31fa-108">Value specifying whether tracking is being activated or deactivated.</span></span> <span data-ttu-id="d31fa-109">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="d31fa-109">This value can be one of the following:</span></span>



| <span data-ttu-id="d31fa-110">值</span><span class="sxs-lookup"><span data-stu-id="d31fa-110">Value</span></span>                                                                                                                                | <span data-ttu-id="d31fa-111">意義</span><span class="sxs-lookup"><span data-stu-id="d31fa-111">Meaning</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="d31fa-112"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="d31fa-112"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="d31fa-113">啟用追蹤。</span><span class="sxs-lookup"><span data-stu-id="d31fa-113">Activate tracking.</span></span><br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="d31fa-114"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="d31fa-114"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="d31fa-115">停用追蹤。</span><span class="sxs-lookup"><span data-stu-id="d31fa-115">Deactivate tracking.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d31fa-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d31fa-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d31fa-117">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，此結構會識別要套用此訊息的工具。</span><span class="sxs-lookup"><span data-stu-id="d31fa-117">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that identifies the tool to which this message applies.</span></span> <span data-ttu-id="d31fa-118">**Hwnd** 和 **uId** 成員會識別工具，而 **cbSize** 成員會指定結構的大小。</span><span class="sxs-lookup"><span data-stu-id="d31fa-118">The **hwnd** and **uId** members identify the tool, and the **cbSize** member specifies the size of the structure.</span></span> <span data-ttu-id="d31fa-119">所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="d31fa-119">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d31fa-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="d31fa-120">Return value</span></span>

<span data-ttu-id="d31fa-121">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="d31fa-121">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d31fa-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d31fa-122">Requirements</span></span>



| <span data-ttu-id="d31fa-123">需求</span><span class="sxs-lookup"><span data-stu-id="d31fa-123">Requirement</span></span> | <span data-ttu-id="d31fa-124">值</span><span class="sxs-lookup"><span data-stu-id="d31fa-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d31fa-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d31fa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d31fa-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d31fa-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d31fa-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d31fa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d31fa-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d31fa-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d31fa-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d31fa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d31fa-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d31fa-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d31fa-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d31fa-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d31fa-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="d31fa-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d31fa-133">**TTM \_ TRACKPOSITION**</span><span class="sxs-lookup"><span data-stu-id="d31fa-133">**TTM\_TRACKPOSITION**</span></span>](ttm-trackposition.md)
</dt> <dt>

<span data-ttu-id="d31fa-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="d31fa-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d31fa-135">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="d31fa-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





