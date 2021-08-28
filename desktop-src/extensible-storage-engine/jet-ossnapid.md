---
description: 深入瞭解： JET_OSSNAPID
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: d6185f17c16cbdb2a45e172a14af346c3519aa12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468365"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**適用于：** Windows |Windows伺服器_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

**JET_OSSNAPID** 資料類型包含資料庫快照集的控制碼。

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>資料類型

JET_OSSNAPID

資料庫快照集的控制碼。 此控制碼用於與快照集備份相關的 JET API 元素中。

**Null** 可以用來表示不正確控制碼。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


