---
title: 'CBN_DBLCLK (Winuser 的通知碼) '
description: 當使用者在下拉式方塊的清單方塊中按兩下字串時傳送。 下拉式方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- CBN_DBLCLK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001316"
---
# <a name="cbn_dblclk-notification-code"></a><span data-ttu-id="f7c3f-105">CBN \_ DBLCLK 通知碼</span><span class="sxs-lookup"><span data-stu-id="f7c3f-105">CBN\_DBLCLK notification code</span></span>

<span data-ttu-id="f7c3f-106">當使用者在下拉式方塊的清單方塊中按兩下字串時傳送。</span><span class="sxs-lookup"><span data-stu-id="f7c3f-106">Sent when the user double-clicks a string in the list box of a combo box.</span></span> <span data-ttu-id="f7c3f-107">下拉式方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="f7c3f-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f7c3f-108">參數</span><span class="sxs-lookup"><span data-stu-id="f7c3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7c3f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7c3f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7c3f-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含下拉式方塊的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7c3f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="f7c3f-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="f7c3f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="f7c3f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7c3f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7c3f-113">下拉式方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7c3f-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7c3f-114">備註</span><span class="sxs-lookup"><span data-stu-id="f7c3f-114">Remarks</span></span>

<span data-ttu-id="f7c3f-115">此通知程式碼只會針對具有 [**CBS \_ 簡單**](combo-box-styles.md) 樣式的下拉式方塊進行。</span><span class="sxs-lookup"><span data-stu-id="f7c3f-115">This notification code occurs only for a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="f7c3f-116">在具有 [**CBS \_ 下拉式清單**](combo-box-styles.md) 或 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md) 樣式的下拉式方塊中，只要按一下即可關閉清單方塊，就無法按兩下。</span><span class="sxs-lookup"><span data-stu-id="f7c3f-116">In a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, a double-click cannot occur because a single click closes the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c3f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7c3f-117">Requirements</span></span>



| <span data-ttu-id="f7c3f-118">需求</span><span class="sxs-lookup"><span data-stu-id="f7c3f-118">Requirement</span></span> | <span data-ttu-id="f7c3f-119">值</span><span class="sxs-lookup"><span data-stu-id="f7c3f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c3f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7c3f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c3f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7c3f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f7c3f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7c3f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c3f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7c3f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f7c3f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f7c3f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7c3f-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f7c3f-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7c3f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7c3f-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7c3f-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="f7c3f-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f7c3f-128">CBN \_ SELCHANGE</span><span class="sxs-lookup"><span data-stu-id="f7c3f-128">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="f7c3f-129">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="f7c3f-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="f7c3f-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7c3f-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f7c3f-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7c3f-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f7c3f-132">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="f7c3f-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

