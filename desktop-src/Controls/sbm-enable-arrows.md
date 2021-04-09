---
title: 'SBM_ENABLE_ARROWS 訊息 (Winuser .h) '
description: 應用程式會傳送 SBM \_ 啟用 \_ 箭號訊息，以啟用或停用捲軸控制項的一個或兩個箭號。
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934791"
---
# <a name="sbm_enable_arrows-message"></a><span data-ttu-id="a8791-104">SBM \_ 啟用 \_ 箭號訊息</span><span class="sxs-lookup"><span data-stu-id="a8791-104">SBM\_ENABLE\_ARROWS message</span></span>

<span data-ttu-id="a8791-105">應用程式會傳送 **SBM \_ 啟用 \_ 箭** 號訊息，以啟用或停用捲軸控制項的一個或兩個箭號。</span><span class="sxs-lookup"><span data-stu-id="a8791-105">An application sends the **SBM\_ENABLE\_ARROWS** message to enable or disable one or both arrows of a scroll bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8791-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8791-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8791-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8791-108">指定捲軸箭號是否為啟用或停用，以及表示已啟用或停用的箭號。</span><span class="sxs-lookup"><span data-stu-id="a8791-108">Specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled.</span></span> <span data-ttu-id="a8791-109">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a8791-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a8791-110">值</span><span class="sxs-lookup"><span data-stu-id="a8791-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="a8791-111">意義</span><span class="sxs-lookup"><span data-stu-id="a8791-111">Meaning</span></span>                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <span data-ttu-id="a8791-112"><dt>**ESB \_ 停用 \_ 兩者**</dt></span><span class="sxs-lookup"><span data-stu-id="a8791-112"><dt>**ESB\_DISABLE\_BOTH**</dt></span></span> </dl> | <span data-ttu-id="a8791-113">停用捲軸上的兩個箭號。</span><span class="sxs-lookup"><span data-stu-id="a8791-113">Disables both arrows on a scroll bar.</span></span><br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <span data-ttu-id="a8791-114"><dt>**ESB \_ 停 \_ 用**</dt></span><span class="sxs-lookup"><span data-stu-id="a8791-114"><dt>**ESB\_DISABLE\_DOWN**</dt></span></span> </dl> | <span data-ttu-id="a8791-115">停用垂直捲動條上的向下箭號。</span><span class="sxs-lookup"><span data-stu-id="a8791-115">Disables the down arrow on a vertical scroll bar.</span></span><br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <span data-ttu-id="a8791-116"><dt>**ESB \_ 停用 \_ LTUP**</dt></span><span class="sxs-lookup"><span data-stu-id="a8791-116"><dt>**ESB\_DISABLE\_LTUP**</dt></span></span> </dl> | <span data-ttu-id="a8791-117">停用水準捲軸上的向左箭號或垂直捲動條上的向上箭號。</span><span class="sxs-lookup"><span data-stu-id="a8791-117">Disables the left arrow on a horizontal scroll bar or the up arrow on a vertical scroll bar.</span></span><br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <span data-ttu-id="a8791-118"><dt>**ESB \_ 停用 \_ 左**</dt></span><span class="sxs-lookup"><span data-stu-id="a8791-118"><dt>**ESB\_DISABLE\_LEFT**</dt></span></span> </dl> | <span data-ttu-id="a8791-119">停用水準捲軸上的向左鍵。</span><span class="sxs-lookup"><span data-stu-id="a8791-119">Disables the left arrow on a horizontal scroll bar.</span></span><br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <span data-ttu-id="a8791-120"><dt>**ESB \_ 停用 \_ RTDN**</dt></span><span class="sxs-lookup"><span data-stu-id="a8791-120"><dt>**ESB\_DISABLE\_RTDN**</dt></span></span> </dl> | <span data-ttu-id="a8791-121">停用水準捲軸上的向右箭號或垂直捲動條上的向下箭號。</span><span class="sxs-lookup"><span data-stu-id="a8791-121">Disables the right arrow on a horizontal scroll bar or the down arrow on a vertical scroll bar.</span></span><br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <span data-ttu-id="a8791-122"><dt>**ESB \_ 停 \_ 用**</dt></span><span class="sxs-lookup"><span data-stu-id="a8791-122"><dt>**ESB\_DISABLE\_UP**</dt></span></span> </dl>       | <span data-ttu-id="a8791-123">停用垂直捲動條上的向上箭號。</span><span class="sxs-lookup"><span data-stu-id="a8791-123">Disables the up arrow on a vertical scroll bar.</span></span><br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <span data-ttu-id="a8791-124"><dt>**ESB \_ 啟用 \_ 兩者**</dt></span><span class="sxs-lookup"><span data-stu-id="a8791-124"><dt>**ESB\_ENABLE\_BOTH**</dt></span></span> </dl>    | <span data-ttu-id="a8791-125">在捲軸上啟用這兩個箭號。</span><span class="sxs-lookup"><span data-stu-id="a8791-125">Enables both arrows on a scroll bar.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="a8791-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8791-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8791-127">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="a8791-127">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8791-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8791-128">Return value</span></span>

<span data-ttu-id="a8791-129">如果訊息成功，則傳回值為 **TRUE**;否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a8791-129">If the message succeeds, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8791-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8791-130">Requirements</span></span>



| <span data-ttu-id="a8791-131">需求</span><span class="sxs-lookup"><span data-stu-id="a8791-131">Requirement</span></span> | <span data-ttu-id="a8791-132">值</span><span class="sxs-lookup"><span data-stu-id="a8791-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8791-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8791-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a8791-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8791-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8791-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8791-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a8791-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8791-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8791-137">標頭</span><span class="sxs-lookup"><span data-stu-id="a8791-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8791-138"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a8791-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





