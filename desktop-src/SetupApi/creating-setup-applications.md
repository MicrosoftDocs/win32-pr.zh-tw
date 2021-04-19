---
description: 建立 INF 檔案之後，您通常會為安裝應用程式撰寫原始程式碼。 您可以從安裝應用程式呼叫安裝程式函數，以執行許多安裝作業。
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: 建立安裝程式應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975346"
---
# <a name="creating-setup-applications"></a><span data-ttu-id="c1987-104">建立安裝程式應用程式</span><span class="sxs-lookup"><span data-stu-id="c1987-104">Creating Setup Applications</span></span>

<span data-ttu-id="c1987-105">建立 INF 檔案之後，您通常會為安裝應用程式撰寫原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="c1987-105">After you create an INF file, you will typically write the source code for your setup application.</span></span> <span data-ttu-id="c1987-106">您可以從安裝應用程式呼叫安裝程式函數，以執行許多安裝作業。</span><span class="sxs-lookup"><span data-stu-id="c1987-106">You call the setup functions from your setup application to perform many installation operations.</span></span>

<span data-ttu-id="c1987-107">下列步驟說明使用安裝函式來建立安裝程式的一種方式。</span><span class="sxs-lookup"><span data-stu-id="c1987-107">The following steps cover one way to use the setup functions to create a setup application.</span></span> <span data-ttu-id="c1987-108">您可以使用此範例作為起點，或開發您自己的安裝演算法。</span><span class="sxs-lookup"><span data-stu-id="c1987-108">You can use this example as a starting point, or develop your own installation algorithm.</span></span>

<span data-ttu-id="c1987-109">**初始 化**</span><span class="sxs-lookup"><span data-stu-id="c1987-109">**Initialization**</span></span>

-   [<span data-ttu-id="c1987-110">開啟 INF，並在適當的情況下附加其他 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="c1987-110">Open the INF and, if appropriate, append other INF files.</span></span>](opening-the-inf-file.md)
-   [<span data-ttu-id="c1987-111">從 INF 檔案解壓縮檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="c1987-111">Extract file information from the INF file.</span></span>](extracting-file-information-from-the-inf-file.md)
-   [<span data-ttu-id="c1987-112">收集使用者的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="c1987-112">Gather setup information from the user.</span></span>](gathering-setup-information-from-the-user.md)
-   [<span data-ttu-id="c1987-113">建立佇列。</span><span class="sxs-lookup"><span data-stu-id="c1987-113">Create a queue.</span></span>](creating-a-queue-and-queuing-file-operations.md)

<span data-ttu-id="c1987-114">**安裝檔案**</span><span class="sxs-lookup"><span data-stu-id="c1987-114">**Install files**</span></span>

-   [<span data-ttu-id="c1987-115">認可佇列，並指定回呼常式。</span><span class="sxs-lookup"><span data-stu-id="c1987-115">Commit the queue, specifying a callback routine.</span></span>](committing-the-queue.md)
-   [<span data-ttu-id="c1987-116">更新登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="c1987-116">Update registry information.</span></span>](updating-registry-information.md)

<span data-ttu-id="c1987-117">**清理**</span><span class="sxs-lookup"><span data-stu-id="c1987-117">**Clean up**</span></span>

-   [<span data-ttu-id="c1987-118">關閉檔案佇列和 INF。</span><span class="sxs-lookup"><span data-stu-id="c1987-118">Close the file queue and INF.</span></span>](closing-the-file-queue-and-inf-file.md)
-   [<span data-ttu-id="c1987-119">釋放任何其他系統資源並結束程式。</span><span class="sxs-lookup"><span data-stu-id="c1987-119">Release any other system resources and end the program.</span></span>](releasing-other-system-resources.md)

 

 



