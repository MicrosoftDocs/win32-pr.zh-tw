---
title: 'WM_CLIPBOARDUPDATE 訊息 (Winuser .h) '
description: 當剪貼簿的內容變更時傳送。
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- WM_CLIPBOARDUPDATE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303110f0d094cfed336a9f92006b3720a0ccc83b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104087"
---
# <a name="wm_clipboardupdate-message"></a><span data-ttu-id="b5769-104">WM \_ CLIPBOARDUPDATE 訊息</span><span class="sxs-lookup"><span data-stu-id="b5769-104">WM\_CLIPBOARDUPDATE message</span></span>

<span data-ttu-id="b5769-105">當剪貼簿的內容變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="b5769-105">Sent when the contents of the clipboard have changed.</span></span>


```C++
#define WM_CLIPBOARDUPDATE              0x031D
```



## <a name="parameters"></a><span data-ttu-id="b5769-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5769-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5769-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5769-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5769-108">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="b5769-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5769-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5769-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5769-110">未使用此參數，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="b5769-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5769-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5769-111">Return value</span></span>

<span data-ttu-id="b5769-112">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b5769-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5769-113">備註</span><span class="sxs-lookup"><span data-stu-id="b5769-113">Remarks</span></span>

<span data-ttu-id="b5769-114">若要註冊視窗以接收此訊息，請使用 [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) 函數。</span><span class="sxs-lookup"><span data-stu-id="b5769-114">To register a window to receive this message, use the [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5769-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5769-115">Requirements</span></span>



| <span data-ttu-id="b5769-116">需求</span><span class="sxs-lookup"><span data-stu-id="b5769-116">Requirement</span></span> | <span data-ttu-id="b5769-117">值</span><span class="sxs-lookup"><span data-stu-id="b5769-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5769-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5769-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5769-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5769-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5769-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5769-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5769-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5769-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5769-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b5769-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5769-123"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b5769-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5769-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5769-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5769-125">**AddClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="b5769-125">**AddClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="b5769-126">**RemoveClipboardFormatListener**</span><span class="sxs-lookup"><span data-stu-id="b5769-126">**RemoveClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[<span data-ttu-id="b5769-127">**GetClipboardSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="b5769-127">**GetClipboardSequenceNumber**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 





