---
description: 加上標籤的 \_ SYSTEMTIME 結構會定義在偵測到特定的 SYSTEMTIME 屬性值時所顯示的標籤。
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: 'LABELED_SYSTEMTIME 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852711"
---
# <a name="labeled_systemtime-structure"></a>標記的 \_ SYSTEMTIME 結構

加上 **標籤的 \_ SYSTEMTIME** 結構會定義在偵測到特定的 SYSTEMTIME 屬性值時所顯示的標籤。

## <a name="syntax"></a>語法


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a>成員

<dl> <dt>

**值**
</dt> <dd>

您要偵測之屬性的 SYSTEMTIME 值。

</dd> <dt>

**標籤**
</dt> <dd>

偵測到在 **值** 成員中指定的 SYSTEMTIME 值時，所顯示的文字描述或標籤。

</dd> </dl>

## <a name="remarks"></a>備註

[Set](set.md)結構的 **lpLabeledSystemTimeTable** 成員會指向定義一或多個標籤值 **組的集合** 結構陣列。 當您想要顯示標籤來取代在通訊協定封包中找到的特定 LARGEINT 值時，會使用配對。

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

 

 




