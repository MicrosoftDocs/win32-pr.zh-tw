---
description: 描述矩陣。
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: 'D3DMATRIX (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b4339d2e44e1add46103bae58ad3e02c8a6509b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976713"
---
# <a name="d3dmatrix"></a><span data-ttu-id="eadb8-103">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="eadb8-103">D3DMATRIX</span></span>

<span data-ttu-id="eadb8-104">描述矩陣。</span><span class="sxs-lookup"><span data-stu-id="eadb8-104">Describes a matrix.</span></span>

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

<span data-ttu-id="eadb8-105">衍生類型： \* LPD3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="eadb8-105">Derived types: \*LPD3DMATRIX</span></span>

## <a name="members"></a><span data-ttu-id="eadb8-106">成員</span><span class="sxs-lookup"><span data-stu-id="eadb8-106">Members</span></span>



| <span data-ttu-id="eadb8-107">項目</span><span class="sxs-lookup"><span data-stu-id="eadb8-107">Item</span></span>                                                        | <span data-ttu-id="eadb8-108">描述</span><span class="sxs-lookup"><span data-stu-id="eadb8-108">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eadb8-109"><span id="_ij"></span><span id="_IJ"></span>\_Ij</span><span class="sxs-lookup"><span data-stu-id="eadb8-109"><span id="_ij"></span><span id="_IJ"></span>\_ij</span></span><br/> | <span data-ttu-id="eadb8-110">代表4x4 矩陣的浮點數陣列，其中 i 是資料列編號，而 j 是資料行編號。</span><span class="sxs-lookup"><span data-stu-id="eadb8-110">An array of floats that represent a 4x4 matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="eadb8-111">例如， \_ 34 表示與 \[ ₃₄相同 \] ，第三個數據列和第四個數據行中的元件。</span><span class="sxs-lookup"><span data-stu-id="eadb8-111">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eadb8-112">備註</span><span class="sxs-lookup"><span data-stu-id="eadb8-112">Remarks</span></span>

<span data-ttu-id="eadb8-113">在 Direct3D 中， \_ 投射矩陣的34元素不能是負數。</span><span class="sxs-lookup"><span data-stu-id="eadb8-113">In Direct3D, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="eadb8-114">如果您的應用程式需要在這個位置使用負值，則應該改為將整個投射矩陣調整為-1。</span><span class="sxs-lookup"><span data-stu-id="eadb8-114">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="eadb8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="eadb8-115">Requirements</span></span>



| <span data-ttu-id="eadb8-116">需求</span><span class="sxs-lookup"><span data-stu-id="eadb8-116">Requirement</span></span> | <span data-ttu-id="eadb8-117">值</span><span class="sxs-lookup"><span data-stu-id="eadb8-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eadb8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="eadb8-118">Header</span></span><br/> | <dl> <span data-ttu-id="eadb8-119"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="eadb8-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eadb8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eadb8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadb8-121">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="eadb8-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="eadb8-122">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="eadb8-122">**GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="eadb8-123">**MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="eadb8-123">**MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="eadb8-124">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="eadb8-124">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

<span data-ttu-id="eadb8-125">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="eadb8-125">**SetTransform**</span></span>
</dt> <dt>

[<span data-ttu-id="eadb8-126">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="eadb8-126">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> <dt>

[<span data-ttu-id="eadb8-127">轉換 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="eadb8-127">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
