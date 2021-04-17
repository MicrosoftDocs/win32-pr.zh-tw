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
ms.openlocfilehash: d1c7031d376fbd6b9d946fb9e41561ce4c4b1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469456"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a><span data-ttu-id="ed980-104">建立登錄提供者的 WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="ed980-104">Creating a WHERE clause for the registry provider</span></span>

<span data-ttu-id="ed980-105">為 System Registry 提供者建立適當的 WHERE 子句時，要考慮的重點是，每個事件查詢都必須完整且明確。</span><span class="sxs-lookup"><span data-stu-id="ed980-105">The main points to consider when creating a proper WHERE clause for the System Registry provider is that each event query must be complete and explicit.</span></span> <span data-ttu-id="ed980-106">無法完成且明確地將會產生錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="ed980-106">Failure to be complete and explicit will result in an error message.</span></span>

<span data-ttu-id="ed980-107">若要完成， [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)的 *bstrQuery* 參數中的每個事件查詢都必須包含 WHERE 子句，其中包含指定事件類別中的每個屬性。</span><span class="sxs-lookup"><span data-stu-id="ed980-107">To be complete, each event query in the *bstrQuery* parameter of [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) must contain a WHERE clause that includes each of the properties in the specified event class.</span></span>

<span data-ttu-id="ed980-108">下列範例示範如何設定 *bstrQuery* ，以在「HKEY \_ 本機 \_ 電腦軟體」樹狀結構中註冊樹狀變更事件 \\ 。</span><span class="sxs-lookup"><span data-stu-id="ed980-108">The following example shows how to set *bstrQuery* to register for tree change events in the "HKEY\_LOCAL\_MACHINE\\Software" tree.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



<span data-ttu-id="ed980-109">為了明確地，提供者應該能夠從查詢推斷事件類別中每個屬性的可能值清單。</span><span class="sxs-lookup"><span data-stu-id="ed980-109">To be explicit, the provider should be able to infer from the query a list of possible values for every property in the event class.</span></span>

<span data-ttu-id="ed980-110">下列範例會顯示正確註冊樹狀變更事件的事件查詢。</span><span class="sxs-lookup"><span data-stu-id="ed980-110">The following example shows the event query that correctly registers for tree change events.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



<span data-ttu-id="ed980-111">以下是註冊不正確的範例。</span><span class="sxs-lookup"><span data-stu-id="ed980-111">The following is an example of an incorrect registration.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



<span data-ttu-id="ed980-112">因為沒有任何方法可以評估每個屬性的可能值，WMI 會拒絕錯誤 WBEM E，也就 \_ 是 \_ \_ 任何沒有 WHERE 子句的查詢，或 WHERE 子句過於廣泛而無法使用。</span><span class="sxs-lookup"><span data-stu-id="ed980-112">Because there is no way to evaluate the possible values for each of the properties, WMI rejects with the error WBEM\_E\_TOO\_BROAD any query that either does not have a WHERE clause or if the WHERE clause is too broad to be of any use.</span></span>

 

 



