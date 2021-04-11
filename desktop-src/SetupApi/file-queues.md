---
description: 安裝函數包含檔案佇列功能。
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: 檔案佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944607"
---
# <a name="file-queues"></a><span data-ttu-id="3ed4d-103">檔案佇列</span><span class="sxs-lookup"><span data-stu-id="3ed4d-103">File Queues</span></span>

<span data-ttu-id="3ed4d-104">安裝函數包含檔案佇列功能。</span><span class="sxs-lookup"><span data-stu-id="3ed4d-104">The setup functions include file queue functionality.</span></span> <span data-ttu-id="3ed4d-105">檔案佇列是檔案複製、重新命名和刪除作業的清單。</span><span class="sxs-lookup"><span data-stu-id="3ed4d-105">A file queue is a list of file copying, renaming, and deletion operations.</span></span> <span data-ttu-id="3ed4d-106">您可以依任何順序將這些作業傳送至佇列。</span><span class="sxs-lookup"><span data-stu-id="3ed4d-106">These operations can be sent to the queue in any order.</span></span> <span data-ttu-id="3ed4d-107">認可佇列時，這些作業會以批次方式處理（依作業類型的順序）。</span><span class="sxs-lookup"><span data-stu-id="3ed4d-107">When the queue is committed, these operations are processed as a batch, in order of the operation type.</span></span>

<span data-ttu-id="3ed4d-108">下列各節說明佇列是什麼，以及如何在建立安裝程式應用程式時使用它。</span><span class="sxs-lookup"><span data-stu-id="3ed4d-108">The following sections explain what a queue is and how to use it when creating a setup application.</span></span> <span data-ttu-id="3ed4d-109">此外，也會討論在佇列認可時，排入佇列檔案作業的處理順序，以及佇列傳送至每個階段之回呼常式的通知。</span><span class="sxs-lookup"><span data-stu-id="3ed4d-109">Also discussed is the order in which the enqueued file operations are processed as the queue commits and what notifications the queue sends to a callback routine at each stage.</span></span>

-   [<span data-ttu-id="3ed4d-110">關於檔案佇列</span><span class="sxs-lookup"><span data-stu-id="3ed4d-110">About File Queues</span></span>](about-file-queues.md)
-   [<span data-ttu-id="3ed4d-111">使用檔案佇列</span><span class="sxs-lookup"><span data-stu-id="3ed4d-111">Using File Queues</span></span>](using-file-queues.md)
-   [<span data-ttu-id="3ed4d-112">檔案佇列參考</span><span class="sxs-lookup"><span data-stu-id="3ed4d-112">File Queue Reference</span></span>](file-queue-reference.md)

 

 



