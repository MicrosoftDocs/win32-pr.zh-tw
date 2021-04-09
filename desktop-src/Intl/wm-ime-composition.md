---
description: 當 IME 將組合狀態變更為擊鍵結果時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: 'WM_IME_COMPOSITION 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945420"
---
# <a name="wm_ime_composition-message"></a><span data-ttu-id="f40f1-104">WM \_ IME \_ 組合訊息</span><span class="sxs-lookup"><span data-stu-id="f40f1-104">WM\_IME\_COMPOSITION message</span></span>

<span data-ttu-id="f40f1-105">當 IME 將組合狀態變更為擊鍵結果時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="f40f1-105">Sent to an application when the IME changes composition status as a result of a keystroke.</span></span> <span data-ttu-id="f40f1-106">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="f40f1-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a><span data-ttu-id="f40f1-107">參數</span><span class="sxs-lookup"><span data-stu-id="f40f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f40f1-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="f40f1-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f40f1-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f40f1-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="f40f1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f40f1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f40f1-111">表示組合字元串之最新變更的 DBCS 字元。</span><span class="sxs-lookup"><span data-stu-id="f40f1-111">DBCS character representing the latest change to the composition string.</span></span>

</dd> <dt>

<span data-ttu-id="f40f1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f40f1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f40f1-113">指定組合字元串或字元變更方式的值。</span><span class="sxs-lookup"><span data-stu-id="f40f1-113">Value specifying how the composition string or character changed.</span></span> <span data-ttu-id="f40f1-114">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="f40f1-114">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="f40f1-115">如需這些值的詳細資訊，請參閱 [IME 組合字元串值](ime-composition-string-values.md)。</span><span class="sxs-lookup"><span data-stu-id="f40f1-115">For more information about these values, see [IME Composition String Values](ime-composition-string-values.md).</span></span>

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

<span data-ttu-id="f40f1-116">**GC \_ COMPATTR**</span><span class="sxs-lookup"><span data-stu-id="f40f1-116">**GCS\_COMPATTR**</span></span>
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

<span data-ttu-id="f40f1-117">**GC \_ COMPCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="f40f1-117">**GCS\_COMPCLAUSE**</span></span>
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

<span data-ttu-id="f40f1-118">**GC \_ COMPREADSTR**</span><span class="sxs-lookup"><span data-stu-id="f40f1-118">**GCS\_COMPREADSTR**</span></span>
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

<span data-ttu-id="f40f1-119">**GC \_ COMPREADATTR**</span><span class="sxs-lookup"><span data-stu-id="f40f1-119">**GCS\_COMPREADATTR**</span></span>
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

<span data-ttu-id="f40f1-120">**GC \_ COMPREADCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="f40f1-120">**GCS\_COMPREADCLAUSE**</span></span>
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

<span data-ttu-id="f40f1-121">**GC \_ COMPSTR**</span><span class="sxs-lookup"><span data-stu-id="f40f1-121">**GCS\_COMPSTR**</span></span>
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

<span data-ttu-id="f40f1-122">**GC \_ CURSORPOS**</span><span class="sxs-lookup"><span data-stu-id="f40f1-122">**GCS\_CURSORPOS**</span></span>
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

<span data-ttu-id="f40f1-123">**GC \_ DELTASTART**</span><span class="sxs-lookup"><span data-stu-id="f40f1-123">**GCS\_DELTASTART**</span></span>
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

<span data-ttu-id="f40f1-124">**GC \_ RESULTCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="f40f1-124">**GCS\_RESULTCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

<span data-ttu-id="f40f1-125">**GC \_ RESULTREADCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="f40f1-125">**GCS\_RESULTREADCLAUSE**</span></span>
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

<span data-ttu-id="f40f1-126">**GC \_ RESULTREADSTR**</span><span class="sxs-lookup"><span data-stu-id="f40f1-126">**GCS\_RESULTREADSTR**</span></span>
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

<span data-ttu-id="f40f1-127">**GC \_ RESULTSTR**</span><span class="sxs-lookup"><span data-stu-id="f40f1-127">**GCS\_RESULTSTR**</span></span>
</dt> </dl>

<span data-ttu-id="f40f1-128">*LParam* 參數也可以具有下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="f40f1-128">The *lParam* parameter can also have one or more of the following values.</span></span>



