---
description: 應用程式會將 WM \_ MDIDESTROY 訊息傳送至多重文件介面 (mdi) 用戶端視窗來關閉 mdi 子視窗。
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: 'WM_MDIDESTROY 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690283"
---
# <a name="wm_mdidestroy-message"></a><span data-ttu-id="21841-103">WM \_ MDIDESTROY 訊息</span><span class="sxs-lookup"><span data-stu-id="21841-103">WM\_MDIDESTROY message</span></span>

<span data-ttu-id="21841-104">應用程式會將 **WM \_ MDIDESTROY** 訊息傳送至多重文件介面 (mdi) 用戶端視窗來關閉 mdi 子視窗。</span><span class="sxs-lookup"><span data-stu-id="21841-104">An application sends the **WM\_MDIDESTROY** message to a multiple-document interface (MDI) client window to close an MDI child window.</span></span>


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a><span data-ttu-id="21841-105">參數</span><span class="sxs-lookup"><span data-stu-id="21841-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21841-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21841-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21841-107">要關閉之 MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="21841-107">A handle to the MDI child window to be closed.</span></span>

</dd> <dt>

<span data-ttu-id="21841-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21841-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21841-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="21841-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21841-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="21841-110">Return value</span></span>

<span data-ttu-id="21841-111">類型： **零**</span><span class="sxs-lookup"><span data-stu-id="21841-111">Type: **zero**</span></span>

<span data-ttu-id="21841-112">此訊息一律會傳回零。</span><span class="sxs-lookup"><span data-stu-id="21841-112">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="21841-113">備註</span><span class="sxs-lookup"><span data-stu-id="21841-113">Remarks</span></span>

<span data-ttu-id="21841-114">此訊息會從 MDI 框架視窗移除 MDI 子視窗的標題，並停用子視窗。</span><span class="sxs-lookup"><span data-stu-id="21841-114">This message removes the title of the MDI child window from the MDI frame window and deactivates the child window.</span></span> <span data-ttu-id="21841-115">應用程式應該使用此訊息來關閉所有 MDI 子視窗。</span><span class="sxs-lookup"><span data-stu-id="21841-115">An application should use this message to close all MDI child windows.</span></span>

<span data-ttu-id="21841-116">如果 MDI 用戶端視窗收到的訊息會變更其子視窗的啟用，而且使用中的 MDI 子視窗最大化，系統會還原使用中的子視窗，並將新啟動的子視窗最大化。</span><span class="sxs-lookup"><span data-stu-id="21841-116">If an MDI client window receives a message that changes the activation of its child windows and the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="21841-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="21841-117">Requirements</span></span>



| <span data-ttu-id="21841-118">需求</span><span class="sxs-lookup"><span data-stu-id="21841-118">Requirement</span></span> | <span data-ttu-id="21841-119">值</span><span class="sxs-lookup"><span data-stu-id="21841-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21841-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21841-120">Minimum supported client</span></span><br/> | <span data-ttu-id="21841-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21841-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="21841-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21841-122">Minimum supported server</span></span><br/> | <span data-ttu-id="21841-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21841-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="21841-124">標頭</span><span class="sxs-lookup"><span data-stu-id="21841-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="21841-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="21841-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21841-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21841-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="21841-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="21841-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="21841-128">**WM \_ MDICREATE**</span><span class="sxs-lookup"><span data-stu-id="21841-128">**WM\_MDICREATE**</span></span>](wm-mdicreate.md)
</dt> <dt>

<span data-ttu-id="21841-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="21841-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="21841-130">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="21841-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




