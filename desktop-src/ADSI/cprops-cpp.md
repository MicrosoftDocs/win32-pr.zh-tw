---
title: CPROPS.Cpp
description: 在範例提供者元件中，可以在 cprops 中找到屬性快取執行的範例。 下表列出支援的方法。
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839216"
---
# <a name="cpropscpp"></a><span data-ttu-id="0ac41-104">CPROPS.Cpp</span><span class="sxs-lookup"><span data-stu-id="0ac41-104">CPROPS.CPP</span></span>

<span data-ttu-id="0ac41-105">在範例提供者元件中，可以在 cprops 中找到屬性快取執行的範例。</span><span class="sxs-lookup"><span data-stu-id="0ac41-105">In the example provider component, an example of a property cache implementation can be found in cprops.cpp.</span></span> <span data-ttu-id="0ac41-106">下表列出支援的方法。</span><span class="sxs-lookup"><span data-stu-id="0ac41-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="0ac41-107">方法</span><span class="sxs-lookup"><span data-stu-id="0ac41-107">Method</span></span>                                           | <span data-ttu-id="0ac41-108">描述</span><span class="sxs-lookup"><span data-stu-id="0ac41-108">Description</span></span>                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac41-109">**CPropertyCache：： addproperty**</span><span class="sxs-lookup"><span data-stu-id="0ac41-109">**CPropertyCache::addproperty**</span></span>                  | <span data-ttu-id="0ac41-110">藉由加入新的屬性快取來擴充它。</span><span class="sxs-lookup"><span data-stu-id="0ac41-110">Extend the property cache by adding a new one.</span></span>                                                                      |
| <span data-ttu-id="0ac41-111">**CPropertyCache::updateproperty**</span><span class="sxs-lookup"><span data-stu-id="0ac41-111">**CPropertyCache::updateproperty**</span></span>               | <span data-ttu-id="0ac41-112">查閱屬性，釋出其內容，並改用新的值;然後，將此屬性的快取標記為已變更。</span><span class="sxs-lookup"><span data-stu-id="0ac41-112">Look up the property, free its contents, and use new values instead; then mark the cache changed for this property.</span></span> |
| <span data-ttu-id="0ac41-113">**CPropertyCache::findproperty**</span><span class="sxs-lookup"><span data-stu-id="0ac41-113">**CPropertyCache::findproperty**</span></span>                 | <span data-ttu-id="0ac41-114">依名稱查閱此屬性;儲存其索引。</span><span class="sxs-lookup"><span data-stu-id="0ac41-114">Look up this property by name; save its index.</span></span>                                                                      |
| <span data-ttu-id="0ac41-115">**CPropertyCache：： getproperty**</span><span class="sxs-lookup"><span data-stu-id="0ac41-115">**CPropertyCache::getproperty**</span></span>                  | <span data-ttu-id="0ac41-116">在快取中尋找屬性（如果有的話），否則呼叫 **GetInfo**。</span><span class="sxs-lookup"><span data-stu-id="0ac41-116">Find the property in the cache if available, otherwise call **GetInfo**.</span></span> <span data-ttu-id="0ac41-117">設定索引，並複製新值。</span><span class="sxs-lookup"><span data-stu-id="0ac41-117">Set the index and copy in the new values.</span></span>  |
| <span data-ttu-id="0ac41-118">**CPropertyCache：:p utproperty**</span><span class="sxs-lookup"><span data-stu-id="0ac41-118">**CPropertyCache::putproperty**</span></span>                  | <span data-ttu-id="0ac41-119">尋找屬性。</span><span class="sxs-lookup"><span data-stu-id="0ac41-119">Find the property.</span></span> <span data-ttu-id="0ac41-120">釋出，並放入新值。</span><span class="sxs-lookup"><span data-stu-id="0ac41-120">Free what was there and put in new values.</span></span>                                                       |
| <span data-ttu-id="0ac41-121">**CPropertyCache::CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="0ac41-121">**CPropertyCache::CPropertyCache**</span></span>               | <span data-ttu-id="0ac41-122">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="0ac41-122">Standard constructor.</span></span>                                                                                               |
| <span data-ttu-id="0ac41-123">**CPropertyCache：： ~ CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="0ac41-123">**CPropertyCache::~CPropertyCache**</span></span>              | <span data-ttu-id="0ac41-124">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="0ac41-124">Standard destructor.</span></span>                                                                                                |
| <span data-ttu-id="0ac41-125">**CPropertyCache::createpropertycache**</span><span class="sxs-lookup"><span data-stu-id="0ac41-125">**CPropertyCache::createpropertycache**</span></span>          | <span data-ttu-id="0ac41-126">建立快取。</span><span class="sxs-lookup"><span data-stu-id="0ac41-126">Create the cache.</span></span>                                                                                                   |
| <span data-ttu-id="0ac41-127">**CPropertyCache::unboundgetproperty**</span><span class="sxs-lookup"><span data-stu-id="0ac41-127">**CPropertyCache::unboundgetproperty**</span></span>           | <span data-ttu-id="0ac41-128">在快取中尋找屬性，並將它設定為這些值。</span><span class="sxs-lookup"><span data-stu-id="0ac41-128">Find the property in the cache and set it to these values.</span></span>                                                          |
| <span data-ttu-id="0ac41-129">**CPropertyCache::SampleDSMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="0ac41-129">**CPropertyCache::SampleDSMarshallProperties**</span></span>   | <span data-ttu-id="0ac41-130">封送處理屬性資料和值。</span><span class="sxs-lookup"><span data-stu-id="0ac41-130">Marshal property data and values.</span></span>                                                                                   |
| <span data-ttu-id="0ac41-131">**CPropertyCache::marshallproperty**</span><span class="sxs-lookup"><span data-stu-id="0ac41-131">**CPropertyCache::marshallproperty**</span></span>             | <span data-ttu-id="0ac41-132">封送處理屬性。</span><span class="sxs-lookup"><span data-stu-id="0ac41-132">Marshal a property.</span></span>                                                                                                 |
| <span data-ttu-id="0ac41-133">**CPropertyCache::SampleDSUnMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="0ac41-133">**CPropertyCache::SampleDSUnMarshallProperties**</span></span> | <span data-ttu-id="0ac41-134">Unmarshal 屬性資料和值。</span><span class="sxs-lookup"><span data-stu-id="0ac41-134">Unmarshal property data and values.</span></span>                                                                                 |
| <span data-ttu-id="0ac41-135">**CPropertyCache::unmarshallproperty**</span><span class="sxs-lookup"><span data-stu-id="0ac41-135">**CPropertyCache::unmarshallproperty**</span></span>           | <span data-ttu-id="0ac41-136">Unmarshal 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ac41-136">Unmarshal a property.</span></span>                                                                                               |



 

 

 




