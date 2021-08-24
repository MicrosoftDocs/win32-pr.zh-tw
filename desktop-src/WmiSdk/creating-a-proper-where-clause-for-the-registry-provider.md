---
title: 建立登錄提供者的 WHERE 子句
description: 為 System Registry 提供者建立適當的 WHERE 子句時，要考慮的重點是，每個事件查詢都必須完整且明確。 無法完成且明確地將會產生錯誤訊息。
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0fc037b746233bd9eb2f9bdd4afad942d07dc832b4dfd60cd9ca6ae9f273efca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679828"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>建立登錄提供者的 WHERE 子句

為 System Registry 提供者建立適當的 WHERE 子句時，要考慮的重點是，每個事件查詢都必須完整且明確。 無法完成且明確地將會產生錯誤訊息。

若要完成， [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)的 *bstrQuery* 參數中的每個事件查詢都必須包含 WHERE 子句，其中包含指定事件類別中的每個屬性。

下列範例示範如何設定 *bstrQuery* ，以在「HKEY \_ 本機 \_ 電腦軟體」樹狀結構中註冊樹狀變更事件 \\ 。


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



為了明確地，提供者應該能夠從查詢推斷事件類別中每個屬性的可能值清單。

下列範例會顯示正確註冊樹狀變更事件的事件查詢。


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



以下是註冊不正確的範例。


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



因為沒有任何方法可以評估每個屬性的可能值，WMI 會拒絕錯誤 WBEM E，也就 \_ 是 \_ \_ 任何沒有 WHERE 子句的查詢，或 WHERE 子句過於廣泛而無法使用。

 

 



