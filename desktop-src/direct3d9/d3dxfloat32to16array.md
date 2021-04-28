---
description: D3DXFloat32To16Array 函式 (D3dx9math) -將32位浮點數的陣列轉換成16位浮點數。
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: 'D3DXFloat32To16Array 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc00df150c48e285d5478eb9b11df6c5203d6bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094256"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="c27b1-103">D3DXFloat32To16Array 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="c27b1-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="c27b1-104">將32位浮點數的陣列轉換成16位浮點數。</span><span class="sxs-lookup"><span data-stu-id="c27b1-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="c27b1-105">語法</span><span class="sxs-lookup"><span data-stu-id="c27b1-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="c27b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="c27b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c27b1-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c27b1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c27b1-108">類型： **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="c27b1-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="c27b1-109">16位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c27b1-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="c27b1-110">*pIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c27b1-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c27b1-111">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c27b1-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c27b1-112">32位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c27b1-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="c27b1-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c27b1-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c27b1-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c27b1-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c27b1-115">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="c27b1-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c27b1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c27b1-116">Return value</span></span>

<span data-ttu-id="c27b1-117">類型： **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="c27b1-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="c27b1-118">16位浮點數陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c27b1-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="c27b1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c27b1-119">Requirements</span></span>



| <span data-ttu-id="c27b1-120">需求</span><span class="sxs-lookup"><span data-stu-id="c27b1-120">Requirement</span></span> | <span data-ttu-id="c27b1-121">值</span><span class="sxs-lookup"><span data-stu-id="c27b1-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c27b1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c27b1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c27b1-123"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c27b1-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c27b1-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="c27b1-124">Library</span></span><br/> | <dl> <span data-ttu-id="c27b1-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c27b1-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c27b1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c27b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c27b1-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="c27b1-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
