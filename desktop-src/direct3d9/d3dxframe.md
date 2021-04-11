---
description: 封裝轉換框架階層中的轉換框架。
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: 'D3DXFRAME 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196258"
---
# <a name="d3dxframe-structure"></a><span data-ttu-id="f13c9-103">D3DXFRAME 結構</span><span class="sxs-lookup"><span data-stu-id="f13c9-103">D3DXFRAME structure</span></span>

<span data-ttu-id="f13c9-104">封裝轉換框架階層中的轉換框架。</span><span class="sxs-lookup"><span data-stu-id="f13c9-104">Encapsulates a transform frame in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="f13c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="f13c9-105">Syntax</span></span>


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a><span data-ttu-id="f13c9-106">成員</span><span class="sxs-lookup"><span data-stu-id="f13c9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f13c9-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f13c9-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="f13c9-108">類型： **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="f13c9-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f13c9-109">框架的名稱。</span><span class="sxs-lookup"><span data-stu-id="f13c9-109">Name of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="f13c9-110">**TransformationMatrix**</span><span class="sxs-lookup"><span data-stu-id="f13c9-110">**TransformationMatrix**</span></span>
</dt> <dd>

<span data-ttu-id="f13c9-111">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="f13c9-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f13c9-112">轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="f13c9-112">Transformation matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f13c9-113">**pMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="f13c9-113">**pMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="f13c9-114">類型： **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="f13c9-114">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f13c9-115">網格容器的指標。</span><span class="sxs-lookup"><span data-stu-id="f13c9-115">Pointer to the mesh container.</span></span>

</dd> <dt>

<span data-ttu-id="f13c9-116">**pFrameSibling**</span><span class="sxs-lookup"><span data-stu-id="f13c9-116">**pFrameSibling**</span></span>
</dt> <dd>

<span data-ttu-id="f13c9-117">類型： \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="f13c9-117">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="f13c9-118">指向同級框架的指標。</span><span class="sxs-lookup"><span data-stu-id="f13c9-118">Pointer to a sibling frame.</span></span>

</dd> <dt>

<span data-ttu-id="f13c9-119">**pFrameFirstChild**</span><span class="sxs-lookup"><span data-stu-id="f13c9-119">**pFrameFirstChild**</span></span>
</dt> <dd>

<span data-ttu-id="f13c9-120">類型： \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="f13c9-120">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="f13c9-121">子框架的指標。</span><span class="sxs-lookup"><span data-stu-id="f13c9-121">Pointer to a child frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f13c9-122">備註</span><span class="sxs-lookup"><span data-stu-id="f13c9-122">Remarks</span></span>

<span data-ttu-id="f13c9-123">應用程式可以從此結構衍生，以新增其他資料。</span><span class="sxs-lookup"><span data-stu-id="f13c9-123">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f13c9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f13c9-124">Requirements</span></span>



| <span data-ttu-id="f13c9-125">需求</span><span class="sxs-lookup"><span data-stu-id="f13c9-125">Requirement</span></span> | <span data-ttu-id="f13c9-126">值</span><span class="sxs-lookup"><span data-stu-id="f13c9-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f13c9-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f13c9-127">Header</span></span><br/> | <dl> <span data-ttu-id="f13c9-128"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="f13c9-128"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f13c9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f13c9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f13c9-130">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="f13c9-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




