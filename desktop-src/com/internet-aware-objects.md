---
title: Internet-Aware 物件
description: Internet-Aware 物件
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933659"
---
# <a name="internet-aware-objects"></a><span data-ttu-id="0d871-103">Internet-Aware 物件</span><span class="sxs-lookup"><span data-stu-id="0d871-103">Internet-Aware Objects</span></span>

<span data-ttu-id="0d871-104">某些類別會識別為涵蓋持續性介面;這是因為定義控制項在網際網路上的運作方式所造成的。</span><span class="sxs-lookup"><span data-stu-id="0d871-104">There are certain categories identified to cover the persistency interfaces; these have been identified as a result of defining how controls function across the Internet.</span></span> <span data-ttu-id="0d871-105">不支援完整範圍持續性介面的容器應確定它不會裝載需要不支援的介面組合的控制項。</span><span class="sxs-lookup"><span data-stu-id="0d871-105">A container that does not support the full range of persistency interfaces should ensure that it does not host a control that requires a combination of interfaces that it does not support.</span></span>

<span data-ttu-id="0d871-106">下表說明各種類別的意義，這兩個類別都是已實和必要的類別。</span><span class="sxs-lookup"><span data-stu-id="0d871-106">The following tables describe the meaning for various categories as both implemented and required categories.</span></span>



| <span data-ttu-id="0d871-107">必要類別</span><span class="sxs-lookup"><span data-stu-id="0d871-107">Required Categories</span></span>                                                                                                                                                                                | <span data-ttu-id="0d871-108">Description</span><span class="sxs-lookup"><span data-stu-id="0d871-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d871-109">CATID \_ PersistsToMoniker、catid \_ PERSISTSTOSTREAMINIT、catid \_ PersisitsToStream、CATID \_ PersistsToStorage、CATID \_ PERSISTSTOMEMORY、catid \_ PersistsToFile、catid \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0d871-109">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersisitsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0d871-110">這些類別中的每一個都是互斥的，只有在物件只支援一個持續性機制時，才會使用，因此會) 相互排除的 (。</span><span class="sxs-lookup"><span data-stu-id="0d871-110">Each of these categories is mutually exclusive and only used when an object supports only one persistence mechanism at all (hence the mutual exclusion).</span></span> <span data-ttu-id="0d871-111">不支援其中一個類別所描述之持續性機制的容器，應該防止自己建立任何類別的物件，因此會標示出來。</span><span class="sxs-lookup"><span data-stu-id="0d871-111">Containers that do not support the persistence mechanism described by one of these categories should prevent themselves from creating any objects of classes so marked.</span></span><br/> |
| <span data-ttu-id="0d871-112">CATID \_ RequiresDataPathHost</span><span class="sxs-lookup"><span data-stu-id="0d871-112">CATID\_RequiresDataPathHost</span></span><br/>                                                                                                                                                             | <span data-ttu-id="0d871-113">物件需要能夠將資料儲存至一或多個路徑，而且需要容器介入，因此需要 [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85))的容器支援。</span><span class="sxs-lookup"><span data-stu-id="0d871-113">The object requires the ability to save data to one or more paths and requires container involvement, therefore requiring container support for [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span></span><br/>                                                                                                                                  |



 



| <span data-ttu-id="0d871-114">實作為類別</span><span class="sxs-lookup"><span data-stu-id="0d871-114">Implemented Categories</span></span>                                                                                                                                                                            | <span data-ttu-id="0d871-115">Description</span><span class="sxs-lookup"><span data-stu-id="0d871-115">Description</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d871-116">CATID \_ PersistsToMoniker、catid \_ PERSISTSTOSTREAMINIT、catid \_ PersistsToStream、CATID \_ PersistsToStorage、CATID \_ PERSISTSTOMEMORY、catid \_ PersistsToFile、catid \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0d871-116">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersistsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0d871-117">物件支援類別的對應 IPersist \* 機制。</span><span class="sxs-lookup"><span data-stu-id="0d871-117">Object supports the corresponding IPersist\* mechanism for the category.</span></span><br/> |



 

<span data-ttu-id="0d871-118">下表提供指派給每個類別目錄的確切 Catid：</span><span class="sxs-lookup"><span data-stu-id="0d871-118">The following table provides the exact CATIDs assigned to each category:</span></span>



| <span data-ttu-id="0d871-119">類別</span><span class="sxs-lookup"><span data-stu-id="0d871-119">Category</span></span>                                | <span data-ttu-id="0d871-120">CATID</span><span class="sxs-lookup"><span data-stu-id="0d871-120">CATID</span></span>                                           |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="0d871-121">CATID \_ RequiresDataPathHost</span><span class="sxs-lookup"><span data-stu-id="0d871-121">CATID\_RequiresDataPathHost</span></span><br/>  | <span data-ttu-id="0d871-122">0de86a50-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d871-122">0de86a50-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d871-123">CATID \_ PersistsToMoniker</span><span class="sxs-lookup"><span data-stu-id="0d871-123">CATID\_PersistsToMoniker</span></span> <br/>    | <span data-ttu-id="0d871-124">0de86a51-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d871-124">0de86a51-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d871-125">CATID \_ PersistsToStorage</span><span class="sxs-lookup"><span data-stu-id="0d871-125">CATID\_PersistsToStorage</span></span> <br/>    | <span data-ttu-id="0d871-126">0de86a52-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d871-126">0de86a52-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d871-127">CATID \_ PersistsToStreamInit</span><span class="sxs-lookup"><span data-stu-id="0d871-127">CATID\_PersistsToStreamInit</span></span> <br/> | <span data-ttu-id="0d871-128">0de86a53-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d871-128">0de86a53-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d871-129">CATID \_ PersistsToStream</span><span class="sxs-lookup"><span data-stu-id="0d871-129">CATID\_PersistsToStream</span></span> <br/>     | <span data-ttu-id="0d871-130">0de86a54-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d871-130">0de86a54-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d871-131">CATID \_ PersistsToMemory</span><span class="sxs-lookup"><span data-stu-id="0d871-131">CATID\_PersistsToMemory</span></span> <br/>     | <span data-ttu-id="0d871-132">0de86a55-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d871-132">0de86a55-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d871-133">CATID \_ PersistsToFile</span><span class="sxs-lookup"><span data-stu-id="0d871-133">CATID\_PersistsToFile</span></span> <br/>       | <span data-ttu-id="0d871-134">0de86a56-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d871-134">0de86a56-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d871-135">CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0d871-135">CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0d871-136">0de86a57-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d871-136">0de86a57-2baa-11cf-a229-00aa003d7352</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0d871-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d871-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d871-138">元件類別</span><span class="sxs-lookup"><span data-stu-id="0d871-138">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

