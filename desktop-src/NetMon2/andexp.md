---
description: ANDEXP 結構包含用來評估框架資料的模式比對陣列。
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: 'ANDEXP 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319711"
---
# <a name="andexp-structure"></a>ANDEXP 結構

**ANDEXP** 結構包含用來評估框架資料的模式比對陣列。

## <a name="syntax"></a>語法


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a>成員

<dl> <dt>

**nPatternMatches**
</dt> <dd>

模式相符專案的數目。

</dd> <dt>

**PatternMatch**
</dt> <dd>

模式比對元素的陣列。 請注意，每個 **ANDEXP** 結構最多可包含四個模式 match 元素。 如需此成員的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md)」。

</dd> </dl>

## <a name="remarks"></a>備註

**PatternMatch** \[ MAX 模式陣列中的 \_ 模式 \] 會聯結為邏輯 OR 語句中的對等，格式為

 (模式 1 \| \| 模式2模式 \| \| 3) 。

如需有關如何執行此結構的詳細資訊，請參閱「 [捕獲篩選準則](capture-filters.md) 」。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




