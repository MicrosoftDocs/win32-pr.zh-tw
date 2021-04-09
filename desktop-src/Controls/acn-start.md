---
title: 'ACN_START (Commctrl 的通知碼) '
description: 通知動畫控制項的父視窗，相關聯的 AVI 剪輯已開始播放。 此通知碼會以 WM 命令訊息的形式傳送 \_ 。
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- ACN_START 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685662"
---
# <a name="acn_start-notification-code"></a><span data-ttu-id="b8f4f-105">ACN \_ 啟動通知碼</span><span class="sxs-lookup"><span data-stu-id="b8f4f-105">ACN\_START notification code</span></span>

<span data-ttu-id="b8f4f-106">通知動畫控制項的父視窗，相關聯的 AVI 剪輯已開始播放。</span><span class="sxs-lookup"><span data-stu-id="b8f4f-106">Notifies an animation control's parent window that the associated AVI clip has started playing.</span></span> <span data-ttu-id="b8f4f-107">此通知碼會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="b8f4f-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b8f4f-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8f4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8f4f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f4f-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含動畫控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8f4f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="b8f4f-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="b8f4f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b8f4f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8f4f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f4f-113">指定動畫控制項之控制碼的 **HWND** 。</span><span class="sxs-lookup"><span data-stu-id="b8f4f-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8f4f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8f4f-114">Requirements</span></span>



| <span data-ttu-id="b8f4f-115">需求</span><span class="sxs-lookup"><span data-stu-id="b8f4f-115">Requirement</span></span> | <span data-ttu-id="b8f4f-116">值</span><span class="sxs-lookup"><span data-stu-id="b8f4f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f4f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8f4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f4f-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8f4f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8f4f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8f4f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f4f-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8f4f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8f4f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b8f4f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f4f-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8f4f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

