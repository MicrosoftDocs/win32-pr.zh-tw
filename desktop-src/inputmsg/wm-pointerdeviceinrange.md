---
title: WM_POINTERDEVICEINRANGE 訊息
description: 在輸入數位板的範圍內偵測到指標裝置時，傳送至視窗。 此訊息包含裝置及其鄰近性的相關資訊。
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- WM_POINTERDEVICEINRANGE 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509235"
---
# <a name="wm_pointerdeviceinrange-message"></a><span data-ttu-id="1dfcd-105">WM_POINTERDEVICEINRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="1dfcd-105">WM_POINTERDEVICEINRANGE message</span></span>

<span data-ttu-id="1dfcd-106">在輸入數位板的範圍內偵測到指標裝置時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-106">Sent to a window when a pointer device is detected within range of an input digitizer.</span></span> <span data-ttu-id="1dfcd-107">此訊息包含裝置及其鄰近性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="1dfcd-108">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="1dfcd-108">\[!Important\]</span></span>  
> <span data-ttu-id="1dfcd-109">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="1dfcd-110">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="1dfcd-111">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="1dfcd-112">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a><span data-ttu-id="1dfcd-113">參數</span><span class="sxs-lookup"><span data-stu-id="1dfcd-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfcd-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dfcd-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfcd-115">其他特定訊息資訊。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="1dfcd-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dfcd-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfcd-117">其他特定訊息資訊。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfcd-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1dfcd-118">Return value</span></span>

<span data-ttu-id="1dfcd-119">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="1dfcd-120">如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="1dfcd-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfcd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dfcd-121">Requirements</span></span>



| <span data-ttu-id="1dfcd-122">需求</span><span class="sxs-lookup"><span data-stu-id="1dfcd-122">Requirement</span></span> | <span data-ttu-id="1dfcd-123">值</span><span class="sxs-lookup"><span data-stu-id="1dfcd-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfcd-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1dfcd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfcd-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dfcd-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="1dfcd-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1dfcd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfcd-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dfcd-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1dfcd-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1dfcd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfcd-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1dfcd-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfcd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1dfcd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfcd-131">訊息</span><span class="sxs-lookup"><span data-stu-id="1dfcd-131">Messages</span></span>](messages.md)
</dt> </dl>

 

