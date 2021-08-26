---
description: IUpdateServiceManager 介面會定義下列方法。
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: IUpdateServiceManager 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1486727db4ed4e9b561c19a1a2f3994bca0085e836ae774fda1c7db76df38144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994348"
---
# <a name="iupdateservicemanager-methods"></a>IUpdateServiceManager 方法

[**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)介面會定義下列方法。



| 方法                                                                           | 描述                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | 使用 Windows Update 代理程式 (WUA) 註冊掃描封裝即服務，然後傳回 [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)介面。    |
| [**AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | 向 WUA 註冊服務。                                                                                                                    |
| [**RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | 使用自動更新註冊服務。                                                                                                      |
| [**RemoveService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | 從 WUA 移除服務註冊。                                                                                                         |
| [**SetOption**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | 設定指定服務識別碼之物件的選項，以及在變更自動更新的註冊時是否顯示警告。 |
| [**UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | 使用自動更新取消註冊服務。                                                                                                    |



 

 

 



