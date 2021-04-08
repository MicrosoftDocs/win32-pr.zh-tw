---
title: 將已捕捉的資料儲存至新檔案
description: 將已捕捉的資料儲存至新檔案
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS 訊息
- capFileSaveAs 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673167"
---
# <a name="saving-captured-data-to-a-new-file"></a><span data-ttu-id="b5797-105">將已捕捉的資料儲存至新檔案</span><span class="sxs-lookup"><span data-stu-id="b5797-105">Saving Captured Data to a New File</span></span>

<span data-ttu-id="b5797-106">如果使用者想要儲存已捕捉的資料，則應用程式應該使用 WM CAP 檔案的 [ [**\_ \_ \_ 另存**](wm-cap-file-saveas.md) 新檔] 訊息 (或 [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) 宏) ，將該檔案的內容儲存至另一個檔案。</span><span class="sxs-lookup"><span data-stu-id="b5797-106">If the user wants to save captured data, the application should save the contents of the capture file to another file by using the [**WM\_CAP\_FILE\_SAVEAS**](wm-cap-file-saveas.md) message (or the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro).</span></span> <span data-ttu-id="b5797-107">此訊息不會變更 capture 檔案的名稱或內容。</span><span class="sxs-lookup"><span data-stu-id="b5797-107">This message does not change the name or contents of the capture file.</span></span> <span data-ttu-id="b5797-108">您的應用程式必須指定新檔案的名稱，因為 capture 檔會保留其原始檔案名。</span><span class="sxs-lookup"><span data-stu-id="b5797-108">Your application must specify a name for the new file because the capture file retains its original filename.</span></span>

<span data-ttu-id="b5797-109">一般情況下，會針對預期的最大 capture 區段預先配置 capture 檔案，而且只會使用其中一部分來捕捉資料。</span><span class="sxs-lookup"><span data-stu-id="b5797-109">Typically, a capture file is preallocated for the largest capture segment anticipated, and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="b5797-110">此訊息只會複製包含 capture 資料之 capture 檔案的部分。</span><span class="sxs-lookup"><span data-stu-id="b5797-110">This message copies only the portion of the capture file containing the capture data.</span></span>

 

 




