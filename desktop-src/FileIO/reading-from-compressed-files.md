---
description: 應用程式可以使用 LZSeek 和 LZRead 函數，一次將壓縮檔案解壓縮。
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: 從壓縮檔案讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984642"
---
# <a name="reading-from-compressed-files"></a><span data-ttu-id="d4cd6-103">從壓縮檔案讀取</span><span class="sxs-lookup"><span data-stu-id="d4cd6-103">Reading from Compressed Files</span></span>

<span data-ttu-id="d4cd6-104">除了在單一作業中解壓縮完整的檔案之外，應用程式也可以使用 [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) 和 [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) 函式，一次將壓縮檔案解壓縮到一個部分。</span><span class="sxs-lookup"><span data-stu-id="d4cd6-104">In addition to decompressing a complete file in a single operation, an application can decompress a compressed file a portion at a time by using the [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) and [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) functions.</span></span> <span data-ttu-id="d4cd6-105">當需要解壓縮大型檔案的元件時，這些函數特別有用。</span><span class="sxs-lookup"><span data-stu-id="d4cd6-105">These functions are particularly useful when it is necessary to extract parts of large files.</span></span> <span data-ttu-id="d4cd6-106">例如，除了字元資料以外，字型製造商可能會有包含字型度量的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="d4cd6-106">For example, a font manufacturer may have compressed files containing font metrics in addition to character data.</span></span> <span data-ttu-id="d4cd6-107">若要使用這些檔案中的資訊，應用程式必須解壓縮檔案;不過，大部分的應用程式在任何特定時間都只會使用部分檔案。</span><span class="sxs-lookup"><span data-stu-id="d4cd6-107">To use the information in these files, an application would need to decompress the file; however, most applications would use only part of the file at any particular time.</span></span> <span data-ttu-id="d4cd6-108">為了取得字型計量的相關資訊，應用程式會從標頭中提取資料。</span><span class="sxs-lookup"><span data-stu-id="d4cd6-108">To get information about font metrics, the application would extract data from the header.</span></span> <span data-ttu-id="d4cd6-109">若要從文字取得資訊，應用程式會藉由呼叫 **LZSeek** 並藉由呼叫 **LZRead** 來解壓縮字元資料，來重新放置檔案指標的位置。</span><span class="sxs-lookup"><span data-stu-id="d4cd6-109">To get information from the text, the application would reposition the file pointer by calling **LZSeek** and extract character data by calling **LZRead**.</span></span>

 

 



