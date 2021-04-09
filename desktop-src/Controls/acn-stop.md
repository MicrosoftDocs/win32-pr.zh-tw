---
title: 'ACN_STOP (Commctrl 的通知碼) '
description: 通知動畫控制項的父視窗，相關聯的 AVI 剪輯已停止播放。 此通知碼會以 WM 命令訊息的形式傳送 \_ 。
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- ACN_STOP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024803"
---
# <a name="acn_stop-notification-code"></a><span data-ttu-id="1b921-105">ACN \_ 停止通知碼</span><span class="sxs-lookup"><span data-stu-id="1b921-105">ACN\_STOP notification code</span></span>

<span data-ttu-id="1b921-106">通知動畫控制項的父視窗，相關聯的 AVI 剪輯已停止播放。</span><span class="sxs-lookup"><span data-stu-id="1b921-106">Notifies the parent window of an animation control that the associated AVI clip has stopped playing.</span></span> <span data-ttu-id="1b921-107">此通知碼會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="1b921-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="1b921-108">參數</span><span class="sxs-lookup"><span data-stu-id="1b921-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b921-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b921-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b921-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含動畫控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1b921-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="1b921-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="1b921-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="1b921-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b921-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b921-113">指定動畫控制項之控制碼的 **HWND** 。</span><span class="sxs-lookup"><span data-stu-id="1b921-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b921-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b921-114">Requirements</span></span>



| <span data-ttu-id="1b921-115">需求</span><span class="sxs-lookup"><span data-stu-id="1b921-115">Requirement</span></span> | <span data-ttu-id="1b921-116">值</span><span class="sxs-lookup"><span data-stu-id="1b921-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b921-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b921-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1b921-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b921-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b921-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b921-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1b921-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b921-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b921-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1b921-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b921-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1b921-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

