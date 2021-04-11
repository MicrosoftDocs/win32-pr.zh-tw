---
description: IUpdateSession3 介面會定義下列方法。
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: IUpdateSession3 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112160"
---
# <a name="iupdatesession3-methods"></a>IUpdateSession3 方法

[**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3)介面會定義下列方法。



| 方法                                                                           | 描述                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpdateServiceManager**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | 傳回會話的 [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) 介面指標。                                                                                                                                                                                                                |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | 傳回 [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) 介面的指標。 介面包含電腦上相符的事件記錄。 這會導致 [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) 方法同步查詢電腦，以取得更新事件的歷程記錄。 |



 

如需此介面所繼承之成員的相關資訊，請參閱下列介面：

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



