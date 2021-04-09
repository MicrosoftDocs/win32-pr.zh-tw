---
title: Windows 投射的檔案系統
description: '介紹 Windows 投射的檔案系統 (ProjFS) '
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 8391ec63f23c9ebae5b47e4cac862f6ab3079ceb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842375"
---
# <a name="windows-projected-file-system-projfs"></a><span data-ttu-id="f556f-103">Windows 投射的檔案系統 (ProjFS) </span><span class="sxs-lookup"><span data-stu-id="f556f-103">Windows Projected File System (ProjFS)</span></span>

<span data-ttu-id="f556f-104">Windows 投射的檔案系統 (ProjFS) 允許名為「提供者」的使用者模式應用程式，將階層式資料從支援資料存放區投射到檔案系統，使其顯示為檔案系統中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="f556f-104">The Windows Projected File System (ProjFS) allows a user-mode application called a "provider" to project hierarchical data from a backing data store into the file system, making it appear as files and directories in the file system.</span></span> <span data-ttu-id="f556f-105">例如，簡單的提供者可以將 Windows 登錄投射到檔案系統中，讓登錄機碼和值分別顯示為檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="f556f-105">For example, a simple provider could project the Windows registry into the file system, making registry keys and values appear as files and directories, respectively.</span></span> <span data-ttu-id="f556f-106">更複雜的提供者範例是 [適用于 git 的 VFS](https://github.com/Microsoft/VFSForGit)，可用來將非常大型的 git 存放庫虛擬化。</span><span class="sxs-lookup"><span data-stu-id="f556f-106">An example of a more complex provider is [VFS for Git](https://github.com/Microsoft/VFSForGit), which is used to virtualize very large git repos.</span></span>

> [!NOTE]
> <span data-ttu-id="f556f-107">ProjFS 的設計目的是要搭配高速支援資料存放區使用。</span><span class="sxs-lookup"><span data-stu-id="f556f-107">ProjFS is designed for use with high-speed backing data stores.</span></span> <span data-ttu-id="f556f-108">其中一個設計目標是要讓投射的資料看起來像是在本機出現，並隱藏資料可能是遠端的事實。</span><span class="sxs-lookup"><span data-stu-id="f556f-108">One of its design goals is to make the projected data appear as if it were locally present, hiding the fact that the data may be remote.</span></span> <span data-ttu-id="f556f-109">因此，ProjFS 並不提供：報告資料回收進度的機制;指出檔案的線上與離線狀態;以及當您使用緩慢的支援資料存放區時，可能需要的其他功能。</span><span class="sxs-lookup"><span data-stu-id="f556f-109">As such, ProjFS doesn't provide: mechanisms for reporting progress of data recall; indication of the online versus offline state of a file; nor other features that may be desirable when working with backing data stores that are slow.</span></span> <span data-ttu-id="f556f-110">在這類情況下，請考慮改為使用 [雲端檔案 API](../cfapi/cloud-files-api-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="f556f-110">For such scenarios, consider instead using the [Cloud Files API](../cfapi/cloud-files-api-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f556f-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="f556f-111">In this section</span></span>

| <span data-ttu-id="f556f-112">主題</span><span class="sxs-lookup"><span data-stu-id="f556f-112">Topic</span></span>                                                                                                       | <span data-ttu-id="f556f-113">描述</span><span class="sxs-lookup"><span data-stu-id="f556f-113">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="f556f-114">Windows 投射的檔案系統程式設計指南</span><span class="sxs-lookup"><span data-stu-id="f556f-114">Windows Projected File System Programming Guide</span></span>](projfs-programming-guide.md)                              | <span data-ttu-id="f556f-115">有關執行 ProjFS 提供者應用程式的概念資訊。</span><span class="sxs-lookup"><span data-stu-id="f556f-115">Conceptual information on implementing a ProjFS provider application.</span></span>
| [<span data-ttu-id="f556f-116">Windows 投射的檔案系統 API 參考</span><span class="sxs-lookup"><span data-stu-id="f556f-116">Windows Projected File System API Reference</span></span>](projfs-reference.md)                                          | <span data-ttu-id="f556f-117">ProjFS 程式設計介面的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="f556f-117">Reference information for the ProjFS programming interface.</span></span>
| [<span data-ttu-id="f556f-118">Windows 投射的檔案系統詞彙</span><span class="sxs-lookup"><span data-stu-id="f556f-118">Windows Projected File System glossary</span></span>](projfs-glossary.md)                                                | <span data-ttu-id="f556f-119">ProjFS 中使用的特殊字詞。</span><span class="sxs-lookup"><span data-stu-id="f556f-119">Special terms used in ProjFS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f556f-120">其他資源</span><span class="sxs-lookup"><span data-stu-id="f556f-120">Additional Resources</span></span>

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="f556f-121">RegFS 範例</span><span class="sxs-lookup"><span data-stu-id="f556f-121">RegFS Sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | <span data-ttu-id="f556f-122">將 Windows 登錄投射到檔案系統的範例 ProjFS 提供者。</span><span class="sxs-lookup"><span data-stu-id="f556f-122">A sample ProjFS provider that projects the Windows registry into the file system.</span></span> |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->