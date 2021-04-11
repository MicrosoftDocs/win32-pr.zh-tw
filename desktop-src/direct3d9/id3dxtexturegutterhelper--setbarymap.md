---
description: 設定材質 barycentric 座標。
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'ID3DXTextureGutterHelper：： SetBaryMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196402"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a><span data-ttu-id="87c33-103">ID3DXTextureGutterHelper：： SetBaryMap 方法</span><span class="sxs-lookup"><span data-stu-id="87c33-103">ID3DXTextureGutterHelper::SetBaryMap method</span></span>

<span data-ttu-id="87c33-104">設定材質 barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="87c33-104">Sets texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c33-105">語法</span><span class="sxs-lookup"><span data-stu-id="87c33-105">Syntax</span></span>


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="87c33-106">參數</span><span class="sxs-lookup"><span data-stu-id="87c33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c33-107">*pBaryData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87c33-107">*pBaryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c33-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="87c33-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="87c33-109">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，其中包含每個材質的前兩個 barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="87c33-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87c33-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="87c33-110">Return value</span></span>

<span data-ttu-id="87c33-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87c33-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87c33-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="87c33-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="87c33-113">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="87c33-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="87c33-114">備註</span><span class="sxs-lookup"><span data-stu-id="87c33-114">Remarks</span></span>

<span data-ttu-id="87c33-115">第三個 barycentric 座標是由下列各項所提供：</span><span class="sxs-lookup"><span data-stu-id="87c33-115">The third barycentric coordinate is given by:</span></span>


```
1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="87c33-116">Barycentric 會將輸入協調為此方法的輸入，僅適用于有效的 (非類別 0) 材質。</span><span class="sxs-lookup"><span data-stu-id="87c33-116">The barycentric coordinates input to this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="87c33-117">[**ID3DXTextureGutterHelper：： GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) 會針對有效的材質傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="87c33-117">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

<span data-ttu-id="87c33-118">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="87c33-118">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="87c33-119">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](http://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="87c33-119">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](http://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="87c33-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="87c33-120">Requirements</span></span>



| <span data-ttu-id="87c33-121">需求</span><span class="sxs-lookup"><span data-stu-id="87c33-121">Requirement</span></span> | <span data-ttu-id="87c33-122">值</span><span class="sxs-lookup"><span data-stu-id="87c33-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87c33-123">標頭</span><span class="sxs-lookup"><span data-stu-id="87c33-123">Header</span></span><br/>  | <dl> <span data-ttu-id="87c33-124"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="87c33-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="87c33-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="87c33-125">Library</span></span><br/> | <dl> <span data-ttu-id="87c33-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="87c33-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87c33-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87c33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c33-128">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="87c33-128">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




