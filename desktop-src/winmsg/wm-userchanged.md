---
description: 在使用者登入或登出之後傳送到所有視窗。 當使用者登入時，系統會更新使用者特定的設定。 系統會在更新設定之後立即傳送此訊息。
title: 'WM_USERCHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945152"
---
# <a name="wm_userchanged-message"></a><span data-ttu-id="db3e9-105">WM \_ USERCHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="db3e9-105">WM\_USERCHANGED message</span></span>

<span data-ttu-id="db3e9-106">在使用者登入或登出之後傳送到所有視窗。</span><span class="sxs-lookup"><span data-stu-id="db3e9-106">Sent to all windows after the user has logged on or off.</span></span> <span data-ttu-id="db3e9-107">當使用者登入時，系統會更新使用者特定的設定。</span><span class="sxs-lookup"><span data-stu-id="db3e9-107">When the user logs on or off, the system updates the user-specific settings.</span></span> <span data-ttu-id="db3e9-108">系統會在更新設定之後立即傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="db3e9-108">The system sends this message immediately after updating the settings.</span></span>

<span data-ttu-id="db3e9-109">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="db3e9-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="db3e9-110">Windows Vista 不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="db3e9-110">This message is not supported as of Windows Vista.</span></span>

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a><span data-ttu-id="db3e9-111">參數</span><span class="sxs-lookup"><span data-stu-id="db3e9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db3e9-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db3e9-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db3e9-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="db3e9-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="db3e9-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db3e9-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db3e9-115">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="db3e9-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db3e9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="db3e9-116">Return value</span></span>

<span data-ttu-id="db3e9-117">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="db3e9-117">Type: **LRESULT**</span></span>

<span data-ttu-id="db3e9-118">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="db3e9-118">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="db3e9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="db3e9-119">Requirements</span></span>



| <span data-ttu-id="db3e9-120">需求</span><span class="sxs-lookup"><span data-stu-id="db3e9-120">Requirement</span></span> | <span data-ttu-id="db3e9-121">值</span><span class="sxs-lookup"><span data-stu-id="db3e9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db3e9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db3e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="db3e9-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db3e9-123">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="db3e9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db3e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="db3e9-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="db3e9-125">None supported</span></span><br/>                                                                                |
| <span data-ttu-id="db3e9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="db3e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="db3e9-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="db3e9-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db3e9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db3e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3e9-129">Windows 總覽</span><span class="sxs-lookup"><span data-stu-id="db3e9-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
