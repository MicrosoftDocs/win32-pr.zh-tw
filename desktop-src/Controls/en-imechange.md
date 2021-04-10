---
title: 'EN_IMECHANGE (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父系，IME 轉換狀態已變更。
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025129"
---
# <a name="en_imechange-notification-code"></a><span data-ttu-id="8bc5e-104">EN \_ IMECHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="8bc5e-104">EN\_IMECHANGE notification code</span></span>

<span data-ttu-id="8bc5e-105">通知 rich edit 控制項的父系，IME 轉換狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-105">Notifies a rich edit control's parent that the IME conversion status has changed.</span></span> <span data-ttu-id="8bc5e-106">此通知碼 *僅* 適用于亞洲語言版本的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-106">This notification code is available *only* for Asian-language versions of the operating system.</span></span> <span data-ttu-id="8bc5e-107">Rich edit 控制項會以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8bc5e-108">參數</span><span class="sxs-lookup"><span data-stu-id="8bc5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bc5e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bc5e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bc5e-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含 rich edit 控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="8bc5e-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8bc5e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bc5e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bc5e-113">Rich edit 控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bc5e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8bc5e-114">Return value</span></span>

<span data-ttu-id="8bc5e-115">此通知碼會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-115">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bc5e-116">備註</span><span class="sxs-lookup"><span data-stu-id="8bc5e-116">Remarks</span></span>

<span data-ttu-id="8bc5e-117">若要接收 EN \_ IMECHANGE 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-117">To receive EN\_IMECHANGE notification codes, specify [**ENM\_IMECHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="8bc5e-118">只有亞洲版 Rich Edit 1.0 支援此通知碼。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-118">This notification code is only supported in the Asian version of Rich Edit 1.0.</span></span> <span data-ttu-id="8bc5e-119">較新的版本不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-119">It is not supported in later versions.</span></span> <span data-ttu-id="8bc5e-120">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="8bc5e-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8bc5e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bc5e-121">Requirements</span></span>



| <span data-ttu-id="8bc5e-122">需求</span><span class="sxs-lookup"><span data-stu-id="8bc5e-122">Requirement</span></span> | <span data-ttu-id="8bc5e-123">值</span><span class="sxs-lookup"><span data-stu-id="8bc5e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bc5e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bc5e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8bc5e-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bc5e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8bc5e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bc5e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8bc5e-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bc5e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8bc5e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="8bc5e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bc5e-129"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="8bc5e-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bc5e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bc5e-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="8bc5e-131">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="8bc5e-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="8bc5e-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8bc5e-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8bc5e-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8bc5e-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8bc5e-134">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="8bc5e-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

