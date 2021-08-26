---
description: 深入瞭解： JET_PWSTR
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: ca4478684e79dfb698dd30bb21132f597129fdac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479334"
---
# <a name="jet_pwstr"></a>JET_PWSTR


_**適用于：** Windows |Windows伺服器_

## <a name="jet_pwstr"></a>JET_PWSTR

**JET_PWSTR** 資料類型包含以 null 終止的 **Unicode** 字串 (char \*) 。

**Windows vista： JET_PWSTR** 是在 Windows vista 中引進。

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a>資料類型

JET_PWSTR

以 Null 結束的 Unicode 字串 (char \*) 。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


