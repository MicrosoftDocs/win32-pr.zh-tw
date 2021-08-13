---
title: QMGR 介面
description: 使用下列佇列管理員 (QMGR) 介面，以下載檔案並監視下載佇列中的作業。
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17bd3c27fad81416b916b52b055bc879b44f251113d43b6118e179b609762fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679992"
---
# <a name="qmgr-interfaces"></a>QMGR 介面

\[佇列管理員 (QMGR) 介面可用於主題的需求一節中指定的作業系統。 在後續的版本中，我們可能會修改其功能或不再提供。 請改用 [BITS 介面](bits-interfaces.md)。\]

使用下列佇列管理員 (QMGR) 介面，以下載檔案並監視下載佇列中的作業。



| 介面                                                                 | 描述                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBackgroundCopyCallback1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | 當事件發生時，執行以接收通知。<br/>                                                                                               |
| [**IBackgroundCopyGroup**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | 使用管理群組。 例如，將作業新增至群組、設定群組的屬性，以及啟動和停止下載佇列中的群組。<br/> |
| [**IBackgroundCopyJob1**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | 用來將檔案新增至作業，並取得作業的狀態。<br/>                                                                                         |
| [**IBackgroundCopyQMgr**](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | 用來建立新的群組、取出現有的群組，或列舉佇列中的所有群組。<br/>                                                       |
| [**IEnumBackgroundCopyGroups**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | 用來取得下載佇列中的群組清單。<br/>                                                                                            |
| [**IEnumBackgroundCopyJobs1**](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | 用來取得群組中的作業清單。<br/>                                                                                                       |



 

 

 





