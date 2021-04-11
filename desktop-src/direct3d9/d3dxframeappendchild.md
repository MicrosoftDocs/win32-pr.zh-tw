---
description: 將子框架新增至框架。
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: 'D3DXFrameAppendChild 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a27c8b31abf982c7cfaaa2a53d49d8859fa2c8bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196257"
---
# <a name="d3dxframeappendchild-function"></a><span data-ttu-id="8f23f-103">D3DXFrameAppendChild 函式</span><span class="sxs-lookup"><span data-stu-id="8f23f-103">D3DXFrameAppendChild function</span></span>

<span data-ttu-id="8f23f-104">將子框架新增至框架。</span><span class="sxs-lookup"><span data-stu-id="8f23f-104">Adds a child frame to a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f23f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f23f-105">Syntax</span></span>


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a><span data-ttu-id="8f23f-106">參數</span><span class="sxs-lookup"><span data-stu-id="8f23f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f23f-107">*pFrameParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f23f-107">*pFrameParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f23f-108">類型： **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="8f23f-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="8f23f-109">父節點的指標。</span><span class="sxs-lookup"><span data-stu-id="8f23f-109">Pointer to the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="8f23f-110">*pFrameChild* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f23f-110">*pFrameChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f23f-111">Type： **Const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f23f-111">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="8f23f-112">子節點的指標。</span><span class="sxs-lookup"><span data-stu-id="8f23f-112">Pointer to the child node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f23f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f23f-113">Return value</span></span>

<span data-ttu-id="8f23f-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8f23f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8f23f-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8f23f-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8f23f-116">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="8f23f-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f23f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f23f-117">Requirements</span></span>



| <span data-ttu-id="8f23f-118">需求</span><span class="sxs-lookup"><span data-stu-id="8f23f-118">Requirement</span></span> | <span data-ttu-id="8f23f-119">值</span><span class="sxs-lookup"><span data-stu-id="8f23f-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f23f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8f23f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8f23f-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f23f-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8f23f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f23f-122">Library</span></span><br/> | <dl> <span data-ttu-id="8f23f-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f23f-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8f23f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f23f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f23f-125">動畫函數</span><span class="sxs-lookup"><span data-stu-id="8f23f-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




