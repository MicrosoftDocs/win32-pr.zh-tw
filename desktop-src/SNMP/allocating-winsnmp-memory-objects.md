---
title: 配置的 WinSNMP 記憶體物件
description: 描述元、資源控制碼和 C 樣式字串是在 WinSNMP 程式設計環境中的三種記憶體物件類型。
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020774"
---
# <a name="allocating-winsnmp-memory-objects"></a><span data-ttu-id="4939d-103">配置的 WinSNMP 記憶體物件</span><span class="sxs-lookup"><span data-stu-id="4939d-103">Allocating WinSNMP Memory Objects</span></span>

<span data-ttu-id="4939d-104">描述元、資源控制碼和 C 樣式字串是在 WinSNMP 程式設計環境中的三種記憶體物件類型。</span><span class="sxs-lookup"><span data-stu-id="4939d-104">Descriptors, resource handles and C-style strings are the three types of memory objects in the WinSNMP programming environment.</span></span>

<span data-ttu-id="4939d-105">物件的類型會決定 Microsoft WinSNMP 執行或 WinSNMP 應用程式是否配置並解除配置物件的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4939d-105">The type of object determines whether the Microsoft WinSNMP implementation or the WinSNMP application allocates and deallocates the memory for the object.</span></span> <span data-ttu-id="4939d-106">這可減少暫存緩衝區空間的不必要配置，以及不必要的緩衝區複製。</span><span class="sxs-lookup"><span data-stu-id="4939d-106">This reduces unnecessary allocation of temporary buffer space and unnecessary copying of buffers.</span></span>

<span data-ttu-id="4939d-107">下表摘要說明如何配置和解除配置 WinSNMP 記憶體物件的資源。</span><span class="sxs-lookup"><span data-stu-id="4939d-107">The following table summarizes the allocation and deallocation of resources for WinSNMP memory objects.</span></span>



| <span data-ttu-id="4939d-108">物件型別</span><span class="sxs-lookup"><span data-stu-id="4939d-108">Object type</span></span>                                                                   | <span data-ttu-id="4939d-109">說明</span><span class="sxs-lookup"><span data-stu-id="4939d-109">Description</span></span>                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4939d-110">[**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 或 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 描述項</span><span class="sxs-lookup"><span data-stu-id="4939d-110">[**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor</span></span> | <span data-ttu-id="4939d-111">如果 WinSNMP 應用程式佈建記憶體，則必須呼叫適當的函式來解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="4939d-111">If the WinSNMP application allocates the memory, it must deallocate the memory with a call to an appropriate function.</span></span> <span data-ttu-id="4939d-112">如果執行配置記憶體，則應用程式必須呼叫 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) 函式來解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="4939d-112">If the implementation allocates the memory, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to deallocate the memory.</span></span> |
| <span data-ttu-id="4939d-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) 結構</span><span class="sxs-lookup"><span data-stu-id="4939d-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure</span></span>                                    | <span data-ttu-id="4939d-114">如果 **值** 成員是 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 或 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 描述元，則應用程式必須如上面所示針對描述項繼續進行。</span><span class="sxs-lookup"><span data-stu-id="4939d-114">If the **value** member is an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor, the application must proceed as indicated above for descriptors.</span></span>                                                                                                     |
| <span data-ttu-id="4939d-115">資源控制碼</span><span class="sxs-lookup"><span data-stu-id="4939d-115">Resource handle</span></span>                                                               | <span data-ttu-id="4939d-116">此實作為配置、管理和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4939d-116">The implementation allocates, manages, and frees the memory.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="4939d-117">C 樣式字串</span><span class="sxs-lookup"><span data-stu-id="4939d-117">C-style string</span></span>                                                                | <span data-ttu-id="4939d-118">WinSNMP 應用程式必須管理和釋放它所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4939d-118">The WinSNMP application must manage and free the memory it allocates.</span></span>                                                                                                                                                                                                                |



 

<span data-ttu-id="4939d-119">如需詳細資訊，請參閱 [釋放 WinSNMP 描述](freeing-winsnmp-descriptors.md)項。</span><span class="sxs-lookup"><span data-stu-id="4939d-119">For more information, see [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).</span></span>

 

 




