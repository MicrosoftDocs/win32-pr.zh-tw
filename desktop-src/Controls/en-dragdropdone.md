---
title: 'EN_DRAGDROPDONE (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，拖放作業已完成。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- EN_DRAGDROPDONE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933963"
---
# <a name="en_dragdropdone-notification-code"></a><span data-ttu-id="514cd-105">EN \_ DRAGDROPDONE 通知碼</span><span class="sxs-lookup"><span data-stu-id="514cd-105">EN\_DRAGDROPDONE notification code</span></span>

<span data-ttu-id="514cd-106">通知 rich edit 控制項的父視窗，拖放作業已完成。</span><span class="sxs-lookup"><span data-stu-id="514cd-106">Notifies a rich edit control's parent window that the drag-and-drop operation has completed.</span></span> <span data-ttu-id="514cd-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="514cd-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="514cd-108">參數</span><span class="sxs-lookup"><span data-stu-id="514cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="514cd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="514cd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="514cd-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構。</span><span class="sxs-lookup"><span data-stu-id="514cd-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="514cd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="514cd-111">Return value</span></span>

<span data-ttu-id="514cd-112">此通知碼不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="514cd-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="514cd-113">備註</span><span class="sxs-lookup"><span data-stu-id="514cd-113">Remarks</span></span>

<span data-ttu-id="514cd-114">若要接收 EN \_ DRAGDROPDONE 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ DRAGDROPDONE**](rich-edit-control-event-mask-flags.md)旗標。</span><span class="sxs-lookup"><span data-stu-id="514cd-114">To receive an EN\_DRAGDROPDONE notification code, specify the [**ENM\_DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="514cd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="514cd-115">Requirements</span></span>



| <span data-ttu-id="514cd-116">需求</span><span class="sxs-lookup"><span data-stu-id="514cd-116">Requirement</span></span> | <span data-ttu-id="514cd-117">值</span><span class="sxs-lookup"><span data-stu-id="514cd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="514cd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="514cd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="514cd-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="514cd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="514cd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="514cd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="514cd-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="514cd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="514cd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="514cd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="514cd-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="514cd-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514cd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="514cd-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="514cd-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="514cd-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="514cd-126">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="514cd-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> </dl>

 

 





