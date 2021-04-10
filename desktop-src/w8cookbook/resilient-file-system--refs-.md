---
title: 復原檔案系統
description: 復原檔案系統
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "104024271"
---
# <a name="resilient-file-system"></a><span data-ttu-id="49809-103">復原檔案系統</span><span class="sxs-lookup"><span data-stu-id="49809-103">Resilient file system</span></span>

## <a name="platform"></a><span data-ttu-id="49809-104">平台</span><span class="sxs-lookup"><span data-stu-id="49809-104">Platform</span></span>

<span data-ttu-id="49809-105">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49809-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="49809-106">Description</span><span class="sxs-lookup"><span data-stu-id="49809-106">Description</span></span>

<span data-ttu-id="49809-107">復原檔案系統 (ReFS) 是新的本機檔案系統。</span><span class="sxs-lookup"><span data-stu-id="49809-107">Resilient File System (ReFS) is a new local file system.</span></span> <span data-ttu-id="49809-108">它可將資料的可用性最大化，儘管過去發生的錯誤會造成資料遺失或停機。</span><span class="sxs-lookup"><span data-stu-id="49809-108">It maximizes data availability, despite errors that would historically cause data loss or downtime.</span></span> <span data-ttu-id="49809-109">資料完整性可確保商務關鍵資料受到保護，避免發生錯誤並可在需要時使用。</span><span class="sxs-lookup"><span data-stu-id="49809-109">Data integrity ensures that business critical data is protected from errors and available when needed.</span></span> <span data-ttu-id="49809-110">其架構的設計目的是為了在不斷成長的資料集大小和動態工作負載的時代提供可調整性和效能。</span><span class="sxs-lookup"><span data-stu-id="49809-110">Its architecture is designed to provide scalability and performance in an era of constantly growing data set sizes and dynamic workloads.</span></span>

<span data-ttu-id="49809-111">ReFS 的主要功能如下：</span><span class="sxs-lookup"><span data-stu-id="49809-111">The key features of ReFS are:</span></span>

-   <span data-ttu-id="49809-112">**完整性**： ReFS 會儲存資料，以防止許多可能導致資料遺失的常見錯誤。</span><span class="sxs-lookup"><span data-stu-id="49809-112">**Integrity**: ReFS stores data so that it is protected from many of the common errors that can cause data loss.</span></span> <span data-ttu-id="49809-113">檔案系統中繼資料一律受到保護。</span><span class="sxs-lookup"><span data-stu-id="49809-113">File system metadata is always protected.</span></span> <span data-ttu-id="49809-114">（選擇性）您可以針對每個磁片區、每個目錄或每個檔案來保護使用者資料。</span><span class="sxs-lookup"><span data-stu-id="49809-114">Optionally, user data can be protected on a per-volume, per-directory, or per-file basis.</span></span> <span data-ttu-id="49809-115">如果發生損毀，ReFS 可以偵測到，當設定儲存空間時，會自動校正損毀。</span><span class="sxs-lookup"><span data-stu-id="49809-115">If corruption occurs, ReFS can detect and, when configured with Storage Spaces, automatically correct the corruption.</span></span> <span data-ttu-id="49809-116">發生系統錯誤時，ReFS 的設計是為了快速從該錯誤復原，而不會遺失使用者資料。</span><span class="sxs-lookup"><span data-stu-id="49809-116">In the event of a system error, ReFS is designed to recover from that error rapidly, with no loss of user data.</span></span>
-   <span data-ttu-id="49809-117">**可用性**： ReFS 的設計目的是要排定資料的可用性。</span><span class="sxs-lookup"><span data-stu-id="49809-117">**Availability**: ReFS is designed to prioritize the availability of data.</span></span> <span data-ttu-id="49809-118">使用 ReFS 時，如果發生損毀，而且無法自動修復，線上搶救程式就會當地語系化為損毀區域，而且不需要任何磁片區停機時間。</span><span class="sxs-lookup"><span data-stu-id="49809-118">With ReFS, if corruption occurs, and it cannot be repaired automatically, the online salvage process is localized to the area of corruption, requiring no volume down-time.</span></span> <span data-ttu-id="49809-119">簡言之，如果發生損毀，ReFS 將保持連線。</span><span class="sxs-lookup"><span data-stu-id="49809-119">In short, if corruption occurs, ReFS will stay online.</span></span>
-   <span data-ttu-id="49809-120">擴充 **性**： ReFS 是針對目前的資料集大小和明天的資料集大小所設計。它已針對高擴充性優化。</span><span class="sxs-lookup"><span data-stu-id="49809-120">**Scalability**: ReFS is designed for the data set sizes of today and the data set sizes of tomorrow; it’s optimized for high scalability.</span></span>
-   <span data-ttu-id="49809-121">**應用程式相容性**：若要最大化 AppCompat，REFS 支援 NTFS 功能的子集，以及廣泛採用的 Win32 api。</span><span class="sxs-lookup"><span data-stu-id="49809-121">**App Compatibility**: To maximize AppCompat, ReFS supports a subset of NTFS features plus Win32 APIs that are widely adopted.</span></span>
-   <span data-ttu-id="49809-122">**主動式錯誤識別**： ReFS 的完整性功能是透過資料完整性掃描器來利用 (「清除程式」 ) 會定期掃描磁片區、嘗試找出潛在損毀，然後主動觸發修復損毀的資料。</span><span class="sxs-lookup"><span data-stu-id="49809-122">**Proactive Error Identification**: The integrity capabilities of ReFS are leveraged by a data integrity scanner (a “scrubber”) that periodically scans the volume, attempts to identify latent corruption, and then proactively triggers a repair of that corrupt data.</span></span>

## <a name="resources"></a><span data-ttu-id="49809-123">資源</span><span class="sxs-lookup"><span data-stu-id="49809-123">Resources</span></span>

-   [<span data-ttu-id="49809-124">建立 Windows 8 的 Blog 文章–為 Windows 建立新一代的檔案系統： ReFS</span><span class="sxs-lookup"><span data-stu-id="49809-124">Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS</span></span>](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [<span data-ttu-id="49809-125">應用程式相容性和 ReFS</span><span class="sxs-lookup"><span data-stu-id="49809-125">Application Compatibility and ReFS</span></span>](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 