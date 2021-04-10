---
title: 'LBN_SETFOCUS (Winuser 的通知碼) '
description: 通知應用程式清單方塊已收到鍵盤焦點。 清單方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: d9e5e035-98a5-4ece-ba40-6d341c101859
keywords:
- LBN_SETFOCUS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e56043982cec6606f7c78d3469ab2583951f88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843611"
---
# <a name="lbn_setfocus-notification-code"></a><span data-ttu-id="50574-105">LBN \_ SETFOCUS 通知碼</span><span class="sxs-lookup"><span data-stu-id="50574-105">LBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="50574-106">通知應用程式清單方塊已收到鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="50574-106">Notifies the application that the list box has received the keyboard focus.</span></span> <span data-ttu-id="50574-107">清單方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="50574-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="50574-108">參數</span><span class="sxs-lookup"><span data-stu-id="50574-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50574-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50574-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50574-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含清單方塊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="50574-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="50574-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="50574-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="50574-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50574-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50574-113">清單方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="50574-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50574-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="50574-114">Requirements</span></span>



| <span data-ttu-id="50574-115">需求</span><span class="sxs-lookup"><span data-stu-id="50574-115">Requirement</span></span> | <span data-ttu-id="50574-116">值</span><span class="sxs-lookup"><span data-stu-id="50574-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50574-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50574-117">Minimum supported client</span></span><br/> | <span data-ttu-id="50574-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50574-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50574-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50574-119">Minimum supported server</span></span><br/> | <span data-ttu-id="50574-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50574-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50574-121">標頭</span><span class="sxs-lookup"><span data-stu-id="50574-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="50574-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="50574-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50574-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50574-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="50574-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="50574-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="50574-125">LBN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="50574-125">LBN\_KILLFOCUS</span></span>](lbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="50574-126">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="50574-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="50574-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50574-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="50574-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50574-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="50574-129">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="50574-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

