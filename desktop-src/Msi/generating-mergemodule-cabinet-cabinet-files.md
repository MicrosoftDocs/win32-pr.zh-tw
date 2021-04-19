---
description: 合併模組傳遞至目標安裝套件的每個檔案都必須儲存在 .msm 檔案內內嵌為數據流的封包檔中。 此封包的名稱一律 MergeModule.CABinet。
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: 產生 MergeModule.CABinet 封包檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975161"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a><span data-ttu-id="3926c-104">產生 MergeModule.CABinet 封包檔</span><span class="sxs-lookup"><span data-stu-id="3926c-104">Generating MergeModule.CABinet Cabinet Files</span></span>

<span data-ttu-id="3926c-105">合併模組傳遞至目標安裝套件的每個檔案都必須儲存在 .msm 檔案內內嵌為數據流的封包檔中。</span><span class="sxs-lookup"><span data-stu-id="3926c-105">Every file that is delivered to the target installation package by the merge module must be stored inside of a cabinet file embedded as a stream inside the .msm file.</span></span> <span data-ttu-id="3926c-106">此封包的名稱一律 MergeModule.CABinet。</span><span class="sxs-lookup"><span data-stu-id="3926c-106">The name of this cabinet is always MergeModule.CABinet.</span></span>

<span data-ttu-id="3926c-107">MergeModule.CABinet 中的檔案名必須符合合併模組的檔案 [資料表](file-table.md) 中所使用的主鍵，而且必須遵守在 [合併模組資料庫中命名主鍵](naming-primary-keys-in-merge-module-databases.md)所述的慣例。</span><span class="sxs-lookup"><span data-stu-id="3926c-107">The names of files in MergeModule.CABinet must match the primary keys used in the merge module's [File table](file-table.md) and must adhere to the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="3926c-108">安裝程式會略過包含在 MergeModule.CABinet 中的額外檔案，這些檔案未列在合併模組的檔案 [資料表](file-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="3926c-108">The installer skips extra files included in MergeModule.CABinet that are not listed in the merge module's [File table](file-table.md).</span></span> <span data-ttu-id="3926c-109">檔案資料表中指定的檔案序號不需要連續，但它們的順序必須與 MergeModule.CABinet 內儲存的檔案相同。</span><span class="sxs-lookup"><span data-stu-id="3926c-109">The sequence numbers of files specified in the File table do not need to be consecutive, but they must follow the same sequence as the files stored inside MergeModule.CABinet.</span></span> <span data-ttu-id="3926c-110">如需詳細資訊，請參閱 [撰寫合併模組檔案資料表](authoring-merge-module-file-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="3926c-110">For more information, see [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

<span data-ttu-id="3926c-111">這表示單一封包檔可以包含合併模組支援多種語言所需的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="3926c-111">This means that a single cabinet file can contain all the files needed for a merge module to support multiple languages.</span></span> <span data-ttu-id="3926c-112">所有語言檔案都可在封包中提供唯一的序號，然後您可以使用語言轉換來新增或移除檔案資料表中的檔案，以取得特定語言的合併模組。</span><span class="sxs-lookup"><span data-stu-id="3926c-112">All the language files can be given unique sequence numbers in the cabinet and then a language transform can be used to add or remove files from the File table to obtain a merge module for a particular language.</span></span> <span data-ttu-id="3926c-113">如需詳細資訊，請參閱 [撰寫多個語言合併模組](authoring-multiple-language-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="3926c-113">For details, see [Authoring Multiple Language Merge Modules](authoring-multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="3926c-114">您可以藉由開啟暫存[ \_ 資料流程資料表](-streams-table.md)，將 MergeModule.CABinet 加入至合併模組。</span><span class="sxs-lookup"><span data-stu-id="3926c-114">MergeModule.CABinet can be added to the merge module by opening a temporary [\_Streams Table](-streams-table.md).</span></span> <span data-ttu-id="3926c-115">例如，Windows Installer SDK 提供的工具 Msidb.exe 可以用來將 MergeModule.CABinet 加入至合併模組。</span><span class="sxs-lookup"><span data-stu-id="3926c-115">For example, the tool Msidb.exe provided with the Windows Installer SDK can be used to add the MergeModule.CABinet to the merge module.</span></span> <span data-ttu-id="3926c-116">如需詳細資訊，請參閱 [在安裝中包含封包](including-a-cabinet-file-in-an-installation.md)檔。</span><span class="sxs-lookup"><span data-stu-id="3926c-116">For more information, see [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



