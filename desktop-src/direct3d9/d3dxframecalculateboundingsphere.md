---
description: 計算框架階層中所有網格的周框球體。
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: 'D3DXFrameCalculateBoundingSphere 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999970"
---
# <a name="d3dxframecalculateboundingsphere-function"></a><span data-ttu-id="2fd58-103">D3DXFrameCalculateBoundingSphere 函式</span><span class="sxs-lookup"><span data-stu-id="2fd58-103">D3DXFrameCalculateBoundingSphere function</span></span>

<span data-ttu-id="2fd58-104">計算框架階層中所有網格的周框球體。</span><span class="sxs-lookup"><span data-stu-id="2fd58-104">Computes the bounding sphere of all the meshes in the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd58-105">語法</span><span class="sxs-lookup"><span data-stu-id="2fd58-105">Syntax</span></span>


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a><span data-ttu-id="2fd58-106">參數</span><span class="sxs-lookup"><span data-stu-id="2fd58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fd58-107">*pFrameRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2fd58-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd58-108">Type： **Const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="2fd58-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="2fd58-109">根節點的指標。</span><span class="sxs-lookup"><span data-stu-id="2fd58-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="2fd58-110">*pObjectCenter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2fd58-110">*pObjectCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd58-111">類型： **[ **LPD3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="2fd58-111">Type: **[**LPD3DXVECTOR3**](d3dxvector3.md)**</span></span>

<span data-ttu-id="2fd58-112">傳回周框球體的中心。</span><span class="sxs-lookup"><span data-stu-id="2fd58-112">Returns the center of the bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="2fd58-113">*pObjectRadius* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2fd58-113">*pObjectRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd58-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fd58-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2fd58-115">傳回周框球體的半徑。</span><span class="sxs-lookup"><span data-stu-id="2fd58-115">Returns the radius of the bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fd58-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fd58-116">Return value</span></span>

<span data-ttu-id="2fd58-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2fd58-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2fd58-118">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2fd58-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2fd58-119">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2fd58-119">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd58-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fd58-120">Requirements</span></span>



| <span data-ttu-id="2fd58-121">需求</span><span class="sxs-lookup"><span data-stu-id="2fd58-121">Requirement</span></span> | <span data-ttu-id="2fd58-122">值</span><span class="sxs-lookup"><span data-stu-id="2fd58-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd58-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2fd58-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2fd58-124"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd58-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2fd58-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="2fd58-125">Library</span></span><br/> | <dl> <span data-ttu-id="2fd58-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fd58-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2fd58-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fd58-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd58-128">動畫函數</span><span class="sxs-lookup"><span data-stu-id="2fd58-128">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
