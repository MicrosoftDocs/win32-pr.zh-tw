---
description: 資源使用量統計資料。
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: 'D3DDEVINFO_ResourceManager 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696588"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="579a0-103">D3DDEVINFO \_ ResourceManager 結構</span><span class="sxs-lookup"><span data-stu-id="579a0-103">D3DDEVINFO\_ResourceManager structure</span></span>

<span data-ttu-id="579a0-104">資源使用量統計資料。</span><span class="sxs-lookup"><span data-stu-id="579a0-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="579a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="579a0-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a><span data-ttu-id="579a0-106">成員</span><span class="sxs-lookup"><span data-stu-id="579a0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="579a0-107">**統計**</span><span class="sxs-lookup"><span data-stu-id="579a0-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="579a0-108">類型： **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="579a0-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="579a0-109">資源統計資料元素的陣列。</span><span class="sxs-lookup"><span data-stu-id="579a0-109">Array of resource statistics elements.</span></span> <span data-ttu-id="579a0-110">請參閱 [**D3DRESOURCESTATS**](d3dresourcestats.md)。</span><span class="sxs-lookup"><span data-stu-id="579a0-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="579a0-111">備註</span><span class="sxs-lookup"><span data-stu-id="579a0-111">Remarks</span></span>

<span data-ttu-id="579a0-112">D3DRTYPECOUNT 指的是 [**D3DRESOURCETYPE**](./d3dresourcetype.md)中的列舉數目。</span><span class="sxs-lookup"><span data-stu-id="579a0-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="579a0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="579a0-113">Requirements</span></span>



| <span data-ttu-id="579a0-114">需求</span><span class="sxs-lookup"><span data-stu-id="579a0-114">Requirement</span></span> | <span data-ttu-id="579a0-115">值</span><span class="sxs-lookup"><span data-stu-id="579a0-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="579a0-116">標頭</span><span class="sxs-lookup"><span data-stu-id="579a0-116">Header</span></span><br/> | <dl> <span data-ttu-id="579a0-117"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="579a0-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="579a0-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="579a0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579a0-119">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="579a0-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
