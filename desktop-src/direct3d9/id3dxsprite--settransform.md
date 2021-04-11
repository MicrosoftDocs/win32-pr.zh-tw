---
description: 設定 sprite 轉換。
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'ID3DXSprite：： SetTransform 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 316e7e2c68dfa8f25a712c2077ece03d09455050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196321"
---
# <a name="id3dxspritesettransform-method"></a><span data-ttu-id="9b7f2-103">ID3DXSprite：： SetTransform 方法</span><span class="sxs-lookup"><span data-stu-id="9b7f2-103">ID3DXSprite::SetTransform method</span></span>

<span data-ttu-id="9b7f2-104">設定 sprite 轉換。</span><span class="sxs-lookup"><span data-stu-id="9b7f2-104">Sets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b7f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="9b7f2-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="9b7f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b7f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b7f2-107">*pTransform* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b7f2-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b7f2-108">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9b7f2-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9b7f2-109">[**D3DXMATRIX**](d3dxmatrix.md)的指標，其中包含原始世界空間中 sprite 的轉換。</span><span class="sxs-lookup"><span data-stu-id="9b7f2-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="9b7f2-110">您可以使用此轉換來調整、旋轉或轉換 sprite。</span><span class="sxs-lookup"><span data-stu-id="9b7f2-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b7f2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b7f2-111">Return value</span></span>

<span data-ttu-id="9b7f2-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b7f2-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b7f2-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9b7f2-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9b7f2-114">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="9b7f2-114">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="9b7f2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b7f2-115">Requirements</span></span>



| <span data-ttu-id="9b7f2-116">需求</span><span class="sxs-lookup"><span data-stu-id="9b7f2-116">Requirement</span></span> | <span data-ttu-id="9b7f2-117">值</span><span class="sxs-lookup"><span data-stu-id="9b7f2-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7f2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="9b7f2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9b7f2-119"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b7f2-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9b7f2-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b7f2-120">Library</span></span><br/> | <dl> <span data-ttu-id="9b7f2-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b7f2-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b7f2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b7f2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b7f2-123">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="9b7f2-123">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="9b7f2-124">轉換 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="9b7f2-124">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




