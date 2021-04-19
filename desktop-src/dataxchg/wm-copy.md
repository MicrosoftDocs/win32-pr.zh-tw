---
title: 'WM_COPY 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 複製訊息傳送至編輯控制項或下拉式方塊，以 CF 文字格式將目前的選取範圍複製到剪貼簿 \_ 。
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY 訊息資料交換
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "106986452"
---
# <a name="wm_copy-message"></a><span data-ttu-id="7a5c6-104">WM \_ 複製訊息</span><span class="sxs-lookup"><span data-stu-id="7a5c6-104">WM\_COPY message</span></span>

<span data-ttu-id="7a5c6-105">應用程式會將 **WM \_ 複製** 訊息傳送至編輯控制項或下拉式方塊，以 [**CF \_ 文字**](standard-clipboard-formats.md) 格式將目前的選取範圍複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="7a5c6-105">An application sends the **WM\_COPY** message to an edit control or combo box to copy the current selection to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a><span data-ttu-id="7a5c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a5c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a5c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a5c6-108">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="7a5c6-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7a5c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a5c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a5c6-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="7a5c6-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5c6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a5c6-111">Return value</span></span>

<span data-ttu-id="7a5c6-112">在成功時傳回非零值，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="7a5c6-112">Returns nonzero value on success, else zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a5c6-113">備註</span><span class="sxs-lookup"><span data-stu-id="7a5c6-113">Remarks</span></span>

<span data-ttu-id="7a5c6-114">傳送至下拉式方塊時，會由其編輯控制項來處理 **WM \_ 複製** 訊息。</span><span class="sxs-lookup"><span data-stu-id="7a5c6-114">When sent to a combo box, the **WM\_COPY** message is handled by its edit control.</span></span> <span data-ttu-id="7a5c6-115">將此訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) 樣式的下拉式方塊時，不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="7a5c6-115">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a5c6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a5c6-116">Requirements</span></span>



| <span data-ttu-id="7a5c6-117">需求</span><span class="sxs-lookup"><span data-stu-id="7a5c6-117">Requirement</span></span> | <span data-ttu-id="7a5c6-118">值</span><span class="sxs-lookup"><span data-stu-id="7a5c6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5c6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a5c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5c6-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a5c6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7a5c6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a5c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5c6-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a5c6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a5c6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7a5c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a5c6-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7a5c6-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a5c6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a5c6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7a5c6-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="7a5c6-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7a5c6-127">**WM \_ 清除**</span><span class="sxs-lookup"><span data-stu-id="7a5c6-127">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="7a5c6-128">**WM \_ 剪下**</span><span class="sxs-lookup"><span data-stu-id="7a5c6-128">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="7a5c6-129">**WM \_ 貼上**</span><span class="sxs-lookup"><span data-stu-id="7a5c6-129">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="7a5c6-130">**WM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="7a5c6-130">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="7a5c6-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="7a5c6-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7a5c6-132">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="7a5c6-132">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

