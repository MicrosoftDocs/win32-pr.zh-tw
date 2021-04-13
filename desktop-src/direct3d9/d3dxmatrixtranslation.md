---
description: 使用指定的位移來建立矩陣。
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: 'D3DXMatrixTranslation 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c74d56eaa0e41bc6ce9060ff291885a8a5c05a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322891"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a><span data-ttu-id="30fab-103">D3DXMatrixTranslation 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="30fab-103">D3DXMatrixTranslation function (D3dx9math.h)</span></span>

<span data-ttu-id="30fab-104">使用指定的位移來建立矩陣。</span><span class="sxs-lookup"><span data-stu-id="30fab-104">Builds a matrix using the specified offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="30fab-105">語法</span><span class="sxs-lookup"><span data-stu-id="30fab-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="30fab-106">參數</span><span class="sxs-lookup"><span data-stu-id="30fab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30fab-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="30fab-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30fab-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="30fab-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="30fab-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="30fab-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="30fab-110">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="30fab-110">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30fab-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30fab-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30fab-112">X 座標位移。</span><span class="sxs-lookup"><span data-stu-id="30fab-112">X-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="30fab-113">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30fab-113">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30fab-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30fab-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30fab-115">Y 座標位移。</span><span class="sxs-lookup"><span data-stu-id="30fab-115">Y-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="30fab-116">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30fab-116">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30fab-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30fab-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30fab-118">Z 座標位移。</span><span class="sxs-lookup"><span data-stu-id="30fab-118">Z-coordinate offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30fab-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="30fab-119">Return value</span></span>

<span data-ttu-id="30fab-120">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="30fab-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="30fab-121">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，其中包含翻譯的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="30fab-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains a translated transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="30fab-122">備註</span><span class="sxs-lookup"><span data-stu-id="30fab-122">Remarks</span></span>

<span data-ttu-id="30fab-123">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="30fab-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="30fab-124">如此一來，D3DXMATRIXTranslation 就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="30fab-124">In this way, the D3DXMATRIXTranslation can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="30fab-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="30fab-125">Requirements</span></span>



| <span data-ttu-id="30fab-126">需求</span><span class="sxs-lookup"><span data-stu-id="30fab-126">Requirement</span></span> | <span data-ttu-id="30fab-127">值</span><span class="sxs-lookup"><span data-stu-id="30fab-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30fab-128">標頭</span><span class="sxs-lookup"><span data-stu-id="30fab-128">Header</span></span><br/>  | <dl> <span data-ttu-id="30fab-129"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="30fab-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="30fab-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="30fab-130">Library</span></span><br/> | <dl> <span data-ttu-id="30fab-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="30fab-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30fab-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30fab-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30fab-133">數學函數</span><span class="sxs-lookup"><span data-stu-id="30fab-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
