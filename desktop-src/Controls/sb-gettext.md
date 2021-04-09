---
title: 'SB_GETTEXT 訊息 (Commctrl .h) '
description: 從狀態視窗的指定部分抓取文字。
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025333"
---
# <a name="sb_gettext-message"></a><span data-ttu-id="7fd93-104">SB \_ GETTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="7fd93-104">SB\_GETTEXT message</span></span>

<span data-ttu-id="7fd93-105">從狀態視窗的指定部分抓取文字。</span><span class="sxs-lookup"><span data-stu-id="7fd93-105">Retrieves the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fd93-106">參數</span><span class="sxs-lookup"><span data-stu-id="7fd93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd93-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fd93-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fd93-108">以零為基底的索引，這是要從中取得文字的部分。</span><span class="sxs-lookup"><span data-stu-id="7fd93-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="7fd93-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fd93-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fd93-110">以 null 終止字串的形式接收文字之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="7fd93-110">Pointer to the buffer that receives the text as a null-terminated string.</span></span> <span data-ttu-id="7fd93-111">使用 [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) 訊息來判斷所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="7fd93-111">Use the [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message to determine the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd93-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fd93-112">Return value</span></span>

<span data-ttu-id="7fd93-113">傳回包含 2 16 位值的32位值。</span><span class="sxs-lookup"><span data-stu-id="7fd93-113">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="7fd93-114">[低] 字組指定文字的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd93-114">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="7fd93-115">High 單字指定用來繪製文字的作業類型。</span><span class="sxs-lookup"><span data-stu-id="7fd93-115">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="7fd93-116">此類型可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7fd93-116">The type can be one of the following values.</span></span>



| <span data-ttu-id="7fd93-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7fd93-117">Return code</span></span>                                                                                    | <span data-ttu-id="7fd93-118">Description</span><span class="sxs-lookup"><span data-stu-id="7fd93-118">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fd93-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd93-119"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="7fd93-120">文字會以框線繪製，並顯示為低於視窗的平面。</span><span class="sxs-lookup"><span data-stu-id="7fd93-120">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>  |
| <dl> <span data-ttu-id="7fd93-121"><dt>**SBT \_ NOBORDERS**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd93-121"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="7fd93-122">不以框線繪製文字。</span><span class="sxs-lookup"><span data-stu-id="7fd93-122">The text is drawn without borders.</span></span><br/>                                             |
| <dl> <span data-ttu-id="7fd93-123"><dt>**SBT \_ 彈出**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd93-123"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="7fd93-124">文字會以框線繪製，並顯示在視窗的平面的上方。</span><span class="sxs-lookup"><span data-stu-id="7fd93-124">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/> |
| <dl> <span data-ttu-id="7fd93-125"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="7fd93-125"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="7fd93-126">文字會在父視窗中以相反的方向顯示文字。</span><span class="sxs-lookup"><span data-stu-id="7fd93-126">The text displays in the opposite direction of the text in the parent window.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="7fd93-127">備註</span><span class="sxs-lookup"><span data-stu-id="7fd93-127">Remarks</span></span>

<span data-ttu-id="7fd93-128">**安全性警告：** 不當使用此訊息可能會危及程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="7fd93-128">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="7fd93-129">此訊息不會提供您知道緩衝區大小的方法。</span><span class="sxs-lookup"><span data-stu-id="7fd93-129">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="7fd93-130">如果您使用此訊息，請先呼叫 [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) 來取得所需的字元數，然後呼叫訊息以取得字串。</span><span class="sxs-lookup"><span data-stu-id="7fd93-130">If you use this message, first call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="7fd93-131">如果您在呼叫 Sb 之前等候 **\_ GETTEXT** ，文字可能會變更，因此會使 **SB \_ GETTEXTLENGTH** 的傳回值失效。</span><span class="sxs-lookup"><span data-stu-id="7fd93-131">If you wait before calling **SB\_GETTEXT** the text could change, thereby invalidating the return value of **SB\_GETTEXTLENGTH**.</span></span> <span data-ttu-id="7fd93-132">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="7fd93-132">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="7fd93-133">此訊息最多會傳回65535個字元。</span><span class="sxs-lookup"><span data-stu-id="7fd93-133">This message returns a maximum of 65,535 characters.</span></span> <span data-ttu-id="7fd93-134">如果文字字串的長度超過該字串，則會被截斷。</span><span class="sxs-lookup"><span data-stu-id="7fd93-134">If the text string is longer than that, it is truncated.</span></span>

<span data-ttu-id="7fd93-135">如果文字具有 SBT \_ OWNERDRAW 繪圖類型，則此訊息會傳回與文字相關聯的32位值，而不是長度和作業類型。</span><span class="sxs-lookup"><span data-stu-id="7fd93-135">If the text has the SBT\_OWNERDRAW drawing type, this message returns the 32-bit value associated with the text instead of the length and operation type.</span></span>

<span data-ttu-id="7fd93-136">一般視窗會將文字從左至右顯示 (LTR) 。</span><span class="sxs-lookup"><span data-stu-id="7fd93-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="7fd93-137">Windows 可以進行 *鏡像* ，以顯示如希伯來文或阿拉伯文等語言，由右至左 (RTL) 。</span><span class="sxs-lookup"><span data-stu-id="7fd93-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="7fd93-138">如果 \_ 設定了 SBT RTLREADING，則 *lParam* 字串會從父視窗中的文字以相反的方向讀取。</span><span class="sxs-lookup"><span data-stu-id="7fd93-138">If SBT\_RTLREADING is set, the *lParam* string reads in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd93-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fd93-139">Requirements</span></span>



| <span data-ttu-id="7fd93-140">需求</span><span class="sxs-lookup"><span data-stu-id="7fd93-140">Requirement</span></span> | <span data-ttu-id="7fd93-141">值</span><span class="sxs-lookup"><span data-stu-id="7fd93-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd93-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fd93-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd93-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fd93-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fd93-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fd93-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd93-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fd93-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fd93-146">標頭</span><span class="sxs-lookup"><span data-stu-id="7fd93-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fd93-147"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd93-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7fd93-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7fd93-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7fd93-149">**SB \_GETTEXTW** (Unicode) 和 **SB \_ GETTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7fd93-149">**SB\_GETTEXTW** (Unicode) and **SB\_GETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="7fd93-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fd93-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd93-151">**SB \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="7fd93-151">**SB\_SETTEXT**</span></span>](sb-settext.md)
</dt> </dl>

 

 





