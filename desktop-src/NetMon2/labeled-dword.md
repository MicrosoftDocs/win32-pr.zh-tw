---
description: 加上標籤的 \_ dword 結構會定義在偵測到特定的 dword 屬性值時所顯示的標籤。
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: 'LABELED_DWORD 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 10f3e0dd09b37821a00f2c10f99c0ea6d509ff388e9d7394a8b2c4958438f979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364843"
---
# <a name="labeled_dword-structure"></a>標記的 \_ DWORD 結構

加上 **標籤的 \_ dword** 結構會定義在偵測到特定的 dword 屬性值時所顯示的標籤。

## <a name="syntax"></a>語法


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a>成員

<dl> <dt>

**值**
</dt> <dd>

您要偵測之屬性的 DWORD 值。

</dd> <dt>

**標籤**
</dt> <dd>

偵測到在 **值** 成員中指定的 DWORD 值時所顯示的文字描述或標籤。

</dd> </dl>

## <a name="remarks"></a>備註

[Set](set.md)結構的 **lpLabeledDwordTable** 成員會指向定義一個或多個 DWORD 值組之 **Label** 成員的 **集合** 結構陣列。 當您想要顯示標籤來取代在通訊協定封包中找到的特定 DWORD 值時，會使用配對。

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

 

 




