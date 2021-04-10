---
title: 'SB_GETTEXTLENGTH 訊息 (Commctrl .h) '
description: 從狀態視窗的指定部分抓取文字長度（以字元為單位）。
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934796"
---
# <a name="sb_gettextlength-message"></a><span data-ttu-id="02f2d-104">SB \_ GETTEXTLENGTH 訊息</span><span class="sxs-lookup"><span data-stu-id="02f2d-104">SB\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="02f2d-105">從狀態視窗的指定部分抓取文字長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="02f2d-105">Retrieves the length, in characters, of the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="02f2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="02f2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02f2d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02f2d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02f2d-108">以零為基底的索引，這是要從中取得文字的部分。</span><span class="sxs-lookup"><span data-stu-id="02f2d-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="02f2d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02f2d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="02f2d-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="02f2d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02f2d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="02f2d-111">Return value</span></span>

<span data-ttu-id="02f2d-112">傳回包含 2 16 位值的32位值。</span><span class="sxs-lookup"><span data-stu-id="02f2d-112">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="02f2d-113">[低] 字組指定文字的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="02f2d-113">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="02f2d-114">High 單字指定用來繪製文字的作業類型。</span><span class="sxs-lookup"><span data-stu-id="02f2d-114">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="02f2d-115">此類型可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="02f2d-115">The type can be one of the following values:</span></span>



| <span data-ttu-id="02f2d-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="02f2d-116">Return code</span></span>                                                                                    | <span data-ttu-id="02f2d-117">Description</span><span class="sxs-lookup"><span data-stu-id="02f2d-117">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02f2d-118"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="02f2d-118"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="02f2d-119">文字會以框線繪製，並顯示為低於視窗的平面。</span><span class="sxs-lookup"><span data-stu-id="02f2d-119">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>          |
| <dl> <span data-ttu-id="02f2d-120"><dt>**SBT \_ NOBORDERS**</dt></span><span class="sxs-lookup"><span data-stu-id="02f2d-120"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="02f2d-121">不以框線繪製文字。</span><span class="sxs-lookup"><span data-stu-id="02f2d-121">The text is drawn without borders.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="02f2d-122"><dt>**SBT \_ OWNERDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="02f2d-122"><dt>**SBT\_OWNERDRAW**</dt></span></span> </dl>  | <span data-ttu-id="02f2d-123">文字是由父視窗繪製。</span><span class="sxs-lookup"><span data-stu-id="02f2d-123">The text is drawn by the parent window.</span></span><br/>                                                |
| <dl> <span data-ttu-id="02f2d-124"><dt>**SBT \_ 彈出**</dt></span><span class="sxs-lookup"><span data-stu-id="02f2d-124"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="02f2d-125">文字會以框線繪製，並顯示在視窗的平面的上方。</span><span class="sxs-lookup"><span data-stu-id="02f2d-125">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/>         |
| <dl> <span data-ttu-id="02f2d-126"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="02f2d-126"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="02f2d-127">文字將會以相反方向顯示在父視窗中的文字。</span><span class="sxs-lookup"><span data-stu-id="02f2d-127">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02f2d-128">備註</span><span class="sxs-lookup"><span data-stu-id="02f2d-128">Remarks</span></span>

<span data-ttu-id="02f2d-129">一般視窗會將文字從左至右顯示 (LTR) 。</span><span class="sxs-lookup"><span data-stu-id="02f2d-129">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="02f2d-130">Windows 可以進行 *鏡像* ，以顯示如希伯來文或阿拉伯文等語言，由右至左 (RTL) 。</span><span class="sxs-lookup"><span data-stu-id="02f2d-130">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="02f2d-131">如果 \_ 已設定 [SBT RTLREADING]，則會從父視窗中的文字，以相反的方向讀取指定的狀態視窗文字。</span><span class="sxs-lookup"><span data-stu-id="02f2d-131">If SBT\_RTLREADING is set, the specified status window text will read in the opposite direction from the text in the parent window.</span></span>

<span data-ttu-id="02f2d-132">此訊息會傳回65535個字元的字串長度上限。</span><span class="sxs-lookup"><span data-stu-id="02f2d-132">This message returns a maximum string length of 65,535 characters.</span></span> <span data-ttu-id="02f2d-133">如果實際文字字串的長度超過該字串，則 [**SB \_ GETTEXT**](sb-gettext.md) 訊息會將它截斷。</span><span class="sxs-lookup"><span data-stu-id="02f2d-133">If the actual text string is longer than that, the [**SB\_GETTEXT**](sb-gettext.md) message truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f2d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="02f2d-134">Requirements</span></span>



| <span data-ttu-id="02f2d-135">需求</span><span class="sxs-lookup"><span data-stu-id="02f2d-135">Requirement</span></span> | <span data-ttu-id="02f2d-136">值</span><span class="sxs-lookup"><span data-stu-id="02f2d-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02f2d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02f2d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="02f2d-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02f2d-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02f2d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02f2d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="02f2d-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02f2d-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02f2d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="02f2d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="02f2d-142"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="02f2d-142"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="02f2d-143">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="02f2d-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="02f2d-144">**SB \_GETTEXTLENGTHW** (Unicode) 和 **SB \_ GETTEXTLENGTHA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="02f2d-144">**SB\_GETTEXTLENGTHW** (Unicode) and **SB\_GETTEXTLENGTHA** (ANSI)</span></span><br/>         |



 

 





