---
description: Windows Installer 套件的開發人員可能會注意到，在重複編輯和儲存之後，其 .msi 檔案的結果會大於預期。
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: 減少 .msi 檔案的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944155"
---
# <a name="reducing-the-size-of-an-msi-file"></a><span data-ttu-id="6e0eb-103">減少 .msi 檔案的大小</span><span class="sxs-lookup"><span data-stu-id="6e0eb-103">Reducing the Size of an .msi File</span></span>

<span data-ttu-id="6e0eb-104">Windows Installer 套件的開發人員可能會注意到，在重複編輯和儲存之後，其 .msi 檔案的結果會大於預期。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-104">Developers of Windows Installer packages may notice their .msi files getting larger than expected after repeated edits and saves.</span></span> <span data-ttu-id="6e0eb-105">Windows Installer .msi 檔案是包含儲存和資料流程的複合檔案，而且具有與 OLE 檔檔案相同的儲存限制。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-105">Windows Installer .msi files are compound files that contain storages and streams, and have some of the same storage limitations as OLE document files.</span></span> <span data-ttu-id="6e0eb-106">如果您編輯和儲存相同的 .msi 檔案，它會在檔案中建立浪費的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-106">If you edit and save the same .msi file over and over, it creates wasted storage space in the file.</span></span> <span data-ttu-id="6e0eb-107">這只會影響 .msi 檔案的作者，對 Windows Installer 使用者沒有影響。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-107">This only affects authors of .msi files and has no effect on Windows Installer users.</span></span> <span data-ttu-id="6e0eb-108">開發人員可能會想要移除此浪費的儲存空間，然後再寄出其最終的 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-108">Developers may want to remove this wasted storage space before shipping their final .msi file.</span></span>

<span data-ttu-id="6e0eb-109">若要移除浪費的儲存空間並減少 .msi 檔案的最終大小，您可以選擇下列選項。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-109">To remove wasted storage space and reduce the final size of .msi files, you have the following options.</span></span>

-   <span data-ttu-id="6e0eb-110">將資料庫中的所有資料表匯出為 idt 檔案，然後將它們匯入至新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-110">Export all of the tables in the database to .idt files, and then import those into a new database.</span></span> <span data-ttu-id="6e0eb-111">這樣可以產生最精簡的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-111">This produces the most compact storage possible.</span></span>
-   <span data-ttu-id="6e0eb-112">使用軟體公用程式壓縮 OLE 檔檔案的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="6e0eb-112">Use a software utility for compacting the storage space of OLE document files.</span></span>

 

 



