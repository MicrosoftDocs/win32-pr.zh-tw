---
description: IInstallationJob 介面會定義下列方法。
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: IInstallationJob 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9c188b1d4d749e3bdd9a6f7bdcac179e3703eeb757fd0698dd3bfb67d98fac7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994748"
---
# <a name="iinstallationjob-methods"></a>IInstallationJob 方法

[**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob)介面會定義下列方法。



| 方法                                                | 描述                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**清理**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | 等候非同步作業完成，然後釋放所有回呼。                                                              |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | 傳回 [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) 介面，這個介面會描述安裝或卸載的目前進度。 |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | 提出取消安裝或卸載的要求。                                                                                         |



 

 

 



