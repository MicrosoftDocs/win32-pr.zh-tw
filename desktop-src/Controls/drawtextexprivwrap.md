---
title: DrawTextExPrivWrap 函式
description: 在指定的矩形中繪製格式化的文字。 此函數會包裝對 DrawTextEx 的呼叫。
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- DrawTextExPrivWrap 函式 Windows 控制項
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935097"
---
# <a name="drawtextexprivwrap-function"></a><span data-ttu-id="3ae42-105">DrawTextExPrivWrap 函式</span><span class="sxs-lookup"><span data-stu-id="3ae42-105">DrawTextExPrivWrap function</span></span>

<span data-ttu-id="3ae42-106">\[**DrawTextExPrivWrap** 可透過 Windows XP Service Pack 2 (SP2) 取得。</span><span class="sxs-lookup"><span data-stu-id="3ae42-106">\[**DrawTextExPrivWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="3ae42-107">它可能會在後續版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="3ae42-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3ae42-108">建議您改為直接使用 [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) 。\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-108">It is recommended to use [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directly instead.\]</span></span>

<span data-ttu-id="3ae42-109">在指定的矩形中繪製格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="3ae42-109">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="3ae42-110">此函數會包裝對 [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3ae42-110">This function wraps a call to [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae42-111">語法</span><span class="sxs-lookup"><span data-stu-id="3ae42-111">Syntax</span></span>


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="3ae42-112">參數</span><span class="sxs-lookup"><span data-stu-id="3ae42-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ae42-113">*hdc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae42-114">類型： **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ae42-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ae42-115">要在其中繪製的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="3ae42-115">A handle to the device context in which to draw.</span></span>

</dd> <dt>

<span data-ttu-id="3ae42-116">*lpchText* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-116">*lpchText* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae42-117">類型： **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ae42-117">Type: **[**LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ae42-118">包含要繪製之文字的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="3ae42-118">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="3ae42-119">如果 *cchText* 參數為-1，則字串必須以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="3ae42-119">If the *cchText* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="3ae42-120">如果 *dwDTFormat* 包含 DT \_ MODIFYSTRING，此函式最多可能會在此字串中加上四個額外的字元。</span><span class="sxs-lookup"><span data-stu-id="3ae42-120">If *dwDTFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="3ae42-121">包含字串的緩衝區必須夠大，才能容納這些額外的字元。</span><span class="sxs-lookup"><span data-stu-id="3ae42-121">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="3ae42-122">*cchText* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-122">*cchText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae42-123">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="3ae42-123">Type: **int**</span></span>

<span data-ttu-id="3ae42-124">*LpchText* 所指向之字串的長度。</span><span class="sxs-lookup"><span data-stu-id="3ae42-124">The length of the string pointed to by *lpchText*.</span></span> <span data-ttu-id="3ae42-125">如果 *cchText* 為-1，則會假設 *lpchText* 參數是以 null 終止之字串的指標，而 [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) 會自動計算字元計數。</span><span class="sxs-lookup"><span data-stu-id="3ae42-125">If *cchText* is -1, then the *lpchText* parameter is assumed to be a pointer to a null-terminated string and [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="3ae42-126">*lprc* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-126">*lprc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae42-127">類型： **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="3ae42-127">Type: **LPRECT**</span></span>

<span data-ttu-id="3ae42-128">[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，其中包含要格式化文字的矩形（以邏輯座標表示）。</span><span class="sxs-lookup"><span data-stu-id="3ae42-128">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="3ae42-129">*dwDTFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-129">*dwDTFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae42-130">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ae42-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ae42-131">格式化選項。</span><span class="sxs-lookup"><span data-stu-id="3ae42-131">The formatting options.</span></span> <span data-ttu-id="3ae42-132">如需完整的選項清單，請參閱 [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) 檔。</span><span class="sxs-lookup"><span data-stu-id="3ae42-132">See the documentation for [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="3ae42-133">*lpDTParams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-133">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae42-134">類型： **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="3ae42-134">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="3ae42-135">[**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams)結構的指標，指定其他格式化選項。</span><span class="sxs-lookup"><span data-stu-id="3ae42-135">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="3ae42-136">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3ae42-136">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ae42-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ae42-137">Return value</span></span>

<span data-ttu-id="3ae42-138">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="3ae42-138">Type: **int**</span></span>

<span data-ttu-id="3ae42-139">如果函式成功，則傳回值為邏輯單元中的文字高度。</span><span class="sxs-lookup"><span data-stu-id="3ae42-139">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="3ae42-140">如果指定了 **DT \_ VCENTER** 或 **dt \_ 底端**，則傳回值會是從 *lprc* **頂端** 成員到所繪製文字底部的位移。</span><span class="sxs-lookup"><span data-stu-id="3ae42-140">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text.</span></span>

<span data-ttu-id="3ae42-141">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="3ae42-141">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="3ae42-142">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="3ae42-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ae42-143">備註</span><span class="sxs-lookup"><span data-stu-id="3ae42-143">Remarks</span></span>

<span data-ttu-id="3ae42-144">**DrawTextExPrivWrap** 不會依名稱匯出，也不會在公用標頭檔中宣告。</span><span class="sxs-lookup"><span data-stu-id="3ae42-144">**DrawTextExPrivWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="3ae42-145">若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數416來取得函式指標。</span><span class="sxs-lookup"><span data-stu-id="3ae42-145">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 416 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="3ae42-146">如需其他備註，請參閱 [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa)。</span><span class="sxs-lookup"><span data-stu-id="3ae42-146">For additional remarks, please see [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae42-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ae42-147">Requirements</span></span>



| <span data-ttu-id="3ae42-148">需求</span><span class="sxs-lookup"><span data-stu-id="3ae42-148">Requirement</span></span> | <span data-ttu-id="3ae42-149">值</span><span class="sxs-lookup"><span data-stu-id="3ae42-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae42-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ae42-150">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae42-151">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-151">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="3ae42-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ae42-152">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae42-153">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ae42-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ae42-154">DLL</span><span class="sxs-lookup"><span data-stu-id="3ae42-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae42-155"><dt>Comctl32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3ae42-155"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

