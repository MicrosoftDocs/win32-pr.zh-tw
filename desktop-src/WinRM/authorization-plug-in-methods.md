---
title: 授權外掛程式方法
description: 所有授權外掛程式進入點都有回呼機制，可報告呼叫成功或失敗。 某些回呼機制會呼叫多次，直到報告所有結果為止。
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db09430d83e91a8df25dbbc09607c3a9ac3cad266f3a15c1738565c651271b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955328"
---
# <a name="authorization-plug-in-methods"></a>授權外掛程式方法

所有授權外掛程式進入點都有回呼機制，可報告呼叫成功或失敗。 某些回呼機制會呼叫多次，直到報告所有結果為止。

下表提供授權回呼方法的總覽。



| 方法                                                                           | 描述                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | 報告成功或失敗的使用者操作。                |
| [**WSManPluginAuthzQueryQuotaComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | 報告與指定使用者相關的配額詳細資料。      |
| [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | 報告成功或失敗的使用者連接授權。 |



 

 

 




