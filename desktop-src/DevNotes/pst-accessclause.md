---
description: 包含受保護儲存體之存取子句的相關資訊。
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: 'PST_ACCESSCLAUSE 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: e5933b762ac19ac188e2d7253e86482caae968abd58ecb02087c32657d250216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386178"
---
# <a name="pst_accessclause-structure"></a>PST \_ ACCESSCLAUSE 結構

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

包含受保護儲存體之存取子句的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

此結構的大小。

</dd> <dt>

**ClauseType**
</dt> <dd>

**PbClauseData** 成員所指向的資料類型。 如需詳細資訊，請參閱 [**PStore 類型**](pstore-types.md)。

</dd> <dt>

**cbClauseData**
</dt> <dd>

**PbClauseData** 成員所指向之資料的大小。

</dd> <dt>

**pbClauseData**
</dt> <dd>

存取子句資料的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PST \_ ACCESSRULE**](pst-accessrule.md)
</dt> </dl>

 

 
