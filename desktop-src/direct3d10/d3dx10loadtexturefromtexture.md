---
description: 從材質載入紋理。
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: 'D3DX10LoadTextureFromTexture 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322751"
---
# <a name="d3dx10loadtexturefromtexture-function"></a><span data-ttu-id="c4727-103">D3DX10LoadTextureFromTexture 函式</span><span class="sxs-lookup"><span data-stu-id="c4727-103">D3DX10LoadTextureFromTexture function</span></span>

<span data-ttu-id="c4727-104">從材質載入紋理。</span><span class="sxs-lookup"><span data-stu-id="c4727-104">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4727-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4727-105">Syntax</span></span>


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c4727-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4727-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4727-107">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="c4727-107">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="c4727-108">類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="c4727-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="c4727-109">來源紋理的指標。</span><span class="sxs-lookup"><span data-stu-id="c4727-109">Pointer to the source texture.</span></span> <span data-ttu-id="c4727-110">請參閱 [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。</span><span class="sxs-lookup"><span data-stu-id="c4727-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="c4727-111">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="c4727-111">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c4727-112">類型： **[ **D3DX10 \_ 材質 \_ 載入 \_ 資訊**](d3dx10-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4727-112">Type: **[**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md)\***</span></span>

<span data-ttu-id="c4727-113">材質載入參數的指標。</span><span class="sxs-lookup"><span data-stu-id="c4727-113">Pointer to texture loading parameters.</span></span> <span data-ttu-id="c4727-114">請參閱 [**D3DX10 \_ 材質 \_ 載入 \_ 資訊**](d3dx10-texture-load-info.md)。</span><span class="sxs-lookup"><span data-stu-id="c4727-114">See [**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4727-115">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="c4727-115">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="c4727-116">類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="c4727-116">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="c4727-117">目的地材質的指標。</span><span class="sxs-lookup"><span data-stu-id="c4727-117">Pointer to the destination texture.</span></span> <span data-ttu-id="c4727-118">請參閱 [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。</span><span class="sxs-lookup"><span data-stu-id="c4727-118">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4727-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4727-119">Return value</span></span>

<span data-ttu-id="c4727-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4727-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4727-121">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c4727-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4727-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4727-122">Requirements</span></span>



| <span data-ttu-id="c4727-123">需求</span><span class="sxs-lookup"><span data-stu-id="c4727-123">Requirement</span></span> | <span data-ttu-id="c4727-124">值</span><span class="sxs-lookup"><span data-stu-id="c4727-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4727-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c4727-125">Header</span></span><br/> | <dl> <span data-ttu-id="c4727-126"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4727-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4727-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4727-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4727-128">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="c4727-128">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




