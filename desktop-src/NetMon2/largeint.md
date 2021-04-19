---
description: LARGEINT 資料類型會定義大型 \_ 整數值。
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: 'LARGEINT (Netmon. h) '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967773"
---
# <a name="largeint"></a>LARGEINT

**LARGEINT** 資料類型會定義 [**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)值。


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>備註

[**Set**](set.md)結構的 **lpLargeIntTable** 成員會指向定義一個或多個 LARGEINT 值的 **集合** 結構陣列。 當指定這種類型的 **集合** 結構時，網路監視器會顯示下列其中一個標籤，其中包含在通訊協定封包中找到的每個 LARGEINT 值。

-   符合設定的值。 LARGEINT 值會包含在集合中。
-   未知的設定值。 LARGEINT 值未包含在集合中。

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

 

