---
description: 將檔案作業排入佇列很有用，因為它可讓您處理整個安裝，而不是透過 INF 區段。
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: 建立佇列和佇列檔案作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977996"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a><span data-ttu-id="a8310-103">建立佇列和佇列檔案作業</span><span class="sxs-lookup"><span data-stu-id="a8310-103">Creating a Queue and Queuing File Operations</span></span>

<span data-ttu-id="a8310-104">將檔案作業排入佇列很有用，因為它可讓您處理整個安裝，而不是透過 INF 區段。</span><span class="sxs-lookup"><span data-stu-id="a8310-104">Queuing the file operations is useful because it enables you to process the installation as a whole, instead of by INF section.</span></span>

<span data-ttu-id="a8310-105">若要建立檔案佇列，請宣告變數來儲存佇列控制碼，然後呼叫 [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) 函數。</span><span class="sxs-lookup"><span data-stu-id="a8310-105">To create a file queue, declare a variable to store the queue handle, then call the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function.</span></span> <span data-ttu-id="a8310-106">建立佇列之後，您可以將複製、重新命名和刪除作業排入佇列，以及掃描檔案佇列以驗證已排入佇列的作業。</span><span class="sxs-lookup"><span data-stu-id="a8310-106">After the queue is created, you can queue copy, rename, and delete operations, as well as scan the file queue to verify enqueued operations.</span></span>

<span data-ttu-id="a8310-107">若要將單一檔案作業加入至佇列，請使用 [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)、 [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)和 [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) 函數。</span><span class="sxs-lookup"><span data-stu-id="a8310-107">To add single file operations to the queue, use the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea), and [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) functions.</span></span>

<span data-ttu-id="a8310-108">[ **複製** 檔案]、[ **刪除** 檔案] 或 [ **重新命名** 檔案] 區段中所列的所有檔案作業，都可以分別使用 [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)、 [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)或 [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)新增至佇列。</span><span class="sxs-lookup"><span data-stu-id="a8310-108">All the file operations listed in a **Copy Files**, **Delete Files**, or **Rename Files** section can be added to the queue by using [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona), or [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectively.</span></span>

<span data-ttu-id="a8310-109">另一種將 INF **安裝** 區段中所列的 [**複製** 檔案] 區段中的所有檔案排入佇列的另一種方式是使用 [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)函式。</span><span class="sxs-lookup"><span data-stu-id="a8310-109">Another way to queue all the files in the **Copy Files** sections listed in an **Install** section of an INF is to use the function, [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span></span>

<span data-ttu-id="a8310-110">下列範例會使用 [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) 函式，將 INF 檔案的 [ **複製** 檔案] 區段中所列之所有檔案的複製作業排入佇列。</span><span class="sxs-lookup"><span data-stu-id="a8310-110">The following example uses the [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) function to enqueue copy operations for all the files listed in a **Copy Files** section of an INF file.</span></span>

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

<span data-ttu-id="a8310-111">在此範例中，MyQueue 是要新增複製作業的佇列，"A： \\ " 指定來源的路徑，而 MyInf 是開啟的 INF 檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8310-111">In the example, MyQueue is the queue to add copy operations to, "A:\\" specifies the path to the source, and MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="a8310-112">參數 *ListInfHandle* 設定為 **Null**，表示複製的區段位於 MyInf 中。</span><span class="sxs-lookup"><span data-stu-id="a8310-112">The parameter *ListInfHandle* is set to **NULL**, indicating that the section for copying is in MyInf.</span></span> <span data-ttu-id="a8310-113">MySection 是 MyInf 中的區段，其中包含要排入佇列以供複製的檔案。</span><span class="sxs-lookup"><span data-stu-id="a8310-113">MySection is the section in MyInf containing the files to queue for copying.</span></span>

<span data-ttu-id="a8310-114">旗標 SP \_ 複製 \_ NOSKIP 和 sp \_ 複製 \_ NOBROWSE 已使用 OR 運算子結合，指出如果發生錯誤，則不應提供使用者略過或流覽檔案的選項。</span><span class="sxs-lookup"><span data-stu-id="a8310-114">The flags SP\_COPY\_NOSKIP and SP\_COPY\_NOBROWSE have been combined using an OR operator to indicate that the user should not be offered options to skip or browse for files if errors occur.</span></span>

 

 



