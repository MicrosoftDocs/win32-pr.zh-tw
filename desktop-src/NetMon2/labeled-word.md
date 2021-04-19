---
description: 加上標籤的 \_ 單字結構會定義在偵測到特定單字屬性值時所顯示的標籤。
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: 'LABELED_WORD 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985003"
---
# <a name="labeled_word-structure"></a>標記的 \_ WORD 結構

加上 **標籤的 \_ 單字** 結構會定義在偵測到特定單字屬性值時所顯示的標籤。

## <a name="syntax"></a>語法


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a>成員

<dl> <dt>

**值**
</dt> <dd>

您要偵測之屬性的文字值。

</dd> <dt>

**標籤**
</dt> <dd>

偵測到 **值** 成員中指定的文字值時，所顯示的文字描述或標籤。

</dd> </dl>

## <a name="remarks"></a>備註

[Set](set.md)結構的 **lpLabeledWordTable** 成員會指向設定結構的陣列，以定義一或多個標籤值組。 當您想要顯示標籤來取代在通訊協定封包中找到的特定字組值時，會使用這些配對。

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

 

 




