---
description: 設定適用于所有 sprite 的視圖轉換。
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'ID3DX10Sprite：： SetViewTransform 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988627"
---
# <a name="id3dx10spritesetviewtransform-method"></a><span data-ttu-id="90c9e-103">ID3DX10Sprite：： SetViewTransform 方法</span><span class="sxs-lookup"><span data-stu-id="90c9e-103">ID3DX10Sprite::SetViewTransform method</span></span>

<span data-ttu-id="90c9e-104">設定適用于所有 sprite 的視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="90c9e-104">Set the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="90c9e-105">Syntax</span></span>


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="90c9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="90c9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c9e-107">*pViewTransform* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90c9e-107">*pViewTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90c9e-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="90c9e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="90c9e-109">D3DXMATRIX 的指標，其中包含原始世界空間中 sprite 的轉換。</span><span class="sxs-lookup"><span data-stu-id="90c9e-109">Pointer to a D3DXMATRIX that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="90c9e-110">您可以使用此轉換來調整、旋轉或轉換 sprite。</span><span class="sxs-lookup"><span data-stu-id="90c9e-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90c9e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="90c9e-111">Return value</span></span>

<span data-ttu-id="90c9e-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90c9e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90c9e-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="90c9e-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="90c9e-114">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="90c9e-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="90c9e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="90c9e-115">Requirements</span></span>



| <span data-ttu-id="90c9e-116">需求</span><span class="sxs-lookup"><span data-stu-id="90c9e-116">Requirement</span></span> | <span data-ttu-id="90c9e-117">值</span><span class="sxs-lookup"><span data-stu-id="90c9e-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90c9e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="90c9e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="90c9e-119"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="90c9e-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="90c9e-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="90c9e-120">Library</span></span><br/> | <dl> <span data-ttu-id="90c9e-121"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="90c9e-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90c9e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90c9e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c9e-123">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="90c9e-123">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="90c9e-124">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="90c9e-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
