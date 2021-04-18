---
title: 'EN_ALIGNRTL (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，段落方向已從右至左變更。 Rich edit 控制項會以 WM 命令訊息的形式傳送此通知碼 \_ 。
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- EN_ALIGNRTL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464893"
---
# <a name="en_alignrtl-notification-code"></a><span data-ttu-id="6df9f-105">EN \_ ALIGNRTL 通知碼</span><span class="sxs-lookup"><span data-stu-id="6df9f-105">EN\_ALIGNRTL notification code</span></span>

<span data-ttu-id="6df9f-106">通知 rich edit 控制項的父視窗，段落方向已從右至左變更。</span><span class="sxs-lookup"><span data-stu-id="6df9f-106">Notifies a rich edit control's parent window that the paragraph direction changed to right-to-left.</span></span> <span data-ttu-id="6df9f-107">Rich edit 控制項會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="6df9f-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="6df9f-108">參數</span><span class="sxs-lookup"><span data-stu-id="6df9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df9f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6df9f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6df9f-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含 rich edit 控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6df9f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="6df9f-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="6df9f-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6df9f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6df9f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6df9f-113">Rich edit 控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6df9f-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df9f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6df9f-114">Return value</span></span>

<span data-ttu-id="6df9f-115">此通知碼不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6df9f-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df9f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6df9f-116">Requirements</span></span>



| <span data-ttu-id="6df9f-117">需求</span><span class="sxs-lookup"><span data-stu-id="6df9f-117">Requirement</span></span> | <span data-ttu-id="6df9f-118">值</span><span class="sxs-lookup"><span data-stu-id="6df9f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6df9f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6df9f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6df9f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6df9f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6df9f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6df9f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6df9f-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6df9f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6df9f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6df9f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6df9f-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6df9f-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df9f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6df9f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6df9f-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="6df9f-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6df9f-127">**EN \_ ALIGNLTR**</span><span class="sxs-lookup"><span data-stu-id="6df9f-127">**EN\_ALIGNLTR**</span></span>](en-alignltr.md)
</dt> <dt>

<span data-ttu-id="6df9f-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="6df9f-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6df9f-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6df9f-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6df9f-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6df9f-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6df9f-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="6df9f-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

