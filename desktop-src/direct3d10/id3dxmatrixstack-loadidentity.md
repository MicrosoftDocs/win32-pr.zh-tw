---
description: 在目前的矩陣中載入識別。
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: 'ID3DXMATRIXStack：： LoadIdentity 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 85a58529be3bfcb4d52ba096bb6134fe08994d77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989228"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="289de-103">ID3DXMATRIXStack：： LoadIdentity 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="289de-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="289de-104">在目前的矩陣中載入識別。</span><span class="sxs-lookup"><span data-stu-id="289de-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="289de-105">語法</span><span class="sxs-lookup"><span data-stu-id="289de-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="289de-106">參數</span><span class="sxs-lookup"><span data-stu-id="289de-106">Parameters</span></span>

<span data-ttu-id="289de-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="289de-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="289de-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="289de-108">Return value</span></span>

<span data-ttu-id="289de-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="289de-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="289de-110">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="289de-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="289de-111">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="289de-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="289de-112">備註</span><span class="sxs-lookup"><span data-stu-id="289de-112">Remarks</span></span>

<span data-ttu-id="289de-113">身分識別矩陣是矩陣，其中所有係數都是0.0，但 \[ 1、1 \] \[ 2、2 \] \[ 3、3 \] \[ 4、4 \] 係數會設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="289de-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="289de-114">識別矩陣的特殊之處，就是當它套用至頂點時，不會變更。</span><span class="sxs-lookup"><span data-stu-id="289de-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="289de-115">身分識別矩陣可作為矩陣的起點，以修改頂點值以建立旋轉、轉譯，以及可由4x4 矩陣表示的任何其他轉換。</span><span class="sxs-lookup"><span data-stu-id="289de-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="289de-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="289de-116">Requirements</span></span>



| <span data-ttu-id="289de-117">需求</span><span class="sxs-lookup"><span data-stu-id="289de-117">Requirement</span></span> | <span data-ttu-id="289de-118">值</span><span class="sxs-lookup"><span data-stu-id="289de-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="289de-119">標頭</span><span class="sxs-lookup"><span data-stu-id="289de-119">Header</span></span><br/>  | <dl> <span data-ttu-id="289de-120"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="289de-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="289de-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="289de-121">Library</span></span><br/> | <dl> <span data-ttu-id="289de-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="289de-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="289de-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="289de-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="289de-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="289de-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="289de-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="289de-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




