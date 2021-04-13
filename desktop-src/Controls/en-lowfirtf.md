---
title: 'EN_LOWFIRTF (Richedit 的通知碼) '
description: 通知 Microsoft Rich Edit 控制項的父視窗，表示收到不支援的 Rtf 格式 (RTF) 關鍵字。 Rich Edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74a6e5dada471fdd8364b34bf2ed1b4da7f2314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509164"
---
# <a name="en_lowfirtf-notification-code"></a><span data-ttu-id="579f8-105">EN \_ LOWFIRTF 通知碼</span><span class="sxs-lookup"><span data-stu-id="579f8-105">EN\_LOWFIRTF notification code</span></span>

<span data-ttu-id="579f8-106">通知 Microsoft Rich Edit 控制項的父視窗，表示收到不支援的 Rtf 格式 (RTF) 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="579f8-106">Notifies the parent window of a Microsoft Rich Edit control that an unsupported Rich Text Format (RTF) keyword was received.</span></span> <span data-ttu-id="579f8-107">Rich Edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="579f8-107">A Rich Edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="579f8-108">參數</span><span class="sxs-lookup"><span data-stu-id="579f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579f8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="579f8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="579f8-110">[**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)結構。</span><span class="sxs-lookup"><span data-stu-id="579f8-110">The [**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579f8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="579f8-111">Return value</span></span>

<span data-ttu-id="579f8-112">此通知碼不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="579f8-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="579f8-113">備註</span><span class="sxs-lookup"><span data-stu-id="579f8-113">Remarks</span></span>

<span data-ttu-id="579f8-114">若要接收 EN \_ LOWFIRTF 通知，請 \_ 在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息傳送的遮罩中指定 ENM LOWFIRTF 旗標。</span><span class="sxs-lookup"><span data-stu-id="579f8-114">To receive an EN\_LOWFIRTF notification, specify the ENM\_LOWFIRTF flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="579f8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="579f8-115">Requirements</span></span>



| <span data-ttu-id="579f8-116">需求</span><span class="sxs-lookup"><span data-stu-id="579f8-116">Requirement</span></span> | <span data-ttu-id="579f8-117">值</span><span class="sxs-lookup"><span data-stu-id="579f8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="579f8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="579f8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="579f8-119">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="579f8-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="579f8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="579f8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="579f8-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="579f8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="579f8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="579f8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="579f8-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="579f8-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="579f8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="579f8-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="579f8-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="579f8-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="579f8-126">**ENLOWFIRTF**</span><span class="sxs-lookup"><span data-stu-id="579f8-126">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[<span data-ttu-id="579f8-127">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="579f8-127">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





