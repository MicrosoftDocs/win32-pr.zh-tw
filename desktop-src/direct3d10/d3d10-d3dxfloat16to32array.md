---
description: D3DXFloat16To32Array 函式 (D3DX10Math) -將16位浮點數的陣列轉換為32位浮點數。
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: 'D3DXFloat16To32Array 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ae624fb05ce10447bd3b9082e171dc01224baaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113286"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a><span data-ttu-id="3ee01-103">D3DXFloat16To32Array 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="3ee01-103">D3DXFloat16To32Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="3ee01-104">將16位浮點數的陣列轉換為32位浮點數。</span><span class="sxs-lookup"><span data-stu-id="3ee01-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee01-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ee01-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="3ee01-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ee01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ee01-107">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ee01-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee01-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ee01-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3ee01-109">32位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="3ee01-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="3ee01-110">*pIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ee01-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee01-111">Type： **Const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="3ee01-111">Type: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="3ee01-112">16位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="3ee01-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="3ee01-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ee01-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee01-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ee01-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ee01-115">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="3ee01-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ee01-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ee01-116">Return value</span></span>

<span data-ttu-id="3ee01-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ee01-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3ee01-118">32位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="3ee01-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ee01-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ee01-119">Requirements</span></span>



| <span data-ttu-id="3ee01-120">需求</span><span class="sxs-lookup"><span data-stu-id="3ee01-120">Requirement</span></span> | <span data-ttu-id="3ee01-121">值</span><span class="sxs-lookup"><span data-stu-id="3ee01-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee01-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3ee01-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3ee01-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ee01-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3ee01-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ee01-124">Library</span></span><br/> | <dl> <span data-ttu-id="3ee01-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ee01-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ee01-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ee01-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee01-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="3ee01-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
