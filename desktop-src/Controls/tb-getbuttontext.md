---
title: 'TB_GETBUTTONTEXT 訊息 (Commctrl .h) '
description: 抓取工具列上按鈕的顯示文字。
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- TB_GETBUTTONTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104183"
---
# <a name="tb_getbuttontext-message"></a><span data-ttu-id="1f00f-104">TB \_ GETBUTTONTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="1f00f-104">TB\_GETBUTTONTEXT message</span></span>

<span data-ttu-id="1f00f-105">抓取工具列上按鈕的顯示文字。</span><span class="sxs-lookup"><span data-stu-id="1f00f-105">Retrieves the display text of a button on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f00f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f00f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f00f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f00f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f00f-108">要取出其文字之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f00f-108">Command identifier of the button whose text is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="1f00f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f00f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f00f-110">接收按鈕文字之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="1f00f-110">Pointer to a buffer that receives the button text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f00f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f00f-111">Return value</span></span>

<span data-ttu-id="1f00f-112">傳回 *lParam* 所指向之字串的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f00f-112">Returns the length, in characters, of the string pointed to by *lParam*.</span></span> <span data-ttu-id="1f00f-113">長度不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="1f00f-113">The length does not include the terminating null character.</span></span> <span data-ttu-id="1f00f-114">如果不成功，則傳回值為-1。</span><span class="sxs-lookup"><span data-stu-id="1f00f-114">If unsuccessful, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f00f-115">備註</span><span class="sxs-lookup"><span data-stu-id="1f00f-115">Remarks</span></span>

<span data-ttu-id="1f00f-116">**安全性警告：** 不當使用此訊息可能會危及程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="1f00f-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="1f00f-117">此訊息不會提供您知道緩衝區大小的方法。</span><span class="sxs-lookup"><span data-stu-id="1f00f-117">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="1f00f-118">如果您使用此訊息，請先呼叫在 *lParam* 中傳遞 **null** 的訊息，這會傳回字元數，但不包括需要的 **null** 。</span><span class="sxs-lookup"><span data-stu-id="1f00f-118">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="1f00f-119">然後第二次呼叫訊息以抓取字串。</span><span class="sxs-lookup"><span data-stu-id="1f00f-119">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="1f00f-120">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="1f00f-120">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="1f00f-121">傳回的字串會對應至按鈕目前所顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="1f00f-121">The returned string corresponds to the text that is currently displayed by the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f00f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f00f-122">Requirements</span></span>



| <span data-ttu-id="1f00f-123">需求</span><span class="sxs-lookup"><span data-stu-id="1f00f-123">Requirement</span></span> | <span data-ttu-id="1f00f-124">值</span><span class="sxs-lookup"><span data-stu-id="1f00f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f00f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f00f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1f00f-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f00f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f00f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f00f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1f00f-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f00f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f00f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1f00f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f00f-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f00f-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1f00f-131">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1f00f-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1f00f-132">**TB \_GETBUTTONTEXTW** (Unicode) 和 **TB \_ GETBUTTONTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1f00f-132">**TB\_GETBUTTONTEXTW** (Unicode) and **TB\_GETBUTTONTEXTA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="1f00f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f00f-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f00f-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="1f00f-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f00f-135">**TB \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="1f00f-135">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="1f00f-136">**TB \_ GETSTRING**</span><span class="sxs-lookup"><span data-stu-id="1f00f-136">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="1f00f-137">**TB \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="1f00f-137">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> </dl>

 

 





