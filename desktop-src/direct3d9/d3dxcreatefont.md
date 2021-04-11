---
description: 建立裝置和字型的字型物件。
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: 'D3DXCreateFont 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696739"
---
# <a name="d3dxcreatefont-function"></a><span data-ttu-id="5c4f2-103">D3DXCreateFont 函式</span><span class="sxs-lookup"><span data-stu-id="5c4f2-103">D3DXCreateFont function</span></span>

<span data-ttu-id="5c4f2-104">建立裝置和字型的字型物件。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-104">Creates a font object for a device and font.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c4f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c4f2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="5c4f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c4f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c4f2-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5c4f2-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與字型物件相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-110">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-111">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-111">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-112">邏輯單元中字元的高度。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-112">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-113">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-113">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-115">邏輯單元中字元的寬度。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-115">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-116">*權數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-116">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-118">字型權數。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-118">Typeface weight.</span></span> <span data-ttu-id="5c4f2-119">其中一個範例是粗體。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-119">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-120">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-122">Mipmap 層級的數目。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-122">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-123">*斜體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-123">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-124">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-124">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-125">若為斜體字型，則為 True，否則為 false。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-125">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-126">*字元集* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-126">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-127">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-128">字型的字元集。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-128">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-129">*OutputPrecision* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-129">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-130">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-131">指定 Windows 應該如何嘗試符合所需的字型大小和特性與實際字型。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-131">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="5c4f2-132">\_ \_ 例如，只使用 OUT TT \_ PRECIS，以確保一律取得 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-132">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-133">*品質* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-133">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-134">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-135">指定 Windows 如何以真實字型符合所需的字型。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-135">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="5c4f2-136">它只適用于點陣字型，不應該影響 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-136">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-137">*PitchAndFamily* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-137">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-138">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-139">音調和系列索引。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-139">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-140">*pFacename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-140">*pFacename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-141">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-141">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4f2-142">包含字樣名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-142">String containing the typeface name.</span></span> <span data-ttu-id="5c4f2-143">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-143">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5c4f2-144">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-144">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="5c4f2-145">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-145">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5c4f2-146">*ppFont* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5c4f2-146">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4f2-147">類型： **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c4f2-147">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="5c4f2-148">傳回 [**ID3DXFont**](id3dxfont.md) 介面的指標，表示所建立的字型物件。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-148">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c4f2-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c4f2-149">Return value</span></span>

<span data-ttu-id="5c4f2-150">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c4f2-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c4f2-151">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-151">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5c4f2-152">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-152">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c4f2-153">備註</span><span class="sxs-lookup"><span data-stu-id="5c4f2-153">Remarks</span></span>

<span data-ttu-id="5c4f2-154">建立 ID3DXFont 物件需要裝置支援32位色彩。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-154">The creation of an ID3DXFont object requires that the device supports 32-bit color.</span></span>

<span data-ttu-id="5c4f2-155">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="5c4f2-156">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateFontW。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="5c4f2-157">否則，函式呼叫會解析為 D3DXCreateFontA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="5c4f2-158">如果您需要有關字型參數的詳細資訊，請參閱 [邏輯字型](../gdi/creating-a-logical-font.md)。</span><span class="sxs-lookup"><span data-stu-id="5c4f2-158">If you want more information about font parameters, see [The Logical Font](../gdi/creating-a-logical-font.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c4f2-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c4f2-159">Requirements</span></span>



| <span data-ttu-id="5c4f2-160">需求</span><span class="sxs-lookup"><span data-stu-id="5c4f2-160">Requirement</span></span> | <span data-ttu-id="5c4f2-161">值</span><span class="sxs-lookup"><span data-stu-id="5c4f2-161">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4f2-162">標頭</span><span class="sxs-lookup"><span data-stu-id="5c4f2-162">Header</span></span><br/>  | <dl> <span data-ttu-id="5c4f2-163"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c4f2-163"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5c4f2-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="5c4f2-164">Library</span></span><br/> | <dl> <span data-ttu-id="5c4f2-165"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c4f2-165"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c4f2-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c4f2-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c4f2-167">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="5c4f2-167">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
