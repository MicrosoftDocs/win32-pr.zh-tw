---
description: 加上標籤的 \_ 位元組結構會定義加上標籤的位配對。 當偵測到特定的位元組屬性值時，就會顯示標記位組的標籤。
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: 'LABELED_BYTE 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997849"
---
# <a name="labeled_byte-structure"></a>標記的 \_ 位元組結構

加上 **標籤的 \_ 位元組** 結構會定義加上標籤的位配對。 當偵測到特定的位元組屬性值時，就會顯示標記位組的 **標籤** 。

## <a name="syntax"></a>語法


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a>成員

<dl> <dt>

**值**
</dt> <dd>

您要偵測之屬性的位元組值。

</dd> <dt>

**標籤**
</dt> <dd>

偵測到 **值** 成員中指定的值時，所顯示的文字描述或標籤。

</dd> </dl>

## <a name="remarks"></a>備註

[Set](set.md)結構的 **lpLabeledByteTable** 成員會指向定義一個或多個位元組值組之 **標籤** 成員的 **集合** 結構陣列。 當您想要顯示標籤來取代在通訊協定封包中找到的特定位元組值時，會使用這些配對。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




