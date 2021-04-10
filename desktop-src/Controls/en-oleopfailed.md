---
title: 'EN_OLEOPFAILED (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗， (COM) 物件的元件物件模型上的使用者動作失敗。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 139c51642c8cb6d5efd369cf6b373068604439b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843672"
---
# <a name="en_oleopfailed-notification-code"></a><span data-ttu-id="c93fe-105">EN \_ OLEOPFAILED 通知碼</span><span class="sxs-lookup"><span data-stu-id="c93fe-105">EN\_OLEOPFAILED notification code</span></span>

<span data-ttu-id="c93fe-106">通知 rich edit 控制項的父視窗， (COM) 物件的元件物件模型上的使用者動作失敗。</span><span class="sxs-lookup"><span data-stu-id="c93fe-106">Notifies a rich edit control's parent window that a user action on a Component Object Model (COM) object has failed.</span></span> <span data-ttu-id="c93fe-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c93fe-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c93fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="c93fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c93fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c93fe-110">[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)結構，其中包含失敗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c93fe-110">An [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) structure that contains information about the failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93fe-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c93fe-111">Return value</span></span>

<span data-ttu-id="c93fe-112">此通知碼會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c93fe-112">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c93fe-113">備註</span><span class="sxs-lookup"><span data-stu-id="c93fe-113">Remarks</span></span>

<span data-ttu-id="c93fe-114">父視窗一律會取得這個事件的 [**WM \_ 通知**](wm-notify.md) 訊息，不需要以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)傳送通知遮罩。</span><span class="sxs-lookup"><span data-stu-id="c93fe-114">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c93fe-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c93fe-115">Requirements</span></span>



| <span data-ttu-id="c93fe-116">需求</span><span class="sxs-lookup"><span data-stu-id="c93fe-116">Requirement</span></span> | <span data-ttu-id="c93fe-117">值</span><span class="sxs-lookup"><span data-stu-id="c93fe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c93fe-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c93fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c93fe-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c93fe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c93fe-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c93fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c93fe-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c93fe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c93fe-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c93fe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c93fe-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c93fe-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93fe-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c93fe-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="c93fe-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="c93fe-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c93fe-126">**ENOLEOPFAILED**</span><span class="sxs-lookup"><span data-stu-id="c93fe-126">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





