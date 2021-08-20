---
description: 下列通知適用于 SetupInstallFile、SetupInstallFileEx 和 SetupInstallFromInfSection 函數。 如需有關通知格式和使用的詳細資訊，請參閱通知。
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: INF 檔案通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b48aff261cd867b1d2f01dbcad79f6e8fdefe49b1cfbba8dd07bb6c4572354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965492"
---
# <a name="inf-file-notifications"></a>INF 檔案通知

下列通知適用于 [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)、 [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)和 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 函數。 如需有關通知格式和使用的詳細資訊，請參閱 [通知](notifications.md)。



| 通知                                                      | 描述                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md) | 檔案正在使用中，而目前的操作會延遲到系統重新開機為止。 |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)   | 目前檔案的語言與系統語言不符。                   |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)   | 目標上已有指定檔案的複本。                             |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)     | 目標上有較新版本的指定檔案。                            |



 

> [!Note]  
> 因為 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 會建立並認可內部檔案佇列，所以它也會使用檔案 [佇列通知](file-queue-notifications.md)。

 

 

 



