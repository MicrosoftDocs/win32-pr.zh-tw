---
description: 每個合併模組都必須要有一個檔案資料表，而且每個檔案的記錄都應該由合併模組傳遞至目標安裝套件。
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: 撰寫合併模組檔案資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026642"
---
# <a name="authoring-merge-module-file-tables"></a><span data-ttu-id="308ee-103">撰寫合併模組檔案資料表</span><span class="sxs-lookup"><span data-stu-id="308ee-103">Authoring Merge Module File Tables</span></span>

<span data-ttu-id="308ee-104">每個合併模組都必須要有一個檔案 [資料表](file-table.md) ，而且每個檔案的記錄都應該由合併模組傳遞至目標安裝套件。</span><span class="sxs-lookup"><span data-stu-id="308ee-104">A [File Table](file-table.md) is required in every merge module, and should have a record for each file that is being delivered to the target installation package by the merge module.</span></span> <span data-ttu-id="308ee-105">合併模組合併為 .msi 檔案時，合併模組檔案資料表中的每個檔案都會儲存在 .msm 檔案的封 [*包*](c-gly.md) 檔中。</span><span class="sxs-lookup"><span data-stu-id="308ee-105">When the merge module is merged into a .msi file, every file in the merge module File Table is stored inside a [*cabinet file*](c-gly.md) in the .msm file.</span></span> <span data-ttu-id="308ee-106">合併模組中的封包名稱一律如下： MergeModule.CABinet。</span><span class="sxs-lookup"><span data-stu-id="308ee-106">The name of the cabinet in a merge module is always the following: MergeModule.CABinet.</span></span>

<span data-ttu-id="308ee-107">如需詳細資訊，請參閱 [產生 MergeModule.CABinet 封包](generating-mergemodule-cabinet-cabinet-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="308ee-107">For more information, see [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).</span></span>

-   <span data-ttu-id="308ee-108">因為合併模組的檔案一律儲存在封包檔中，所以不需要在檔案 [資料表](file-table.md)的 [屬性] 資料行中設定 **msidbFileAttributesNoncompressed** 或 **msidbFileAttributesCompressed** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="308ee-108">Because the files of a merge module are always stored inside a cabinet file, it is not necessary to set the **msidbFileAttributesNoncompressed** or **msidbFileAttributesCompressed** bit flags in the Attributes column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="308ee-109">MergeModule.CABinet 中的檔案名必須符合合併模組的檔案 [資料表](file-table.md)中的主鍵。</span><span class="sxs-lookup"><span data-stu-id="308ee-109">The names of files in MergeModule.CABinet must match the primary key in the merge module's [File Table](file-table.md).</span></span>

    <span data-ttu-id="308ee-110">File 資料行是檔案 [資料表](file-table.md) 的主鍵，而此欄位中的專案必須遵循在 [合併模組資料庫中命名主鍵](naming-primary-keys-in-merge-module-databases.md)所述的慣例。</span><span class="sxs-lookup"><span data-stu-id="308ee-110">The File column is the primary key of the [File Table](file-table.md) and the entries in this field must follow the convention that is described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

-   <span data-ttu-id="308ee-111">檔案序號是在 [File 資料表](file-table.md)的 sequence 資料行中指定。</span><span class="sxs-lookup"><span data-stu-id="308ee-111">File sequence numbers are specified in the Sequence column of the [File Table](file-table.md).</span></span>

    <span data-ttu-id="308ee-112">檔案必須以儲存在 MergeModule.CABinet 中的相同順序，列在合併模組的檔案 [資料表](file-table.md) 中。</span><span class="sxs-lookup"><span data-stu-id="308ee-112">Files must be listed in the merge module's [File Table](file-table.md) in the same sequence that they are stored in MergeModule.CABinet.</span></span> <span data-ttu-id="308ee-113">檔案的序號不需要連續，但它們的順序必須與儲存在封包內的檔案相同。</span><span class="sxs-lookup"><span data-stu-id="308ee-113">The sequence numbers of files do not need to be consecutive, but they must follow the same sequence as the files that are stored inside the cabinet.</span></span> <span data-ttu-id="308ee-114">例如，儲存在封包中的第一個、第二個和第三個檔案的序號可能是100、200和300。</span><span class="sxs-lookup"><span data-stu-id="308ee-114">For example, the first, second, and third files stored in the cabinet can have the sequence numbers 100, 200, and 300.</span></span>

-   <span data-ttu-id="308ee-115">安裝程式會略過未列在檔案 [資料表](file-table.md)中 MergeModule.CABinet 包含的額外檔案。</span><span class="sxs-lookup"><span data-stu-id="308ee-115">The Installer skips extra files included in MergeModule.CABinet that are not listed in the [File Table](file-table.md).</span></span>

    <span data-ttu-id="308ee-116">一個封包檔可以包含使用轉換支援多種語言的合併模組所需的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="308ee-116">One cabinet file can contain all the files necessary for a merge module that supports multiple languages using transforms.</span></span> <span data-ttu-id="308ee-117">所有語言檔案都可在封包中提供唯一的序號，然後當特定語言需要時，轉換可以在檔案 [資料表](file-table.md) 中新增或移除檔案。</span><span class="sxs-lookup"><span data-stu-id="308ee-117">All the language files can be given a unique sequence number in the cabinet, and then a transform can add or remove files from the [File Table](file-table.md) when needed for a specific language.</span></span> <span data-ttu-id="308ee-118">如需詳細資訊，請參閱 [撰寫多個語言合併模組](authoring-multiple-language-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="308ee-118">For more information, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="308ee-119">如需詳細資訊，請參閱檔案 [資料表](file-table.md)。</span><span class="sxs-lookup"><span data-stu-id="308ee-119">For more information, see [File Table](file-table.md).</span></span>

 

 



