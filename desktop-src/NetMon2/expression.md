---
description: 包含評估為對等的 ANDEXP 陣列群組。
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: " (Netmon. h) 的運算式結構"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971173"
---
# <a name="expression-structure"></a>運算式結構

**運算式** 結構包含 **ANDEXP** 陣列的群組，其會評估為邏輯 AND 運算式中的對等，其格式為

 (ANDEXP 1 && ANDEXP 2 && ANDEXP 3) 。

## <a name="syntax"></a>語法


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a>成員

<dl> <dt>

**nAndExps**
</dt> <dd>

**ANDEXP** 模式的數目。

</dd> <dt>

**AndExp**
</dt> <dd>

**ANDEXP** 模式的陣列。 Capture 篩選器會將這個陣列的所有資料列都排列成邏輯和語句。 請注意，每個運算式結構最多可包含四個 **ANDEXP** 模式。

</dd> </dl>

## <a name="remarks"></a>備註

如需將此結構實作為 capture 篩選器一部分的詳細資訊，請參閱「 [捕獲篩選](capture-filters.md)條件」。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




