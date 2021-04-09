---
title: 'EN_SAVECLIPBOARD (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，指出控制項正在關閉，且剪貼簿包含資訊。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- EN_SAVECLIPBOARD 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843436"
---
# <a name="en_saveclipboard-notification-code"></a><span data-ttu-id="e69bd-105">EN \_ SAVECLIPBOARD 通知碼</span><span class="sxs-lookup"><span data-stu-id="e69bd-105">EN\_SAVECLIPBOARD notification code</span></span>

<span data-ttu-id="e69bd-106">通知 rich edit 控制項的父視窗，指出控制項正在關閉，且剪貼簿包含資訊。</span><span class="sxs-lookup"><span data-stu-id="e69bd-106">Notifies the rich edit control's parent window that the control is closing and the clipboard contains information.</span></span> <span data-ttu-id="e69bd-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="e69bd-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e69bd-108">參數</span><span class="sxs-lookup"><span data-stu-id="e69bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e69bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e69bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e69bd-110">[**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)結構，其中包含剪貼簿資訊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e69bd-110">An [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) structure that contains information about clipboard information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e69bd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e69bd-111">Return value</span></span>

<span data-ttu-id="e69bd-112">如果要讓剪貼簿可供其他應用程式使用，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="e69bd-112">Return zero if the clipboard should be made available to other applications.</span></span>

<span data-ttu-id="e69bd-113">如果不應儲存剪貼簿，則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="e69bd-113">Return a nonzero value if the clipboard should not be saved.</span></span>

## <a name="remarks"></a><span data-ttu-id="e69bd-114">備註</span><span class="sxs-lookup"><span data-stu-id="e69bd-114">Remarks</span></span>

<span data-ttu-id="e69bd-115">父視窗一律會取得這個事件的 [**WM \_ 通知**](wm-notify.md) 訊息，不需要以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)傳送通知遮罩。</span><span class="sxs-lookup"><span data-stu-id="e69bd-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e69bd-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e69bd-116">Requirements</span></span>



| <span data-ttu-id="e69bd-117">需求</span><span class="sxs-lookup"><span data-stu-id="e69bd-117">Requirement</span></span> | <span data-ttu-id="e69bd-118">值</span><span class="sxs-lookup"><span data-stu-id="e69bd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e69bd-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e69bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e69bd-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e69bd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e69bd-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e69bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e69bd-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e69bd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e69bd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e69bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e69bd-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e69bd-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e69bd-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e69bd-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="e69bd-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="e69bd-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e69bd-127">**ENSAVECLIPBOARD**</span><span class="sxs-lookup"><span data-stu-id="e69bd-127">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





