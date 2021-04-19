---
description: PF \_ HANDOFFSET 結構會定義交給剖析器的通訊協定，或剖析器所用的通訊協定。
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: 'PF_HANDOFFSET 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984970"
---
# <a name="pf_handoffset-structure"></a>PF \_ HANDOFFSET 結構

**PF \_ HANDOFFSET** 結構會定義交給剖析器的通訊協定，或剖析器所用的通訊協定。

## <a name="syntax"></a>語法


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a>成員

<dl> <dt>

**nEntries**
</dt> <dd>

通訊協定數目。

</dd> <dt>

**進入**
</dt> <dd>

定義每個通訊協定的 [PF \_ HANDOFFENTRY](pf-handoffentry.md) 結構陣列。

</dd> </dl>

## <a name="remarks"></a>備註

[Pf \_ PARSERINFO](pf-parserinfo.md)結構會使用 **pf \_ HANDOFFSET** 結構來列出下列各項：

-   哪些通訊協定會交給剖析器。
-   剖析器所要關閉的通訊協定。

您必須使用 **HeapAlloc** 來配置 **PF \_ HANDOFFSET** 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[PF \_ HANDOFFENTRY](pf-handoffentry.md)
</dt> </dl>

 

 




