---
title: 'SB_SETTEXT 訊息 (Commctrl .h) '
description: 在狀態視窗的指定部分中設定文字。
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- SB_SETTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105066"
---
# <a name="sb_settext-message"></a><span data-ttu-id="9f01a-104">SB \_ SETTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="9f01a-104">SB\_SETTEXT message</span></span>

<span data-ttu-id="9f01a-105">在狀態視窗的指定部分中設定文字。</span><span class="sxs-lookup"><span data-stu-id="9f01a-105">Sets the text in the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f01a-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f01a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f01a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f01a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f01a-108">低序位單字的 [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) 會指定要設定之元件的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="9f01a-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the low-order word specifies the zero-based index of the part to set.</span></span> <span data-ttu-id="9f01a-109">如果 **LOBYTE** 設定為 SB \_ SIMPLEID，則狀態視窗會假設為簡單模式狀態列，也就是只有一個部分的狀態列。</span><span class="sxs-lookup"><span data-stu-id="9f01a-109">If the **LOBYTE** is set to SB\_SIMPLEID, the status window is assumed to be a simple mode status bar; that is, a status bar with only one part.</span></span>

<span data-ttu-id="9f01a-110">低序位字組的 [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) 會指定繪圖作業的型別。</span><span class="sxs-lookup"><span data-stu-id="9f01a-110">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the low-order word specifies the type of the drawing operation.</span></span> <span data-ttu-id="9f01a-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9f01a-111">This parameter can be one of the following values.</span></span>

<span data-ttu-id="9f01a-112">*WParam* 的高序位單字會被忽略。</span><span class="sxs-lookup"><span data-stu-id="9f01a-112">The high-order word of *wParam* is ignored.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f01a-113">值</span><span class="sxs-lookup"><span data-stu-id="9f01a-113">Value</span></span></th>
<th><span data-ttu-id="9f01a-114">意義</span><span class="sxs-lookup"><span data-stu-id="9f01a-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <span data-ttu-id="9f01a-115"><dt><strong>0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f01a-115"><dt><strong>0</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9f01a-116">文字會以框線繪製，並顯示為低於視窗的平面。</span><span class="sxs-lookup"><span data-stu-id="9f01a-116">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <span data-ttu-id="9f01a-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f01a-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9f01a-118">不以框線繪製文字。</span><span class="sxs-lookup"><span data-stu-id="9f01a-118">The text is drawn without borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <span data-ttu-id="9f01a-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f01a-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9f01a-120">文字是由父視窗繪製。</span><span class="sxs-lookup"><span data-stu-id="9f01a-120">The text is drawn by the parent window.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f01a-121">簡單模式的狀態列不支援「擁有者繪圖」。</span><span class="sxs-lookup"><span data-stu-id="9f01a-121">A simple mode status bar does not support owner drawing.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <span data-ttu-id="9f01a-122"><dt><strong>SBT_POPOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f01a-122"><dt><strong>SBT_POPOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9f01a-123">文字會以框線繪製，並顯示在視窗的平面的上方。</span><span class="sxs-lookup"><span data-stu-id="9f01a-123">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <span data-ttu-id="9f01a-124"><dt><strong>SBT_RTLREADING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f01a-124"><dt><strong>SBT_RTLREADING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9f01a-125">文字將會以相反方向顯示在父視窗中的文字。</span><span class="sxs-lookup"><span data-stu-id="9f01a-125">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <span data-ttu-id="9f01a-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f01a-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9f01a-127">略過 Tab 字元。</span><span class="sxs-lookup"><span data-stu-id="9f01a-127">Tab characters are ignored.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="9f01a-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f01a-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f01a-129">指標，指向以 null 終止的字串，指定要設定的文字。</span><span class="sxs-lookup"><span data-stu-id="9f01a-129">Pointer to a null-terminated string that specifies the text to set.</span></span> <span data-ttu-id="9f01a-130">如果 *wParam* 是 SBT \_ OWNERDRAW，此參數代表32位的資料。</span><span class="sxs-lookup"><span data-stu-id="9f01a-130">If *wParam* is SBT\_OWNERDRAW, this parameter represents 32 bits of data.</span></span> <span data-ttu-id="9f01a-131">父視窗必須解讀資料，並在收到 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息時繪製文字。</span><span class="sxs-lookup"><span data-stu-id="9f01a-131">The parent window must interpret the data and draw the text when it receives the [**WM\_DRAWITEM**](wm-drawitem.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f01a-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f01a-132">Return value</span></span>

<span data-ttu-id="9f01a-133">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9f01a-133">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f01a-134">備註</span><span class="sxs-lookup"><span data-stu-id="9f01a-134">Remarks</span></span>

<span data-ttu-id="9f01a-135">此訊息會使已變更視窗的部分失效，使其在視窗下一次收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時顯示新的文字。</span><span class="sxs-lookup"><span data-stu-id="9f01a-135">The message invalidates the portion of the window that has changed, causing it to display the new text when the window next receives the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="9f01a-136">一般視窗會將文字從左至右顯示 (LTR) 。</span><span class="sxs-lookup"><span data-stu-id="9f01a-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="9f01a-137">Windows 可以進行 *鏡像* ，以顯示如希伯來文或阿拉伯文等語言，由右至左 (RTL) 。</span><span class="sxs-lookup"><span data-stu-id="9f01a-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="9f01a-138">如果 \_ 設定了 SBT RTLREADING，則會從父視窗中的文字，以相反的方向讀取 *lParam* 字串。</span><span class="sxs-lookup"><span data-stu-id="9f01a-138">If SBT\_RTLREADING is set, the *lParam* string will read in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f01a-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f01a-139">Requirements</span></span>



| <span data-ttu-id="9f01a-140">需求</span><span class="sxs-lookup"><span data-stu-id="9f01a-140">Requirement</span></span> | <span data-ttu-id="9f01a-141">值</span><span class="sxs-lookup"><span data-stu-id="9f01a-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f01a-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f01a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9f01a-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f01a-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f01a-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f01a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9f01a-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f01a-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f01a-146">標頭</span><span class="sxs-lookup"><span data-stu-id="9f01a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f01a-147"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f01a-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9f01a-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="9f01a-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9f01a-149">**SB \_SETTEXTW** (Unicode) 和 **SB \_ SETTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="9f01a-149">**SB\_SETTEXTW** (Unicode) and **SB\_SETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="9f01a-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f01a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f01a-151">**SB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="9f01a-151">**SB\_GETTEXT**</span></span>](sb-gettext.md)
</dt> </dl>

 

