---
description: 終結根目錄下的框架子樹，包括根。
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: 'D3DXFrameDestroy 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982013"
---
# <a name="d3dxframedestroy-function"></a><span data-ttu-id="08c64-103">D3DXFrameDestroy 函式</span><span class="sxs-lookup"><span data-stu-id="08c64-103">D3DXFrameDestroy function</span></span>

<span data-ttu-id="08c64-104">終結根目錄下的框架子樹，包括根。</span><span class="sxs-lookup"><span data-stu-id="08c64-104">Destroys the subtree of frames under the root, including the root.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c64-105">語法</span><span class="sxs-lookup"><span data-stu-id="08c64-105">Syntax</span></span>


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="08c64-106">參數</span><span class="sxs-lookup"><span data-stu-id="08c64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c64-107">*pFrameRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08c64-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c64-108">類型： **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="08c64-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="08c64-109">根節點的指標。</span><span class="sxs-lookup"><span data-stu-id="08c64-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="08c64-110">*pAlloc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08c64-110">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c64-111">類型： **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="08c64-111">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="08c64-112">配置介面，用來解除組態架構階層的節點。</span><span class="sxs-lookup"><span data-stu-id="08c64-112">Allocation interface used to deallocate nodes of the frame hierarchy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c64-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="08c64-113">Return value</span></span>

<span data-ttu-id="08c64-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08c64-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08c64-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="08c64-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="08c64-116">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="08c64-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c64-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="08c64-117">Requirements</span></span>



| <span data-ttu-id="08c64-118">需求</span><span class="sxs-lookup"><span data-stu-id="08c64-118">Requirement</span></span> | <span data-ttu-id="08c64-119">值</span><span class="sxs-lookup"><span data-stu-id="08c64-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08c64-120">標頭</span><span class="sxs-lookup"><span data-stu-id="08c64-120">Header</span></span><br/>  | <dl> <span data-ttu-id="08c64-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="08c64-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="08c64-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="08c64-122">Library</span></span><br/> | <dl> <span data-ttu-id="08c64-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="08c64-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="08c64-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08c64-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c64-125">動畫函數</span><span class="sxs-lookup"><span data-stu-id="08c64-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




