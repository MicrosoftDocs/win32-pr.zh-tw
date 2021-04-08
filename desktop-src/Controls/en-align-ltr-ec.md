---
title: 'EN_ALIGN_LTR_EC (Winuser 的通知碼) '
description: 當使用者將編輯控制項方向從左至右變更時傳送。 編輯控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- EN_ALIGN_LTR_EC 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4886c68a024005c4b2fddd71e1480b0a3545bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685780"
---
# <a name="en_align_ltr_ec-notification-code"></a><span data-ttu-id="6c768-105">EN \_ 對齊 \_ LTR \_ EC 通知碼</span><span class="sxs-lookup"><span data-stu-id="6c768-105">EN\_ALIGN\_LTR\_EC notification code</span></span>

<span data-ttu-id="6c768-106">當使用者將編輯控制項方向從左至右變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="6c768-106">Sent when the user has changed the edit control direction to left-to-right.</span></span> <span data-ttu-id="6c768-107">編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="6c768-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGN_LTR_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="6c768-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c768-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c768-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c768-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c768-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c768-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="6c768-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="6c768-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6c768-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c768-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c768-113">傳送通知碼之編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c768-113">A handle to the edit control sending the notification code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c768-114">備註</span><span class="sxs-lookup"><span data-stu-id="6c768-114">Remarks</span></span>

<span data-ttu-id="6c768-115">如果您的系統上已安裝雙向語言（例如阿拉伯文或希伯來文），您可以使用 CTRL + LSHIFT (（由左到右）) 和 CTRL + RSHIFT (（由右至左) ）來變更編輯控制項方向。</span><span class="sxs-lookup"><span data-stu-id="6c768-115">If there is a bidirectional language installed on your system, for example, Arabic or Hebrew, you can change the edit control direction using CTRL+LSHIFT (for left to right) and CTRL+RSHIFT (for right to left).</span></span>

<span data-ttu-id="6c768-116">**Rich Edit：** 不支援此通知碼。</span><span class="sxs-lookup"><span data-stu-id="6c768-116">**Rich Edit:** This notification code is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c768-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c768-117">Requirements</span></span>



| <span data-ttu-id="6c768-118">需求</span><span class="sxs-lookup"><span data-stu-id="6c768-118">Requirement</span></span> | <span data-ttu-id="6c768-119">值</span><span class="sxs-lookup"><span data-stu-id="6c768-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c768-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c768-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c768-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c768-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c768-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c768-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c768-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c768-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6c768-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6c768-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c768-125"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6c768-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c768-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c768-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c768-127">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="6c768-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

