---
description: 當您有 INF 檔案的控制碼之後，您可以透過各種方式來抓取它的資訊。 SetupGetInfInformation、SetupQueryInfFileInformation 和 SetupQueryInfVersionInformation 之類的函式會取得 INF 檔案本身的相關資訊。
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: 從 INF 檔案中取出資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979173"
---
# <a name="retrieving-information-from-an-inf-file"></a><span data-ttu-id="ba289-104">從 INF 檔案中取出資訊</span><span class="sxs-lookup"><span data-stu-id="ba289-104">Retrieving Information From an INF File</span></span>

<span data-ttu-id="ba289-105">當您有 INF 檔案的控制碼之後，您可以透過各種方式來抓取它的資訊。</span><span class="sxs-lookup"><span data-stu-id="ba289-105">After you have a handle to an INF file, you can retrieve information from it in a variety of ways.</span></span> <span data-ttu-id="ba289-106">[**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)、 [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)和 [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)之類的函式會取得 INF 檔案本身的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ba289-106">Functions such as [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa), and [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) retrieve information about the INF file itself.</span></span>

<span data-ttu-id="ba289-107">[**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)和 [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)等其他功能會取得來源檔案和目標目錄的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ba289-107">Other functions such as [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) and [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) acquire information about the source files and target directories.</span></span>

<span data-ttu-id="ba289-108">低層級功能（例如 [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) 和 [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) ）可讓您直接存取儲存在 INF 檔案的行或欄位中的資訊。</span><span class="sxs-lookup"><span data-stu-id="ba289-108">Low-level functions like [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) and [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) enable you to directly access information stored in a line or field of an INF file.</span></span> <span data-ttu-id="ba289-109">這些函式會由較高層級的函式在內部使用，但如果您需要存取行或欄位層級的 INF 資訊，也可以使用這些函式。</span><span class="sxs-lookup"><span data-stu-id="ba289-109">These functions are used internally by the higher-level functions, but are also available should you need to access INF information at the line or field level.</span></span>

 

 



