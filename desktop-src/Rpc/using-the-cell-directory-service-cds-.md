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
# <a name="using-the-cell-directory-service-cds"></a>使用 Cell Directory 服務 (CD) 

如果您有 CD，可以使用它，而不是 Microsoft 定位器。 變更登錄專案，如下所示：

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

變更這些專案將會指向正在執行 NSID 的閘道電腦。 這將會用來做為主要定位器。 當當機時，將不會搜尋替代專案。

 

 




