---
description: 尋找根框架的子框架。
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: 'D3DXFrameFind 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986514"
---
# <a name="d3dxframefind-function"></a><span data-ttu-id="f7574-103">D3DXFrameFind 函式</span><span class="sxs-lookup"><span data-stu-id="f7574-103">D3DXFrameFind function</span></span>

<span data-ttu-id="f7574-104">尋找根框架的子框架。</span><span class="sxs-lookup"><span data-stu-id="f7574-104">Finds the child frame of a root frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7574-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7574-105">Syntax</span></span>


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a><span data-ttu-id="f7574-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7574-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7574-107">*pFrameRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7574-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7574-108">Type： **Const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7574-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="f7574-109">根框架的指標。</span><span class="sxs-lookup"><span data-stu-id="f7574-109">Pointer to the root frame.</span></span> <span data-ttu-id="f7574-110">請參閱 [**D3DXFRAME**](d3dxframe.md)。</span><span class="sxs-lookup"><span data-stu-id="f7574-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7574-111">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7574-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7574-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7574-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7574-113">要尋找的子框架名稱。</span><span class="sxs-lookup"><span data-stu-id="f7574-113">Name of the child frame to find.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7574-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7574-114">Return value</span></span>

<span data-ttu-id="f7574-115">類型： **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="f7574-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="f7574-116">如果找到，則傳回子框架，否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f7574-116">Returns the child frame if it is found, or **NULL** otherwise.</span></span> <span data-ttu-id="f7574-117">請參閱 [**D3DXFRAME**](d3dxframe.md)。</span><span class="sxs-lookup"><span data-stu-id="f7574-117">See [**D3DXFRAME**](d3dxframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7574-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7574-118">Requirements</span></span>



| <span data-ttu-id="f7574-119">需求</span><span class="sxs-lookup"><span data-stu-id="f7574-119">Requirement</span></span> | <span data-ttu-id="f7574-120">值</span><span class="sxs-lookup"><span data-stu-id="f7574-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7574-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f7574-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f7574-122"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7574-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f7574-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7574-123">Library</span></span><br/> | <dl> <span data-ttu-id="f7574-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7574-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7574-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7574-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7574-126">動畫函數</span><span class="sxs-lookup"><span data-stu-id="f7574-126">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
