---
description: 應用程式會將 WM \_ MDINEXT 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以啟動下一個或上一個子視窗。
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: 'WM_MDINEXT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690280"
---
# <a name="wm_mdinext-message"></a><span data-ttu-id="f3783-103">WM \_ MDINEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="f3783-103">WM\_MDINEXT message</span></span>

<span data-ttu-id="f3783-104">應用程式會將 **WM \_ MDINEXT** 訊息傳送至多重文件介面 (MDI) 用戶端視窗，以啟動下一個或上一個子視窗。</span><span class="sxs-lookup"><span data-stu-id="f3783-104">An application sends the **WM\_MDINEXT** message to a multiple-document interface (MDI) client window to activate the next or previous child window.</span></span>


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a><span data-ttu-id="f3783-105">參數</span><span class="sxs-lookup"><span data-stu-id="f3783-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3783-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3783-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3783-107">MDI 子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f3783-107">A handle to the MDI child window.</span></span> <span data-ttu-id="f3783-108">系統會根據 *lParam* 參數的值，啟動緊接在指定子視窗之前或之後的子視窗。</span><span class="sxs-lookup"><span data-stu-id="f3783-108">The system activates the child window that is immediately before or after the specified child window, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="f3783-109">如果 *wParam* 參數為 **Null**，系統會啟動緊接在目前作用中子視窗之前或之後的子視窗。</span><span class="sxs-lookup"><span data-stu-id="f3783-109">If the *wParam* parameter is **NULL**, the system activates the child window that is immediately before or after the currently active child window.</span></span>

</dd> <dt>

<span data-ttu-id="f3783-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3783-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3783-111">如果此參數為零，則系統會啟用下一個 MDI 子視窗，並將 *wParam* 參數所識別的子視窗放在所有其他子視窗後方。</span><span class="sxs-lookup"><span data-stu-id="f3783-111">If this parameter is zero, the system activates the next MDI child window and places the child window identified by the *wParam* parameter behind all other child windows.</span></span> <span data-ttu-id="f3783-112">如果此參數為非零值，則系統會啟動先前的子視窗，並將它放在 *wParam* 所識別的子視窗前方。</span><span class="sxs-lookup"><span data-stu-id="f3783-112">If this parameter is nonzero, the system activates the previous child window, placing it in front of the child window identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3783-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3783-113">Return value</span></span>

<span data-ttu-id="f3783-114">類型： **零**</span><span class="sxs-lookup"><span data-stu-id="f3783-114">Type: **zero**</span></span>

<span data-ttu-id="f3783-115">傳回值永遠是零。</span><span class="sxs-lookup"><span data-stu-id="f3783-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3783-116">備註</span><span class="sxs-lookup"><span data-stu-id="f3783-116">Remarks</span></span>

<span data-ttu-id="f3783-117">如果 MDI 用戶端視窗在使用中的 MDI 子視窗最大化時，收到變更其子視窗啟動的任何訊息，系統就會還原使用中的子視窗，並將新啟動的子視窗最大化。</span><span class="sxs-lookup"><span data-stu-id="f3783-117">If an MDI client window receives any message that changes the activation of its child windows while the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3783-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3783-118">Requirements</span></span>



| <span data-ttu-id="f3783-119">需求</span><span class="sxs-lookup"><span data-stu-id="f3783-119">Requirement</span></span> | <span data-ttu-id="f3783-120">值</span><span class="sxs-lookup"><span data-stu-id="f3783-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3783-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3783-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f3783-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3783-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f3783-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3783-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f3783-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3783-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f3783-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f3783-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3783-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f3783-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3783-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3783-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3783-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="f3783-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f3783-129">**WM \_ MDIACTI加值稅E**</span><span class="sxs-lookup"><span data-stu-id="f3783-129">**WM\_MDIACTIVATE**</span></span>](wm-mdiactivate.md)
</dt> <dt>

[<span data-ttu-id="f3783-130">**WM \_ MDIGETACTIVE**</span><span class="sxs-lookup"><span data-stu-id="f3783-130">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

<span data-ttu-id="f3783-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="f3783-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f3783-132">多個檔介面</span><span class="sxs-lookup"><span data-stu-id="f3783-132">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




