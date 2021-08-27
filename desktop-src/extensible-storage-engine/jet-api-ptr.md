---
description: 深入瞭解： JET_API_PTR
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
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
ms.openlocfilehash: 401c490c667cd8f9842a7ab0429e10a510e3b06e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466395"
---
# <a name="jet_api_ptr"></a>JET_API_PTR


_**適用于：** Windows |Windows伺服器_

## <a name="jet_api_ptr"></a>JET_API_PTR

**JET_API_PTR** 資料類型會保存整數或指標值。

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a>資料類型

JET_API_PTR

如同 **DWORD_PTR** 資料類型， **JET_API_PTR** 資料類型在32位電腦上定義為4個位元組，在64位電腦上定義為8個位元組。

### <a name="remarks"></a>備註

**JET_API_PTR** 資料類型是用來定義下列資料類型：

  - [JET_HANDLE](./jet-handle.md)

  - [JET_INSTANCE](./jet-instance.md)

  - [JET_SESID](./jet-sesid.md)

  - [JET_TABLEID](./jet-tableid.md)

  - [JET_LS](./jet-ls.md)

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 

