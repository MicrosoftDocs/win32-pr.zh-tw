---
description: 深入瞭解： JET_PCWSTR
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: 1eda03d9c08e0e18f1a60e088405919f3982e9de
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476148"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**適用于：** Windows |Windows伺服器_

## <a name="jet_pcwstr"></a>JET_PCWSTR

**JET_PCWSTR** 資料類型包含以 null 終止的常數 **Unicode** 字串 (char \*) 。

**Windows vista： JET_PCWSTR** 是在 Windows vista 中引進。

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>資料類型

JET_PCWSTR

以 Null 終止的常數 Unicode 字串 (char \*) 。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


