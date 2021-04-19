---
description: 您可以透過兩種方式從封包中解壓縮檔案。 第一個最簡單的方式是利用內建于安裝函式的自動封包處理。
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: 從封包解壓縮檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970849"
---
# <a name="extracting-files-from-cabinets"></a><span data-ttu-id="cbbe3-104">從封包解壓縮檔案</span><span class="sxs-lookup"><span data-stu-id="cbbe3-104">Extracting Files from Cabinets</span></span>

<span data-ttu-id="cbbe3-105">您可以透過兩種方式從封包中解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-105">You can extract files from a cabinet in two ways.</span></span> <span data-ttu-id="cbbe3-106">第一個最簡單的方式是利用內建于安裝函式的自動封包處理。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-106">The first and simplest way is to take advantage of the automatic cabinet processing built into the setup functions.</span></span>

<span data-ttu-id="cbbe3-107">安裝功能（例如 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)、 [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)和 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)）會檢查每個檔案的壓縮。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-107">The installation functions, such as [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), check the compression on each file.</span></span> <span data-ttu-id="cbbe3-108">如果檔案位於封包中，則函式會先在封包外搜尋該名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-108">If the file is in a cabinet, the functions first search for a file of that name outside the cabinet.</span></span> <span data-ttu-id="cbbe3-109">如果找到，則函式會安裝外部檔案，並忽略封包內的檔案。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-109">If found, the functions install the external file, ignoring the file inside the cabinet.</span></span> <span data-ttu-id="cbbe3-110">這可讓您更新封包內的單一檔案，而不需要重建封包。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-110">This enables you to update a single file inside the cabinet without rebuilding the cabinet.</span></span>

<span data-ttu-id="cbbe3-111">安裝函式也會追蹤封包中的哪些檔案已被抓取，因此檔案只會解壓縮一次，即使已安裝多次。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-111">The setup functions also track which files in a cabinet have been retrieved, so that a file is extracted only once, even if it is installed several times.</span></span>

<span data-ttu-id="cbbe3-112">從封包解壓縮檔案的第二種方式是使用 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-112">The second way to extract files from a cabinet is by using [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="cbbe3-113">此函式會逐一查看封包中的每個檔案，將通知傳送給找到的每個檔案的回呼常式。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-113">This function iterates through each file in a cabinet, sending a notification to a callback routine for each file found.</span></span> <span data-ttu-id="cbbe3-114">回呼常式接著會傳回值，指出是否應該解壓縮或略過檔案。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-114">The callback routine then returns a value that indicates whether the file should be extracted or skipped.</span></span>

> [!Note]  
> <span data-ttu-id="cbbe3-115">安裝程式 API 不提供預設回呼常式來處理封包通知。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-115">The Setup API does not supply a default callback routine to handle cabinet notifications.</span></span> <span data-ttu-id="cbbe3-116">如果您明確地呼叫 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) ，您必須提供回呼常式來處理函式傳回的封包通知。</span><span class="sxs-lookup"><span data-stu-id="cbbe3-116">If you call [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitly, you must supply a callback routine to process the cabinet notifications that the function returns.</span></span>

 

 

 



