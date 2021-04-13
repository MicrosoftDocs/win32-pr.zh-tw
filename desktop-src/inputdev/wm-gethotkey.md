---
title: 'WM_GETHOTKEY 訊息 (Winuser .h) '
description: 傳送以判斷與視窗相關聯的快速鍵。
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- WM_GETHOTKEY 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464936"
---
# <a name="wm_gethotkey-message"></a><span data-ttu-id="b0b77-104">WM \_ GETHOTKEY 訊息</span><span class="sxs-lookup"><span data-stu-id="b0b77-104">WM\_GETHOTKEY message</span></span>

<span data-ttu-id="b0b77-105">傳送以判斷與視窗相關聯的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="b0b77-105">Sent to determine the hot key associated with a window.</span></span>


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a><span data-ttu-id="b0b77-106">參數</span><span class="sxs-lookup"><span data-stu-id="b0b77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0b77-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b77-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b0b77-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b0b77-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0b77-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b77-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="b0b77-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b77-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0b77-111">Return value</span></span>

<span data-ttu-id="b0b77-112">傳回值是快速鍵的虛擬機器碼和修飾詞，如果沒有任何熱鍵與視窗相關聯，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b0b77-112">The return value is the virtual-key code and modifiers for the hot key, or **NULL** if no hot key is associated with the window.</span></span> <span data-ttu-id="b0b77-113">虛擬機器碼是在傳回值的低位元組內，而修飾詞是在高位元組中。</span><span class="sxs-lookup"><span data-stu-id="b0b77-113">The virtual-key code is in the low byte of the return value and the modifiers are in the high byte.</span></span> <span data-ttu-id="b0b77-114">修飾詞可以是下列 CommCtrl 旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="b0b77-114">The modifiers can be a combination of the following flags from CommCtrl.h.</span></span>



| <span data-ttu-id="b0b77-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b0b77-115">Return code/value</span></span>                                                                                                                                         | <span data-ttu-id="b0b77-116">Description</span><span class="sxs-lookup"><span data-stu-id="b0b77-116">Description</span></span>             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="b0b77-117"><dt>**HOTKEYF \_ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="b0b77-117"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>     | <span data-ttu-id="b0b77-118">ALT 鍵</span><span class="sxs-lookup"><span data-stu-id="b0b77-118">ALT key</span></span><br/>      |
| <dl> <span data-ttu-id="b0b77-119"><dt>**HOTKEYF \_控制**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="b0b77-119"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="b0b77-120">CTRL 鍵</span><span class="sxs-lookup"><span data-stu-id="b0b77-120">CTRL key</span></span><br/>     |
| <dl> <span data-ttu-id="b0b77-121"><dt>**HOTKEYF \_EXT**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="b0b77-121"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>     | <span data-ttu-id="b0b77-122">擴充金鑰</span><span class="sxs-lookup"><span data-stu-id="b0b77-122">Extended key</span></span><br/> |
| <dl> <span data-ttu-id="b0b77-123"><dt>**HOTKEYF \_SHIFT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="b0b77-123"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>   | <span data-ttu-id="b0b77-124">SHIFT 鍵</span><span class="sxs-lookup"><span data-stu-id="b0b77-124">SHIFT key</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="b0b77-125">備註</span><span class="sxs-lookup"><span data-stu-id="b0b77-125">Remarks</span></span>

<span data-ttu-id="b0b77-126">這些快速鍵與 [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) 函式所設定的熱鍵無關。</span><span class="sxs-lookup"><span data-stu-id="b0b77-126">These hot keys are unrelated to the hot keys set by the [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b77-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0b77-127">Requirements</span></span>



| <span data-ttu-id="b0b77-128">需求</span><span class="sxs-lookup"><span data-stu-id="b0b77-128">Requirement</span></span> | <span data-ttu-id="b0b77-129">值</span><span class="sxs-lookup"><span data-stu-id="b0b77-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b77-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0b77-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b77-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0b77-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b0b77-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0b77-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b77-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0b77-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b0b77-134">標頭</span><span class="sxs-lookup"><span data-stu-id="b0b77-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0b77-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b0b77-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b77-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0b77-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0b77-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="b0b77-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0b77-138">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="b0b77-138">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="b0b77-139">**WM \_ SETHOTKEY**</span><span class="sxs-lookup"><span data-stu-id="b0b77-139">**WM\_SETHOTKEY**</span></span>](wm-sethotkey.md)
</dt> <dt>

<span data-ttu-id="b0b77-140">**概念**</span><span class="sxs-lookup"><span data-stu-id="b0b77-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0b77-141">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="b0b77-141">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

