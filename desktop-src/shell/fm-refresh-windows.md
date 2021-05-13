---
description: 由檔管理程式延伸模組傳送，使檔管理程式重新繪製其使用中視窗或所有視窗。
title: 'FM_REFRESH_WINDOWS 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_REFRESH_WINDOWS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 210168c6-d83b-4ffd-93d4-d22fa748cef2
ms.openlocfilehash: 0513955fd1b03dfae321d52fe9a5df3794f54782
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842349"
---
# <a name="fm_refresh_windows-message"></a><span data-ttu-id="840a1-103">FM \_ REFRESH \_ WINDOWS 訊息</span><span class="sxs-lookup"><span data-stu-id="840a1-103">FM\_REFRESH\_WINDOWS message</span></span>

<span data-ttu-id="840a1-104">由檔管理程式延伸模組傳送，使檔管理程式重新繪製其使用中視窗或所有視窗。</span><span class="sxs-lookup"><span data-stu-id="840a1-104">Sent by a File Manager extension to cause File Manager to repaint either its active window or all of its windows.</span></span>

## <a name="parameters"></a><span data-ttu-id="840a1-105">參數</span><span class="sxs-lookup"><span data-stu-id="840a1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="840a1-106">*fRepaint*</span><span class="sxs-lookup"><span data-stu-id="840a1-106">*fRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="840a1-107">值，這個值會指出檔管理程式是否會重新繪製其使用中視窗或所有視窗。</span><span class="sxs-lookup"><span data-stu-id="840a1-107">A value that indicates whether File Manager repaints its active window or all of its windows.</span></span> <span data-ttu-id="840a1-108">如果此參數為 **TRUE**，則 [檔案管理員] 會重新繪製其所有視窗。</span><span class="sxs-lookup"><span data-stu-id="840a1-108">If this parameter is **TRUE**, File Manager repaints all of its windows.</span></span> <span data-ttu-id="840a1-109">否則，[檔案管理員] 只會重繪其使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="840a1-109">Otherwise, File Manager repaints only its active window.</span></span>

</dd> <dt>

<span data-ttu-id="840a1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="840a1-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="840a1-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="840a1-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="840a1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="840a1-112">Return value</span></span>

<span data-ttu-id="840a1-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="840a1-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="840a1-114">備註</span><span class="sxs-lookup"><span data-stu-id="840a1-114">Remarks</span></span>

<span data-ttu-id="840a1-115">檔案管理員會自動偵測延伸模組所造成的檔案系統變更。</span><span class="sxs-lookup"><span data-stu-id="840a1-115">File system changes caused by an extension are automatically detected by File Manager.</span></span> <span data-ttu-id="840a1-116">只有在建立或取消磁片磁碟機連線的情況下，延伸模組才應該使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="840a1-116">An extension should use this message only in situations where drive connections are made or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="840a1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="840a1-117">Requirements</span></span>



| <span data-ttu-id="840a1-118">需求</span><span class="sxs-lookup"><span data-stu-id="840a1-118">Requirement</span></span> | <span data-ttu-id="840a1-119">值</span><span class="sxs-lookup"><span data-stu-id="840a1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="840a1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="840a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="840a1-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="840a1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="840a1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="840a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="840a1-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="840a1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="840a1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="840a1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="840a1-125"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="840a1-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="840a1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="840a1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="840a1-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="840a1-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




