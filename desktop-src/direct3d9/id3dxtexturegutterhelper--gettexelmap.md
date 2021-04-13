---
description: 抓取每個材質的 (u，v) 材質座標。
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'ID3DXTextureGutterHelper：： GetTexelMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322976"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a><span data-ttu-id="16260-103">ID3DXTextureGutterHelper：： GetTexelMap 方法</span><span class="sxs-lookup"><span data-stu-id="16260-103">ID3DXTextureGutterHelper::GetTexelMap method</span></span>

<span data-ttu-id="16260-104">抓取每個材質的 (u，v) 材質座標。</span><span class="sxs-lookup"><span data-stu-id="16260-104">Retrieves the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="16260-105">語法</span><span class="sxs-lookup"><span data-stu-id="16260-105">Syntax</span></span>


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="16260-106">參數</span><span class="sxs-lookup"><span data-stu-id="16260-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16260-107">*pTexelData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16260-107">*pTexelData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16260-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="16260-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="16260-109">以圖元為單位的位置指標 (u，v) 材質座標（每個材質所在位置）。</span><span class="sxs-lookup"><span data-stu-id="16260-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16260-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="16260-110">Return value</span></span>

<span data-ttu-id="16260-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16260-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16260-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="16260-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="16260-113">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="16260-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="16260-114">備註</span><span class="sxs-lookup"><span data-stu-id="16260-114">Remarks</span></span>

<span data-ttu-id="16260-115">針對 [**類別2和4材質**](id3dxtexturegutterhelper.md)，傳回的 (u，v) 材質座標會對應到最接近的三角形上最接近的點。</span><span class="sxs-lookup"><span data-stu-id="16260-115">For [**class 2 and 4 texels**](id3dxtexturegutterhelper.md), the returned (u, v) texture coordinates correspond to the closest point on the closest triangle.</span></span>

<span data-ttu-id="16260-116">應用程式必須配置並管理 pTexelData。</span><span class="sxs-lookup"><span data-stu-id="16260-116">The application must allocate and manage pTexelData.</span></span>

## <a name="requirements"></a><span data-ttu-id="16260-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="16260-117">Requirements</span></span>



| <span data-ttu-id="16260-118">需求</span><span class="sxs-lookup"><span data-stu-id="16260-118">Requirement</span></span> | <span data-ttu-id="16260-119">值</span><span class="sxs-lookup"><span data-stu-id="16260-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16260-120">標頭</span><span class="sxs-lookup"><span data-stu-id="16260-120">Header</span></span><br/>  | <dl> <span data-ttu-id="16260-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="16260-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="16260-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="16260-122">Library</span></span><br/> | <dl> <span data-ttu-id="16260-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16260-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16260-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16260-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16260-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="16260-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




