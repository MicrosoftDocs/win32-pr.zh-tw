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
ms.openlocfilehash: c08b5cdc07280a2851636a555415ecce515fa79b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417041"
---
# <a name="dml_random_generator_type-enumeration-directmlh"></a><span data-ttu-id="2a90f-103">DML_RANDOM_GENERATOR_TYPE 列舉 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="2a90f-103">DML_RANDOM_GENERATOR_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="2a90f-104">定義常數，指定隨機亂數產生器的類型。</span><span class="sxs-lookup"><span data-stu-id="2a90f-104">Defines constants that specify types of random random-number generator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a90f-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="2a90f-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="2a90f-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="2a90f-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a90f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a90f-107">Syntax</span></span>
```cpp
enum DML_RANDOM_GENERATOR_TYPE
{
  DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10
};
```

## <a name="constants"></a><span data-ttu-id="2a90f-108">常數</span><span class="sxs-lookup"><span data-stu-id="2a90f-108">Constants</span></span>

| <span data-ttu-id="2a90f-109">Name</span><span class="sxs-lookup"><span data-stu-id="2a90f-109">Name</span></span> | <span data-ttu-id="2a90f-110">描述</span><span class="sxs-lookup"><span data-stu-id="2a90f-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="2a90f-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span><span class="sxs-lookup"><span data-stu-id="2a90f-111">DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10</span></span> | <span data-ttu-id="2a90f-112">根據 [Philox 4x32-10 演算法](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)，指定虛擬亂數的產生器。</span><span class="sxs-lookup"><span data-stu-id="2a90f-112">Specifies a generator for pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span> |


## <a name="requirements"></a><span data-ttu-id="2a90f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a90f-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2a90f-114">**標頭**</span><span class="sxs-lookup"><span data-stu-id="2a90f-114">**Header**</span></span> | <span data-ttu-id="2a90f-115">directml。h</span><span class="sxs-lookup"><span data-stu-id="2a90f-115">directml.h</span></span> |