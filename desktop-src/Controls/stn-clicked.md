---
title: 'STN_CLICKED (Winuser 的通知碼) '
description: '\_當使用者按一下具有 SS 通知樣式的靜態控制項時，會傳送 STN 點擊通知碼 \_ 。 控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。'
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- STN_CLICKED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91f63bc496469f6edc26b4f9176f3f9157464bdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843136"
---
# <a name="stn_clicked-notification-code"></a><span data-ttu-id="2075d-105">STN \_ 按一下通知碼</span><span class="sxs-lookup"><span data-stu-id="2075d-105">STN\_CLICKED notification code</span></span>

<span data-ttu-id="2075d-106">\_當使用者按一下具有 [**SS \_ 通知**](static-control-styles.md)樣式的靜態控制項時，會傳送 STN 點擊通知碼。</span><span class="sxs-lookup"><span data-stu-id="2075d-106">The STN\_CLICKED notification code is sent when the user clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="2075d-107">控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="2075d-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2075d-108">參數</span><span class="sxs-lookup"><span data-stu-id="2075d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2075d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2075d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2075d-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含靜態控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2075d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="2075d-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="2075d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2075d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2075d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2075d-113">靜態控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2075d-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2075d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2075d-114">Requirements</span></span>



| <span data-ttu-id="2075d-115">需求</span><span class="sxs-lookup"><span data-stu-id="2075d-115">Requirement</span></span> | <span data-ttu-id="2075d-116">值</span><span class="sxs-lookup"><span data-stu-id="2075d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2075d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2075d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2075d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2075d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2075d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2075d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2075d-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2075d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2075d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2075d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2075d-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2075d-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2075d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2075d-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="2075d-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="2075d-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2075d-125">STN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="2075d-125">STN\_DBLCLK</span></span>](stn-dblclk.md)
</dt> <dt>

<span data-ttu-id="2075d-126">**概念**</span><span class="sxs-lookup"><span data-stu-id="2075d-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2075d-127">靜態控制項</span><span class="sxs-lookup"><span data-stu-id="2075d-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="2075d-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="2075d-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2075d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2075d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2075d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2075d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2075d-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="2075d-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

