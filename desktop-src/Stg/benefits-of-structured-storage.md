---
title: 結構化儲存體的優點
description: COM 提供一組統稱為結構化儲存體的服務。
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- 結構化儲存體 Strctd Stg.，優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671672"
---
# <a name="benefits-of-structured-storage"></a><span data-ttu-id="879d6-104">結構化儲存體的優點</span><span class="sxs-lookup"><span data-stu-id="879d6-104">Benefits of Structured Storage</span></span>

<span data-ttu-id="879d6-105">COM 提供一組統稱為結構化儲存體的服務。</span><span class="sxs-lookup"><span data-stu-id="879d6-105">COM provides a set of services collectively called structured storage.</span></span> <span data-ttu-id="879d6-106">這些服務的優點之一，就是減少在一般檔案中儲存個別物件時所產生的效能處罰和負擔。</span><span class="sxs-lookup"><span data-stu-id="879d6-106">Among the benefits of these services is the reduction of performance penalties and overhead associated with storing separate objects in a flat file.</span></span> <span data-ttu-id="879d6-107">COM 會將不同的物件儲存在由兩個主要元素組成的單一結構化檔案中，而不是一般檔案：儲存物件和資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="879d6-107">Instead of a flat file, COM stores the separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="879d6-108">它們會一起運作，如同檔案內的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="879d6-108">Together, they function like a file system within a file.</span></span>

<span data-ttu-id="879d6-109">結構化儲存體可解決效能問題，方法是在每次有新的物件新增至複合檔案時，或現有物件的大小增加時，不需要將檔案完全重寫為儲存區。</span><span class="sxs-lookup"><span data-stu-id="879d6-109">Structured storage solves performance problems by eliminating the need to totally rewrite a file to storage whenever a new object is added to a compound file, or an existing object increases in size.</span></span> <span data-ttu-id="879d6-110">新的資料會寫入至永久儲存區中的下一個可用位置，而儲存物件會更新它所維護之指標的表格，以追蹤其儲存物件和資料流程物件的位置。</span><span class="sxs-lookup"><span data-stu-id="879d6-110">The new data is written to the next available location in permanent storage, and the storage object updates the table of pointers it maintains to track the locations of its storage objects and stream objects.</span></span> <span data-ttu-id="879d6-111">同時，結構化儲存體可讓使用者以單一檔案（而不是個別物件的嵌套階層）來互動和管理複合檔案。</span><span class="sxs-lookup"><span data-stu-id="879d6-111">At the same time, structured storage enables end users to interact and manage a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

<span data-ttu-id="879d6-112">結構化儲存體也有其他優點：</span><span class="sxs-lookup"><span data-stu-id="879d6-112">Structured storage also has other benefits:</span></span>

-   <span data-ttu-id="879d6-113">累加 **式存取**。</span><span class="sxs-lookup"><span data-stu-id="879d6-113">**Incremental access**.</span></span> <span data-ttu-id="879d6-114">如果使用者需要存取複合檔案內的物件，則使用者只能載入和儲存該物件，而不是整個檔案。</span><span class="sxs-lookup"><span data-stu-id="879d6-114">If a user needs access to an object within a compound file, the user can load and save only that object, rather than the entire file.</span></span>
-   <span data-ttu-id="879d6-115">**多重用途**。</span><span class="sxs-lookup"><span data-stu-id="879d6-115">**Multiple use**.</span></span> <span data-ttu-id="879d6-116">有多個使用者或應用程式可以同時在相同的複合檔案中讀取和寫入資訊。</span><span class="sxs-lookup"><span data-stu-id="879d6-116">More than one end user or application can concurrently read and write information in the same compound file.</span></span>
-   <span data-ttu-id="879d6-117">**交易處理**。</span><span class="sxs-lookup"><span data-stu-id="879d6-117">**Transaction processing**.</span></span> <span data-ttu-id="879d6-118">使用者可以在交易模式中讀取或寫入 COM 複合檔案，對檔案所做的變更會經過緩衝處理，之後可以認可至檔案或反轉。</span><span class="sxs-lookup"><span data-stu-id="879d6-118">Users can read or write to COM compound files in transacted mode, where changes made to the file are buffered and can subsequently either be committed to the file or reversed.</span></span>
-   <span data-ttu-id="879d6-119">**記憶體不足的節省**。</span><span class="sxs-lookup"><span data-stu-id="879d6-119">**Low-memory saves**.</span></span> <span data-ttu-id="879d6-120">結構化儲存體提供在記憶體不足的情況下儲存檔案的功能。</span><span class="sxs-lookup"><span data-stu-id="879d6-120">Structured storage provides facilities for saving files in low-memory situations.</span></span>

 

 




