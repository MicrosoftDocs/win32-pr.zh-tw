---
description: 設定每個材質的 (u，v) 材質座標。
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: 'ID3DXTextureGutterHelper：： SetTexelMap 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee00394e81dadf147d54dffe0dc02199b2274e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106974884"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a><span data-ttu-id="cd6db-103">ID3DXTextureGutterHelper：： SetTexelMap 方法</span><span class="sxs-lookup"><span data-stu-id="cd6db-103">ID3DXTextureGutterHelper::SetTexelMap method</span></span>

<span data-ttu-id="cd6db-104">設定每個材質的 (u，v) 材質座標。</span><span class="sxs-lookup"><span data-stu-id="cd6db-104">Sets the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd6db-105">語法</span><span class="sxs-lookup"><span data-stu-id="cd6db-105">Syntax</span></span>


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="cd6db-106">參數</span><span class="sxs-lookup"><span data-stu-id="cd6db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd6db-107">*pTexelData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd6db-107">*pTexelData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd6db-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd6db-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="cd6db-109">以圖元為單位的位置指標 (u，v) 材質座標（每個材質所在位置）。</span><span class="sxs-lookup"><span data-stu-id="cd6db-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd6db-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd6db-110">Return value</span></span>

<span data-ttu-id="cd6db-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd6db-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd6db-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="cd6db-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cd6db-113">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="cd6db-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6db-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd6db-114">Requirements</span></span>



| <span data-ttu-id="cd6db-115">需求</span><span class="sxs-lookup"><span data-stu-id="cd6db-115">Requirement</span></span> | <span data-ttu-id="cd6db-116">值</span><span class="sxs-lookup"><span data-stu-id="cd6db-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6db-117">標頭</span><span class="sxs-lookup"><span data-stu-id="cd6db-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cd6db-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd6db-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cd6db-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd6db-119">Library</span></span><br/> | <dl> <span data-ttu-id="cd6db-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd6db-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd6db-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd6db-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6db-122">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="cd6db-122">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




