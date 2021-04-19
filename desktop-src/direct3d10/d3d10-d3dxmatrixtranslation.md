---
description: 建立轉譯矩陣。
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: 'D3DXMatrixTranslation 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999043"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a><span data-ttu-id="c2be5-103">D3DXMatrixTranslation 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="c2be5-103">D3DXMatrixTranslation function (D3DX10Math.h)</span></span>

<span data-ttu-id="c2be5-104">建立轉譯矩陣。</span><span class="sxs-lookup"><span data-stu-id="c2be5-104">Create a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2be5-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2be5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="c2be5-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2be5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2be5-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c2be5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be5-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2be5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2be5-109">將成為轉譯矩陣的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c2be5-109">The matrix that will become a translation matrix.</span></span> <span data-ttu-id="c2be5-110">請參閱 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="c2be5-110">See [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2be5-111">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="c2be5-111">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be5-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2be5-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2be5-113">轉譯的 x 元件。</span><span class="sxs-lookup"><span data-stu-id="c2be5-113">The x-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="c2be5-114">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2be5-114">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be5-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2be5-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2be5-116">轉譯的 y 元件。</span><span class="sxs-lookup"><span data-stu-id="c2be5-116">The y-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="c2be5-117">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2be5-117">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be5-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2be5-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2be5-119">轉譯的 z 元件。</span><span class="sxs-lookup"><span data-stu-id="c2be5-119">The z-component of the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2be5-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2be5-120">Return value</span></span>

<span data-ttu-id="c2be5-121">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2be5-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2be5-122">轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="c2be5-122">The translation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2be5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2be5-123">Requirements</span></span>



| <span data-ttu-id="c2be5-124">需求</span><span class="sxs-lookup"><span data-stu-id="c2be5-124">Requirement</span></span> | <span data-ttu-id="c2be5-125">值</span><span class="sxs-lookup"><span data-stu-id="c2be5-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2be5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c2be5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c2be5-127"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2be5-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c2be5-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2be5-128">Library</span></span><br/> | <dl> <span data-ttu-id="c2be5-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2be5-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2be5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2be5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2be5-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="c2be5-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
