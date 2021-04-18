---
description: ICE60 會驗證 Windows Installer 資料庫的檔案資料表。
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978039"
---
# <a name="ice60"></a><span data-ttu-id="0b8fe-103">ICE60</span><span class="sxs-lookup"><span data-stu-id="0b8fe-103">ICE60</span></span>

<span data-ttu-id="0b8fe-104">ICE60 會檢查 [File 資料表](file-table.md) 中的檔案是否符合下列條件：</span><span class="sxs-lookup"><span data-stu-id="0b8fe-104">ICE60 checks that files in the [File table](file-table.md) meet the following condition:</span></span>

-   <span data-ttu-id="0b8fe-105">如果檔案不是字型且具有版本，則必須有語言。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-105">If the file is not a font and has a version, then it must have a language.</span></span>
-   <span data-ttu-id="0b8fe-106">ICE60 會檢查 [MsiFileHash 資料表](msifilehash-table.md)中沒有列出任何已建立版本的檔案。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-106">ICE60 checks that no versioned files are listed in the [MsiFileHash table](msifilehash-table.md).</span></span>

<span data-ttu-id="0b8fe-107">若無法修正 ICE60 回報的警告，通常會導致在產品修復完成時不必要地重新安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-107">Failure to fix a warning reported by ICE60 generally leads to a file being needlessly reinstalled when a product repair is done.</span></span> <span data-ttu-id="0b8fe-108">發生這種情況的原因是，要在修復中安裝的檔案和磁片上的現有檔案都有相同的版本 (它們是相同的檔案) 但不同的語言。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-108">This happens because the file to be installed in the repair and the existing file on disk have the same version (they are the same file) but different languages.</span></span> <span data-ttu-id="0b8fe-109">File 資料表將語言列為 null，但檔案本身在資源中具有語言值。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-109">The file table lists the language as null, but the file itself has a language value in the resource.</span></span> <span data-ttu-id="0b8fe-110">根據檔案 [版本控制規則](file-versioning-rules.md)，安裝程式會優先處理要安裝的檔案，因此重新複製不必要。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-110">Based on the [file versioning rules](file-versioning-rules.md), the installer favors the file to be installed, so it is recopied needlessly.</span></span>

## <a name="result"></a><span data-ttu-id="0b8fe-111">結果</span><span class="sxs-lookup"><span data-stu-id="0b8fe-111">Result</span></span>

<span data-ttu-id="0b8fe-112">如果檔案 [資料表](file-table.md) 中不是字型且擁有版本的檔案沒有語言，ICE60 會張貼警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-112">ICE60 posts a warning or an error if a file in the [File table](file-table.md) that is not a font and has a version, does not have a language.</span></span>

<span data-ttu-id="0b8fe-113">如果已建立 MsiFileHash 資料表中所列的檔案版本，ICE60 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-113">ICE60 posts the following error if a file listed in the MsiFileHash table is versioned.</span></span>

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a><span data-ttu-id="0b8fe-114">範例</span><span class="sxs-lookup"><span data-stu-id="0b8fe-114">Example</span></span>

<span data-ttu-id="0b8fe-115">ICE60 會針對所顯示的範例報告下列錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-115">ICE60 reports the following error and warning for the example shown.</span></span> <span data-ttu-id="0b8fe-116"> (檔 B 是字型;其他檔案則不是。 ) </span><span class="sxs-lookup"><span data-stu-id="0b8fe-116">(File B is a font; the other files are not.)</span></span>

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

<span data-ttu-id="0b8fe-117">>filea.docx 具有版本和語言;因此，不會產生警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-117">FileA has both a version and a language; therefore no warning or error is generated.</span></span>

<span data-ttu-id="0b8fe-118">>fileb.docx 具有版本，但沒有語言。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-118">FileB has a version but no language.</span></span> <span data-ttu-id="0b8fe-119">但是，不會產生警告或錯誤，因為它是字型。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-119">No warning or error is generated, however, because it is a font.</span></span>

<span data-ttu-id="0b8fe-120">FileC 是隨附的參考，因此不需要有語言。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-120">FileC is a companion reference, so it does not have to have a language.</span></span> <span data-ttu-id="0b8fe-121">不會產生警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-121">No warning or error is generated.</span></span>

