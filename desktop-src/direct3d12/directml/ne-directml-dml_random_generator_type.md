---
UID: NE:directml.DML_RANDOM_GENERATOR_TYPE
title: DML_RANDOM_GENERATOR_TYPE
description: 定義常數，指定隨機亂數產生器的類型。
helpviewer_keywords:
- DML_RANDOM_GENERATOR_TYPE
- DML_RANDOM_GENERATOR_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_RANDOM_GENERATOR_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_TYPE, DML_RANDOM_GENERATOR_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_RANDOM_GENERATOR_TYPE
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_RANDOM_GENERATOR_TYPE
- directml/DML_RANDOM_GENERATOR_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RANDOM_GENERATOR_TYPE
ms.openlocfilehash: bcb79fe7737e8b9ddb461c8da8a901960a4b23f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106998183"
---
# <a name="dml_random_generator_type-enumeration-directmlh"></a><span data-ttu-id="bc41c-103">DML_RANDOM_GENERATOR_TYPE 列舉 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="bc41c-103">DML_RANDOM_GENERATOR_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="bc41c-104">定義常數，指定隨機亂數產生器的類型。</span><span class="sxs-lookup"><span data-stu-id="bc41c-104">Defines constants that specify types of random random-number generator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc41c-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。</span><span class="sxs-lookup"><span data-stu-id="bc41c-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="bc41c-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="bc41c-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc41c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc41c-107">Syntax</span></span>
```cpp
enum DML_RANDOM_GENERATOR_TYPE
{
  DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10
};
```

## <a name="constants"></a><span data-ttu-id="bc41c-108">常數</span><span class="sxs-lookup"><span data-stu-id="bc41c-108">Constants</span></span>

| <span data-ttu-id="bc41c-109">Name</span><span class="sxs-lookup"><span data-stu-id="bc41c-109">Name</span></span> | <span data-ttu-id="bc41c-110">描述</span><span class="sxs-lookup"><span data-stu-id="bc41c-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="bc41c-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span><span class="sxs-lookup"><span data-stu-id="bc41c-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span></span> | <span data-ttu-id="bc41c-112">根據 [Philox 4x32-10 演算法](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)，指定虛擬亂數的產生器。</span><span class="sxs-lookup"><span data-stu-id="bc41c-112">Specifies a generator for pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span> |


## <a name="requirements"></a><span data-ttu-id="bc41c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc41c-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bc41c-114">**標頭**</span><span class="sxs-lookup"><span data-stu-id="bc41c-114">**Header**</span></span> | <span data-ttu-id="bc41c-115">directml。h</span><span class="sxs-lookup"><span data-stu-id="bc41c-115">directml.h</span></span> |