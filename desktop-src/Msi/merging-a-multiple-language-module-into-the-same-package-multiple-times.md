---
description: 當模組支援多種語言時，您可以將它合併到相同的 Windows Installer 資料庫多次，但請確定每個合併都使用不同的語言。
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: 將多個語言模組合併成相同的封裝多次
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998143"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a><span data-ttu-id="5d66b-103">將多個語言模組合併成相同的封裝多次</span><span class="sxs-lookup"><span data-stu-id="5d66b-103">Merging a Multiple Language Module into the Same Package Multiple Times</span></span>

<span data-ttu-id="5d66b-104">當模組支援多種語言時，您可以將它合併到相同的 Windows Installer 資料庫多次，但請確定每個合併都使用不同的語言。</span><span class="sxs-lookup"><span data-stu-id="5d66b-104">When a module supports multiple languages, you can merge it into the same Windows Installer database multiple times, but make sure that each merge uses a different language.</span></span> <span data-ttu-id="5d66b-105">在每次合併之前，請向模組要求不同的語言。</span><span class="sxs-lookup"><span data-stu-id="5d66b-105">Before each merge, request a different language from the module.</span></span> <span data-ttu-id="5d66b-106">結果 .msi 資料庫會在每個模組合併的 [ModuleSignature 資料表](modulesignature-table.md) 中包含一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="5d66b-106">The resulting .msi database then has a record in the [ModuleSignature Table](modulesignature-table.md) for each merge of the module.</span></span> <span data-ttu-id="5d66b-107">在語言之間共用的元件只會在 [元件資料表](component-table.md)中存在一次，但會與 [ModuleComponents 資料表](modulecomponents-table.md)中的每個語言相關聯。</span><span class="sxs-lookup"><span data-stu-id="5d66b-107">Components that are shared between languages exist only one time in the [Component Table](component-table.md), but are associated with each language in the [ModuleComponents Table](modulecomponents-table.md).</span></span>

<span data-ttu-id="5d66b-108">將模組的多個語言合併成相同的封裝時，每個合併都必須滿足與單一語言模組相同的字碼頁限制。</span><span class="sxs-lookup"><span data-stu-id="5d66b-108">When merging multiple languages of a module into the same package, each merge must satisfy the same restrictions on code pages as single-language modules.</span></span> <span data-ttu-id="5d66b-109">這些模組不能包含不同字碼頁中的字串。</span><span class="sxs-lookup"><span data-stu-id="5d66b-109">The modules cannot contain strings in different code pages.</span></span>

<span data-ttu-id="5d66b-110">將模組多次合併成單一 .msi 檔案時，您可能需要修改檔案 [資料表](file-table.md) 中檔案的順序，以直接在安裝中使用模組中的現有 .cab。</span><span class="sxs-lookup"><span data-stu-id="5d66b-110">When merging a module multiple times into a single .msi file, you may need to modify the order of the files in the [File Table](file-table.md) to use the existing .cab from the module directly in your installation.</span></span> <span data-ttu-id="5d66b-111">檔案資料表中的檔案順序必須符合 .cab 檔的順序。</span><span class="sxs-lookup"><span data-stu-id="5d66b-111">The order of files in the File Table must match the order of files in the .cab.</span></span> <span data-ttu-id="5d66b-112">將模組多次合併到安裝資料庫時，可能會修改序列，因為語言之間共用的檔案可能已存在於先前合併的模組中，而且具有不同的相對序號。</span><span class="sxs-lookup"><span data-stu-id="5d66b-112">When merging a module multiple times into an installation database the sequence may be modified, because files shared between the languages may already exist in the module from a prior merge, and they have a different relative sequence number.</span></span>

 

 



