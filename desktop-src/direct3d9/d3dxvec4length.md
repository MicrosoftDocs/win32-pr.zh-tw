---
description: 傳回4D 向量的長度。
ms.assetid: cb332160-3e3d-41b9-bfb0-e3b743d2eafd
title: 'D3DXVec4Length 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea16c6406c217f5e5d76af68a5da3a0c8bd17b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946270"
---
# <a name="d3dxvec4length-function"></a><span data-ttu-id="8c2bd-103">D3DXVec4Length 函式</span><span class="sxs-lookup"><span data-stu-id="8c2bd-103">D3DXVec4Length function</span></span>

<span data-ttu-id="8c2bd-104">傳回4D 向量的長度。</span><span class="sxs-lookup"><span data-stu-id="8c2bd-104">Returns the length of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2bd-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c2bd-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Length(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="8c2bd-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c2bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c2bd-107">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c2bd-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2bd-108">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c2bd-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8c2bd-109">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8c2bd-109">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c2bd-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c2bd-110">Return value</span></span>

<span data-ttu-id="8c2bd-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c2bd-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c2bd-112">向量的長度。</span><span class="sxs-lookup"><span data-stu-id="8c2bd-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2bd-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c2bd-113">Requirements</span></span>



| <span data-ttu-id="8c2bd-114">需求</span><span class="sxs-lookup"><span data-stu-id="8c2bd-114">Requirement</span></span> | <span data-ttu-id="8c2bd-115">值</span><span class="sxs-lookup"><span data-stu-id="8c2bd-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2bd-116">標頭</span><span class="sxs-lookup"><span data-stu-id="8c2bd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8c2bd-117"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c2bd-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c2bd-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c2bd-118">Library</span></span><br/> | <dl> <span data-ttu-id="8c2bd-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c2bd-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c2bd-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c2bd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2bd-121">數學函數</span><span class="sxs-lookup"><span data-stu-id="8c2bd-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8c2bd-122">**D3DXVec4LengthSq**</span><span class="sxs-lookup"><span data-stu-id="8c2bd-122">**D3DXVec4LengthSq**</span></span>](d3dxvec4lengthsq.md)
</dt> </dl>

 

 
