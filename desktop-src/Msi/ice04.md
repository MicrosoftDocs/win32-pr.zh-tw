---
description: ICE04 會驗證檔案資料表中每個檔案的序號是否小於或等於媒體資料表 LastSequence 資料行中的最大序號。
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944541"
---
# <a name="ice04"></a><span data-ttu-id="3a286-103">ICE04</span><span class="sxs-lookup"><span data-stu-id="3a286-103">ICE04</span></span>

<span data-ttu-id="3a286-104">ICE04 會驗證檔案 [資料表](file-table.md) 中每個檔案的序號是否小於或等於 [媒體資料表](media-table.md)LastSequence 資料行中的最大序號。</span><span class="sxs-lookup"><span data-stu-id="3a286-104">ICE04 validates that the sequence number of every file in the [File table](file-table.md) is less than or equal to the largest sequence number in the LastSequence column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="3a286-105">媒體資料表中的每一筆記錄都代表來源媒體上的磁片，其中的序號小於或等於 LastSequence 資料行中的值，且大於前一個磁片記錄中的 LastSequence 值。</span><span class="sxs-lookup"><span data-stu-id="3a286-105">Each record in the Media table represents a disk on the source media containing all the files with a sequence number less than or equal to the value in the LastSequence column and greater than the LastSequence value in the record of the preceding disk.</span></span>

## <a name="result"></a><span data-ttu-id="3a286-106">結果</span><span class="sxs-lookup"><span data-stu-id="3a286-106">Result</span></span>

<span data-ttu-id="3a286-107">如果有序號大於來源媒體的最大 LastSequence 數目的檔案，ICE04 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3a286-107">ICE04 posts an error message if there is a file with a sequence number greater than the largest LastSequence number for the source media.</span></span>

## <a name="example"></a><span data-ttu-id="3a286-108">範例</span><span class="sxs-lookup"><span data-stu-id="3a286-108">Example</span></span>

<span data-ttu-id="3a286-109">ICE04 會針對所顯示的範例報告下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="3a286-109">ICE04 would report the following error for the example shown:</span></span>

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

<span data-ttu-id="3a286-110">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="3a286-110">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="3a286-111">檔案</span><span class="sxs-lookup"><span data-stu-id="3a286-111">File</span></span>   | <span data-ttu-id="3a286-112">順序</span><span class="sxs-lookup"><span data-stu-id="3a286-112">Sequence</span></span> |
|--------|----------|
| <span data-ttu-id="3a286-113">Myfile.txt</span><span class="sxs-lookup"><span data-stu-id="3a286-113">MyFile</span></span> | <span data-ttu-id="3a286-114">210</span><span class="sxs-lookup"><span data-stu-id="3a286-114">210</span></span>      |



 

<span data-ttu-id="3a286-115">[媒體資料表](media-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="3a286-115">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="3a286-116">DiskId</span><span class="sxs-lookup"><span data-stu-id="3a286-116">DiskId</span></span> | <span data-ttu-id="3a286-117">LastSequence</span><span class="sxs-lookup"><span data-stu-id="3a286-117">LastSequence</span></span> |
|--------|--------------|
| <span data-ttu-id="3a286-118">1</span><span class="sxs-lookup"><span data-stu-id="3a286-118">1</span></span>      | <span data-ttu-id="3a286-119">100</span><span class="sxs-lookup"><span data-stu-id="3a286-119">100</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="3a286-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a286-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a286-121">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="3a286-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



