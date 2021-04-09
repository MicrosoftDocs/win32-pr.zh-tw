---
title: 'EN_OBJECTPOSITIONS (Richedit 的通知碼) '
description: 當控制項讀取物件時，通知 rich edit 控制項的父視窗。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843679"
---
# <a name="en_objectpositions-notification-code"></a><span data-ttu-id="95254-105">EN \_ OBJECTPOSITIONS 通知碼</span><span class="sxs-lookup"><span data-stu-id="95254-105">EN\_OBJECTPOSITIONS notification code</span></span>

<span data-ttu-id="95254-106">當控制項讀取物件時，通知 rich edit 控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="95254-106">Notifies a rich edit control's parent window when the control reads in objects.</span></span> <span data-ttu-id="95254-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="95254-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="95254-108">參數</span><span class="sxs-lookup"><span data-stu-id="95254-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95254-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95254-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95254-110">[**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)結構。</span><span class="sxs-lookup"><span data-stu-id="95254-110">An [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95254-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95254-111">Return value</span></span>

<span data-ttu-id="95254-112">傳回零以繼續 **讀取** 操作。</span><span class="sxs-lookup"><span data-stu-id="95254-112">Return zero to continue the **Read** operation.</span></span>

<span data-ttu-id="95254-113">傳回非零值以停止 **讀取** 作業。</span><span class="sxs-lookup"><span data-stu-id="95254-113">Return a nonzero value to stop the **Read** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="95254-114">備註</span><span class="sxs-lookup"><span data-stu-id="95254-114">Remarks</span></span>

<span data-ttu-id="95254-115">若要接收 EN \_ OBJECTPOSITIONS 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md)旗標。</span><span class="sxs-lookup"><span data-stu-id="95254-115">To receive an EN\_OBJECTPOSITIONS notification code, specify the [**ENM\_OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="95254-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="95254-116">Requirements</span></span>



| <span data-ttu-id="95254-117">需求</span><span class="sxs-lookup"><span data-stu-id="95254-117">Requirement</span></span> | <span data-ttu-id="95254-118">值</span><span class="sxs-lookup"><span data-stu-id="95254-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95254-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95254-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95254-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95254-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95254-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95254-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95254-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95254-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95254-123">標頭</span><span class="sxs-lookup"><span data-stu-id="95254-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95254-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="95254-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95254-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95254-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="95254-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="95254-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="95254-127">**EM \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="95254-127">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="95254-128">**OBJECTPOSITIONS**</span><span class="sxs-lookup"><span data-stu-id="95254-128">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[<span data-ttu-id="95254-129">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="95254-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> <dt>

<span data-ttu-id="95254-130">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="95254-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="95254-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95254-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="95254-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95254-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

