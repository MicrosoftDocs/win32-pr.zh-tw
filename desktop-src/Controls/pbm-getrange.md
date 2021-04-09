---
title: 'PBM_GETRANGE 訊息 (Commctrl .h) '
description: 抓取指定進度列控制項目前最高和最低限制的相關資訊。
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934722"
---
# <a name="pbm_getrange-message"></a><span data-ttu-id="75978-104">PBM \_ GETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="75978-104">PBM\_GETRANGE message</span></span>

<span data-ttu-id="75978-105">抓取指定進度列控制項目前最高和最低限制的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="75978-105">Retrieves information about the current high and low limits of a given progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="75978-106">參數</span><span class="sxs-lookup"><span data-stu-id="75978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75978-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75978-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75978-108">旗標值，指定要使用哪個限制值做為訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="75978-108">Flag value specifying which limit value is to be used as the message's return value.</span></span> <span data-ttu-id="75978-109">這個參數可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="75978-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="75978-110">值</span><span class="sxs-lookup"><span data-stu-id="75978-110">Value</span></span>                                                                                                                                    | <span data-ttu-id="75978-111">意義</span><span class="sxs-lookup"><span data-stu-id="75978-111">Meaning</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="75978-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="75978-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="75978-113">傳回低限制。</span><span class="sxs-lookup"><span data-stu-id="75978-113">Return the low limit.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="75978-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="75978-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="75978-115">傳回高限制。</span><span class="sxs-lookup"><span data-stu-id="75978-115">Return the high limit.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="75978-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75978-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75978-117">[**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange)結構的指標，此結構會以進度列控制項的高度和下限來填滿。</span><span class="sxs-lookup"><span data-stu-id="75978-117">Pointer to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with the high and low limits of the progress bar control.</span></span> <span data-ttu-id="75978-118">如果此參數設定為 **Null**，則控制項只會傳回 *wParam* 所指定的限制。</span><span class="sxs-lookup"><span data-stu-id="75978-118">If this parameter is set to **NULL**, the control will return only the limit specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75978-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="75978-119">Return value</span></span>

<span data-ttu-id="75978-120">傳回整數，表示 *wParam* 所指定的限制值。</span><span class="sxs-lookup"><span data-stu-id="75978-120">Returns an INT that represents the limit value specified by *wParam*.</span></span> <span data-ttu-id="75978-121">如果 *lParam* 不是 **Null**，則 *lParam* 必須指向要使用兩個限制值填滿的 [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) 結構。</span><span class="sxs-lookup"><span data-stu-id="75978-121">If *lParam* is not **NULL**, *lParam* must point to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with both limit values.</span></span>

## <a name="requirements"></a><span data-ttu-id="75978-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="75978-122">Requirements</span></span>



| <span data-ttu-id="75978-123">需求</span><span class="sxs-lookup"><span data-stu-id="75978-123">Requirement</span></span> | <span data-ttu-id="75978-124">值</span><span class="sxs-lookup"><span data-stu-id="75978-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75978-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75978-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75978-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75978-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75978-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75978-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75978-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75978-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75978-129">標頭</span><span class="sxs-lookup"><span data-stu-id="75978-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="75978-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="75978-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





