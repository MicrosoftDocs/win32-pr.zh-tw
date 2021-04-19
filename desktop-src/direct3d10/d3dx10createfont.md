---
description: 建立裝置和字型的字型物件。請注意，我們建議您不要使用這個函式，而是使用 DirectWrite 和 DirectXTK library SpriteFont 類別。
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: 'D3DX10CreateFont 函式 (D3DX10Core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975685"
---
# <a name="d3dx10createfont-function"></a><span data-ttu-id="b7090-103">D3DX10CreateFont 函式</span><span class="sxs-lookup"><span data-stu-id="b7090-103">D3DX10CreateFont function</span></span>

<span data-ttu-id="b7090-104">建立裝置和字型的字型物件。</span><span class="sxs-lookup"><span data-stu-id="b7090-104">Creates a font object for a device and font.</span></span>

> [!Note]  
> <span data-ttu-id="b7090-105">我們建議您不要使用這個函式，而是使用 [DirectWrite](../directwrite/direct-write-portal.md) 和 [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 **SpriteFont** 類別。</span><span class="sxs-lookup"><span data-stu-id="b7090-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b7090-106">語法</span><span class="sxs-lookup"><span data-stu-id="b7090-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="b7090-107">參數</span><span class="sxs-lookup"><span data-stu-id="b7090-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7090-108">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-109">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="b7090-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="b7090-110">ID3D10Device 介面的指標，與字型物件相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="b7090-110">Pointer to an ID3D10Device interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-111">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-111">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-112">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-113">邏輯單元中字元的高度。</span><span class="sxs-lookup"><span data-stu-id="b7090-113">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-114">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-116">邏輯單元中字元的寬度。</span><span class="sxs-lookup"><span data-stu-id="b7090-116">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-117">*權數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-117">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-119">字型權數。</span><span class="sxs-lookup"><span data-stu-id="b7090-119">Typeface weight.</span></span> <span data-ttu-id="b7090-120">其中一個範例是粗體。</span><span class="sxs-lookup"><span data-stu-id="b7090-120">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-121">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-121">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-123">Mipmap 層級的數目。</span><span class="sxs-lookup"><span data-stu-id="b7090-123">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-124">*斜體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-124">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-125">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-125">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-126">若為斜體字型，則為 True，否則為 false。</span><span class="sxs-lookup"><span data-stu-id="b7090-126">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-127">*字元集* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-127">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-128">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-129">字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="b7090-129">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-130">*OutputPrecision* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-130">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-131">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-132">指定 Windows 應該如何嘗試符合所需的字型大小和特性與實際字型。</span><span class="sxs-lookup"><span data-stu-id="b7090-132">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="b7090-133">\_ \_ 例如，只使用 OUT TT \_ PRECIS，以確保一律取得 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="b7090-133">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-134">*品質* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-134">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-135">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-136">指定 Windows 如何以真實字型符合所需的字型。</span><span class="sxs-lookup"><span data-stu-id="b7090-136">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="b7090-137">它只適用于點陣字型，不應該影響 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="b7090-137">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-138">*PitchAndFamily* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-138">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-139">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-139">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-140">音調和系列索引。</span><span class="sxs-lookup"><span data-stu-id="b7090-140">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-141">*pFaceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7090-141">*pFaceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-142">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7090-142">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7090-143">包含字樣名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="b7090-143">String containing the typeface name.</span></span> <span data-ttu-id="b7090-144">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="b7090-144">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b7090-145">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="b7090-145">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="b7090-146">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="b7090-146">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b7090-147">*ppFont* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b7090-147">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7090-148">類型： **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7090-148">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="b7090-149">傳回 ID3DX10Font 介面的指標，表示所建立的字型物件。</span><span class="sxs-lookup"><span data-stu-id="b7090-149">Returns a pointer to an ID3DX10Font interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7090-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7090-150">Return value</span></span>

<span data-ttu-id="b7090-151">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7090-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7090-152">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b7090-152">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b7090-153">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b7090-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7090-154">備註</span><span class="sxs-lookup"><span data-stu-id="b7090-154">Remarks</span></span>

<span data-ttu-id="b7090-155">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="b7090-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b7090-156">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateFontW。</span><span class="sxs-lookup"><span data-stu-id="b7090-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="b7090-157">否則，函式呼叫會解析為 D3DXCreateFontA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="b7090-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="b7090-158">如果您需要有關字型參數的詳細資訊，請參閱 [邏輯字型](/previous-versions//ms533985(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b7090-158">If you want more information about font parameters, see [The Logical Font](/previous-versions//ms533985(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7090-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7090-159">Requirements</span></span>



| <span data-ttu-id="b7090-160">需求</span><span class="sxs-lookup"><span data-stu-id="b7090-160">Requirement</span></span> | <span data-ttu-id="b7090-161">值</span><span class="sxs-lookup"><span data-stu-id="b7090-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7090-162">標頭</span><span class="sxs-lookup"><span data-stu-id="b7090-162">Header</span></span><br/>  | <dl> <span data-ttu-id="b7090-163"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7090-163"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="b7090-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7090-164">Library</span></span><br/> | <dl> <span data-ttu-id="b7090-165"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7090-165"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7090-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7090-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7090-167">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="b7090-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
