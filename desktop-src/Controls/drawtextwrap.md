---
title: DrawTextWrap 函式
description: 在指定的矩形中繪製格式化的文字。 它會根據指定的方法將文字格式化 (展開索引標籤、對齊字元、斷線等) 。 此函數會包裝對 DrawText 的呼叫。
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- DrawTextWrap 函式 Windows 控制項
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933967"
---
# <a name="drawtextwrap-function"></a><span data-ttu-id="c8426-106">DrawTextWrap 函式</span><span class="sxs-lookup"><span data-stu-id="c8426-106">DrawTextWrap function</span></span>

<span data-ttu-id="c8426-107">\[**DrawTextWrap** 可透過 Windows XP Service Pack 2 (SP2) 取得。</span><span class="sxs-lookup"><span data-stu-id="c8426-107">\[**DrawTextWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="c8426-108">它可能會在後續版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c8426-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c8426-109">建議您改為直接使用 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) 。\]</span><span class="sxs-lookup"><span data-stu-id="c8426-109">It is recommended to use [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directly instead.\]</span></span>

<span data-ttu-id="c8426-110">在指定的矩形中繪製格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="c8426-110">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="c8426-111">它會根據指定的方法將文字格式化 (展開索引標籤、對齊字元、斷線等) 。</span><span class="sxs-lookup"><span data-stu-id="c8426-111">It formats the text according to the specified method (expanding tabs, justifying characters, breaking lines, and so on).</span></span> <span data-ttu-id="c8426-112">此函數會包裝對 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c8426-112">This function wraps a call to [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8426-113">語法</span><span class="sxs-lookup"><span data-stu-id="c8426-113">Syntax</span></span>


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="c8426-114">參數</span><span class="sxs-lookup"><span data-stu-id="c8426-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8426-115">*hdc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8426-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8426-116">類型： **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8426-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8426-117">裝置內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c8426-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="c8426-118">*lpString* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c8426-118">*lpString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8426-119">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8426-119">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8426-120">包含要繪製之文字的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="c8426-120">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="c8426-121">如果 *nCount* 參數為-1，則字串必須以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="c8426-121">If the *nCount* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="c8426-122">如果 *uFormat* 包含 DT \_ MODIFYSTRING，此函式最多可能會在此字串中加上四個額外的字元。</span><span class="sxs-lookup"><span data-stu-id="c8426-122">If *uFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="c8426-123">包含字串的緩衝區必須夠大，才能容納這些額外的字元。</span><span class="sxs-lookup"><span data-stu-id="c8426-123">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="c8426-124">*nCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8426-124">*nCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8426-125">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="c8426-125">Type: **int**</span></span>

<span data-ttu-id="c8426-126">*LpString* 所指向之字串的長度。</span><span class="sxs-lookup"><span data-stu-id="c8426-126">The length of the string pointed to by *lpString*.</span></span> <span data-ttu-id="c8426-127">如果 *nCount* 為-1，則會假設 *lpString* 參數是以 null 終止之字串的指標，而 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) 會自動計算字元計數。</span><span class="sxs-lookup"><span data-stu-id="c8426-127">If *nCount* is -1, then the *lpString* parameter is assumed to be a pointer to a null-terminated string and [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="c8426-128">*lpRect* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c8426-128">*lpRect* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8426-129">類型： **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="c8426-129">Type: **LPRECT**</span></span>

<span data-ttu-id="c8426-130">[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，其中包含要格式化文字的矩形（以邏輯座標表示）。</span><span class="sxs-lookup"><span data-stu-id="c8426-130">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="c8426-131">*uFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8426-131">*uFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8426-132">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c8426-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c8426-133">格式化選項。</span><span class="sxs-lookup"><span data-stu-id="c8426-133">The formatting options.</span></span> <span data-ttu-id="c8426-134">如需完整的選項清單，請參閱 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) 檔。</span><span class="sxs-lookup"><span data-stu-id="c8426-134">See the documentation for [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="c8426-135">*lpDTParams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8426-135">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8426-136">類型： **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="c8426-136">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="c8426-137">[**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams)結構的指標，指定其他格式化選項。</span><span class="sxs-lookup"><span data-stu-id="c8426-137">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="c8426-138">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c8426-138">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8426-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8426-139">Return value</span></span>

<span data-ttu-id="c8426-140">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="c8426-140">Type: **int**</span></span>

<span data-ttu-id="c8426-141">如果函式成功，則傳回值為邏輯單元中的文字高度。</span><span class="sxs-lookup"><span data-stu-id="c8426-141">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="c8426-142">如果指定了 **DT \_ VCENTER** 或 **Dt \_ 底端**，則如果函式失敗，則傳回值是 *lprc* **頂端** 成員到所繪製文字底部的位移，而傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="c8426-142">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text If the function fails, the return value is zero.</span></span>

<span data-ttu-id="c8426-143">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="c8426-143">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="c8426-144">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="c8426-144">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8426-145">備註</span><span class="sxs-lookup"><span data-stu-id="c8426-145">Remarks</span></span>

<span data-ttu-id="c8426-146">**DrawTextWrap** 不會依名稱匯出，也不會在公用標頭中宣告。</span><span class="sxs-lookup"><span data-stu-id="c8426-146">**DrawTextWrap** is not exported by name or declared in a public header.</span></span> <span data-ttu-id="c8426-147">若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數415來取得函式指標。</span><span class="sxs-lookup"><span data-stu-id="c8426-147">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 415 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="c8426-148">如需其他備註，請參閱 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)。</span><span class="sxs-lookup"><span data-stu-id="c8426-148">For additional remarks, please see [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8426-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8426-149">Requirements</span></span>



| <span data-ttu-id="c8426-150">需求</span><span class="sxs-lookup"><span data-stu-id="c8426-150">Requirement</span></span> | <span data-ttu-id="c8426-151">值</span><span class="sxs-lookup"><span data-stu-id="c8426-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8426-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8426-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c8426-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8426-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="c8426-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8426-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c8426-155">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8426-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8426-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c8426-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8426-157"><dt>Comctl32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="c8426-157"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

