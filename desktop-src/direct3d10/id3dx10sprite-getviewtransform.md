---
description: 取得套用至所有 sprite 的視圖轉換。
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'ID3DX10Sprite：： GetViewTransform 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976754"
---
# <a name="id3dx10spritegetviewtransform-method"></a><span data-ttu-id="68397-103">ID3DX10Sprite：： GetViewTransform 方法</span><span class="sxs-lookup"><span data-stu-id="68397-103">ID3DX10Sprite::GetViewTransform method</span></span>

<span data-ttu-id="68397-104">取得套用至所有 sprite 的視圖轉換。</span><span class="sxs-lookup"><span data-stu-id="68397-104">Get the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="68397-105">語法</span><span class="sxs-lookup"><span data-stu-id="68397-105">Syntax</span></span>


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="68397-106">參數</span><span class="sxs-lookup"><span data-stu-id="68397-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68397-107">*pViewTransform* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="68397-107">*pViewTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68397-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="68397-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="68397-109">[**D3DX10MATRIX**](d3d10-d3dxmatrix.md)的指標，該指標將設定為原始世界空間中的 sprite 轉換。</span><span class="sxs-lookup"><span data-stu-id="68397-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68397-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="68397-110">Return value</span></span>

<span data-ttu-id="68397-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68397-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68397-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="68397-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="68397-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="68397-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="68397-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="68397-114">Requirements</span></span>



| <span data-ttu-id="68397-115">需求</span><span class="sxs-lookup"><span data-stu-id="68397-115">Requirement</span></span> | <span data-ttu-id="68397-116">值</span><span class="sxs-lookup"><span data-stu-id="68397-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68397-117">標頭</span><span class="sxs-lookup"><span data-stu-id="68397-117">Header</span></span><br/>  | <dl> <span data-ttu-id="68397-118"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="68397-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="68397-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="68397-119">Library</span></span><br/> | <dl> <span data-ttu-id="68397-120"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68397-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68397-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68397-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68397-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="68397-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="68397-123">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="68397-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
