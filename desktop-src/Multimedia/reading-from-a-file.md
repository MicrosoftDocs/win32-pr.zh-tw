---
title: 從檔案讀取
description: 從檔案讀取
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021865"
---
# <a name="reading-from-a-file"></a><span data-ttu-id="12d2b-104">從檔案讀取</span><span class="sxs-lookup"><span data-stu-id="12d2b-104">Reading from a File</span></span>

<span data-ttu-id="12d2b-105">您可以使用 [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) 函式來取得開啟檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="12d2b-105">You can retrieve information about an open file by using the [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) function.</span></span> <span data-ttu-id="12d2b-106">此函式會使用這類資訊來填滿 [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) 結構，包括最大資料速率、檔案中的資料流程數目、檔案是否使用索引，以及檔案是否受保護。</span><span class="sxs-lookup"><span data-stu-id="12d2b-106">This function fills the [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) structure with such information as the maximum data rate, the number of streams in the file, whether the file uses an index, and whether the file is copyrighted.</span></span>

<span data-ttu-id="12d2b-107">若要取得 AVI 檔案中的補充資訊，請使用 [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) 函數。</span><span class="sxs-lookup"><span data-stu-id="12d2b-107">To retrieve supplementary information in an AVI file, use the [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) function.</span></span> <span data-ttu-id="12d2b-108">補充資訊適用于整個檔案，而且不會包含在一般檔案標頭中。</span><span class="sxs-lookup"><span data-stu-id="12d2b-108">Supplementary information is applicable to the entire file and is not included in the normal file headers.</span></span> <span data-ttu-id="12d2b-109">例如，持有檔案著作權的公司或人員名稱可能是補充資訊。</span><span class="sxs-lookup"><span data-stu-id="12d2b-109">For example, the name of the company or person who holds the copyrights of a file could be supplementary information.</span></span> <span data-ttu-id="12d2b-110">補充資訊不遵守特定格式;它可以是檔案特定的。</span><span class="sxs-lookup"><span data-stu-id="12d2b-110">Supplementary information does not adhere to a specific format; it can be file specific.</span></span> <span data-ttu-id="12d2b-111">**AVIFileReadData** 會在應用程式提供的緩衝區中傳回補充資訊。</span><span class="sxs-lookup"><span data-stu-id="12d2b-111">**AVIFileReadData** returns the supplementary information in an application-supplied buffer.</span></span>

 

 




