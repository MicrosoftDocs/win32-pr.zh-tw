---
description: 當作業系統即將變更目前的輸入法時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: 'WM_IME_SELECT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986353"
---
# <a name="wm_ime_select-message"></a><span data-ttu-id="e98ec-104">WM \_ 輸入法 \_ 選取訊息</span><span class="sxs-lookup"><span data-stu-id="e98ec-104">WM\_IME\_SELECT message</span></span>

<span data-ttu-id="e98ec-105">當作業系統即將變更目前的輸入法時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="e98ec-105">Sent to an application when the operating system is about to change the current IME.</span></span> <span data-ttu-id="e98ec-106">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e98ec-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="e98ec-107">參數</span><span class="sxs-lookup"><span data-stu-id="e98ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e98ec-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="e98ec-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e98ec-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e98ec-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="e98ec-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e98ec-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e98ec-111">選取指標。</span><span class="sxs-lookup"><span data-stu-id="e98ec-111">Selection indicator.</span></span> <span data-ttu-id="e98ec-112">如果選取了指定的輸入法，此參數會指定 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e98ec-112">This parameter specifies **TRUE** if the indicated IME is selected.</span></span> <span data-ttu-id="e98ec-113">如果不再選取指定的輸入法，參數會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e98ec-113">The parameter is set to **FALSE** if the specified IME is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="e98ec-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e98ec-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e98ec-115">與 IME 相關聯的輸入地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="e98ec-115">Input locale identifier associated with the IME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e98ec-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e98ec-116">Return value</span></span>

<span data-ttu-id="e98ec-117">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e98ec-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e98ec-118">備註</span><span class="sxs-lookup"><span data-stu-id="e98ec-118">Remarks</span></span>

<span data-ttu-id="e98ec-119">已建立 IME 視窗的應用程式應該將此訊息傳遞至該視窗，讓它可以將鍵盤配置控制碼抓取到新選取的輸入。</span><span class="sxs-lookup"><span data-stu-id="e98ec-119">An application that has created an IME window should pass this message to that window so that it can retrieve the keyboard layout handle to the newly selected IME.</span></span>

<span data-ttu-id="e98ec-120">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會藉由將資訊傳遞至預設 IME 視窗來處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="e98ec-120">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing the information to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e98ec-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e98ec-121">Requirements</span></span>



| <span data-ttu-id="e98ec-122">需求</span><span class="sxs-lookup"><span data-stu-id="e98ec-122">Requirement</span></span> | <span data-ttu-id="e98ec-123">值</span><span class="sxs-lookup"><span data-stu-id="e98ec-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e98ec-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e98ec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e98ec-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e98ec-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e98ec-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e98ec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e98ec-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e98ec-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e98ec-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e98ec-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e98ec-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e98ec-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e98ec-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e98ec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98ec-131">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="e98ec-131">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e98ec-132">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="e98ec-132">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
