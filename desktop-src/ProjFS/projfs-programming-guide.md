---
title: 投射的檔案系統程式設計指南
description: 有關執行 ProjFS 提供者應用程式的概念資訊。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: a6b2d186ac3e674c3fa68e17ecd523b2c94f2401
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023793"
---
# <a name="projected-file-system-projfs-programming-guide"></a><span data-ttu-id="5600b-103">投射的檔案系統 (ProjFS) 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="5600b-103">Projected File System (ProjFS) programming guide</span></span>

<span data-ttu-id="5600b-104">Windows 投射的檔案系統 (ProjFS) 允許名為「提供者」的使用者模式應用程式將階層式資料投射到檔案系統，使其顯示為檔案系統中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="5600b-104">The Windows Projected File System (ProjFS) allows a user-mode application called a "provider" to project hierarchical data into the file system, making it appear as files and directories in the file system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5600b-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="5600b-105">In this section</span></span>

| <span data-ttu-id="5600b-106">主題</span><span class="sxs-lookup"><span data-stu-id="5600b-106">Topic</span></span>                                                                                                       | <span data-ttu-id="5600b-107">描述</span><span class="sxs-lookup"><span data-stu-id="5600b-107">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="5600b-108">提供者總覽</span><span class="sxs-lookup"><span data-stu-id="5600b-108">Provider Overview</span></span>](provider-overview.md)                                                                   | <span data-ttu-id="5600b-109">提供者應用程式的概念總覽。</span><span class="sxs-lookup"><span data-stu-id="5600b-109">Conceptual overview of a provider application.</span></span>
| [<span data-ttu-id="5600b-110">虛擬化根中的快取狀態</span><span class="sxs-lookup"><span data-stu-id="5600b-110">Cache State in the Virtualization Root</span></span>](cache-state.md)                                                    | <span data-ttu-id="5600b-111">描述不同的快取狀態：提供者所管理的檔案或目錄可能具有。</span><span class="sxs-lookup"><span data-stu-id="5600b-111">Describes the different cache states a file or directory managed by the provider may have.</span></span> 
| [<span data-ttu-id="5600b-112">啟用 Windows 投射的檔案系統</span><span class="sxs-lookup"><span data-stu-id="5600b-112">Enabling Windows Projected File System</span></span>](enabling-windows-projected-file-system.md)                         | <span data-ttu-id="5600b-113">說明如何啟用 ProjFS 選用元件。</span><span class="sxs-lookup"><span data-stu-id="5600b-113">Describes how to enable the ProjFS optional component.</span></span>
| [<span data-ttu-id="5600b-114">虛擬化實例生命週期</span><span class="sxs-lookup"><span data-stu-id="5600b-114">Virtualization Instance Lifecycle</span></span>](virtualization-instance-lifecycle.md)                                   | <span data-ttu-id="5600b-115">ProjFS 虛擬化實例的生命週期總覽。</span><span class="sxs-lookup"><span data-stu-id="5600b-115">Overview of the lifecycle of a ProjFS virtualization instance.</span></span>
| [<span data-ttu-id="5600b-116">列舉檔案和目錄</span><span class="sxs-lookup"><span data-stu-id="5600b-116">Enumerating Files and Directories</span></span>](enumerating-files-and-directories.md)                                   | <span data-ttu-id="5600b-117">描述 ProjFS 提供者如何參與目錄列舉。</span><span class="sxs-lookup"><span data-stu-id="5600b-117">Describes how a ProjFS provider participates in directory enumeration.</span></span>
| [<span data-ttu-id="5600b-118">提供檔案資料</span><span class="sxs-lookup"><span data-stu-id="5600b-118">Providing File Data</span></span>](providing-file-data.md)                                                               | <span data-ttu-id="5600b-119">描述提供者如何提供預留位置資訊和檔案資料。</span><span class="sxs-lookup"><span data-stu-id="5600b-119">Describes how a provider supplies placeholder info and file data.</span></span>
| [<span data-ttu-id="5600b-120">檔案系統作業通知</span><span class="sxs-lookup"><span data-stu-id="5600b-120">File System Operation Notifications</span></span>](file-system-operation-notifications.md)                               | <span data-ttu-id="5600b-121">描述提供者如何接收檔案系統作業的通知。</span><span class="sxs-lookup"><span data-stu-id="5600b-121">Describes how a provider can receive notifications of file system operations.</span></span>
| [<span data-ttu-id="5600b-122">處理視圖變更</span><span class="sxs-lookup"><span data-stu-id="5600b-122">Handling View Changes</span></span>](handling-view-changes.md)                                                           | <span data-ttu-id="5600b-123">說明如何更新提供者備份存放區的用戶端視圖。</span><span class="sxs-lookup"><span data-stu-id="5600b-123">Describes how to update the client view of a provider's backing store.</span></span>
| [<span data-ttu-id="5600b-124">非同步回呼處理</span><span class="sxs-lookup"><span data-stu-id="5600b-124">Asynchronous Callback Handling</span></span>](asynchronous-callback-handling.md)                                         | <span data-ttu-id="5600b-125">描述提供者如何以非同步方式服務回呼。</span><span class="sxs-lookup"><span data-stu-id="5600b-125">Describes how the provider can asynchronously service callbacks.</span></span>
| [<span data-ttu-id="5600b-126">Windows 投射的檔案系統 API 參考</span><span class="sxs-lookup"><span data-stu-id="5600b-126">Windows Projected File System API Reference</span></span>](/windows/desktop/api/_projfs) | <span data-ttu-id="5600b-127">ProjFS 程式設計介面的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="5600b-127">Reference information for the ProjFS programming interface.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5600b-128">其他資源</span><span class="sxs-lookup"><span data-stu-id="5600b-128">Additional Resources</span></span>

|                                                                                                              |                                                                                   |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="5600b-129">RegFS 範例</span><span class="sxs-lookup"><span data-stu-id="5600b-129">RegFS Sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/ProjectedFileSystem) | <span data-ttu-id="5600b-130">將 Windows 登錄投射到檔案系統的範例 ProjFS 提供者。</span><span class="sxs-lookup"><span data-stu-id="5600b-130">A sample ProjFS provider that projects the Windows registry into the file system.</span></span> |
<!--
| [ProjFS.Managed API](https://github.com/Microsoft/URL_TBD)                                                   | A .NET wrapper for the ProjFS API.                                                |
-->