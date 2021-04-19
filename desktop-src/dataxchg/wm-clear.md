---
title: 'WM_CLEAR 訊息 (Winuser .h) '
description: 應用程式會將 WM \_ 清除訊息傳送至編輯控制項或下拉式方塊，以從編輯控制項中刪除 (清除) 目前的選取專案（如果有的話）。
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- WM_CLEAR 訊息資料交換
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965908"
---
# <a name="wm_clear-message"></a><span data-ttu-id="f913f-104">WM \_ 清除訊息</span><span class="sxs-lookup"><span data-stu-id="f913f-104">WM\_CLEAR message</span></span>

<span data-ttu-id="f913f-105">應用程式會將 **WM \_ 清除** 訊息傳送至編輯控制項或下拉式方塊，以從編輯控制項中刪除 (清除) 目前的選取專案（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="f913f-105">An application sends a **WM\_CLEAR** message to an edit control or combo box to delete (clear) the current selection, if any, from the edit control.</span></span>


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a><span data-ttu-id="f913f-106">參數</span><span class="sxs-lookup"><span data-stu-id="f913f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f913f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f913f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f913f-108">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="f913f-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f913f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f913f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f913f-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="f913f-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f913f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f913f-111">Return value</span></span>

<span data-ttu-id="f913f-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f913f-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f913f-113">備註</span><span class="sxs-lookup"><span data-stu-id="f913f-113">Remarks</span></span>

<span data-ttu-id="f913f-114">藉由傳送 [**EM \_ 復原**](../controls/em-undo.md)訊息的編輯控制項，可復原 **WM \_ 清除** 訊息所執行的刪除作業。</span><span class="sxs-lookup"><span data-stu-id="f913f-114">The deletion performed by the **WM\_CLEAR** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="f913f-115">若要刪除目前的選取範圍，並將已刪除的內容放到剪貼簿上，請使用 [**WM \_ 剪**](wm-cut.md) 下訊息。</span><span class="sxs-lookup"><span data-stu-id="f913f-115">To delete the current selection and place the deleted content on the clipboard, use the [**WM\_CUT**](wm-cut.md) message.</span></span>

<span data-ttu-id="f913f-116">傳送至下拉式方塊時，會由其編輯控制項來處理 **WM \_ 清除** 訊息。</span><span class="sxs-lookup"><span data-stu-id="f913f-116">When sent to a combo box, the **WM\_CLEAR** message is handled by its edit control.</span></span> <span data-ttu-id="f913f-117">將此訊息傳送至具有 [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) 樣式的下拉式方塊時，不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="f913f-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f913f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f913f-118">Requirements</span></span>



| <span data-ttu-id="f913f-119">需求</span><span class="sxs-lookup"><span data-stu-id="f913f-119">Requirement</span></span> | <span data-ttu-id="f913f-120">值</span><span class="sxs-lookup"><span data-stu-id="f913f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f913f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f913f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f913f-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f913f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f913f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f913f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f913f-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f913f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f913f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f913f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f913f-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f913f-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f913f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f913f-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f913f-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="f913f-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f913f-129">**WM \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="f913f-129">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="f913f-130">**WM \_ 剪下**</span><span class="sxs-lookup"><span data-stu-id="f913f-130">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="f913f-131">**WM \_ 貼上**</span><span class="sxs-lookup"><span data-stu-id="f913f-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="f913f-132">**WM \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="f913f-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="f913f-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="f913f-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f913f-134">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="f913f-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

