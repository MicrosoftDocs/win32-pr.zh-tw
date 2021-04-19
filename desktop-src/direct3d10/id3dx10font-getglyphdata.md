---
description: 傳回字元資料格中圖像位置和方向的相關資訊。
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'ID3DX10Font：： GetGlyphData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982032"
---
# <a name="id3dx10fontgetglyphdata-method"></a><span data-ttu-id="9b2a2-103">ID3DX10Font：： GetGlyphData 方法</span><span class="sxs-lookup"><span data-stu-id="9b2a2-103">ID3DX10Font::GetGlyphData method</span></span>

<span data-ttu-id="9b2a2-104">傳回字元資料格中圖像位置和方向的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-104">Return information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2a2-105">語法</span><span class="sxs-lookup"><span data-stu-id="9b2a2-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="9b2a2-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b2a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b2a2-107">圖像 \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b2a2-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2a2-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b2a2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b2a2-109">字元識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9b2a2-110">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9b2a2-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2a2-111">類型： **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="9b2a2-111">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="9b2a2-112">包含圖像之 ID3D10Texture 物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-112">Address of a pointer to a ID3D10Texture object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="9b2a2-113">*pBlackBox* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b2a2-113">*pBlackBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2a2-114">類型： **[ **RECT**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="9b2a2-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="9b2a2-115">完全括住圖像之最小矩形物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span> <span data-ttu-id="9b2a2-116">請參閱 [RECT](/previous-versions//ms536136(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-116">See [RECT](/previous-versions//ms536136(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9b2a2-117">*pCellInc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b2a2-117">*pCellInc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2a2-118">類型： **POINT \***</span><span class="sxs-lookup"><span data-stu-id="9b2a2-118">Type: **POINT\***</span></span>

<span data-ttu-id="9b2a2-119">二維向量的指標，可將目前字元資料格的原點連接至下一個字元資料格的來源。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-119">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="9b2a2-120">請參閱 [點](/previous-versions//ms536119(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-120">See [POINT](/previous-versions//ms536119(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b2a2-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b2a2-121">Return value</span></span>

<span data-ttu-id="9b2a2-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b2a2-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b2a2-123">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9b2a2-124">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="9b2a2-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b2a2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b2a2-125">Requirements</span></span>



| <span data-ttu-id="9b2a2-126">需求</span><span class="sxs-lookup"><span data-stu-id="9b2a2-126">Requirement</span></span> | <span data-ttu-id="9b2a2-127">值</span><span class="sxs-lookup"><span data-stu-id="9b2a2-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b2a2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9b2a2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9b2a2-129"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b2a2-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b2a2-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b2a2-130">Library</span></span><br/> | <dl> <span data-ttu-id="9b2a2-131"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b2a2-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b2a2-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b2a2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b2a2-133">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="9b2a2-133">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="9b2a2-134">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="9b2a2-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
