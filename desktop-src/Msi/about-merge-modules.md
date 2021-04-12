---
description: 合併模組基本上是簡化的 .msi 檔案，也就是 Windows Installer 安裝套件的副檔名。 標準合併模組的副檔名為 .msm。
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: 關於合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319044"
---
# <a name="about-merge-modules"></a><span data-ttu-id="8bcbd-104">關於合併模組</span><span class="sxs-lookup"><span data-stu-id="8bcbd-104">About Merge Modules</span></span>

<span data-ttu-id="8bcbd-105">合併模組基本上是簡化的 .msi 檔案，也就是 Windows Installer 安裝套件的副檔名。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-105">Merge modules are essentially simplified .msi files, which is the file name extension for a Windows Installer installation package.</span></span> <span data-ttu-id="8bcbd-106">標準合併模組的副檔名為 .msm。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-106">A standard merge module has an .msm file name extension.</span></span>

<span data-ttu-id="8bcbd-107">無法單獨安裝合併模組，因為它缺少安裝資料庫中有的一些重要資料庫資料表。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-107">A merge module cannot be installed alone because its lacks some vital database tables that are present in an installation database.</span></span> <span data-ttu-id="8bcbd-108">合併模組也包含本身特有的其他資料表。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-108">Merge modules also contain additional tables that are unique to themselves.</span></span> <span data-ttu-id="8bcbd-109">若要安裝合併模組與應用程式所提供的資訊，模組必須先合併到應用程式的 .msi 檔案中。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-109">To install the information delivered by a merge module with an application, the module must first be merged into the application's .msi file.</span></span>

<span data-ttu-id="8bcbd-110">合併模組包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="8bcbd-110">A merge module consists of the following parts:</span></span>

-   <span data-ttu-id="8bcbd-111">[合併模組資料庫](merge-module-database.md)，包含合併模組所傳遞的安裝屬性和安裝邏輯。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-111">A [Merge Module Database](merge-module-database.md) containing the installation properties and setup logic being delivered by the merge module.</span></span>
-   <span data-ttu-id="8bcbd-112">描述模組的 [合併模組摘要資訊資料流程參考](merge-module-summary-information-stream-reference.md) 。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-112">A [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md) describing the module.</span></span>
-   <span data-ttu-id="8bcbd-113">[MergeModule.CABinet](mergemodule-cabinet.md)封包檔儲存為合併模組內的資料流程。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-113">A [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file stored as a stream inside the merge module.</span></span> <span data-ttu-id="8bcbd-114">此封包包含合併模組所傳遞的元件所需的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-114">This cabinet contains all the files required by the components delivered by the merge module.</span></span>

<span data-ttu-id="8bcbd-115">[多個語言合併模組](multiple-language-merge-modules.md) 可將元件傳遞至多個語言的安裝套件。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-115">[Multiple language merge modules](multiple-language-merge-modules.md) can deliver components to an installation package in multiple languages.</span></span> <span data-ttu-id="8bcbd-116">在多個語言合併模組中，資料庫包含多個語言的安裝屬性和邏輯，而 MergeModule.CABinet 封包包含安裝元件所需的所有檔案，以及模組支援的所有語言。</span><span class="sxs-lookup"><span data-stu-id="8bcbd-116">In a multiple language merge module the database contains the installation properties and logic for more than one language and the MergeModule.CABinet cabinet includes all the files necessary to install components with all the languages supported by the module.</span></span>

 

 



