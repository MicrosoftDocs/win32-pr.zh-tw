---
description: D3DXFloat16To32Array 函式 (D3dx9math) -將16位浮點數的陣列轉換為32位浮點數。
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: 'D3DXFloat16To32Array 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107596"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="36351-103">D3DXFloat16To32Array 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="36351-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="36351-104">將16位浮點數的陣列轉換為32位浮點數。</span><span class="sxs-lookup"><span data-stu-id="36351-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="36351-105">語法</span><span class="sxs-lookup"><span data-stu-id="36351-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="36351-106">參數</span><span class="sxs-lookup"><span data-stu-id="36351-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36351-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="36351-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="36351-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="36351-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="36351-109">32位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="36351-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="36351-110">*pIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36351-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36351-111">Type： **Const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="36351-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="36351-112">16位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="36351-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="36351-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36351-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36351-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36351-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36351-115">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="36351-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36351-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="36351-116">Return value</span></span>

<span data-ttu-id="36351-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="36351-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="36351-118">32位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="36351-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="36351-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="36351-119">Requirements</span></span>



| <span data-ttu-id="36351-120">需求</span><span class="sxs-lookup"><span data-stu-id="36351-120">Requirement</span></span> | <span data-ttu-id="36351-121">值</span><span class="sxs-lookup"><span data-stu-id="36351-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36351-122">標頭</span><span class="sxs-lookup"><span data-stu-id="36351-122">Header</span></span><br/>  | <dl> <span data-ttu-id="36351-123"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="36351-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="36351-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="36351-124">Library</span></span><br/> | <dl> <span data-ttu-id="36351-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="36351-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36351-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36351-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36351-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="36351-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
