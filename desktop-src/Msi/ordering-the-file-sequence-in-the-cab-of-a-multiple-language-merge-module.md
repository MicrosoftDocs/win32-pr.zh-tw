---
description: 必須撰寫多語言合併模組、語言轉換和封包檔，使檔案的順序符合檔案資料表中指定的順序。
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: 排序多個語言合併模組 CAB 中的檔案順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195273"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a><span data-ttu-id="402e9-103">排序多個語言合併模組 CAB 中的檔案順序</span><span class="sxs-lookup"><span data-stu-id="402e9-103">Ordering the File Sequence in the CAB of a Multiple Language Merge Module</span></span>

<span data-ttu-id="402e9-104">您必須撰寫多語言合併模組、語言轉換和封包檔，使 .cab 中的檔案順序符合 [File 資料表](file-table.md)中指定的檔案安裝順序，即使是在語言轉換的應用程式之後也一樣。</span><span class="sxs-lookup"><span data-stu-id="402e9-104">Multiple-language merge modules, language transforms, and cabinet files must be authored such that the order of the files in the .cab matches the installation order of files specified in the [File Table](file-table.md), even after the application of the language transform.</span></span> <span data-ttu-id="402e9-105">如果模組和 .cab 中的順序不相符，就無法使用合併模組。</span><span class="sxs-lookup"><span data-stu-id="402e9-105">If the order in the module and in the .cab do not match, the merge module cannot be used.</span></span>

<span data-ttu-id="402e9-106">指派給模組中的每個檔案，這是與語言無關的唯一序號，然後一律使用該檔案的序號。</span><span class="sxs-lookup"><span data-stu-id="402e9-106">Assign to each file in the module, a unique sequence number that is independent of its language, and then always use that sequence number for the file.</span></span> <span data-ttu-id="402e9-107">建立封包檔和撰寫語言轉換時，請使用相同的順序。</span><span class="sxs-lookup"><span data-stu-id="402e9-107">Use the same sequence when building the cabinet file and authoring a language transform.</span></span>

