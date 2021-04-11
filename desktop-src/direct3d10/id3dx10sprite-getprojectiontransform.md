---
description: 取得套用至所有 sprite 的 sprite 投影矩陣。
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'ID3DX10Sprite：： GetProjectionTransform 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696864"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a><span data-ttu-id="54218-103">ID3DX10Sprite：： GetProjectionTransform 方法</span><span class="sxs-lookup"><span data-stu-id="54218-103">ID3DX10Sprite::GetProjectionTransform method</span></span>

<span data-ttu-id="54218-104">取得套用至所有 sprite 的 sprite 投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="54218-104">Get the sprite projection matrix that is applied to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="54218-105">語法</span><span class="sxs-lookup"><span data-stu-id="54218-105">Syntax</span></span>


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="54218-106">參數</span><span class="sxs-lookup"><span data-stu-id="54218-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54218-107">*pProjectionTransform* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="54218-107">*pProjectionTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54218-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="54218-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54218-109">將設定為 sprite 投射矩陣的 [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="54218-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the sprite's projection matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54218-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="54218-110">Return value</span></span>

<span data-ttu-id="54218-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="54218-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="54218-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="54218-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54218-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="54218-113">Requirements</span></span>



| <span data-ttu-id="54218-114">需求</span><span class="sxs-lookup"><span data-stu-id="54218-114">Requirement</span></span> | <span data-ttu-id="54218-115">值</span><span class="sxs-lookup"><span data-stu-id="54218-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54218-116">標頭</span><span class="sxs-lookup"><span data-stu-id="54218-116">Header</span></span><br/>  | <dl> <span data-ttu-id="54218-117"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="54218-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="54218-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="54218-118">Library</span></span><br/> | <dl> <span data-ttu-id="54218-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="54218-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54218-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54218-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54218-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="54218-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="54218-122">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="54218-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
