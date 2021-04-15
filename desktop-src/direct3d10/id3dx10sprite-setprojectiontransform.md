---
description: 設定所有 sprite 的投射矩陣。
ms.assetid: cb4c5546-1a31-40d9-a943-af4fbddcee01
title: 'ID3DX10Sprite：： SetProjectionTransform 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c49fb570f87c8c86313e1f4adcf1560fee909433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514717"
---
# <a name="id3dx10spritesetprojectiontransform-method"></a><span data-ttu-id="67446-103">ID3DX10Sprite：： SetProjectionTransform 方法</span><span class="sxs-lookup"><span data-stu-id="67446-103">ID3DX10Sprite::SetProjectionTransform method</span></span>

<span data-ttu-id="67446-104">設定所有 sprite 的投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="67446-104">Set the projection matrix for all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="67446-105">語法</span><span class="sxs-lookup"><span data-stu-id="67446-105">Syntax</span></span>


```C++
HRESULT SetProjectionTransform(
  [in] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="67446-106">參數</span><span class="sxs-lookup"><span data-stu-id="67446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67446-107">*pProjectionTransform* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67446-107">*pProjectionTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67446-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="67446-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="67446-109">要用於所有 sprite 的投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="67446-109">The projection matrix to be used on all sprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67446-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="67446-110">Return value</span></span>

<span data-ttu-id="67446-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="67446-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="67446-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="67446-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67446-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="67446-113">Requirements</span></span>



| <span data-ttu-id="67446-114">需求</span><span class="sxs-lookup"><span data-stu-id="67446-114">Requirement</span></span> | <span data-ttu-id="67446-115">值</span><span class="sxs-lookup"><span data-stu-id="67446-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67446-116">標頭</span><span class="sxs-lookup"><span data-stu-id="67446-116">Header</span></span><br/>  | <dl> <span data-ttu-id="67446-117"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="67446-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="67446-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="67446-118">Library</span></span><br/> | <dl> <span data-ttu-id="67446-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="67446-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67446-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67446-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67446-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="67446-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="67446-122">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="67446-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
