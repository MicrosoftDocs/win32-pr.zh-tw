---
title: DM_POINTERHITTEST 訊息
description: 傳送至視窗時，在第一次偵測到指標輸入時，為了判斷直接操作最可能的輸入目標。
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- DM_POINTERHITTEST 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104862"
---
# <a name="dm_pointerhittest-message"></a><span data-ttu-id="2ddab-104">DM_POINTERHITTEST 訊息</span><span class="sxs-lookup"><span data-stu-id="2ddab-104">DM_POINTERHITTEST message</span></span>

<span data-ttu-id="2ddab-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="2ddab-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2ddab-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="2ddab-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2ddab-107">傳送至視窗時，在第一次偵測到指標輸入時，為了判斷 [直接操作](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)最可能的輸入目標。</span><span class="sxs-lookup"><span data-stu-id="2ddab-107">Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal).</span></span>

> <span data-ttu-id="2ddab-108">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="2ddab-108">\[!Important\]</span></span>  
> <span data-ttu-id="2ddab-109">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="2ddab-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="2ddab-110">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="2ddab-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="2ddab-111">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="2ddab-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="2ddab-112">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2ddab-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a><span data-ttu-id="2ddab-113">參數</span><span class="sxs-lookup"><span data-stu-id="2ddab-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddab-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ddab-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ddab-115">未使用的。</span><span class="sxs-lookup"><span data-stu-id="2ddab-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="2ddab-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ddab-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ddab-117">未使用的。</span><span class="sxs-lookup"><span data-stu-id="2ddab-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddab-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ddab-118">Return value</span></span>

<span data-ttu-id="2ddab-119">NULL</span><span class="sxs-lookup"><span data-stu-id="2ddab-119">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddab-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ddab-120">Requirements</span></span>



| <span data-ttu-id="2ddab-121">需求</span><span class="sxs-lookup"><span data-stu-id="2ddab-121">Requirement</span></span> | <span data-ttu-id="2ddab-122">值</span><span class="sxs-lookup"><span data-stu-id="2ddab-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddab-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ddab-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2ddab-124">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ddab-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2ddab-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ddab-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2ddab-126">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ddab-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2ddab-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2ddab-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ddab-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2ddab-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ddab-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ddab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddab-130">訊息</span><span class="sxs-lookup"><span data-stu-id="2ddab-130">Messages</span></span>](messages.md)
</dt> </dl>

 

