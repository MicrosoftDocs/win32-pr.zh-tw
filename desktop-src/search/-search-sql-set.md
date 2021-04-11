---
description: SET 語句會指定查詢的 PROPERTYNAME 和 RANKMETHOD 選項。
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: SET 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112413"
---
# <a name="set-statement"></a>SET 語句

SET 語句會指定查詢的 PROPERTYNAME 和 RANKMETHOD 選項。

## <a name="propertyname"></a>PROPERTYNAME

您可以使用下列語法，將屬性與查詢的易記別名建立關聯：


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a>RANKMETHOD

您可以使用下列語法，針對具有 ISABOUT 詞彙的查詢指定 rank 方法：


```
SET RANKMETHOD <rankmethod>      
```



可以使用 SET 語句來指定的 RANKMETHOD 方法為 JACCARD 係數、骰子係數和內部乘積。

 

 



