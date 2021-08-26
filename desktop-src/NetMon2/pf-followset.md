---
description: PF \_ FOLLOWSET 結構會定義可能在通訊協定之前或之後的通訊協定。
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: 'PF_FOLLOWSET 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d404e602e78452a38343a6e62fce8c5b16941270eaa2825de8339f583c064a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036828"
---
# <a name="pf_followset-structure"></a>PF \_ FOLLOWSET 結構

**PF \_ FOLLOWSET** 結構會定義可能在通訊協定之前或之後的通訊協定。

## <a name="syntax"></a>語法


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a>成員

<dl> <dt>

**nEntries**
</dt> <dd>

清單中的通訊協定數目。

</dd> <dt>

**進入**
</dt> <dd>

描述每個通訊協定的 [PF \_ FOLLOWENTRY](pf-followentry.md) 結構陣列。

</dd> </dl>

## <a name="remarks"></a>備註

[Pf \_ PARSERINFO](pf-parserinfo.md)結構會使用 **pf \_ FOLLOWSET** 結構來列出剖析器偵測到的通訊協定之前或之後的通訊協定。

網路監視器使用 **PF \_ FOLLOWSET** 結構中的資訊來更新下列特定剖析器的集合。 您必須使用 **HeapAlloc** 來配置 **PF \_ FOLLOWSET** 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PF \_ FOLLOWENTRY](pf-followentry.md)
</dt> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> </dl>

 

 




