---
title: 寫入檔案
description: 寫入檔案
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967836"
---
# <a name="writing-to-a-file"></a><span data-ttu-id="878e6-104">寫入檔案</span><span class="sxs-lookup"><span data-stu-id="878e6-104">Writing to a File</span></span>

<span data-ttu-id="878e6-105">您可以使用 [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) 函式，將補充資訊寫入已使用寫入權限開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="878e6-105">You can write supplementary information to a file that has been opened with write privileges by using the [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) function.</span></span> <span data-ttu-id="878e6-106">此函式會從應用程式提供的緩衝區複製資訊，並將其放入檔案中的一或多個區塊。</span><span class="sxs-lookup"><span data-stu-id="878e6-106">This function copies the information from an application-supplied buffer and places it in one or more chunks in the file.</span></span> <span data-ttu-id="878e6-107">"INFO" 區塊是一種常見的 RIFF 區塊類型，其中函數會儲存補充資訊。</span><span class="sxs-lookup"><span data-stu-id="878e6-107">The "INFO" chunk is a common RIFF chunk type in which the function stores supplementary information.</span></span> <span data-ttu-id="878e6-108">如需 RIFF 檔及其資料區塊的說明，請參閱 [資源交換檔案格式服務](resource-interchange-file-format-services.md)。</span><span class="sxs-lookup"><span data-stu-id="878e6-108">For a description of RIFF files and their data chunks, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

 

 




