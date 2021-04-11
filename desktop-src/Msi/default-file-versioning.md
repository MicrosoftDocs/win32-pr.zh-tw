---
description: 下列各節中的流程圖說明當所安裝元件的金鑰檔與已安裝在目標位置中的檔案同名時，所使用的預設檔案版本控制規則。
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: 預設檔案版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850244"
---
# <a name="default-file-versioning"></a><span data-ttu-id="9f197-103">預設檔案版本控制</span><span class="sxs-lookup"><span data-stu-id="9f197-103">Default File Versioning</span></span>

<span data-ttu-id="9f197-104">下列各節中的流程圖說明當所安裝元件的金鑰檔與已安裝在目標位置中的檔案同名時，所使用的預設檔案版本控制規則。</span><span class="sxs-lookup"><span data-stu-id="9f197-104">The flow diagrams in the following sections illustrate the default file versioning rules used when the key file of a component being installed has the same name as a file already installed in the target location.</span></span> <span data-ttu-id="9f197-105">[取代現有](replacing-existing-files.md)的檔案也會說明預設檔案版本控制。</span><span class="sxs-lookup"><span data-stu-id="9f197-105">Default file versioning is also illustrated in [Replacing Existing Files](replacing-existing-files.md).</span></span>

<span data-ttu-id="9f197-106">請注意，使用 Windows Installer 時，可使用檔案雜湊來優化檔案的複製。</span><span class="sxs-lookup"><span data-stu-id="9f197-106">Note that with Windows Installer, file hashing is available to optimize the copying of files.</span></span> <span data-ttu-id="9f197-107">如需詳細資訊，請參閱 [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) 和 [MsiFileHash 資料表](msifilehash-table.md)。</span><span class="sxs-lookup"><span data-stu-id="9f197-107">For details, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="9f197-108">MsiFileHash 資料表只能搭配未建立版本檔使用。</span><span class="sxs-lookup"><span data-stu-id="9f197-108">The MsiFileHash table can only be used with unversioned files.</span></span>

-   [<span data-ttu-id="9f197-109">這兩個檔案都有版本</span><span class="sxs-lookup"><span data-stu-id="9f197-109">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="9f197-110">這兩個檔案都沒有版本</span><span class="sxs-lookup"><span data-stu-id="9f197-110">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="9f197-111">這兩個檔案都沒有具有檔案雜湊檢查的版本</span><span class="sxs-lookup"><span data-stu-id="9f197-111">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="9f197-112">一個檔案有版本</span><span class="sxs-lookup"><span data-stu-id="9f197-112">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



