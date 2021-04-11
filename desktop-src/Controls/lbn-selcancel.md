---
title: 'LBN_SELCANCEL (Winuser 的通知碼) '
description: 通知應用程式使用者已在清單方塊中取消選取。 清單方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 82e39f22-090e-4dda-8ddc-6a1fe4704fc7
keywords:
- LBN_SELCANCEL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LBN_SELCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c192fbdfdb7a351d51993bee89b9b6ec3dab387
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934903"
---
# <a name="lbn_selcancel-notification-code"></a><span data-ttu-id="d769f-105">LBN \_ SELCANCEL 通知碼</span><span class="sxs-lookup"><span data-stu-id="d769f-105">LBN\_SELCANCEL notification code</span></span>

<span data-ttu-id="d769f-106">通知應用程式使用者已在清單方塊中取消選取。</span><span class="sxs-lookup"><span data-stu-id="d769f-106">Notifies the application that the user has canceled the selection in a list box.</span></span> <span data-ttu-id="d769f-107">清單方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="d769f-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d769f-108">參數</span><span class="sxs-lookup"><span data-stu-id="d769f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d769f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d769f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d769f-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含清單方塊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d769f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="d769f-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="d769f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d769f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d769f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d769f-113">清單方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d769f-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d769f-114">備註</span><span class="sxs-lookup"><span data-stu-id="d769f-114">Remarks</span></span>

<span data-ttu-id="d769f-115">此通知碼只會由具有 L [**BS \_ 通知**](button-styles.md) 樣式的清單方塊來傳送。</span><span class="sxs-lookup"><span data-stu-id="d769f-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d769f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d769f-116">Requirements</span></span>



| <span data-ttu-id="d769f-117">需求</span><span class="sxs-lookup"><span data-stu-id="d769f-117">Requirement</span></span> | <span data-ttu-id="d769f-118">值</span><span class="sxs-lookup"><span data-stu-id="d769f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d769f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d769f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d769f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d769f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d769f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d769f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d769f-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d769f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d769f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d769f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d769f-124"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d769f-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d769f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d769f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d769f-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="d769f-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d769f-127">**LB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="d769f-127">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="d769f-128">LBN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="d769f-128">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="d769f-129">LBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="d769f-129">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="d769f-130">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="d769f-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d769f-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d769f-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d769f-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d769f-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d769f-133">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="d769f-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

