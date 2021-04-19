---
description: 雲端篩選 API 會在使用者模式與檔案系統之間的界限提供功能。
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: 雲端同步引擎
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106985729"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="3d9b9-103">雲端同步引擎</span><span class="sxs-lookup"><span data-stu-id="3d9b9-103">Cloud Sync Engines</span></span>

<span data-ttu-id="3d9b9-104">另請參閱 [雲端鏡像範例](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample)。</span><span class="sxs-lookup"><span data-stu-id="3d9b9-104">Also see [Cloud Mirror sample](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span></span>

<span data-ttu-id="3d9b9-105">從 Windows 10 版本1709開始，Windows 提供雲端檔案 *API*。</span><span class="sxs-lookup"><span data-stu-id="3d9b9-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="3d9b9-106">此 API 是由數個原生 Win32 和 WinRT Api 所組成，可將雲端同步引擎的支援正規化，並處理工作，例如建立和管理預留位置檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="3d9b9-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="3d9b9-107">此 API 的使用者通常是同步處理提供者，以及某些範圍的 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3d9b9-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3d9b9-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="3d9b9-108">In this section</span></span>

| <span data-ttu-id="3d9b9-109">主題</span><span class="sxs-lookup"><span data-stu-id="3d9b9-109">Topic</span></span>                                                                | <span data-ttu-id="3d9b9-110">描述</span><span class="sxs-lookup"><span data-stu-id="3d9b9-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d9b9-111">建立支援預留位置檔案的雲端同步處理引擎</span><span class="sxs-lookup"><span data-stu-id="3d9b9-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="3d9b9-112">瞭解如何使用雲端檔案 API 來建立包含預留位置檔案和檔案總管整合的雲端檔案同步處理引擎。</span><span class="sxs-lookup"><span data-stu-id="3d9b9-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="3d9b9-113">雲端篩選參考</span><span class="sxs-lookup"><span data-stu-id="3d9b9-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="3d9b9-114">雲端篩選 API 是原生 WIN32 API，屬於更廣泛的雲端檔案 API。</span><span class="sxs-lookup"><span data-stu-id="3d9b9-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="3d9b9-115">雲端篩選 API 會在使用者模式與檔案系統之間的界限提供功能。</span><span class="sxs-lookup"><span data-stu-id="3d9b9-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="3d9b9-116">此 API 會處理預留位置檔案和目錄的建立和管理。</span><span class="sxs-lookup"><span data-stu-id="3d9b9-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |

