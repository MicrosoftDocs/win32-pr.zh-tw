---
description: 深入瞭解： JET_PSTR
title: JET_PSTR
TOCTitle: JET_PSTR
ms:assetid: acb1143f-a5ee-4088-9f05-cc2aeef23442
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294056(v=EXCHG.10)
ms:contentKeyID: 32765667
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
ms.openlocfilehash: 442af61595f8bfdd81d0d36d0d8687f0e0418761
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986091"
---
# <a name="jet_pstr"></a>JET_PSTR


_**適用于：** Windows |Windows伺服器_

## <a name="jet_pstr"></a>JET_PSTR

JET_PSTR 資料類型包含以 null 終止的 ASCII 字串 (char \*) 。

**Windows vista： JET_PSTR** 是在 Windows vista 中引進。

```cpp
    typedef __nullterminated char *  JET_PSTR;
```

### <a name="data-types"></a>資料類型

JET_PSTR

以 Null 終止的 ASCII 字串 (char \*) 。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


