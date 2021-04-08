---
title: SIS 一般存放區和 Common-Store 檔案
description: 單一實例存放區所維護的所有備份檔 (SIS) 備份都稱為一般存放區檔案。
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- 一般存放區備份
- 單一實例存放區 (SIS) 備份、一般存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842536"
---
# <a name="the-sis-common-store-and-common-store-files"></a><span data-ttu-id="86068-105">SIS 一般存放區和 Common-Store 檔案</span><span class="sxs-lookup"><span data-stu-id="86068-105">The SIS Common Store and Common-Store Files</span></span>

<span data-ttu-id="86068-106">單一實例存放區所維護的所有備份檔 (SIS) 備份都稱為 *一般存放區* 檔案。</span><span class="sxs-lookup"><span data-stu-id="86068-106">All backing files maintained by single-instance store (SIS) backup are called *common-store files*.</span></span> <span data-ttu-id="86068-107">其中一個 *常見的存放區* 存在於每個 SIS 維護的磁片區上，並包含存在於該磁片區上的所有通用存放區檔案。</span><span class="sxs-lookup"><span data-stu-id="86068-107">One *common store* exists on each SIS-maintained volume and contains all of the common-store files that exist on that volume.</span></span> <span data-ttu-id="86068-108">此目錄位於磁片區的根目錄中，名為「 \\ SIS 通用存放區」。</span><span class="sxs-lookup"><span data-stu-id="86068-108">This directory is located in the root directory of the volume and is named "\\SIS Common Store".</span></span> <span data-ttu-id="86068-109">一般存放區會實作為保護標準使用者存取的目錄，因為一般存放區檔案僅供 SIS 備份 API 函式存取，而不是備份和還原應用程式。</span><span class="sxs-lookup"><span data-stu-id="86068-109">The common store is implemented as a directory that is protected against normal user access, because common-store files are intended to be accessed directly only by SIS backup API functions and not backup and restore applications.</span></span>

<span data-ttu-id="86068-110">一般存放區檔案的屬性如下：</span><span class="sxs-lookup"><span data-stu-id="86068-110">The properties of a common-store file are the following:</span></span>

-   <span data-ttu-id="86068-111">一般存放區檔案可能會有一或多個指向該檔案的連結。</span><span class="sxs-lookup"><span data-stu-id="86068-111">A common-store file may have one or more links pointing to it.</span></span>
-   <span data-ttu-id="86068-112">建立之後，通用存放區檔案的內容永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="86068-112">After it is created, the contents of a common-store file never change.</span></span>
-   <span data-ttu-id="86068-113">通用存放區檔案的名稱是全域唯一的，也就是說，它們在世界各地所有系統的所有磁片區都是唯一的，而且通用存放區檔案名與其資料之間的系結是全域靜態的。</span><span class="sxs-lookup"><span data-stu-id="86068-113">The names of common-store files are globally unique—that is, they are unique across all volumes across all systems in the world, and the binding between a common-store file name and its data is globally static.</span></span>

<span data-ttu-id="86068-114">在磁片區上啟用 SIS 時，系統會將一份重複的檔案複製到一般存放區，並將所有重複的檔案取代為指向一般存放區檔案的 [SIS 連結](sis-links-and-reparse-points.md) 。</span><span class="sxs-lookup"><span data-stu-id="86068-114">When SIS is enabled on a volume, one copy of the duplicate files is then created to the common store, and all of the duplicate files are replaced with [SIS links](sis-links-and-reparse-points.md) pointing to the common-store file.</span></span> <span data-ttu-id="86068-115">如需詳細資訊，請參閱 TechNet 檔中的 [啟用或停用磁片區上的 SIS](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) 。</span><span class="sxs-lookup"><span data-stu-id="86068-115">For more information, see [Enabling or Disabling SIS on a Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in the TechNet documentation.</span></span>

<span data-ttu-id="86068-116">當針對寫入作業存取其中一個 SIS 連結時，SIS 篩選器會先從通用存放區檔案還原 SIS 連結檔案的原始內容，並移除將 SIS 連結檔案連結至一般存放區的重新分析點，然後在原始目的地檔案上執行寫入操作。</span><span class="sxs-lookup"><span data-stu-id="86068-116">When one of the SIS links is accessed for a write operation, the SIS filter first restores the original contents of the SIS link file from the common-store file, the reparse point linking the SIS link file to the common store is removed, and then the write operation is performed on the original destination file.</span></span>

<span data-ttu-id="86068-117">只有當最後一個指向它的 SIS 連結被刪除時，才會移除一般存放區檔案。</span><span class="sxs-lookup"><span data-stu-id="86068-117">The common-store file is removed only when the last SIS link pointing to it is deleted.</span></span>

 

 