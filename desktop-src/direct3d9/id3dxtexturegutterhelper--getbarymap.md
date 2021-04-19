---
description: 抓取材質 barycentric 座標。
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'ID3DXTextureGutterHelper：： GetBaryMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991968"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a><span data-ttu-id="d4f39-103">ID3DXTextureGutterHelper：： GetBaryMap 方法</span><span class="sxs-lookup"><span data-stu-id="d4f39-103">ID3DXTextureGutterHelper::GetBaryMap method</span></span>

<span data-ttu-id="d4f39-104">抓取材質 barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="d4f39-104">Retrieves texel barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f39-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4f39-105">Syntax</span></span>


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a><span data-ttu-id="d4f39-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4f39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f39-107">*pBaryData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d4f39-107">*pBaryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f39-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4f39-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4f39-109">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，其中包含每個材質的前兩個 barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="d4f39-109">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that contains the first two barycentric coordinates of each texel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f39-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4f39-110">Return value</span></span>

<span data-ttu-id="d4f39-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4f39-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4f39-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d4f39-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4f39-113">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="d4f39-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="d4f39-114">備註</span><span class="sxs-lookup"><span data-stu-id="d4f39-114">Remarks</span></span>

<span data-ttu-id="d4f39-115">第三個 barycentric 座標是由下列各項所提供：</span><span class="sxs-lookup"><span data-stu-id="d4f39-115">The third barycentric coordinate is given by:</span></span>


```
    1 - ( pBaryData.x + pBaryData.y )
```



<span data-ttu-id="d4f39-116">相對於 [**ID3DXTextureGutterHelper：： GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)所傳回的三角形，一律會指定 Barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="d4f39-116">Barycentric coordinates are always specified with respect to the triangle returned by [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).</span></span>

<span data-ttu-id="d4f39-117">這個方法所傳回的 barycentric 座標僅適用于有效的 (非類別 0) 材質。</span><span class="sxs-lookup"><span data-stu-id="d4f39-117">The barycentric coordinates returned by this method are valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="d4f39-118">[**ID3DXTextureGutterHelper：： GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) 會針對有效的材質傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d4f39-118">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid texels.</span></span>

<span data-ttu-id="d4f39-119">[**類別2材質**](id3dxtexturegutterhelper.md) 會對應到材質空間中三角形的最接近點。</span><span class="sxs-lookup"><span data-stu-id="d4f39-119">[**Class 2 texels**](id3dxtexturegutterhelper.md) are mapped to the nearest point on the triangle in texel space.</span></span>

<span data-ttu-id="d4f39-120">應用程式必須配置並管理 pBaryData。</span><span class="sxs-lookup"><span data-stu-id="d4f39-120">The application must allocate and manage pBaryData.</span></span>

<span data-ttu-id="d4f39-121">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="d4f39-121">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="d4f39-122">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="d4f39-122">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f39-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4f39-123">Requirements</span></span>



| <span data-ttu-id="d4f39-124">需求</span><span class="sxs-lookup"><span data-stu-id="d4f39-124">Requirement</span></span> | <span data-ttu-id="d4f39-125">值</span><span class="sxs-lookup"><span data-stu-id="d4f39-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f39-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d4f39-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d4f39-127"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f39-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d4f39-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4f39-128">Library</span></span><br/> | <dl> <span data-ttu-id="d4f39-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4f39-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4f39-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4f39-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f39-131">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="d4f39-131">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




