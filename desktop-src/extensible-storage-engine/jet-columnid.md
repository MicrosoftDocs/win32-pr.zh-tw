---
description: 深入瞭解： JET_COLUMNID
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d898a5943b5b80e738a331971595995d0fdee4eb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482294"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**適用于：** Windows |Windows伺服器_

## <a name="jet_columnid"></a>JET_COLUMNID

**JET_COLUMNID** 資料類型會識別資料表中的資料行。

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>資料類型

JET_COLUMNID

識別資料表內的資料行。

### <a name="remarks"></a>備註

資料行識別碼在單一資料表中是唯一的。 一旦已知資料行有特定的資料行識別碼，它一定會有該資料行識別碼。 從備份還原將不會變更資料行識別碼的值。 但是，如果在特定資料表資料行之前刪除一或多個資料表資料行，則 compact 資料庫會接著變更資料行識別碼的值。

在某些情況下，資料行識別碼是識別資料行的唯一方法。 建立臨時表時，其資料行沒有名稱，但 create 函數會傳回資料行識別碼的陣列。

不同資料表中的資料行可以有相同的資料行識別碼。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


