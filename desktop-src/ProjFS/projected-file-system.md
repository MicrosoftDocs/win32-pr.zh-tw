---
title: Windows 投射的檔案系統
description: '介紹 Windows 投射的檔案系統 (ProjFS) '
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/14/2018
ms.topic: article
ms.openlocfilehash: 68f121162efdf75fb9226b41f9b3a1121bef6480
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120583"
---
# <a name="windows-projected-file-system-projfs"></a><span data-ttu-id="1c616-103">Windows 投射的檔案系統 (ProjFS) </span><span class="sxs-lookup"><span data-stu-id="1c616-103">Windows Projected File System (ProjFS)</span></span>

<span data-ttu-id="1c616-104">Windows 投射的檔案系統 (ProjFS) 允許名為「提供者」的使用者模式應用程式，將階層式資料從支援資料存放區投射到檔案系統，使其顯示為檔案系統中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="1c616-104">The Windows Projected File System (ProjFS) allows a user-mode application called a "provider" to project hierarchical data from a backing data store into the file system, making it appear as files and directories in the file system.</span></span> <span data-ttu-id="1c616-105">例如，簡單的提供者可以將 Windows 登錄投射到檔案系統中，讓登錄機碼和值分別顯示為檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="1c616-105">For example, a simple provider could project the Windows registry into the file system, making registry keys and values appear as files and directories, respectively.</span></span> <span data-ttu-id="1c616-106">更複雜的提供者範例是 [適用于 git 的 VFS](https://github.com/Microsoft/VFSForGit)，可用來將非常大型的 git 存放庫虛擬化。</span><span class="sxs-lookup"><span data-stu-id="1c616-106">An example of a more complex provider is [VFS for Git](https://github.com/Microsoft/VFSForGit), which is used to virtualize very large git repos.</span></span>

> [!NOTE]
> <span data-ttu-id="1c616-107">ProjFS 的設計目的是要搭配高速支援資料存放區使用。</span><span class="sxs-lookup"><span data-stu-id="1c616-107">ProjFS is designed for use with high-speed backing data stores.</span></span> <span data-ttu-id="1c616-108">其中一個設計目標是要讓投射的資料看起來像是在本機出現，並隱藏資料可能是遠端的事實。</span><span class="sxs-lookup"><span data-stu-id="1c616-108">One of its design goals is to make the projected data appear as if it were locally present, hiding the fact that the data may be remote.</span></span> <span data-ttu-id="1c616-109">因此，ProjFS 並不提供：報告資料回收進度的機制;指出檔案的線上與離線狀態;以及當您使用緩慢的支援資料存放區時，可能需要的其他功能。</span><span class="sxs-lookup"><span data-stu-id="1c616-109">As such, ProjFS doesn't provide: mechanisms for reporting progress of data recall; indication of the online versus offline state of a file; nor other features that may be desirable when working with backing data stores that are slow.</span></span> <span data-ttu-id="1c616-110">在這類情況下，請考慮改為使用 [雲端檔案 API](../cfapi/cloud-files-api-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="1c616-110">For such scenarios, consider instead using the [Cloud Files API](../cfapi/cloud-files-api-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1c616-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="1c616-111">In this section</span></span>

| <span data-ttu-id="1c616-112">主題</span><span class="sxs-lookup"><span data-stu-id="1c616-112">Topic</span></span>                                                                                                       | <span data-ttu-id="1c616-113">描述</span><span class="sxs-lookup"><span data-stu-id="1c616-113">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="1c616-114">Windows 投射的檔案系統程式設計指南</span><span class="sxs-lookup"><span data-stu-id="1c616-114">Windows Projected File System Programming Guide</span></span>](projfs-programming-guide.md)                              | <span data-ttu-id="1c616-115">有關執行 ProjFS 提供者應用程式的概念資訊。</span><span class="sxs-lookup"><span data-stu-id="1c616-115">Conceptual information on implementing a ProjFS provider application.</span></span>
| [<span data-ttu-id="1c616-116">Windows 投射的檔案系統 API 參考</span><span class="sxs-lookup"><span data-stu-id="1c616-116">Windows Projected File System API Reference</span></span>](projfs-reference.md)                                          | <span data-ttu-id="1c616-117">ProjFS 程式設計介面的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="1c616-117">Reference information for the ProjFS programming interface.</span></span>
| [<span data-ttu-id="1c616-118">Windows 投射的檔案系統詞彙</span><span class="sxs-lookup"><span data-stu-id="1c616-118">Windows Projected File System glossary</span></span>](projfs-glossary.md)                                                | <span data-ttu-id="1c616-119">ProjFS 中使用的特殊字詞。</span><span class="sxs-lookup"><span data-stu-id="1c616-119">Special terms used in ProjFS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c616-120">其他資源</span><span class="sxs-lookup"><span data-stu-id="1c616-120">Additional Resources</span></span>

| <span data-ttu-id="1c616-121">主題</span><span class="sxs-lookup"><span data-stu-id="1c616-121">Topic</span></span>                                                                                                             | <span data-ttu-id="1c616-122">描述</span><span class="sxs-lookup"><span data-stu-id="1c616-122">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1c616-123">RegFS 範例</span><span class="sxs-lookup"><span data-stu-id="1c616-123">RegFS Sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | <span data-ttu-id="1c616-124">將 Windows 登錄投射到檔案系統的範例 ProjFS 提供者。</span><span class="sxs-lookup"><span data-stu-id="1c616-124">A sample ProjFS provider that projects the Windows registry into the file system.</span></span> |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->