<span data-ttu-id="0b8fe-122">歸檔沒有任何版本，因此不需要有語言。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-122">FileD has no version, so it does not need to have a language.</span></span> <span data-ttu-id="0b8fe-123">不會產生警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-123">No warning or error is generated.</span></span>

<span data-ttu-id="0b8fe-124">檔案具有版本，但沒有語言。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-124">FileE has a version but no language.</span></span> <span data-ttu-id="0b8fe-125">因此會產生警告。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-125">Therefore a warning is generated.</span></span>

<span data-ttu-id="0b8fe-126">若要修正此警告，請將語言新增至檔案。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-126">To fix this warning, add a language to FileE.</span></span>

<span data-ttu-id="0b8fe-127">檔案應該盡可能在版本資源中儲存語言值。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-127">Files should have language values stored in the version resource whenever possible.</span></span> <span data-ttu-id="0b8fe-128">如果檔案為中性語言，請使用 [LANGID](column-data-types.md) 0。</span><span class="sxs-lookup"><span data-stu-id="0b8fe-128">If a file is language neutral, use the [LANGID](column-data-types.md) 0.</span></span>

<span data-ttu-id="0b8fe-129">[File Table](file-table.md) (>fileb.docx 是字型;其他檔案則不是。 ) </span><span class="sxs-lookup"><span data-stu-id="0b8fe-129">[File Table](file-table.md) (FileB is a font; the other files are not.)</span></span>



| <span data-ttu-id="0b8fe-130">檔案</span><span class="sxs-lookup"><span data-stu-id="0b8fe-130">File</span></span>  | <span data-ttu-id="0b8fe-131">版本</span><span class="sxs-lookup"><span data-stu-id="0b8fe-131">Version</span></span> | <span data-ttu-id="0b8fe-132">語言</span><span class="sxs-lookup"><span data-stu-id="0b8fe-132">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="0b8fe-133">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="0b8fe-133">FileA</span></span> | <span data-ttu-id="0b8fe-134">1.0</span><span class="sxs-lookup"><span data-stu-id="0b8fe-134">1.0</span></span>     | <span data-ttu-id="0b8fe-135">1033</span><span class="sxs-lookup"><span data-stu-id="0b8fe-135">1033</span></span>     |
| <span data-ttu-id="0b8fe-136">>fileb.docx</span><span class="sxs-lookup"><span data-stu-id="0b8fe-136">FileB</span></span> | <span data-ttu-id="0b8fe-137">1.0</span><span class="sxs-lookup"><span data-stu-id="0b8fe-137">1.0</span></span>     |          |
| <span data-ttu-id="0b8fe-138">FileC</span><span class="sxs-lookup"><span data-stu-id="0b8fe-138">FileC</span></span> | <span data-ttu-id="0b8fe-139">>filea.docx</span><span class="sxs-lookup"><span data-stu-id="0b8fe-139">FileA</span></span>   |          |
| <span data-ttu-id="0b8fe-140">提交</span><span class="sxs-lookup"><span data-stu-id="0b8fe-140">FileD</span></span> |         |          |
| <span data-ttu-id="0b8fe-141">檔案</span><span class="sxs-lookup"><span data-stu-id="0b8fe-141">FileE</span></span> | <span data-ttu-id="0b8fe-142">1.0</span><span class="sxs-lookup"><span data-stu-id="0b8fe-142">1.0</span></span>     |          |



 

[<span data-ttu-id="0b8fe-143">字型資料表</span><span class="sxs-lookup"><span data-stu-id="0b8fe-143">Font Table</span></span>](font-table.md)



| <span data-ttu-id="0b8fe-144">檔案</span><span class="sxs-lookup"><span data-stu-id="0b8fe-144">File</span></span>  | <span data-ttu-id="0b8fe-145">FontTitle</span><span class="sxs-lookup"><span data-stu-id="0b8fe-145">FontTitle</span></span>  |
|-------|------------|
| <span data-ttu-id="0b8fe-146">>fileb.docx</span><span class="sxs-lookup"><span data-stu-id="0b8fe-146">FileB</span></span> | <span data-ttu-id="0b8fe-147">字型標題</span><span class="sxs-lookup"><span data-stu-id="0b8fe-147">Font Title</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0b8fe-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b8fe-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b8fe-149">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="0b8fe-149">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



