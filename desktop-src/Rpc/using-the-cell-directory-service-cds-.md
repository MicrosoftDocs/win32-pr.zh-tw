---
title: '使用 Cell Directory 服務 (CD) '
description: 如果您有 CD，可以使用它，而不是 Microsoft 定位器。
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- 使用資料格目錄服務進行 RPC、工作的遠端程序呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673255"
---
# <a name="using-the-cell-directory-service-cds"></a><span data-ttu-id="2b15e-104">使用 Cell Directory 服務 (CD) </span><span class="sxs-lookup"><span data-stu-id="2b15e-104">Using the Cell Directory Service (CDS)</span></span>

<span data-ttu-id="2b15e-105">如果您有 CD，可以使用它，而不是 Microsoft 定位器。</span><span class="sxs-lookup"><span data-stu-id="2b15e-105">If you have CDS, you can use it instead of Microsoft Locator.</span></span> <span data-ttu-id="2b15e-106">變更登錄專案，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2b15e-106">Change the registry entries as shown:</span></span>

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

<span data-ttu-id="2b15e-107">變更這些專案將會指向正在執行 NSID 的閘道電腦。</span><span class="sxs-lookup"><span data-stu-id="2b15e-107">Changing these entries will point to a gateway computer that is running the NSID.</span></span> <span data-ttu-id="2b15e-108">這將會用來做為主要定位器。</span><span class="sxs-lookup"><span data-stu-id="2b15e-108">This will be used as the master locator.</span></span> <span data-ttu-id="2b15e-109">當當機時，將不會搜尋替代專案。</span><span class="sxs-lookup"><span data-stu-id="2b15e-109">In the event of a crash, there will be no search for a replacement.</span></span>

 

 