<span data-ttu-id="402e9-108">因為安裝程式只會安裝檔案 [資料表](file-table.md)中所列的檔案，所以在封包、檔案 [資料表](file-table.md)和語言轉換中使用全域檔案順序，可讓合併工具略過儲存在封包中未列在檔案 [資料表](file-table.md)中的任何其他檔案。</span><span class="sxs-lookup"><span data-stu-id="402e9-108">Because the Installer only installs the files listed in the [File Table](file-table.md), the use of a global file sequence in the cabinet, [File Table](file-table.md), and language transform enables the merge tool to skip any extra files stored in the cabinet that are not listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="402e9-109">其他檔案可能會存在於封包中，但不能列在檔案 [資料表](file-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="402e9-109">Other files may exist in the cabinet, but they must not be listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="402e9-110">例如，安裝 Code.dll、英文 .dat、德文和法文的模組可以使用下列全域檔案順序順序。</span><span class="sxs-lookup"><span data-stu-id="402e9-110">For example, a module installing Code.dll, English.dat, German.dat, and French.dat can use the following global file sequence order.</span></span>



| <span data-ttu-id="402e9-111">檔案</span><span class="sxs-lookup"><span data-stu-id="402e9-111">File</span></span>        | <span data-ttu-id="402e9-112">順序</span><span class="sxs-lookup"><span data-stu-id="402e9-112">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="402e9-113">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="402e9-113">Code.Dll</span></span>    | <span data-ttu-id="402e9-114">1</span><span class="sxs-lookup"><span data-stu-id="402e9-114">1</span></span>        |
| <span data-ttu-id="402e9-115">英文版 .Dat</span><span class="sxs-lookup"><span data-stu-id="402e9-115">English.Dat</span></span> | <span data-ttu-id="402e9-116">2</span><span class="sxs-lookup"><span data-stu-id="402e9-116">2</span></span>        |
| <span data-ttu-id="402e9-117">德文 .Dat</span><span class="sxs-lookup"><span data-stu-id="402e9-117">German.Dat</span></span>  | <span data-ttu-id="402e9-118">3</span><span class="sxs-lookup"><span data-stu-id="402e9-118">3</span></span>        |
| <span data-ttu-id="402e9-119">法文</span><span class="sxs-lookup"><span data-stu-id="402e9-119">French.Dat</span></span>  | <span data-ttu-id="402e9-120">4</span><span class="sxs-lookup"><span data-stu-id="402e9-120">4</span></span>        |



 

<span data-ttu-id="402e9-121">然後可以撰寫語言轉換來修改模組的檔案 [表格](file-table.md) ，以取得英文、德文或法文。</span><span class="sxs-lookup"><span data-stu-id="402e9-121">Language transforms can then be authored to modify the [File Table](file-table.md) of the module for English, German, or French.</span></span>

<span data-ttu-id="402e9-122">英文) 的[檔資料表](file-table.md) (部分</span><span class="sxs-lookup"><span data-stu-id="402e9-122">[File Table](file-table.md) (partial for English)</span></span>



| <span data-ttu-id="402e9-123">檔案</span><span class="sxs-lookup"><span data-stu-id="402e9-123">File</span></span>        | <span data-ttu-id="402e9-124">順序</span><span class="sxs-lookup"><span data-stu-id="402e9-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="402e9-125">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="402e9-125">Code.Dll</span></span>    | <span data-ttu-id="402e9-126">1</span><span class="sxs-lookup"><span data-stu-id="402e9-126">1</span></span>        |
| <span data-ttu-id="402e9-127">英文版 .Dat</span><span class="sxs-lookup"><span data-stu-id="402e9-127">English.Dat</span></span> | <span data-ttu-id="402e9-128">2</span><span class="sxs-lookup"><span data-stu-id="402e9-128">2</span></span>        |



 

<span data-ttu-id="402e9-129">德文) 的[檔資料表](file-table.md) (部分</span><span class="sxs-lookup"><span data-stu-id="402e9-129">[File Table](file-table.md) (partial for German)</span></span>



| <span data-ttu-id="402e9-130">檔案</span><span class="sxs-lookup"><span data-stu-id="402e9-130">File</span></span>       | <span data-ttu-id="402e9-131">順序</span><span class="sxs-lookup"><span data-stu-id="402e9-131">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="402e9-132">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="402e9-132">Code.Dll</span></span>   | <span data-ttu-id="402e9-133">1</span><span class="sxs-lookup"><span data-stu-id="402e9-133">1</span></span>        |
| <span data-ttu-id="402e9-134">德文 .Dat</span><span class="sxs-lookup"><span data-stu-id="402e9-134">German.Dat</span></span> | <span data-ttu-id="402e9-135">3</span><span class="sxs-lookup"><span data-stu-id="402e9-135">3</span></span>        |



 

<span data-ttu-id="402e9-136">[File 資料表](file-table.md) (部分的法文) </span><span class="sxs-lookup"><span data-stu-id="402e9-136">[File Table](file-table.md) (partial for French)</span></span>



| <span data-ttu-id="402e9-137">檔案</span><span class="sxs-lookup"><span data-stu-id="402e9-137">File</span></span>       | <span data-ttu-id="402e9-138">順序</span><span class="sxs-lookup"><span data-stu-id="402e9-138">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="402e9-139">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="402e9-139">Code.Dll</span></span>   | <span data-ttu-id="402e9-140">1</span><span class="sxs-lookup"><span data-stu-id="402e9-140">1</span></span>        |
| <span data-ttu-id="402e9-141">法文</span><span class="sxs-lookup"><span data-stu-id="402e9-141">French.Dat</span></span> | <span data-ttu-id="402e9-142">4</span><span class="sxs-lookup"><span data-stu-id="402e9-142">4</span></span>        |



 

<span data-ttu-id="402e9-143">如需詳細資訊，請參閱 [撰寫多個語言合併模組的語言轉換](authoring-a-language-transform-for-a-multiple-language-merge-module.md) 和 [撰寫合併模組檔案資料表](authoring-merge-module-file-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="402e9-143">For more information, see [Authoring a Language Transform for a Multiple Language Merge Module](authoring-a-language-transform-for-a-multiple-language-merge-module.md) and [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

 

 



