---
description: 加上標籤的 \_ LARGEINT 結構會定義在偵測到特定的 LARGEINT 屬性值時所顯示的標籤。
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: 'LABELED_LARGEINT 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026813"
---
# <a name="labeled_largeint-structure"></a>標記的 \_ LARGEINT 結構

加上 **標籤的 \_ LARGEINT** 結構會定義在偵測到特定的 LARGEINT 屬性值時所顯示的標籤。

## <a name="syntax"></a>語法


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a>成員

<dl> <dt>

**值**
</dt> <dd>

您要偵測之屬性的 LARGEINT 值。

</dd> <dt>

**標籤**
</dt> <dd>

偵測到在 **值** 成員中指定的 LARGEINT 值時，所顯示的文字描述或標籤。

</dd> </dl>

## <a name="remarks"></a>備註

[集合](set.md)結構的 **lpLabeledLargeIntTable** 成員會指向定義一或多個 LARGEINT 值配對之 **標籤** 成員的 **集合** 結構陣列。 當您想要顯示標籤來取代在通訊協定封包中找到的特定 LARGEINT 值時，會使用配對。

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

 

 




