---
title: 'EN_ALIGNLTR (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，段落方向已從左至右變更。 Rich edit 控制項會以 WM 命令訊息的形式傳送此通知碼 \_ 。
ms.assetid: 754ac2b5-bcec-487b-a1ab-b653f673830a
keywords:
- EN_ALIGNLTR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_ALIGNLTR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55c20a9ae4efb3ba5758ed0740b20b8b57f3877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024934"
---
# <a name="en_alignltr-notification-code"></a><span data-ttu-id="1005d-105">EN \_ ALIGNLTR 通知碼</span><span class="sxs-lookup"><span data-stu-id="1005d-105">EN\_ALIGNLTR notification code</span></span>

<span data-ttu-id="1005d-106">通知 rich edit 控制項的父視窗，段落方向已從左至右變更。</span><span class="sxs-lookup"><span data-stu-id="1005d-106">Notifies a rich edit control's parent window that the paragraph direction has changed to left-to-right.</span></span> <span data-ttu-id="1005d-107">Rich edit 控制項會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="1005d-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNLTR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1005d-108">參數</span><span class="sxs-lookup"><span data-stu-id="1005d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1005d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1005d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1005d-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含 rich edit 控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1005d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="1005d-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="1005d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="1005d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1005d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1005d-113">Rich edit 控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1005d-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1005d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1005d-114">Return value</span></span>

<span data-ttu-id="1005d-115">此通知碼不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1005d-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1005d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1005d-116">Requirements</span></span>



| <span data-ttu-id="1005d-117">需求</span><span class="sxs-lookup"><span data-stu-id="1005d-117">Requirement</span></span> | <span data-ttu-id="1005d-118">值</span><span class="sxs-lookup"><span data-stu-id="1005d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1005d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1005d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1005d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1005d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1005d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1005d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1005d-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1005d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1005d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1005d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1005d-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1005d-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1005d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1005d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1005d-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="1005d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1005d-127">**EN \_ ALIGNRTL**</span><span class="sxs-lookup"><span data-stu-id="1005d-127">**EN\_ALIGNRTL**</span></span>](en-alignrtl.md)
</dt> <dt>

<span data-ttu-id="1005d-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="1005d-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="1005d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1005d-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1005d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1005d-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1005d-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="1005d-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

