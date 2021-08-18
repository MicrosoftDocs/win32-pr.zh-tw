---
title: '使用 Cell Directory 服務 (CD) '
description: 如果您有 CD，可以使用它，而不是 Microsoft 定位器。
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- 使用資料格目錄服務進行 RPC、工作的遠端程序呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df9058d917396a4e2e2dc3579768c3f3d5b46242b34c0fa5411c6d2204ed20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010635"
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

 

 




