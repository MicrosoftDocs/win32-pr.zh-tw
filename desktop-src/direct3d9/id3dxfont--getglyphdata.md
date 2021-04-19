---
description: 傳回字元資料格中圖像位置和方向的相關資訊。
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'ID3DXFont：： GetGlyphData 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974856"
---
# <a name="id3dxfontgetglyphdata-method"></a><span data-ttu-id="d3e5e-103">ID3DXFont：： GetGlyphData 方法</span><span class="sxs-lookup"><span data-stu-id="d3e5e-103">ID3DXFont::GetGlyphData method</span></span>

<span data-ttu-id="d3e5e-104">傳回字元資料格中圖像位置和方向的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d3e5e-104">Returns information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e5e-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3e5e-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="d3e5e-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3e5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3e5e-107">圖像 \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3e5e-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e5e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3e5e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3e5e-109">字元識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3e5e-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d3e5e-110">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d3e5e-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e5e-111">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="d3e5e-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="d3e5e-112">包含圖像之 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="d3e5e-112">Address of a pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="d3e5e-113">*pBlackBox* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d3e5e-113">*pBlackBox* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e5e-114">類型： **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="d3e5e-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="d3e5e-115">完全括住圖像之最小矩形物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d3e5e-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="d3e5e-116">*pCellInc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d3e5e-116">*pCellInc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e5e-117">類型： **[ **POINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3e5e-117">Type: **[**POINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d3e5e-118">二維向量的指標，可將目前字元資料格的原點連接至下一個字元資料格的來源。</span><span class="sxs-lookup"><span data-stu-id="d3e5e-118">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="d3e5e-119">請參閱 [**點**](../winprog/windows-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d3e5e-119">See [**POINT**](../winprog/windows-data-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3e5e-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3e5e-120">Return value</span></span>

<span data-ttu-id="d3e5e-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3e5e-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3e5e-122">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d3e5e-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d3e5e-123">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="d3e5e-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e5e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3e5e-124">Requirements</span></span>



| <span data-ttu-id="d3e5e-125">需求</span><span class="sxs-lookup"><span data-stu-id="d3e5e-125">Requirement</span></span> | <span data-ttu-id="d3e5e-126">值</span><span class="sxs-lookup"><span data-stu-id="d3e5e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e5e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d3e5e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d3e5e-128"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e5e-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d3e5e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3e5e-129">Library</span></span><br/> | <dl> <span data-ttu-id="d3e5e-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3e5e-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3e5e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3e5e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e5e-132">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="d3e5e-132">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