| <span data-ttu-id="f40f1-129">值</span><span class="sxs-lookup"><span data-stu-id="f40f1-129">Value</span></span>                                                                                                                                                            | <span data-ttu-id="f40f1-130">意義</span><span class="sxs-lookup"><span data-stu-id="f40f1-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <span data-ttu-id="f40f1-131"><dt>**CS \_ INSERTCHAR**</dt></span><span class="sxs-lookup"><span data-stu-id="f40f1-131"><dt>**CS\_INSERTCHAR**</dt></span></span> </dl>    | <span data-ttu-id="f40f1-132">在目前的插入點插入 *wParam* 組合字元。</span><span class="sxs-lookup"><span data-stu-id="f40f1-132">Insert the *wParam* composition character at the current insertion point.</span></span> <span data-ttu-id="f40f1-133">如果應用程式處理此訊息，則應該顯示組合字元。</span><span class="sxs-lookup"><span data-stu-id="f40f1-133">An application should display the composition character if it processes this message.</span></span><br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <span data-ttu-id="f40f1-134"><dt>**CS \_ NOMOVECARET**</dt></span><span class="sxs-lookup"><span data-stu-id="f40f1-134"><dt>**CS\_NOMOVECARET**</dt></span></span> </dl> | <span data-ttu-id="f40f1-135">請勿移動插入號位置，因為處理訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="f40f1-135">Do not move the caret position as a result of processing the message.</span></span> <span data-ttu-id="f40f1-136">例如，如果 IME 指定 CS \_ INSERTCHAR 和 cs NOMOVECARET 的組合 \_ ，應用程式應該在目前的插入號位置插入指定的字元，但不應該將插入號移到下一個位置。</span><span class="sxs-lookup"><span data-stu-id="f40f1-136">For example, if an IME specifies a combination of CS\_INSERTCHAR and CS\_NOMOVECARET, the application should insert the specified character at the current caret position but should not move the caret to the next position.</span></span> <span data-ttu-id="f40f1-137">\_具有 gc RESULTSTR 的後續 WM IME \_ 組合訊息 \_ 將會取代此字元。</span><span class="sxs-lookup"><span data-stu-id="f40f1-137">A subsequent WM\_IME\_COMPOSITION message with GCS\_RESULTSTR will replace this character.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f40f1-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="f40f1-138">Return value</span></span>

<span data-ttu-id="f40f1-139">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="f40f1-139">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f40f1-140">備註</span><span class="sxs-lookup"><span data-stu-id="f40f1-140">Remarks</span></span>

<span data-ttu-id="f40f1-141">如果應用程式顯示覆合字元本身，就應該處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="f40f1-141">An application should process this message if it displays composition characters itself.</span></span> <span data-ttu-id="f40f1-142">否則，它應該會將訊息傳送至 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="f40f1-142">Otherwise, it should send the message to the IME window.</span></span>

<span data-ttu-id="f40f1-143">如果應用程式已建立 IME 視窗，則應該將此訊息傳遞至該視窗。</span><span class="sxs-lookup"><span data-stu-id="f40f1-143">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="f40f1-144">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將此訊息傳遞至預設的 IME 視窗來進行處理。</span><span class="sxs-lookup"><span data-stu-id="f40f1-144">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span> <span data-ttu-id="f40f1-145">IME 視窗會根據指定的變更旗標來更新其外觀，以處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="f40f1-145">The IME window processes this message by updating its appearance based on the change flag specified.</span></span> <span data-ttu-id="f40f1-146">應用程式可以呼叫 [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) 來取得新的組合狀態。</span><span class="sxs-lookup"><span data-stu-id="f40f1-146">An application can call [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) to retrieve the new composition status.</span></span>

<span data-ttu-id="f40f1-147">如果未設定任何 GC \_ 值，訊息會指出目前的組合已取消，而繪製組合字元串的應用程式應刪除字串。</span><span class="sxs-lookup"><span data-stu-id="f40f1-147">If none of the GCS\_ values are set, the message indicates that the current composition has been canceled and applications that draw the composition string should delete the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="f40f1-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="f40f1-148">Requirements</span></span>



| <span data-ttu-id="f40f1-149">需求</span><span class="sxs-lookup"><span data-stu-id="f40f1-149">Requirement</span></span> | <span data-ttu-id="f40f1-150">值</span><span class="sxs-lookup"><span data-stu-id="f40f1-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f40f1-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f40f1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f40f1-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f40f1-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f40f1-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f40f1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f40f1-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f40f1-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f40f1-155">標頭</span><span class="sxs-lookup"><span data-stu-id="f40f1-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="f40f1-156"><dt>Winuser (包含 Windows .h) ;</dt><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f40f1-156"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f40f1-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f40f1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f40f1-158">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="f40f1-158">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f40f1-159">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="f40f1-159">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="f40f1-160">**ImmGetCompositionString**</span><span class="sxs-lookup"><span data-stu-id="f40f1-160">**ImmGetCompositionString**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
