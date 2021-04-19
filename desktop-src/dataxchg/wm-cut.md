---
title: 'WM_CUT 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 剪下訊息傳送至編輯控制項或下拉式方塊，以刪除 (剪下) 目前的選取專案（如果有的話），並將已刪除的文字複製到 [剪貼簿] 中的 CF \_ 文字格式。
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT 訊息資料交換
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968959"
---
# <a name="wm_cut-message"></a><span data-ttu-id="23f84-104">WM \_ 剪下訊息</span><span class="sxs-lookup"><span data-stu-id="23f84-104">WM\_CUT message</span></span>

<span data-ttu-id="23f84-105">應用程式會將 **WM \_ 剪** 下訊息傳送至編輯控制項或下拉式方塊，以刪除 (剪下) 目前的選取專案（如果有的話），並將已刪除的文字複製到 [剪貼簿] 中的 [**CF \_ 文字**](standard-clipboard-formats.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="23f84-105">An application sends a **WM\_CUT** message to an edit control or combo box to delete (cut) the current selection, if any, in the edit control and copy the deleted text to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_CUT                          0x0300
```



## <a name="parameters"></a><span data-ttu-id="23f84-106">參數</span><span class="sxs-lookup"><span data-stu-id="23f84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23f84-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23f84-108">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="23f84-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="23f84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23f84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23f84-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="23f84-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f84-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="23f84-111">Return value</span></span>

<span data-ttu-id="23f84-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="23f84-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f84-113">備註</span><span class="sxs-lookup"><span data-stu-id="23f84-113">Remarks</span></span>

<span data-ttu-id="23f84-114">藉由傳送 [**EM \_ 復原**](../controls/em-undo.md)訊息的編輯控制項，可復原由 **WM \_ 剪** 下訊息執行的刪除作業。</span><span class="sxs-lookup"><span data-stu-id="23f84-114">The deletion performed by the **WM\_CUT** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="23f84-115">若要刪除目前的選取範圍，而不將刪除的文字放在剪貼簿上，請使用 [**WM \_ CLEAR**](wm-clear.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="23f84-115">To delete the current selection without placing the deleted text on the clipboard, use the [**WM\_CLEAR**](wm-clear.md) message.</span></span>

<span data-ttu-id="23f84-116">傳送至下拉式方塊時，會由其編輯控制項來處理 **WM \_ 剪** 下訊息。</span><span class="sxs-lookup"><span data-stu-id="23f84-116">When sent to a combo box, the **WM\_CUT** message is handled by its edit control.</span></span> <span data-ttu-id="23f84-117">將此訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) 樣式的下拉式方塊時，不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="23f84-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f84-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="23f84-118">Requirements</span></span>



| <span data-ttu-id="23f84-119">需求</span><span class="sxs-lookup"><span data-stu-id="23f84-119">Requirement</span></span> | <span data-ttu-id="23f84-120">值</span><span class="sxs-lookup"><span data-stu-id="23f84-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f84-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23f84-121">Minimum supported client</span></span><br/> | <span data-ttu-id="23f84-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23f84-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="23f84-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23f84-123">Minimum supported server</span></span><br/> | <span data-ttu-id="23f84-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23f84-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="23f84-125">標頭</span><span class="sxs-lookup"><span data-stu-id="23f84-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="23f84-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="23f84-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f84-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23f84-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="23f84-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="23f84-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="23f84-129">**WM \_ 清除**</span><span class="sxs-lookup"><span data-stu-id="23f84-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="23f84-130">**WM \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="23f84-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="23f84-131">**WM \_ 貼上**</span><span class="sxs-lookup"><span data-stu-id="23f84-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="23f84-132">**WM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="23f84-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="23f84-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="23f84-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="23f84-134">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="23f84-134">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="23f84-135">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="23f84-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="23f84-136">**EM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="23f84-136">**EM\_UNDO**</span></span>](../controls/em-undo.md)
</dt> </dl>

 

