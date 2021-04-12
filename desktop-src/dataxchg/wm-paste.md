---
title: 'WM_PASTE 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 貼上訊息傳送至編輯控制項或下拉式方塊，以將剪貼簿目前的內容複寫到目前插入號位置的編輯控制項。 只有當剪貼簿包含 CF 文字格式的資料時，才會插入資料 \_ 。
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385094"
---
# <a name="wm_paste-message"></a><span data-ttu-id="b7ed8-105">WM \_ 貼上訊息</span><span class="sxs-lookup"><span data-stu-id="b7ed8-105">WM\_PASTE message</span></span>

<span data-ttu-id="b7ed8-106">應用程式會將 **WM \_ 貼** 上訊息傳送至編輯控制項或下拉式方塊，以將剪貼簿目前的內容複寫到目前插入號位置的編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="b7ed8-106">An application sends a **WM\_PASTE** message to an edit control or combo box to copy the current content of the clipboard to the edit control at the current caret position.</span></span> <span data-ttu-id="b7ed8-107">只有當剪貼簿包含 [**CF \_ 文字**](standard-clipboard-formats.md) 格式的資料時，才會插入資料。</span><span class="sxs-lookup"><span data-stu-id="b7ed8-107">Data is inserted only if the clipboard contains data in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a><span data-ttu-id="b7ed8-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7ed8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7ed8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7ed8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7ed8-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="b7ed8-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b7ed8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7ed8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7ed8-112">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="b7ed8-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7ed8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7ed8-113">Return value</span></span>

<span data-ttu-id="b7ed8-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b7ed8-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7ed8-115">備註</span><span class="sxs-lookup"><span data-stu-id="b7ed8-115">Remarks</span></span>

<span data-ttu-id="b7ed8-116">傳送至下拉式方塊時，會由其編輯控制項來處理 **WM \_ 貼** 上訊息。</span><span class="sxs-lookup"><span data-stu-id="b7ed8-116">When sent to a combo box, the **WM\_PASTE** message is handled by its edit control.</span></span> <span data-ttu-id="b7ed8-117">將此訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) 樣式的下拉式方塊時，不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="b7ed8-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ed8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7ed8-118">Requirements</span></span>



| <span data-ttu-id="b7ed8-119">需求</span><span class="sxs-lookup"><span data-stu-id="b7ed8-119">Requirement</span></span> | <span data-ttu-id="b7ed8-120">值</span><span class="sxs-lookup"><span data-stu-id="b7ed8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ed8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7ed8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7ed8-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7ed8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b7ed8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7ed8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7ed8-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7ed8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7ed8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b7ed8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7ed8-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b7ed8-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ed8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7ed8-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7ed8-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="b7ed8-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b7ed8-129">**WM \_ 清除**</span><span class="sxs-lookup"><span data-stu-id="b7ed8-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="b7ed8-130">**WM \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="b7ed8-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="b7ed8-131">**WM \_ 剪下**</span><span class="sxs-lookup"><span data-stu-id="b7ed8-131">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="b7ed8-132">**WM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="b7ed8-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="b7ed8-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="b7ed8-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b7ed8-134">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="b7ed8-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

