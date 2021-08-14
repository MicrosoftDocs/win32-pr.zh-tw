---
description: 瞭解 Windows Shell 中的子查詢引數。 子查詢是一種儲存的搜尋檔案，您可以用來作為新查詢的篩選準則。
title: 'Windows Shell (的子查詢引數) '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fc478c9aff21b20566ffcd8d10580abaf8affa8eb36c39adb8c3c75486ca999d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452864"
---
# <a name="subquery-argument-the-windows-shell"></a>Windows Shell (的子查詢引數) 

子查詢是已儲存的搜尋檔案 (\* . 搜尋-ms) ，您可以用來作為新查詢的篩選準則。 子查詢的結果會用來作為新查詢的來源。 例如，假設您有數個儲存的搜尋檔案，這些檔案會根據電子郵件通訊群組清單來限制查詢： mydepartment。搜尋-ms、j 和 corporatewide。搜尋-毫秒。 使用 `subquery` 引數可讓您將電子郵件搜尋限制在這些儲存的所有搜尋中。

## <a name="example"></a>範例


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>引數資訊



|                              | 值                                   |
|------------------------------|-----------------------------------------|
| **最低作業系統** | Windows Vista 包含 Service Pack 1 (SP1) |



 

 

 



