---
title: 'EN_CORRECTTEXT (Richedit 的通知碼) '
description: 通知 rich edit 控制項父視窗 SYV \_ 正確的手勢發生，讓父視窗有機會取消更正文字。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093931"
---
# <a name="en_correcttext-notification-code"></a><span data-ttu-id="c0f11-105">EN \_ CORRECTTEXT 通知碼</span><span class="sxs-lookup"><span data-stu-id="c0f11-105">EN\_CORRECTTEXT notification code</span></span>

<span data-ttu-id="c0f11-106">通知 rich edit 控制項父視窗 SYV \_ 正確的手勢發生，讓父視窗有機會取消更正文字。</span><span class="sxs-lookup"><span data-stu-id="c0f11-106">Notifies a rich edit control parent window that a SYV\_CORRECT gesture occurred, giving the parent window a chance to cancel correcting the text.</span></span> <span data-ttu-id="c0f11-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c0f11-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c0f11-108">參數</span><span class="sxs-lookup"><span data-stu-id="c0f11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f11-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0f11-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0f11-110">指定要更正之選取範圍的 [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) 結構。</span><span class="sxs-lookup"><span data-stu-id="c0f11-110">An [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) structure specifying the selection to be corrected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f11-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0f11-111">Return value</span></span>

<span data-ttu-id="c0f11-112">傳回零以忽略動作。</span><span class="sxs-lookup"><span data-stu-id="c0f11-112">Return zero to ignore the action.</span></span>

<span data-ttu-id="c0f11-113">傳回非零值以處理動作。</span><span class="sxs-lookup"><span data-stu-id="c0f11-113">Returns a nonzero value to process the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0f11-114">備註</span><span class="sxs-lookup"><span data-stu-id="c0f11-114">Remarks</span></span>

<span data-ttu-id="c0f11-115">只有在有可用的畫筆功能時，才會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="c0f11-115">This notification code is sent only if pen capabilities are available.</span></span>

<span data-ttu-id="c0f11-116">若要接收 EN \_ CORRECTTEXT 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="c0f11-116">To receive EN\_CORRECTTEXT notification codes, specify [**ENM\_CORRECTTEXT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="c0f11-117">\_只有在 rich edit 1.0 版中才支援 EN CORRECTTEXT 通知碼。</span><span class="sxs-lookup"><span data-stu-id="c0f11-117">The EN\_CORRECTTEXT notification code is only supported in rich edit version 1.0.</span></span> <span data-ttu-id="c0f11-118">較新版本的 rich edit 不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="c0f11-118">It is not supported in later versions of rich edit.</span></span> <span data-ttu-id="c0f11-119">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="c0f11-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0f11-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0f11-120">Requirements</span></span>



| <span data-ttu-id="c0f11-121">需求</span><span class="sxs-lookup"><span data-stu-id="c0f11-121">Requirement</span></span> | <span data-ttu-id="c0f11-122">值</span><span class="sxs-lookup"><span data-stu-id="c0f11-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f11-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0f11-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f11-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0f11-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0f11-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0f11-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f11-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0f11-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0f11-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c0f11-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f11-128"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0f11-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f11-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0f11-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c0f11-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="c0f11-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c0f11-131">**ENCORRECTTEXT**</span><span class="sxs-lookup"><span data-stu-id="c0f11-131">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





