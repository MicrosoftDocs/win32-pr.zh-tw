---
description: 傳回四元數的長度平方。
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: 'D3DXQuaternionLengthSq 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0771d571b15ef690b115f12e5fa1d8ff6fea4dad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982897"
---
# <a name="d3dxquaternionlengthsq-function"></a><span data-ttu-id="ea299-103">D3DXQuaternionLengthSq 函式</span><span class="sxs-lookup"><span data-stu-id="ea299-103">D3DXQuaternionLengthSq function</span></span>

<span data-ttu-id="ea299-104">傳回四元數的長度平方。</span><span class="sxs-lookup"><span data-stu-id="ea299-104">Returns the square of the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea299-105">語法</span><span class="sxs-lookup"><span data-stu-id="ea299-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="ea299-106">參數</span><span class="sxs-lookup"><span data-stu-id="ea299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea299-107">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ea299-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea299-108">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea299-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ea299-109">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ea299-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea299-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea299-110">Return value</span></span>

<span data-ttu-id="ea299-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea299-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea299-112">四元數的平方長度。</span><span class="sxs-lookup"><span data-stu-id="ea299-112">The quaternion's squared length.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea299-113">備註</span><span class="sxs-lookup"><span data-stu-id="ea299-113">Remarks</span></span>

<span data-ttu-id="ea299-114">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="ea299-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea299-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea299-115">Requirements</span></span>



| <span data-ttu-id="ea299-116">需求</span><span class="sxs-lookup"><span data-stu-id="ea299-116">Requirement</span></span> | <span data-ttu-id="ea299-117">值</span><span class="sxs-lookup"><span data-stu-id="ea299-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea299-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ea299-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ea299-119"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea299-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ea299-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea299-120">Library</span></span><br/> | <dl> <span data-ttu-id="ea299-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea299-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea299-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea299-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea299-123">數學函數</span><span class="sxs-lookup"><span data-stu-id="ea299-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ea299-124">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="ea299-124">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
</dt> </dl>

 

 
