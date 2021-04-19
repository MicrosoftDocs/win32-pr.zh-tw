---
description: 將 sprite 新增至批次 sprite 的清單。
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: 'ID3DXSprite：:D 原始方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982907"
---
# <a name="id3dxspritedraw-method"></a><span data-ttu-id="ab5d8-103">ID3DXSprite：:D 原始方法</span><span class="sxs-lookup"><span data-stu-id="ab5d8-103">ID3DXSprite::Draw method</span></span>

<span data-ttu-id="ab5d8-104">將 sprite 新增至批次 sprite 的清單。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-104">Adds a sprite to the list of batched sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab5d8-105">Syntax</span></span>


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a><span data-ttu-id="ab5d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab5d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab5d8-107">*pTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab5d8-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5d8-108">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="ab5d8-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="ab5d8-109">代表 sprite 材質之 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the sprite texture.</span></span>

</dd> <dt>

<span data-ttu-id="ab5d8-110">*pSrcRect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab5d8-110">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5d8-111">Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ab5d8-111">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ab5d8-112">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，表示要用於 sprite 的來源材質部分。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that indicates the portion of the source texture to use for the sprite.</span></span> <span data-ttu-id="ab5d8-113">如果此參數為 **Null**，則會使用整個來源影像作為 sprite。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-113">If this parameter is **NULL**, then the entire source image is used for the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="ab5d8-114">*pCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab5d8-114">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5d8-115">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ab5d8-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ab5d8-116">[**D3DXVECTOR3**](d3dxvector3.md)向量的指標，可識別 sprite 的中心。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the center of the sprite.</span></span> <span data-ttu-id="ab5d8-117">如果這個引數是 **Null**，則會使用點 (0、0、0) （左上角）。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-117">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="ab5d8-118">*pPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab5d8-118">*pPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5d8-119">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ab5d8-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ab5d8-120">[**D3DXVECTOR3**](d3dxvector3.md)向量的指標，可識別 sprite 的位置。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the position of the sprite.</span></span> <span data-ttu-id="ab5d8-121">如果這個引數是 **Null**，則會使用點 (0、0、0) （左上角）。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-121">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="ab5d8-122">*色彩* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab5d8-122">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab5d8-123">類型： **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ab5d8-123">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ab5d8-124">[**D3DCOLOR**](d3dcolor.md) 類型。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-124">[**D3DCOLOR**](d3dcolor.md) type.</span></span> <span data-ttu-id="ab5d8-125">色彩和 Alpha 通道會以這個值來調製。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-125">The color and alpha channels are modulated by this value.</span></span> <span data-ttu-id="ab5d8-126">0xFFFFFFFF 的值會維護原始來源色彩和 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-126">A value of 0xFFFFFFFF maintains the original source color and alpha data.</span></span> <span data-ttu-id="ab5d8-127">使用 [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) 宏來協助產生此色彩。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-127">Use the [**D3DCOLOR\_RGBA**](d3dcolor-rgba.md) macro to help generate this color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab5d8-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab5d8-128">Return value</span></span>

<span data-ttu-id="ab5d8-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab5d8-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab5d8-130">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ab5d8-131">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab5d8-132">備註</span><span class="sxs-lookup"><span data-stu-id="ab5d8-132">Remarks</span></span>

<span data-ttu-id="ab5d8-133">若要調整、旋轉或轉譯 sprite，請在呼叫 ID3DXSprite：:D raw 之前，以包含縮放、旋轉和轉譯 (SRT) 值的矩陣來呼叫 [**ID3DXSprite：： SetTransform**](id3dxsprite--settransform.md) 。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-133">To scale, rotate, or translate a sprite, call [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) with a matrix that contains the scale, rotate, and translate (SRT) values, before calling ID3DXSprite::Draw.</span></span> <span data-ttu-id="ab5d8-134">如需有關在矩陣中設定 SRT 值的詳細資訊，請參閱 [矩陣轉換](transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="ab5d8-134">For information about setting SRT values in a matrix, see [Matrix Transforms](transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab5d8-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab5d8-135">Requirements</span></span>



| <span data-ttu-id="ab5d8-136">需求</span><span class="sxs-lookup"><span data-stu-id="ab5d8-136">Requirement</span></span> | <span data-ttu-id="ab5d8-137">值</span><span class="sxs-lookup"><span data-stu-id="ab5d8-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5d8-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ab5d8-138">Header</span></span><br/>  | <dl> <span data-ttu-id="ab5d8-139"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab5d8-139"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ab5d8-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="ab5d8-140">Library</span></span><br/> | <dl> <span data-ttu-id="ab5d8-141"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab5d8-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab5d8-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab5d8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5d8-143">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="ab5d8-143">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="ab5d8-144">**ID3DXSprite::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="ab5d8-144">**ID3DXSprite::GetTransform**</span></span>](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
