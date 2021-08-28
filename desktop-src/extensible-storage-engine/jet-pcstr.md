---
description: 深入瞭解： JET_PCSTR
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 9ed32b23f99ad9e19d5384bfab1f81ff5ee6a181
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478464"
---
# <a name="jet_pcstr"></a>JET_PCSTR


_**適用于：** Windows |Windows伺服器_

## <a name="jet_pcstr"></a>JET_PCSTR

**JET_PCSTR** 資料類型包含以 null 終止的常數 **ASCII** 字串 (char \*) 。

**Windows vista： JET_PCSTR** 是在 Windows vista 中引進。

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a>資料類型

JET_PCSTR

以 Null 終止的常數 ASCII 字串 (char \*) 。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


