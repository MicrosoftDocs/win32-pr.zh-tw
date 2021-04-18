---
title: 授權外掛程式方法
description: 所有授權外掛程式進入點都有回呼機制，可報告呼叫成功或失敗。 某些回呼機制會呼叫多次，直到報告所有結果為止。
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965982"
---
# <a name="authorization-plug-in-methods"></a>授權外掛程式方法

所有授權外掛程式進入點都有回呼機制，可報告呼叫成功或失敗。 某些回呼機制會呼叫多次，直到報告所有結果為止。

下表提供授權回呼方法的總覽。



| 方法                                                                           | 描述                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | 報告成功或失敗的使用者操作。                |
| [**WSManPluginAuthzQueryQuotaComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | 報告與指定使用者相關的配額詳細資料。      |
| [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | 報告成功或失敗的使用者連接授權。 |



 

 

 




