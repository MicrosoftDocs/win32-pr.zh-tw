---
description: 備份和還原作業通常會將磁片上指定的預設位置中的檔案複製到備份媒體，然後從該媒體還原至磁片上的相同預設位置。
ms.assetid: 7609c392-d5f8-48c2-8e7e-f35f56cf94f8
title: 非預設備份和還原位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c809b886886c1d84de1cc3960163a7cc94179cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989939"
---
# <a name="non-default-backup-and-restore-locations"></a><span data-ttu-id="fa132-103">非預設備份和還原位置</span><span class="sxs-lookup"><span data-stu-id="fa132-103">Non-Default Backup and Restore Locations</span></span>

<span data-ttu-id="fa132-104">備份和還原作業通常會將磁片上指定的預設位置中的檔案複製到備份媒體，然後從該媒體還原至磁片上的相同預設位置。</span><span class="sxs-lookup"><span data-stu-id="fa132-104">Backup and restore operations typically copy files from a given, default location on disk to backup media and then restore from that media to the same default location on disk.</span></span>

<span data-ttu-id="fa132-105">原因有很多，特別是在處理執行中的進程時，不是遵循這個簡單的模型。</span><span class="sxs-lookup"><span data-stu-id="fa132-105">There are many reasons, particularly when dealing with running processes, not to follow this simple model.</span></span> <span data-ttu-id="fa132-106">VSS 支援使用非標準來源進行備份，並使用替代目的地進行還原，並包含使用檔案子集和重新對應檔案的機制。</span><span class="sxs-lookup"><span data-stu-id="fa132-106">VSS supports using nonstandard sources for backup and alternate destinations for restore, and includes mechanisms to work with subsets of files and to remap files.</span></span>

-   [<span data-ttu-id="fa132-107">在備份期間使用替代路徑</span><span class="sxs-lookup"><span data-stu-id="fa132-107">Working with Alternate Paths during Backup</span></span>](working-with-alternate-paths-during-backup.md)
-   [<span data-ttu-id="fa132-108">在還原期間使用替代位置</span><span class="sxs-lookup"><span data-stu-id="fa132-108">Working with Alternate Locations during Restore</span></span>](working-with-alternate-locations-during-restore.md)
-   [<span data-ttu-id="fa132-109">在還原期間使用新目標</span><span class="sxs-lookup"><span data-stu-id="fa132-109">Working with New Targets during Restore</span></span>](working-with-new-targets-during-restore.md)
-   [<span data-ttu-id="fa132-110">使用部分檔案</span><span class="sxs-lookup"><span data-stu-id="fa132-110">Working with Partial Files</span></span>](working-with-partial-files.md)
-   [<span data-ttu-id="fa132-111">使用導向的目標</span><span class="sxs-lookup"><span data-stu-id="fa132-111">Working with Directed Targets</span></span>](working-with-directed-targets.md)

 

 



