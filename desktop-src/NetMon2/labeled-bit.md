---
description: 加上標籤的 \_ 位結構會定義標籤位配對。
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: 'LABELED_BIT 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fe08288929a5f14c4a920c52121c2ccfbdb35888f2ed220291e30e53a3ef0c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364833"
---
# <a name="labeled_bit-structure"></a>標記的 \_ 位結構

加上卷 **標的 \_ 位** 結構會定義標籤位配對。

## <a name="syntax"></a>語法


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a>成員

<dl> <dt>

**BitNumber**
</dt> <dd>

標籤位配對的位。 值的範圍是從0到255。 將 **Bitnumber** 成員設定為用於比較屬性值的位。

</dd> <dt>

**LabelOff**
</dt> <dd>

當 **BitNumber** 中指定的位等於零時，所顯示的字串或標籤。 例如，可能的標籤為 "Bit OFF"。

</dd> <dt>

**LabelOn**
</dt> <dd>

在 **BitNumber** 中指定的位等於1時所顯示的字串或標籤。 例如，可能的標籤是「位在」。

</dd> </dl>

## <a name="remarks"></a>備註

加上卷 **標 \_ 位** 結構的陣列，用來定義一組標籤位配對。 陣列的指標是在 [SET](set.md)結構的 **lpLabeledBit** 成員中指定。 當您想要根據每個位的設定來顯示標籤時，會使用配對。 一般而言，這種類型的集合會用來指出位的 ON 或 OF光圈值。

當指定位集時，網路監視器只會顯示 **集合** 結構陣列中包含的位。 不在 **集合** 結構中的位則不會顯示。

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

 

 




