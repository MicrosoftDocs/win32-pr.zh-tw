---
description: 描述基本 i/o 概念。
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: I/o 概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977097"
---
# <a name="io-concepts"></a><span data-ttu-id="20ae4-103">I/o 概念</span><span class="sxs-lookup"><span data-stu-id="20ae4-103">I/O Concepts</span></span>

<span data-ttu-id="20ae4-104">本節將說明下列 i/o 概念。</span><span class="sxs-lookup"><span data-stu-id="20ae4-104">The following I/O concepts are described in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="20ae4-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="20ae4-105">In this section</span></span>



| <span data-ttu-id="20ae4-106">主題</span><span class="sxs-lookup"><span data-stu-id="20ae4-106">Topic</span></span>                                                                               | <span data-ttu-id="20ae4-107">描述</span><span class="sxs-lookup"><span data-stu-id="20ae4-107">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20ae4-108">檔案緩衝</span><span class="sxs-lookup"><span data-stu-id="20ae4-108">File Buffering</span></span>](file-buffering.md)<br/>                                     | <span data-ttu-id="20ae4-109">描述檔案緩衝的應用程式控制考慮，也稱為未緩衝的檔案輸入/輸出 (i/o) 。</span><span class="sxs-lookup"><span data-stu-id="20ae4-109">Describes considerations for application control of file buffering, also known as unbuffered file input/output (I/O).</span></span><br/>                                    |
| [<span data-ttu-id="20ae4-110">檔案快取</span><span class="sxs-lookup"><span data-stu-id="20ae4-110">File Caching</span></span>](file-caching.md)<br/>                                         | <span data-ttu-id="20ae4-111">Windows 會快取從磁片讀取並寫入磁片的檔案資料。</span><span class="sxs-lookup"><span data-stu-id="20ae4-111">Windows caches file data that is read from disks and written to disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="20ae4-112">同步和非同步 i/o</span><span class="sxs-lookup"><span data-stu-id="20ae4-112">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)<br/> | <span data-ttu-id="20ae4-113">有兩種類型的輸入/輸出 (i/o) 同步處理：同步 i/o 和非同步 i/o。</span><span class="sxs-lookup"><span data-stu-id="20ae4-113">There are two types of input/output (I/O) synchronization: synchronous I/O and asynchronous I/O.</span></span> <span data-ttu-id="20ae4-114">非同步 i/o 也稱為重迭 i/o。</span><span class="sxs-lookup"><span data-stu-id="20ae4-114">Asynchronous I/O is also referred to as overlapped I/O.</span></span><br/> |
| [<span data-ttu-id="20ae4-115">解除擱置中的 i/o 作業</span><span class="sxs-lookup"><span data-stu-id="20ae4-115">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)<br/> | <span data-ttu-id="20ae4-116">允許使用者取消緩慢或封鎖的 i/o 要求，可以增強應用程式的可用性和穩定性。</span><span class="sxs-lookup"><span data-stu-id="20ae4-116">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span><br/>                             |
| [<span data-ttu-id="20ae4-117">可提供警示 i/o</span><span class="sxs-lookup"><span data-stu-id="20ae4-117">Alertable I/O</span></span>](alertable-i-o.md)<br/>                                       | <span data-ttu-id="20ae4-118">可提供警示 i/o 是應用程式執行緒只會在處於可提供警示狀態時處理非同步 i/o 要求的方法。</span><span class="sxs-lookup"><span data-stu-id="20ae4-118">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span><br/>                     |
| [<span data-ttu-id="20ae4-119">I/o 完成埠</span><span class="sxs-lookup"><span data-stu-id="20ae4-119">I/O Completion Ports</span></span>](i-o-completion-ports.md)<br/>                         | <span data-ttu-id="20ae4-120">I/o 完成埠可提供有效率的執行緒模型，以處理多處理器系統上的多個非同步 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="20ae4-120">I/O completion ports provide an efficient threading model for processing multiple asynchronous I/O requests on a multiprocessor system.</span></span><br/>                  |



 

 

 




