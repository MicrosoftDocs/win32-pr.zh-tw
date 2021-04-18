---
title: 記憶。Cpp
description: 在範例提供者元件中，顯示記憶體配置和釋出的程式碼範例位於記憶體 .cpp 中。 下表列出支援的常式。
ms.assetid: dc5b3559-02fc-45e8-bbd0-482e4e3a7f8a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9add77dcdbbfc0ddab547cd537b352c9a68bdaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968616"
---
# <a name="memorycpp"></a><span data-ttu-id="9d8a7-104">記憶。Cpp</span><span class="sxs-lookup"><span data-stu-id="9d8a7-104">MEMORY.CPP</span></span>

<span data-ttu-id="9d8a7-105">在範例提供者元件中，顯示記憶體配置和釋出的程式碼範例位於記憶體 .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-105">In the example provider component, a code example showing memory allocation and freeing is in memory.cpp.</span></span> <span data-ttu-id="9d8a7-106">下表列出支援的常式。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="9d8a7-107">項目</span><span class="sxs-lookup"><span data-stu-id="9d8a7-107">Item</span></span>                | <span data-ttu-id="9d8a7-108">描述</span><span class="sxs-lookup"><span data-stu-id="9d8a7-108">Description</span></span>                                                           |
|---------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9d8a7-109">**AllocProvMem**</span><span class="sxs-lookup"><span data-stu-id="9d8a7-109">**AllocProvMem**</span></span>    | <span data-ttu-id="9d8a7-110">配置指定的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-110">Allocate specified memory.</span></span>                                            |
| <span data-ttu-id="9d8a7-111">**FreeProvMem**</span><span class="sxs-lookup"><span data-stu-id="9d8a7-111">**FreeProvMem**</span></span>     | <span data-ttu-id="9d8a7-112">指出的可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-112">Free memory indicated.</span></span>                                                |
| <span data-ttu-id="9d8a7-113">**ReallocProvMem**</span><span class="sxs-lookup"><span data-stu-id="9d8a7-113">**ReallocProvMem**</span></span>  | <span data-ttu-id="9d8a7-114">配置連續的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-114">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="9d8a7-115">**AllocProvStr**</span><span class="sxs-lookup"><span data-stu-id="9d8a7-115">**AllocProvStr**</span></span>    | <span data-ttu-id="9d8a7-116">配置 LPWSTR 字串。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-116">Allocate an LPWSTR string.</span></span>                                            |
| <span data-ttu-id="9d8a7-117">**FreeProvStr**</span><span class="sxs-lookup"><span data-stu-id="9d8a7-117">**FreeProvStr**</span></span>     | <span data-ttu-id="9d8a7-118">如果尚未釋出，則為可用字串。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-118">Free string if not already freed.</span></span>                                     |
| <span data-ttu-id="9d8a7-119">**ReallocProvStr**</span><span class="sxs-lookup"><span data-stu-id="9d8a7-119">**ReallocProvStr**</span></span>  | <span data-ttu-id="9d8a7-120">配置連續的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-120">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="9d8a7-121">**ProvAllocString**</span><span class="sxs-lookup"><span data-stu-id="9d8a7-121">**ProvAllocString**</span></span> | <span data-ttu-id="9d8a7-122">驗證字串和第一個參數。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-122">Verifies string and first parameter.</span></span> <span data-ttu-id="9d8a7-123">如果沒問題，則會執行配置。</span><span class="sxs-lookup"><span data-stu-id="9d8a7-123">If OK, then performs allocation.</span></span> |



 

 

 




