---
description: D3DXSHPRTSPLITMESHVERTDATA 結構
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: 'D3DXSHPRTSPLITMESHVERTDATA 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 55424929a3d415fc1b89f7a1af53be849cf90185
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696627"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a><span data-ttu-id="2f0bc-103">D3DXSHPRTSPLITMESHVERTDATA 結構</span><span class="sxs-lookup"><span data-stu-id="2f0bc-103">D3DXSHPRTSPLITMESHVERTDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="2f0bc-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f0bc-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a><span data-ttu-id="2f0bc-105">成員</span><span class="sxs-lookup"><span data-stu-id="2f0bc-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f0bc-106">**uVertRemap**</span><span class="sxs-lookup"><span data-stu-id="2f0bc-106">**uVertRemap**</span></span>
</dt> <dd>

<span data-ttu-id="2f0bc-107">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f0bc-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2f0bc-108">原始網格中對應的頂點。</span><span class="sxs-lookup"><span data-stu-id="2f0bc-108">Vertex in original mesh this corresponds to.</span></span>

</dd> <dt>

<span data-ttu-id="2f0bc-109">**uSubCluster**</span><span class="sxs-lookup"><span data-stu-id="2f0bc-109">**uSubCluster**</span></span>
</dt> <dd>

<span data-ttu-id="2f0bc-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f0bc-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2f0bc-111">相對於 supercluster 的叢集索引。</span><span class="sxs-lookup"><span data-stu-id="2f0bc-111">Cluster index, relative to the supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="2f0bc-112">**ucVertStatus**</span><span class="sxs-lookup"><span data-stu-id="2f0bc-112">**ucVertStatus**</span></span>
</dt> <dd>

<span data-ttu-id="2f0bc-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f0bc-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2f0bc-114">如果頂點具有有效的資料，則為1，如果是「完整」，則為0。</span><span class="sxs-lookup"><span data-stu-id="2f0bc-114">1 if vertex has valid data, 0 if it is "full".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f0bc-115">備註</span><span class="sxs-lookup"><span data-stu-id="2f0bc-115">Remarks</span></span>

<span data-ttu-id="2f0bc-116">配置於 [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)中。</span><span class="sxs-lookup"><span data-stu-id="2f0bc-116">Allocated in [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f0bc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f0bc-117">Requirements</span></span>



| <span data-ttu-id="2f0bc-118">需求</span><span class="sxs-lookup"><span data-stu-id="2f0bc-118">Requirement</span></span> | <span data-ttu-id="2f0bc-119">值</span><span class="sxs-lookup"><span data-stu-id="2f0bc-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f0bc-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2f0bc-120">Header</span></span><br/> | <dl> <span data-ttu-id="2f0bc-121"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f0bc-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f0bc-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f0bc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f0bc-123">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="2f0bc-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
