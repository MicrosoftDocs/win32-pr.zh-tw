---
description: 計運算元樹中具有非 null 名稱的框架數目。
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: 'D3DXFrameNumNamedMatrices 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c2d535a41d15987df7816cfc23f1bb213b6adc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946098"
---
# <a name="d3dxframenumnamedmatrices-function"></a><span data-ttu-id="4c2e3-103">D3DXFrameNumNamedMatrices 函式</span><span class="sxs-lookup"><span data-stu-id="4c2e3-103">D3DXFrameNumNamedMatrices function</span></span>

<span data-ttu-id="4c2e3-104">計運算元樹中具有非 null 名稱的框架數目。</span><span class="sxs-lookup"><span data-stu-id="4c2e3-104">Counts number of frames in a subtree that have non-null names.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c2e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c2e3-105">Syntax</span></span>


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a><span data-ttu-id="4c2e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c2e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c2e3-107">*pFrameRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c2e3-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c2e3-108">Type： **Const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c2e3-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="4c2e3-109">子樹根節點的指標。</span><span class="sxs-lookup"><span data-stu-id="4c2e3-109">Pointer to the root node of the subtree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c2e3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c2e3-110">Return value</span></span>

<span data-ttu-id="4c2e3-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c2e3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c2e3-112">傳回框架計數。</span><span class="sxs-lookup"><span data-stu-id="4c2e3-112">Returns the frame count.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c2e3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c2e3-113">Requirements</span></span>



| <span data-ttu-id="4c2e3-114">需求</span><span class="sxs-lookup"><span data-stu-id="4c2e3-114">Requirement</span></span> | <span data-ttu-id="4c2e3-115">值</span><span class="sxs-lookup"><span data-stu-id="4c2e3-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2e3-116">標頭</span><span class="sxs-lookup"><span data-stu-id="4c2e3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4c2e3-117"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c2e3-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4c2e3-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c2e3-118">Library</span></span><br/> | <dl> <span data-ttu-id="4c2e3-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c2e3-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c2e3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c2e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c2e3-121">動畫函數</span><span class="sxs-lookup"><span data-stu-id="4c2e3-121">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
