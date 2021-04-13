---
title: 'DM_SETDEFID 訊息 (Winuser .h) '
description: 變更對話方塊的預設按鈕的識別碼。
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID 訊息對話方塊
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509308"
---
# <a name="dm_setdefid-message"></a><span data-ttu-id="57289-104">DM \_ SETDEFID 訊息</span><span class="sxs-lookup"><span data-stu-id="57289-104">DM\_SETDEFID message</span></span>

<span data-ttu-id="57289-105">變更對話方塊的預設按鈕的識別碼。</span><span class="sxs-lookup"><span data-stu-id="57289-105">Changes the identifier of the default push button for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="57289-106">參數</span><span class="sxs-lookup"><span data-stu-id="57289-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57289-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57289-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57289-108">將成為預設值的按鈕控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="57289-108">The identifier of a push button control that will become the default.</span></span>

</dd> <dt>

<span data-ttu-id="57289-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57289-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57289-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="57289-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57289-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="57289-111">Return value</span></span>

<span data-ttu-id="57289-112">傳回值一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="57289-112">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="57289-113">備註</span><span class="sxs-lookup"><span data-stu-id="57289-113">Remarks</span></span>

<span data-ttu-id="57289-114">此訊息是由 [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) 函數處理。</span><span class="sxs-lookup"><span data-stu-id="57289-114">This message is processed by the [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="57289-115">若要設定預設的推播按鈕，函式可以將 [**WM \_ GETDLGCODE**](wm-getdlgcode.md) 和 [**BM \_ >setstyle**](../controls/bm-setstyle.md) 訊息傳送至指定的控制項和目前的預設推送按鈕。</span><span class="sxs-lookup"><span data-stu-id="57289-115">To set the default push button, the function can send [**WM\_GETDLGCODE**](wm-getdlgcode.md) and [**BM\_SETSTYLE**](../controls/bm-setstyle.md) messages to the specified control and the current default push button.</span></span>

<span data-ttu-id="57289-116">使用 **DM \_ SETDEFID** 訊息可能會導致出現一個以上的按鈕，使其具有預設的推播按鈕狀態。</span><span class="sxs-lookup"><span data-stu-id="57289-116">Using the **DM\_SETDEFID** message can result in more than one button appearing to have the default push button state.</span></span> <span data-ttu-id="57289-117">當系統顯示對話方塊時，它會在對話方塊範本中繪製具有預設狀態框線的第一個 push 按鈕。</span><span class="sxs-lookup"><span data-stu-id="57289-117">When the system brings up a dialog, it draws the first push button in the dialog template with the default state border.</span></span> <span data-ttu-id="57289-118">傳送 **DM \_ SETDEFID** 訊息來變更預設按鈕，並不一定會從第一個 push 按鈕移除預設狀態框線。</span><span class="sxs-lookup"><span data-stu-id="57289-118">Sending a **DM\_SETDEFID** message to change the default button will not always remove the default state border from the first push button.</span></span> <span data-ttu-id="57289-119">在這些情況下，應用程式應該傳送 [**BM \_ >setstyle**](../controls/bm-setstyle.md) 訊息來變更第一個 push 按鈕框線樣式。</span><span class="sxs-lookup"><span data-stu-id="57289-119">In these cases, the application should send a [**BM\_SETSTYLE**](../controls/bm-setstyle.md) message to change the first push button border style.</span></span>

## <a name="requirements"></a><span data-ttu-id="57289-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="57289-120">Requirements</span></span>



| <span data-ttu-id="57289-121">需求</span><span class="sxs-lookup"><span data-stu-id="57289-121">Requirement</span></span> | <span data-ttu-id="57289-122">值</span><span class="sxs-lookup"><span data-stu-id="57289-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57289-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57289-123">Minimum supported client</span></span><br/> | <span data-ttu-id="57289-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57289-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="57289-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57289-125">Minimum supported server</span></span><br/> | <span data-ttu-id="57289-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57289-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57289-127">標頭</span><span class="sxs-lookup"><span data-stu-id="57289-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="57289-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="57289-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57289-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57289-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="57289-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="57289-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57289-131">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="57289-131">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="57289-132">**DM \_ GETDEFID**</span><span class="sxs-lookup"><span data-stu-id="57289-132">**DM\_GETDEFID**</span></span>](dm-getdefid.md)
</dt> <dt>

[<span data-ttu-id="57289-133">**WM \_ GETDLGCODE**</span><span class="sxs-lookup"><span data-stu-id="57289-133">**WM\_GETDLGCODE**</span></span>](wm-getdlgcode.md)
</dt> <dt>

<span data-ttu-id="57289-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="57289-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57289-135">對話方塊</span><span class="sxs-lookup"><span data-stu-id="57289-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="57289-136">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="57289-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="57289-137">**BM \_ >SETSTYLE**</span><span class="sxs-lookup"><span data-stu-id="57289-137">**BM\_SETSTYLE**</span></span>](../controls/bm-setstyle.md)
</dt> <dt>

[<span data-ttu-id="57289-138">**EM \_ SETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="57289-138">**EM\_SETLIMITTEXT**</span></span>](../controls/em-setlimittext.md)
</dt> </dl>

 

