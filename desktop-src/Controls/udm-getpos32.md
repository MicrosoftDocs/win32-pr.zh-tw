---
title: 'UDM_GETPOS32 訊息 (Commctrl .h) '
description: 傳回上下按鈕控制項的32位位置。
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464648"
---
# <a name="udm_getpos32-message"></a><span data-ttu-id="446b9-104">UDM \_ GETPOS32 訊息</span><span class="sxs-lookup"><span data-stu-id="446b9-104">UDM\_GETPOS32 message</span></span>

<span data-ttu-id="446b9-105">傳回上下按鈕控制項的32位位置。</span><span class="sxs-lookup"><span data-stu-id="446b9-105">Returns the 32-bit position of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="446b9-106">參數</span><span class="sxs-lookup"><span data-stu-id="446b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="446b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="446b9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="446b9-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="446b9-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="446b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="446b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="446b9-110">如果已成功抓取值，則為 **布林** 值的指標，如果發生錯誤，則會設為非零。</span><span class="sxs-lookup"><span data-stu-id="446b9-110">Pointer to a **BOOL** value that is set to zero if the value is successfully retrieved or nonzero if an error occurs.</span></span> <span data-ttu-id="446b9-111">如果此參數設定為 **Null**，則不會報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="446b9-111">If this parameter is set to **NULL**, errors are not reported.</span></span>

<span data-ttu-id="446b9-112">如果在跨進程的情況下使用 **UDM \_ GETPOS32** ，此參數必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="446b9-112">If **UDM\_GETPOS32** is used in a cross-process situation, this parameter must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="446b9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="446b9-113">Return value</span></span>

<span data-ttu-id="446b9-114">傳回具有32位精確度的上下按鈕控制項的位置。</span><span class="sxs-lookup"><span data-stu-id="446b9-114">Returns the position of an up-down control with 32-bit precision.</span></span> <span data-ttu-id="446b9-115">應用程式必須檢查 *lParam* 值，以判斷傳回值是否有效。</span><span class="sxs-lookup"><span data-stu-id="446b9-115">Applications must check the *lParam* value to determine whether the return value is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="446b9-116">備註</span><span class="sxs-lookup"><span data-stu-id="446b9-116">Remarks</span></span>

<span data-ttu-id="446b9-117">當它處理此訊息時，上下按鈕控制項會根據好友視窗的標題來更新其目前位置。</span><span class="sxs-lookup"><span data-stu-id="446b9-117">When it processes this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="446b9-118">如果沒有好友視窗，或標題指定無效或超出範圍的值，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="446b9-118">It returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span>

## <a name="requirements"></a><span data-ttu-id="446b9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="446b9-119">Requirements</span></span>



| <span data-ttu-id="446b9-120">需求</span><span class="sxs-lookup"><span data-stu-id="446b9-120">Requirement</span></span> | <span data-ttu-id="446b9-121">值</span><span class="sxs-lookup"><span data-stu-id="446b9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="446b9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="446b9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="446b9-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="446b9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="446b9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="446b9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="446b9-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="446b9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="446b9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="446b9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="446b9-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="446b9-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="446b9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="446b9-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="446b9-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="446b9-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="446b9-130">**UDM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="446b9-130">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="446b9-131">**UDM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="446b9-131">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="446b9-132">**UDM \_ SETPOS32**</span><span class="sxs-lookup"><span data-stu-id="446b9-132">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)
</dt> </dl>

 

 





