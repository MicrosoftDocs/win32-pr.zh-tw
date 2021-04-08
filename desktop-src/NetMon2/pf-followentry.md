---
description: PF \_ FOLLOWENTRY 結構會定義網路監視器新增至一組剖析器的通訊協定。
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: 'PF_FOLLOWENTRY 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850147"
---
# <a name="pf_followentry-structure"></a>PF \_ FOLLOWENTRY 結構

**PF \_ FOLLOWENTRY** 結構會定義網路監視器新增至一組剖析器的通訊協定。

## <a name="syntax"></a>語法


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**szProtocol**
</dt> <dd>

通訊協定的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

[Pf \_ FOLLOWSET](pf-followset.md)結構會使用 **pf \_ FOLLOWENTRY** 結構的陣列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> </dl>

 

 




