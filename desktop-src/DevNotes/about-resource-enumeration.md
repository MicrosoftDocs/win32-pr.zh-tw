---
description: 資源列舉可提供應用程式執行時所發生之檢測活動的關閉和精確查看。
ms.assetid: 4a421006-32ff-4555-a3c8-69fffdb46845
title: 關於資源列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601e65550dacbd07d493f35a6c35fece98657b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991617"
---
# <a name="about-resource-enumeration"></a><span data-ttu-id="a9f73-103">關於資源列舉</span><span class="sxs-lookup"><span data-stu-id="a9f73-103">About Resource Enumeration</span></span>

<span data-ttu-id="a9f73-104">資源列舉可提供應用程式執行時所發生之檢測活動的關閉和精確查看。</span><span class="sxs-lookup"><span data-stu-id="a9f73-104">Resource enumeration provides a close and precise view of instrumentation activity that takes place when an application is running.</span></span> <span data-ttu-id="a9f73-105">您可以在偵錯工具中，將檢測資訊抽象化並分類為一組處理常式特定的專案。</span><span class="sxs-lookup"><span data-stu-id="a9f73-105">The instrumentation information can be abstracted and categorized as a set of process-specific items as part of the debugging process.</span></span>

<span data-ttu-id="a9f73-106">工具（例如偵錯工具）通常需要存取檢測資訊，但可能會發現它無法使用。</span><span class="sxs-lookup"><span data-stu-id="a9f73-106">Tools, such as debuggers, often require access to instrumentation information but may find it is unavailable.</span></span> <span data-ttu-id="a9f73-107">為了解決這個問題， [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) 函式會從應用程式中解壓縮這類資訊，為所要進行的問題提供更佳的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="a9f73-107">To solve this problem, the [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) function extracts this type of information from applications to provide better context information for the problem being debugged.</span></span>

 

 



