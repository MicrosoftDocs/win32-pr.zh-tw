---
title: ExtTextOutWrap 函式
description: 使用目前選取的字型、背景色彩和文字色彩來繪製文字。 您可以選擇性地提供要用於剪切、不透明度或兩者的維度。 此函數會包裝對 ExtTextOut 的呼叫。
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- ExtTextOutWrap 函式 Windows 控制項
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093927"
---
# <a name="exttextoutwrap-function"></a><span data-ttu-id="5c762-106">ExtTextOutWrap 函式</span><span class="sxs-lookup"><span data-stu-id="5c762-106">ExtTextOutWrap function</span></span>

<span data-ttu-id="5c762-107">\[**ExtTextOutWrap** 可透過 Windows XP Service Pack 2 (SP2) 取得。</span><span class="sxs-lookup"><span data-stu-id="5c762-107">\[**ExtTextOutWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="5c762-108">它可能會在後續版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5c762-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5c762-109">建議您改為直接使用 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) 。\]</span><span class="sxs-lookup"><span data-stu-id="5c762-109">It is recommended to use [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directly instead.\]</span></span>

<span data-ttu-id="5c762-110">使用目前選取的字型、背景色彩和文字色彩來繪製文字。</span><span class="sxs-lookup"><span data-stu-id="5c762-110">Draws text using the currently selected font, background color, and text color.</span></span> <span data-ttu-id="5c762-111">您可以選擇性地提供要用於剪切、不透明度或兩者的維度。</span><span class="sxs-lookup"><span data-stu-id="5c762-111">You can optionally provide dimensions to be used for clipping, opacity, or both.</span></span> <span data-ttu-id="5c762-112">此函數會包裝對 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="5c762-112">This function wraps a call to [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c762-113">語法</span><span class="sxs-lookup"><span data-stu-id="5c762-113">Syntax</span></span>


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a><span data-ttu-id="5c762-114">參數</span><span class="sxs-lookup"><span data-stu-id="5c762-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c762-115">*hdc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c762-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c762-116">類型： **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c762-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c762-117">裝置內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5c762-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="5c762-118">*X* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="5c762-118">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c762-119">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="5c762-119">Type: **int**</span></span>

<span data-ttu-id="5c762-120">用來定位字串之參考點的 x 座標（以邏輯座標表示）。</span><span class="sxs-lookup"><span data-stu-id="5c762-120">The x-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="5c762-121">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c762-121">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c762-122">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="5c762-122">Type: **int**</span></span>

<span data-ttu-id="5c762-123">用來放置字串的參考點的 y 座標（以邏輯座標表示）。</span><span class="sxs-lookup"><span data-stu-id="5c762-123">The y-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="5c762-124">*uOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c762-124">*uOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c762-125">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c762-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c762-126">值，指定如何使用應用程式定義的矩形。</span><span class="sxs-lookup"><span data-stu-id="5c762-126">Values that specify how to use the application-defined rectangle.</span></span> <span data-ttu-id="5c762-127">如需完整的選項清單，請參閱 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) 。</span><span class="sxs-lookup"><span data-stu-id="5c762-127">See [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="5c762-128">*lprc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c762-128">*lprc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c762-129">類型： \**Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="5c762-129">Type: \**const [**RECT**](/previous-versions//dd162897(v=vs.85))\** _</span></span>

<span data-ttu-id="5c762-130">選擇性 [_ *RECT* \*](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會指定用於裁剪、不透明度或兩者之矩形的維度（以邏輯座標表示）。</span><span class="sxs-lookup"><span data-stu-id="5c762-130">A pointer to an optional [_ *RECT*\*](/previous-versions//dd162897(v=vs.85)) structure that specifies the dimensions, in logical coordinates, of a rectangle that is used for clipping, opacity, or both.</span></span>

</dd> <dt>

<span data-ttu-id="5c762-131">*lpString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c762-131">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c762-132">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c762-132">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c762-133">包含要繪製之文字的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="5c762-133">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="5c762-134">字串不需要以零結束，因為 *cbCount* 會指定字串的長度。</span><span class="sxs-lookup"><span data-stu-id="5c762-134">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="5c762-135">*cbCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c762-135">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c762-136">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c762-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c762-137">*LpString* 所指向的字串長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c762-137">The length of the string, in bytes, pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="5c762-138">*lpDx* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c762-138">*lpDx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c762-139">類型： \**Const [**INT**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="5c762-139">Type: \**const [**INT**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="5c762-140">值的選擇性陣列指標，表示相鄰字元資料格來源之間的距離。</span><span class="sxs-lookup"><span data-stu-id="5c762-140">A pointer to an optional array of values that indicate the distance between origins of adjacent character cells.</span></span> <span data-ttu-id="5c762-141">例如，_lpDx \* \[ x \] 邏輯單元分隔字元資料格 x 和字元資料格的來源 (x + 1) 。</span><span class="sxs-lookup"><span data-stu-id="5c762-141">For example, _lpDx\*\[x\] logical units separate the origins of character cell x and character cell (x + 1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c762-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c762-142">Return value</span></span>

<span data-ttu-id="5c762-143">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c762-143">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c762-144">如果成功繪製字串，則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="5c762-144">Returns a nonzero value if the string is drawn successfully.</span></span> <span data-ttu-id="5c762-145">但是，如果 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) 的 ANSI 版本是以 ETO 圖像索引來呼叫 \_ ，則函式會傳回 \_ **TRUE** ，即使函數沒有任何作用也一樣。</span><span class="sxs-lookup"><span data-stu-id="5c762-145">However, if the ANSI version of [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) is called with ETO\_GLYPH\_INDEX, the function returns **TRUE** even though the function does nothing.</span></span>

<span data-ttu-id="5c762-146">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="5c762-146">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="5c762-147">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="5c762-147">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c762-148">備註</span><span class="sxs-lookup"><span data-stu-id="5c762-148">Remarks</span></span>

<span data-ttu-id="5c762-149">**ExtTextOutWrap** 不會依名稱匯出，也不會在公用標頭檔中宣告。</span><span class="sxs-lookup"><span data-stu-id="5c762-149">**ExtTextOutWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="5c762-150">若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數417來取得函式指標。</span><span class="sxs-lookup"><span data-stu-id="5c762-150">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 417 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="5c762-151">如需其他備註，請參閱 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)。</span><span class="sxs-lookup"><span data-stu-id="5c762-151">For additional remarks, please see [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c762-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c762-152">Requirements</span></span>



| <span data-ttu-id="5c762-153">需求</span><span class="sxs-lookup"><span data-stu-id="5c762-153">Requirement</span></span> | <span data-ttu-id="5c762-154">值</span><span class="sxs-lookup"><span data-stu-id="5c762-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c762-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c762-155">Minimum supported client</span></span><br/> | <span data-ttu-id="5c762-156">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c762-156">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="5c762-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c762-157">Minimum supported server</span></span><br/> | <span data-ttu-id="5c762-158">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c762-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5c762-159">DLL</span><span class="sxs-lookup"><span data-stu-id="5c762-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c762-160"><dt>Comctl32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="5c762-160"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

