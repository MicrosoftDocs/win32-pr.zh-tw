---
description: 應用程式會將 WM \_ MDIMAXIMIZE 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以將 mdi 子視窗最大化。
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: 'WM_MDIMAXIMIZE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970798"
---
# <a name="wm_mdimaximize-message"></a><span data-ttu-id="fcd22-103">WM \_ MDIMAXIMIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="fcd22-103">WM\_MDIMAXIMIZE message</span></span>

<span data-ttu-id="fcd22-104">應用程式會將 **WM \_ MDIMAXIMIZE** 訊息傳送至多重文件介面 (mdi) 用戶端視窗，以將 mdi 子視窗最大化。</span><span class="sxs-lookup"><span data-stu-id="fcd22-104">An application sends the **WM\_MDIMAXIMIZE** message to a multiple-document interface (MDI) client window to maximize an MDI child window.</span></span> <span data-ttu-id="fcd22-105">系統會調整子視窗的大小，使其用戶端區域填滿用戶端視窗。</span><span class="sxs-lookup"><span data-stu-id="fcd22-105">The system resizes the child window to make its client area fill the client window.</span></span> <span data-ttu-id="fcd22-106">系統會將子視窗的 [視窗] 功能表圖示放置在框架視窗的功能表列最右邊的位置，並將子視窗的 [還原] 圖示放在最左邊的位置。</span><span class="sxs-lookup"><span data-stu-id="fcd22-106">The system places the child window's window menu icon in the rightmost position of the frame window's menu bar, and places the child window's restore icon in the leftmost position.</span></span> <span data-ttu-id="fcd22-107">系統也會將子視窗的標題列文字附加至框架視窗的標題列文字。</span><span class="sxs-lookup"><span data-stu-id="fcd22-107">The system also appends the title bar text of the child window to that of the frame window.</span></span>


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a><span data-ttu-id="fcd22-108">參數</span><span class="sxs-lookup"><span data-stu-id="fcd22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd22-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcd22-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcd22-110">要最大化的 MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fcd22-110">A handle to the MDI child window to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="fcd22-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcd22-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcd22-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="fcd22-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd22-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fcd22-113">Return value</span></span>

<span data-ttu-id="fcd22-114">類型： **零**</span><span class="sxs-lookup"><span data-stu-id="fcd22-114">Type: **zero**</span></span>

<span data-ttu-id="fcd22-115">傳回值永遠是零。</span><span class="sxs-lookup"><span data-stu-id="fcd22-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd22-116">備註</span><span class="sxs-lookup"><span data-stu-id="fcd22-116">Remarks</span></span>

<span data-ttu-id="fcd22-117">如果 MDI 用戶端視窗在目前作用中的 MDI 子視窗最大化時，收到變更其子視窗啟動的任何訊息，系統會還原使用中的子視窗，並將新啟動的子視窗最大化。</span><span class="sxs-lookup"><span data-stu-id="fcd22-117">If an MDI client window receives any message that changes the activation of its child windows while the currently active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd22-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcd22-118">Requirements</span></span>



| <span data-ttu-id="fcd22-119">需求</span><span class="sxs-lookup"><span data-stu-id="fcd22-119">Requirement</span></span> | <span data-ttu-id="fcd22-120">值</span><span class="sxs-lookup"><span data-stu-id="fcd22-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd22-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fcd22-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd22-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcd22-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fcd22-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fcd22-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd22-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcd22-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fcd22-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fcd22-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcd22-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fcd22-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd22-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcd22-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="fcd22-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="fcd22-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fcd22-129">**WM \_ MDIRESTORE**</span><span class="sxs-lookup"><span data-stu-id="fcd22-129">**WM\_MDIRESTORE**</span></span>](wm-mdirestore.md)
</dt> <dt>

<span data-ttu-id="fcd22-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="fcd22-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fcd22-131">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="fcd22-131">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




