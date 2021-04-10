---
title: 'EN_CLIPFORMAT (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，貼上有特定剪貼簿格式的貼上。 無視窗的 rich edit 控制項會使用 ITextHost TxNotify 方法傳送這項通知。
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934202"
---
# <a name="en_clipformat-notification-code"></a><span data-ttu-id="ff44f-105">EN \_ CLIPFORMAT 通知碼</span><span class="sxs-lookup"><span data-stu-id="ff44f-105">EN\_CLIPFORMAT notification code</span></span>

<span data-ttu-id="ff44f-106">通知 rich edit 控制項的父視窗，貼上有特定剪貼簿格式的貼上。</span><span class="sxs-lookup"><span data-stu-id="ff44f-106">Notifies a rich edit control's parent window that a paste occurred with a particular clipboard format.</span></span> <span data-ttu-id="ff44f-107">無視窗的 rich edit 控制項會使用 [**ITextHost：： TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) 方法傳送這個通知。</span><span class="sxs-lookup"><span data-stu-id="ff44f-107">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span>


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ff44f-108">參數</span><span class="sxs-lookup"><span data-stu-id="ff44f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff44f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff44f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff44f-110">藉由呼叫 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 函式與 GWL 識別碼值來抓取的視窗識別碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff44f-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="ff44f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff44f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff44f-112">[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)結構的指標，其中包含剪貼簿格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ff44f-112">A pointer to a [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) structure that contains information about the clipboard format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff44f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff44f-113">Return value</span></span>

<span data-ttu-id="ff44f-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="ff44f-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff44f-115">備註</span><span class="sxs-lookup"><span data-stu-id="ff44f-115">Remarks</span></span>

<span data-ttu-id="ff44f-116">若要接收 EN \_ CLIPFORMAT 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="ff44f-116">To receive EN\_CLIPFORMAT notification codes, specify [**ENM\_CLIPFORMAT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff44f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff44f-117">Requirements</span></span>



| <span data-ttu-id="ff44f-118">需求</span><span class="sxs-lookup"><span data-stu-id="ff44f-118">Requirement</span></span> | <span data-ttu-id="ff44f-119">值</span><span class="sxs-lookup"><span data-stu-id="ff44f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff44f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff44f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff44f-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff44f-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ff44f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff44f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff44f-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff44f-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff44f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ff44f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff44f-125"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff44f-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff44f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff44f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff44f-127">**CLIPBOARDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ff44f-127">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

