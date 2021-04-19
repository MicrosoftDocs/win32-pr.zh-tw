---
description: Imagehlp.dll 函式大多是由程式設計工具、應用程式設定公用程式，以及需要存取 PE 映射中所含資料的其他程式所使用。
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: 關於 Imagehlp.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998434"
---
# <a name="about-imagehlp"></a><span data-ttu-id="1ce16-103">關於 Imagehlp.dll</span><span class="sxs-lookup"><span data-stu-id="1ce16-103">About ImageHlp</span></span>

<span data-ttu-id="1ce16-104">Imagehlp.dll 函式大多是由程式設計工具、應用程式設定公用程式，以及需要存取 PE 映射中所含資料的其他程式所使用。</span><span class="sxs-lookup"><span data-stu-id="1ce16-104">The ImageHlp functions are used mostly by programming tools, application setup utilities, and other programs that need access to the data contained in a PE image.</span></span> <span data-ttu-id="1ce16-105">所有 Imagehlp.dll 函數都是單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="1ce16-105">All ImageHlp functions are single threaded.</span></span> <span data-ttu-id="1ce16-106">因此，從多個執行緒到此函式的呼叫可能會導致非預期的行為或記憶體損毀。</span><span class="sxs-lookup"><span data-stu-id="1ce16-106">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="1ce16-107">若要避免這種情況，您必須將多個執行緒的所有並行呼叫，同步處理至此函式。</span><span class="sxs-lookup"><span data-stu-id="1ce16-107">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

<span data-ttu-id="1ce16-108">下列主題描述 PE 映射以及 Imagehlp.dll 函數所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="1ce16-108">The following topics describe PE images and the functionality provided by the ImageHlp functions.</span></span>

-   [<span data-ttu-id="1ce16-109">PE 格式</span><span class="sxs-lookup"><span data-stu-id="1ce16-109">PE Format</span></span>](pe-format.md)
-   [<span data-ttu-id="1ce16-110">影像存取函式</span><span class="sxs-lookup"><span data-stu-id="1ce16-110">Image Access Functions</span></span>](image-access-functions.md)
-   [<span data-ttu-id="1ce16-111">映射完整性函式</span><span class="sxs-lookup"><span data-stu-id="1ce16-111">Image Integrity Functions</span></span>](image-integrity-functions.md)
-   [<span data-ttu-id="1ce16-112">影像修改函式</span><span class="sxs-lookup"><span data-stu-id="1ce16-112">Image Modification Functions</span></span>](image-modification-functions.md)

 

 



