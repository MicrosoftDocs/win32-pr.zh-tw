---
title: 套件資源索引 (PRI) 參考
description: .
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75c0739b4e7673863a21223fbed749c27e65dc4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933241"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="37646-103">套件資源索引 (PRI) 參考</span><span class="sxs-lookup"><span data-stu-id="37646-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="37646-104">使用資源索引子的一組 Api。</span><span class="sxs-lookup"><span data-stu-id="37646-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="37646-105">資源索引子可用來產生 UWP 應用程式 (PRI) 檔的套件資源索引。</span><span class="sxs-lookup"><span data-stu-id="37646-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="37646-106">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="37646-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="37646-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="37646-107">In this section</span></span>

<span data-ttu-id="37646-108">**函數**</span><span class="sxs-lookup"><span data-stu-id="37646-108">**Functions**</span></span>

-   <span data-ttu-id="37646-109">[**MrmCreateConfig**](mrmcreateconfig.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="37646-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="37646-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="37646-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="37646-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="37646-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="37646-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="37646-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="37646-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="37646-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="37646-119">[**MrmDumpPriFile**](mrmdumpprifile.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="37646-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="37646-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="37646-122">[**MrmFreeMemory**](mrmfreememory.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="37646-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="37646-124">[**MrmIndexFile**](mrmindexfile.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="37646-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="37646-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="37646-127">[**MrmIndexString**](mrmindexstring.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="37646-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) 函式</span><span class="sxs-lookup"><span data-stu-id="37646-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="37646-129">**結構**</span><span class="sxs-lookup"><span data-stu-id="37646-129">**Structures**</span></span>

-   <span data-ttu-id="37646-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) 結構</span><span class="sxs-lookup"><span data-stu-id="37646-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="37646-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) 結構</span><span class="sxs-lookup"><span data-stu-id="37646-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="37646-132">**列舉**</span><span class="sxs-lookup"><span data-stu-id="37646-132">**Enumerations**</span></span>

-   <span data-ttu-id="37646-133">[**MrmDumpType**](mrmdumptype.md) 列舉</span><span class="sxs-lookup"><span data-stu-id="37646-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="37646-134">[**MrmPackagingMode**](mrmpackagingmode.md) 列舉</span><span class="sxs-lookup"><span data-stu-id="37646-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="37646-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) 列舉</span><span class="sxs-lookup"><span data-stu-id="37646-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="37646-136">[**MrmPlatformVersion**](mrmplatformversion.md) 列舉</span><span class="sxs-lookup"><span data-stu-id="37646-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="37646-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) 列舉</span><span class="sxs-lookup"><span data-stu-id="37646-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 