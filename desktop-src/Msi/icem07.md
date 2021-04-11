---
description: ICEM07 會確認順序資料表中的檔案順序符合 MergeModule.CABinet 中的檔順序。
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849651"
---
# <a name="icem07"></a><span data-ttu-id="4dae7-103">ICEM07</span><span class="sxs-lookup"><span data-stu-id="4dae7-103">ICEM07</span></span>

<span data-ttu-id="4dae7-104">ICEM07 會確認順序資料表中的檔案順序符合 [MergeModule.CABinet](mergemodule-cabinet.md)中的檔順序。</span><span class="sxs-lookup"><span data-stu-id="4dae7-104">ICEM07 verifies that the order of files in the sequence table matches the order of files in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span>

<span data-ttu-id="4dae7-105">Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。</span><span class="sxs-lookup"><span data-stu-id="4dae7-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="4dae7-106">結果</span><span class="sxs-lookup"><span data-stu-id="4dae7-106">Result</span></span>

<span data-ttu-id="4dae7-107">如果檔案資料表中的檔案順序與封包檔中的順序不符，ICEM07 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="4dae7-107">ICEM07 posts an error if the order of files in the File table does not match the order in the cabinet file.</span></span>

## <a name="example"></a><span data-ttu-id="4dae7-108">範例</span><span class="sxs-lookup"><span data-stu-id="4dae7-108">Example</span></span>

<span data-ttu-id="4dae7-109">IC0M07 會針對所顯示的範例張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4dae7-109">IC0M07 would post the following error message for the example shown.</span></span>

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[<span data-ttu-id="4dae7-110">FileTable</span><span class="sxs-lookup"><span data-stu-id="4dae7-110">File Table</span></span>](file-table.md)



| <span data-ttu-id="4dae7-111">檔案</span><span class="sxs-lookup"><span data-stu-id="4dae7-111">File</span></span>          | <span data-ttu-id="4dae7-112">順序</span><span class="sxs-lookup"><span data-stu-id="4dae7-112">Sequence</span></span> |
|---------------|----------|
| <span data-ttu-id="4dae7-113">>filea.docx.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4dae7-113">FileA.*GUID1*</span></span> | <span data-ttu-id="4dae7-114">1</span><span class="sxs-lookup"><span data-stu-id="4dae7-114">1</span></span>        |
| <span data-ttu-id="4dae7-115">>fileb.docx.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4dae7-115">FileB.*GUID1*</span></span> | <span data-ttu-id="4dae7-116">8</span><span class="sxs-lookup"><span data-stu-id="4dae7-116">8</span></span>        |
| <span data-ttu-id="4dae7-117">FileC.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4dae7-117">FileC.*GUID1*</span></span> | <span data-ttu-id="4dae7-118">52</span><span class="sxs-lookup"><span data-stu-id="4dae7-118">52</span></span>       |



 

<span data-ttu-id="4dae7-119">Embedded [MergeModule.CABinet](mergemodule-cabinet.md)</span><span class="sxs-lookup"><span data-stu-id="4dae7-119">Embedded [MergeModule.CABinet](mergemodule-cabinet.md)</span></span>



| <span data-ttu-id="4dae7-120">檔案</span><span class="sxs-lookup"><span data-stu-id="4dae7-120">File</span></span>          |
|---------------|
| <span data-ttu-id="4dae7-121">>filea.docx.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4dae7-121">FileA.*GUID1*</span></span> |
| <span data-ttu-id="4dae7-122">FileC.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4dae7-122">FileC.*GUID1*</span></span> |
| <span data-ttu-id="4dae7-123">提交。*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4dae7-123">FileD.*GUID1*</span></span> |
| <span data-ttu-id="4dae7-124">>fileb.docx.*GUID1*</span><span class="sxs-lookup"><span data-stu-id="4dae7-124">FileB.*GUID1*</span></span> |



 

<span data-ttu-id="4dae7-125">雖然檔案資料表中的檔案序號不需要是連續的，而且封包檔中可以有額外的檔案，但是檔案資料表中所有檔案的相對順序必須符合 [MergeModule.CABinet](mergemodule-cabinet.md)中的順序。</span><span class="sxs-lookup"><span data-stu-id="4dae7-125">Although the file sequence numbers in the file table do not have to be consecutive, and extra files can exist in the cabinet file, the relative sequence of all files in the File table must match the order in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span> <span data-ttu-id="4dae7-126">若要修正這個錯誤，請將 >fileb.docx 的序號變更為 FileC 後的順序，以符合封包中的檔案順序，或以正確的順序重建 CAB 檔。</span><span class="sxs-lookup"><span data-stu-id="4dae7-126">To fix this error, change the sequence number of FileB to come after FileC to match the file order in the CAB, or rebuild the CAB with the files in the correct order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dae7-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="4dae7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dae7-128">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="4dae7-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



