---
title: 'STN_DISABLE (Winuser 的通知碼) '
description: '\_停用靜態控制項時，會傳送 STN 停用通知碼。'
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- STN_DISABLE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2763fce96b043ec6aebf5339a9f93d6fdf4a8abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094007"
---
# <a name="stn_disable-notification-code"></a><span data-ttu-id="35fc9-104">STN \_ 停用通知碼</span><span class="sxs-lookup"><span data-stu-id="35fc9-104">STN\_DISABLE notification code</span></span>

<span data-ttu-id="35fc9-105">\_停用靜態控制項時，會傳送 STN 停用通知碼。</span><span class="sxs-lookup"><span data-stu-id="35fc9-105">The STN\_DISABLE notification code is sent when a static control is disabled.</span></span> <span data-ttu-id="35fc9-106">靜態控制項必須具有 [**SS \_ 通知**](static-control-styles.md) 樣式才能接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="35fc9-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="35fc9-107">控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="35fc9-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DISABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="35fc9-108">參數</span><span class="sxs-lookup"><span data-stu-id="35fc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fc9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35fc9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35fc9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含靜態控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="35fc9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="35fc9-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="35fc9-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="35fc9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35fc9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35fc9-113">靜態控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="35fc9-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35fc9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="35fc9-114">Requirements</span></span>



| <span data-ttu-id="35fc9-115">需求</span><span class="sxs-lookup"><span data-stu-id="35fc9-115">Requirement</span></span> | <span data-ttu-id="35fc9-116">值</span><span class="sxs-lookup"><span data-stu-id="35fc9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fc9-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35fc9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35fc9-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35fc9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35fc9-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35fc9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35fc9-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35fc9-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35fc9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="35fc9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fc9-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="35fc9-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fc9-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35fc9-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="35fc9-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="35fc9-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35fc9-125">STN \_ 啟用</span><span class="sxs-lookup"><span data-stu-id="35fc9-125">STN\_ENABLE</span></span>](stn-enable.md)
</dt> <dt>

<span data-ttu-id="35fc9-126">**概念**</span><span class="sxs-lookup"><span data-stu-id="35fc9-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35fc9-127">靜態控制項</span><span class="sxs-lookup"><span data-stu-id="35fc9-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="35fc9-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="35fc9-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="35fc9-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35fc9-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="35fc9-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35fc9-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="35fc9-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="35fc9-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

