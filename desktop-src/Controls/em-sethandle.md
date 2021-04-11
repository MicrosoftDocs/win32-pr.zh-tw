---
title: 'EM_SETHANDLE 訊息 (Winuser .h) '
description: 設定多行編輯控制項將使用的記憶體控制碼。
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105575"
---
# <a name="em_sethandle-message"></a><span data-ttu-id="5394e-104">EM \_ SETHANDLE 訊息</span><span class="sxs-lookup"><span data-stu-id="5394e-104">EM\_SETHANDLE message</span></span>

<span data-ttu-id="5394e-105">設定多行編輯控制項將使用的記憶體控制碼。</span><span class="sxs-lookup"><span data-stu-id="5394e-105">Sets the handle of the memory that will be used by a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5394e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5394e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5394e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5394e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5394e-108">記憶體緩衝區的控制碼，編輯控制項會用來儲存目前顯示的文字，而非配置它自己的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5394e-108">A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory.</span></span> <span data-ttu-id="5394e-109">必要時，控制項會重新配置此記憶體。</span><span class="sxs-lookup"><span data-stu-id="5394e-109">If necessary, the control reallocates this memory.</span></span>

</dd> <dt>

<span data-ttu-id="5394e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5394e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5394e-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="5394e-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5394e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5394e-112">Return value</span></span>

<span data-ttu-id="5394e-113">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5394e-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5394e-114">備註</span><span class="sxs-lookup"><span data-stu-id="5394e-114">Remarks</span></span>

<span data-ttu-id="5394e-115">在應用程式設定新的記憶體控制碼之前，它應該傳送 [**EM \_ GETHANDLE**](em-gethandle.md) 訊息來取出目前記憶體緩衝區的控制碼，而且應該釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="5394e-115">Before an application sets a new memory handle, it should send an [**EM\_GETHANDLE**](em-gethandle.md) message to retrieve the handle of the current memory buffer and should free that memory.</span></span>

<span data-ttu-id="5394e-116">編輯控制項會在需要額外的文字空間時，自動重新配置指定的緩衝區，或移除足夠的文字以不再需要額外的空間。</span><span class="sxs-lookup"><span data-stu-id="5394e-116">An edit control automatically reallocates the given buffer whenever it needs additional space for text, or it removes enough text so that additional space is no longer needed.</span></span>

<span data-ttu-id="5394e-117">傳送 **EM \_ SETHANDLE** 訊息會清除復原緩衝區 ([**em \_ CANUNDO**](em-canundo.md) 會傳回零) 和內部修改旗標 ([**EM \_ GETMODIFY**](em-getmodify.md) 會傳回零) 。</span><span class="sxs-lookup"><span data-stu-id="5394e-117">Sending an **EM\_SETHANDLE** message clears the undo buffer ([**EM\_CANUNDO**](em-canundo.md) returns zero) and the internal modification flag ([**EM\_GETMODIFY**](em-getmodify.md) returns zero).</span></span> <span data-ttu-id="5394e-118">會重新繪製編輯控制項視窗。</span><span class="sxs-lookup"><span data-stu-id="5394e-118">The edit control window is redrawn.</span></span>

<span data-ttu-id="5394e-119">**Rich Edit：** 不支援 **EM \_ SETHANDLE** 訊息。</span><span class="sxs-lookup"><span data-stu-id="5394e-119">**Rich Edit:** The **EM\_SETHANDLE** message is not supported.</span></span> <span data-ttu-id="5394e-120">Rich edit 控制項不會將文字儲存為簡單字元陣列。</span><span class="sxs-lookup"><span data-stu-id="5394e-120">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5394e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5394e-121">Requirements</span></span>



| <span data-ttu-id="5394e-122">需求</span><span class="sxs-lookup"><span data-stu-id="5394e-122">Requirement</span></span> | <span data-ttu-id="5394e-123">值</span><span class="sxs-lookup"><span data-stu-id="5394e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5394e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5394e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5394e-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5394e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5394e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5394e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5394e-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5394e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5394e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5394e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5394e-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5394e-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5394e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5394e-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5394e-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="5394e-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5394e-132">**EM \_ CANUNDO**</span><span class="sxs-lookup"><span data-stu-id="5394e-132">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="5394e-133">**EM \_ GETHANDLE**</span><span class="sxs-lookup"><span data-stu-id="5394e-133">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

[<span data-ttu-id="5394e-134">**EM \_ GETMODIFY**</span><span class="sxs-lookup"><span data-stu-id="5394e-134">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> </dl>

 

 





