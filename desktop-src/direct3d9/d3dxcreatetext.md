---
description: 使用與裝置內容相關聯的字型，建立包含指定文字的網格。
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: 'D3DXCreateText 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993883"
---
# <a name="d3dxcreatetext-function"></a><span data-ttu-id="f2bc2-103">D3DXCreateText 函式</span><span class="sxs-lookup"><span data-stu-id="f2bc2-103">D3DXCreateText function</span></span>

<span data-ttu-id="f2bc2-104">使用與裝置內容相關聯的字型，建立包含指定文字的網格。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-104">Creates a mesh containing the specified text, using the font associated with the device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bc2-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2bc2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="f2bc2-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2bc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2bc2-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2bc2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bc2-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f2bc2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f2bc2-109">建立網格之裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-109">Pointer to the device that created the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f2bc2-110">*hDC* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2bc2-110">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bc2-111">類型： **HDC**</span><span class="sxs-lookup"><span data-stu-id="f2bc2-111">Type: **HDC**</span></span>

<span data-ttu-id="f2bc2-112">裝置內容，包含輸出的字型。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-112">Device context, containing the font for output.</span></span> <span data-ttu-id="f2bc2-113">裝置內容所選取的字型必須是 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-113">The font selected by the device context must be a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="f2bc2-114">*pText* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2bc2-114">*pText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bc2-115">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2bc2-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2bc2-116">字串的指標，指定要產生的文字。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-116">Pointer to a string that specifies the text to generate.</span></span> <span data-ttu-id="f2bc2-117">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f2bc2-118">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-118">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="f2bc2-119">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f2bc2-120">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2bc2-120">*Deviation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bc2-121">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2bc2-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2bc2-122">TrueType 字型大綱的最大 chordal 偏差。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-122">Maximum chordal deviation from TrueType font outlines.</span></span>

</dd> <dt>

<span data-ttu-id="f2bc2-123">*延伸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2bc2-123">*Extrusion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bc2-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2bc2-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2bc2-125">要以負 z 方向凸出的文字數量。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-125">Amount to extrude text in the negative z-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f2bc2-126">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f2bc2-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bc2-127">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2bc2-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="f2bc2-128">傳回之網格的指標。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-128">Pointer to the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f2bc2-129">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f2bc2-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bc2-130">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2bc2-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f2bc2-131">包含相鄰資訊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-131">Pointer to a buffer containing adjacency information.</span></span> <span data-ttu-id="f2bc2-132">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-132">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f2bc2-133">*pGlyphMetrics* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f2bc2-133">*pGlyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bc2-134">類型： **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span><span class="sxs-lookup"><span data-stu-id="f2bc2-134">Type: **[**LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span></span>

<span data-ttu-id="f2bc2-135">[**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)結構陣列的指標，其中包含圖像度量資料。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-135">Pointer to an array of [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) structures that contain the glyph metric data.</span></span> <span data-ttu-id="f2bc2-136">每個元素都包含字串中相對應圖像的位置和方向的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-136">Each element contains information about the position and orientation of the corresponding glyph in the string.</span></span> <span data-ttu-id="f2bc2-137">陣列中的元素數目應等於字串中的字元數。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-137">The number of elements in the array should be equal to the number of characters in the string.</span></span> <span data-ttu-id="f2bc2-138">請注意，每個結構中的原點都不是相對於整個字串，而是相對於該字元儲存格。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-138">Note that the origin in each structure is not relative to the entire string, but rather is relative to that character cell.</span></span> <span data-ttu-id="f2bc2-139">若要計算整個周框方塊，請在往返字串時加入每個圖像的遞增。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-139">To compute the entire bounding box, add the increment for each glyph while traversing the string.</span></span> <span data-ttu-id="f2bc2-140">如果您不在意圖像大小，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-140">If you are not concerned with the glyph sizes, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2bc2-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2bc2-141">Return value</span></span>

<span data-ttu-id="f2bc2-142">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2bc2-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2bc2-143">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2bc2-144">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2bc2-145">備註</span><span class="sxs-lookup"><span data-stu-id="f2bc2-145">Remarks</span></span>

<span data-ttu-id="f2bc2-146">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f2bc2-147">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateTextW。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-147">If Unicode is defined, the function call resolves to D3DXCreateTextW.</span></span> <span data-ttu-id="f2bc2-148">否則，函式呼叫會解析為 D3DXCreateTextA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-148">Otherwise, the function call resolves to D3DXCreateTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="f2bc2-149">此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="f2bc2-149">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bc2-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2bc2-150">Requirements</span></span>



| <span data-ttu-id="f2bc2-151">需求</span><span class="sxs-lookup"><span data-stu-id="f2bc2-151">Requirement</span></span> | <span data-ttu-id="f2bc2-152">值</span><span class="sxs-lookup"><span data-stu-id="f2bc2-152">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bc2-153">標頭</span><span class="sxs-lookup"><span data-stu-id="f2bc2-153">Header</span></span><br/>  | <dl> <span data-ttu-id="f2bc2-154"><dt>D3dx9shape。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2bc2-154"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="f2bc2-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2bc2-155">Library</span></span><br/> | <dl> <span data-ttu-id="f2bc2-156"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2bc2-156"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f2bc2-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2bc2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2bc2-158">圖形繪圖函數</span><span class="sxs-lookup"><span data-stu-id="f2bc2-158">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
