---
description: D3DXFloat32To16Array 函式 (D3DX10Math) -將32位浮點數的陣列轉換成16位浮點數。
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: 'D3DXFloat32To16Array 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 600cc2cd333aaea08b38c252c206c1a74c1ca059
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103516"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="355e2-103">D3DXFloat32To16Array 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="355e2-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="355e2-104">將32位浮點數的陣列轉換成16位浮點數。</span><span class="sxs-lookup"><span data-stu-id="355e2-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="355e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="355e2-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="355e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="355e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="355e2-107">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="355e2-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="355e2-108">類型： **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="355e2-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="355e2-109">16位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="355e2-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="355e2-110">*pIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="355e2-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="355e2-111">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="355e2-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="355e2-112">32位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="355e2-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="355e2-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="355e2-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="355e2-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="355e2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="355e2-115">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="355e2-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="355e2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="355e2-116">Return value</span></span>

<span data-ttu-id="355e2-117">類型： **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="355e2-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="355e2-118">16位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="355e2-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="355e2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="355e2-119">Requirements</span></span>



| <span data-ttu-id="355e2-120">需求</span><span class="sxs-lookup"><span data-stu-id="355e2-120">Requirement</span></span> | <span data-ttu-id="355e2-121">值</span><span class="sxs-lookup"><span data-stu-id="355e2-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="355e2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="355e2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="355e2-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="355e2-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="355e2-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="355e2-124">Library</span></span><br/> | <dl> <span data-ttu-id="355e2-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="355e2-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="355e2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="355e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="355e2-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="355e2-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
