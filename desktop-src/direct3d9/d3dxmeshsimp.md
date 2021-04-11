---
description: 指定網格的簡化選項。
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: 'D3DXMESHSIMP 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116217"
---
# <a name="d3dxmeshsimp-enumeration"></a><span data-ttu-id="75267-103">D3DXMESHSIMP 列舉</span><span class="sxs-lookup"><span data-stu-id="75267-103">D3DXMESHSIMP enumeration</span></span>

<span data-ttu-id="75267-104">指定網格的簡化選項。</span><span class="sxs-lookup"><span data-stu-id="75267-104">Specifies simplification options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="75267-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75267-105">Syntax</span></span>


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a><span data-ttu-id="75267-106">常數</span><span class="sxs-lookup"><span data-stu-id="75267-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="75267-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP \_ 頂點**</span><span class="sxs-lookup"><span data-stu-id="75267-107"><span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP\_VERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="75267-108">網格會依 MinValue 參數中指定的頂點數目來簡化。</span><span class="sxs-lookup"><span data-stu-id="75267-108">The mesh will be simplified by the number of vertices specified in the MinValue parameter.</span></span>

</dd> <dt>

<span data-ttu-id="75267-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP \_ 臉部**</span><span class="sxs-lookup"><span data-stu-id="75267-109"><span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP\_FACE**</span></span>
</dt> <dd>

<span data-ttu-id="75267-110">網格會由 MinValue 參數中指定的臉部數目簡化。</span><span class="sxs-lookup"><span data-stu-id="75267-110">The mesh will be simplified by the number of faces specified in the MinValue parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75267-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="75267-111">Requirements</span></span>



| <span data-ttu-id="75267-112">需求</span><span class="sxs-lookup"><span data-stu-id="75267-112">Requirement</span></span> | <span data-ttu-id="75267-113">值</span><span class="sxs-lookup"><span data-stu-id="75267-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75267-114">標頭</span><span class="sxs-lookup"><span data-stu-id="75267-114">Header</span></span><br/> | <dl> <span data-ttu-id="75267-115"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="75267-115"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75267-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75267-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75267-117">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="75267-117">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="75267-118">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="75267-118">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 




