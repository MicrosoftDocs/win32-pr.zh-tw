---
title: 'EN_STOPNOUNDO (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，表示控制項無法配置足夠的記憶體來維持復原狀態。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105546"
---
# <a name="en_stopnoundo-notification-code"></a><span data-ttu-id="6cfd7-105">EN \_ STOPNOUNDO 通知碼</span><span class="sxs-lookup"><span data-stu-id="6cfd7-105">EN\_STOPNOUNDO notification code</span></span>

<span data-ttu-id="6cfd7-106">通知 rich edit 控制項的父視窗，表示控制項無法配置足夠的記憶體來維持復原狀態。</span><span class="sxs-lookup"><span data-stu-id="6cfd7-106">Notifies a rich edit control's parent window that an action occurred for which the control cannot allocate enough memory to maintain the undo state.</span></span> <span data-ttu-id="6cfd7-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="6cfd7-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6cfd7-108">參數</span><span class="sxs-lookup"><span data-stu-id="6cfd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cfd7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cfd7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfd7-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構。</span><span class="sxs-lookup"><span data-stu-id="6cfd7-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cfd7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cfd7-111">Return value</span></span>

<span data-ttu-id="6cfd7-112">傳回零以繼續執行 **復原** 操作。</span><span class="sxs-lookup"><span data-stu-id="6cfd7-112">Return zero to continue the **Undo** operation.</span></span>

<span data-ttu-id="6cfd7-113">傳回非零值以停止 **復原** 作業。</span><span class="sxs-lookup"><span data-stu-id="6cfd7-113">Return a nonzero value to stop the **Undo** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cfd7-114">備註</span><span class="sxs-lookup"><span data-stu-id="6cfd7-114">Remarks</span></span>

<span data-ttu-id="6cfd7-115">父視窗一律會取得這個事件的 [**WM \_ 通知**](wm-notify.md) 訊息，不需要以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)傳送通知遮罩。</span><span class="sxs-lookup"><span data-stu-id="6cfd7-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cfd7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cfd7-116">Requirements</span></span>



| <span data-ttu-id="6cfd7-117">需求</span><span class="sxs-lookup"><span data-stu-id="6cfd7-117">Requirement</span></span> | <span data-ttu-id="6cfd7-118">值</span><span class="sxs-lookup"><span data-stu-id="6cfd7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfd7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cfd7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6cfd7-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cfd7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cfd7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cfd7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6cfd7-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cfd7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cfd7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6cfd7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cfd7-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6cfd7-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cfd7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cfd7-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6cfd7-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="6cfd7-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6cfd7-127">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="6cfd7-127">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[<span data-ttu-id="6cfd7-128">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="6cfd7-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





