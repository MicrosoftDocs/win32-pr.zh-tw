---
title: 'EN_DROPFILES (Richedit 的通知碼) '
description: 通知 rich edit 控制項父視窗，使用者嘗試將檔案放入控制項。 Rich edit 控制項會在 \_ 收到 wm DROPFILES 訊息時，以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464425"
---
# <a name="en_dropfiles-notification-code"></a><span data-ttu-id="6ef76-105">EN \_ DROPFILES 通知碼</span><span class="sxs-lookup"><span data-stu-id="6ef76-105">EN\_DROPFILES notification code</span></span>

<span data-ttu-id="6ef76-106">通知 rich edit 控制項父視窗，使用者嘗試將檔案放入控制項。</span><span class="sxs-lookup"><span data-stu-id="6ef76-106">Notifies a rich edit control parent window that the user is attempting to drop files into the control.</span></span> <span data-ttu-id="6ef76-107">Rich edit 控制項會在收到 [**wm \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles)訊息時，以 [**WM \_ 通知**](wm-notify.md)訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="6ef76-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message when it receives the [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) message.</span></span>


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6ef76-108">參數</span><span class="sxs-lookup"><span data-stu-id="6ef76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef76-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ef76-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ef76-110">接收已卸載檔案資訊的 [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) 結構。</span><span class="sxs-lookup"><span data-stu-id="6ef76-110">An [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure that receives dropped files information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ef76-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ef76-111">Return value</span></span>

<span data-ttu-id="6ef76-112">傳回非零值以允許 drop 作業。</span><span class="sxs-lookup"><span data-stu-id="6ef76-112">Return a nonzero value to allow the drop operation.</span></span>

<span data-ttu-id="6ef76-113">傳回零以忽略 drop 作業。</span><span class="sxs-lookup"><span data-stu-id="6ef76-113">Return zero to ignore the drop operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef76-114">備註</span><span class="sxs-lookup"><span data-stu-id="6ef76-114">Remarks</span></span>

<span data-ttu-id="6ef76-115">若要讓 rich edit 控制項接收 [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) 訊息，父視窗必須使用 [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) 函數，將控制項註冊為放置目標。</span><span class="sxs-lookup"><span data-stu-id="6ef76-115">For a rich edit control to receive [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) messages, the parent window must register the control as a drop target by using the [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) function.</span></span> <span data-ttu-id="6ef76-116">控制項不會自行註冊。</span><span class="sxs-lookup"><span data-stu-id="6ef76-116">The control does not register itself.</span></span>

<span data-ttu-id="6ef76-117">若要接收 EN \_ DROPFILES 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="6ef76-117">To receive EN\_DROPFILES notification codes, specify [**ENM\_DROPFILES**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef76-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ef76-118">Requirements</span></span>



| <span data-ttu-id="6ef76-119">需求</span><span class="sxs-lookup"><span data-stu-id="6ef76-119">Requirement</span></span> | <span data-ttu-id="6ef76-120">值</span><span class="sxs-lookup"><span data-stu-id="6ef76-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef76-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ef76-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef76-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ef76-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ef76-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ef76-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef76-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ef76-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ef76-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6ef76-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ef76-126"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ef76-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef76-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ef76-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ef76-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="6ef76-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6ef76-129">**ENDROPFILES**</span><span class="sxs-lookup"><span data-stu-id="6ef76-129">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

