---
description: SET 結構會定義一組值。
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: '將結構設定 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d66ba5dd3a977967d0020a00d5813c3f689142b1e58c631c99f9bd10fceba3ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074398"
---
# <a name="set-structure"></a>設定結構

**Set** 結構會定義一組值。

## <a name="syntax"></a>語法


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a>成員

<dl> <dt>

**nEntries**
</dt> <dd>

集合中的總專案數。

</dd> <dt>

**lpByteTable**
</dt> <dd>

位元組值陣列的指標。

</dd> <dt>

**lpWordTable**
</dt> <dd>

文字值陣列的指標。

</dd> <dt>

**lpDwordTable**
</dt> <dd>

DWORD 值陣列的指標。

</dd> <dt>

**lpLargeIntTable**
</dt> <dd>

[LARGEINT](largeint.md)結構陣列的指標。

</dd> <dt>

**lpSystemTimeTable**
</dt> <dd>

SYSTEMTIME 值陣列的指標。

</dd> <dt>

**lpLabeledByteTable**
</dt> <dd>

[標記之 \_ 位元組](labeled-byte.md)結構陣列的指標。 每個 **標示的 \_ 位元組** 結構都會定義值和標籤。 如果在通訊協定封包中找到對應的值，網路監視器會顯示標籤。

</dd> <dt>

**lpLabeledWordTable**
</dt> <dd>

[標記的 \_ 單字](labeled-word.md)結構陣列的指標，此陣列會定義一組文字值和標籤。

</dd> <dt>

**lpLabeledDwordTable**
</dt> <dd>

[標記 \_ dword](labeled-dword.md)結構陣列的指標，該陣列會定義一組 dword 值和標籤。

</dd> <dt>

**lpLabeledLargeIntTable**
</dt> <dd>

[標記 \_ LARGEINT](labeled-largeint.md)結構陣列的指標，這些結構會定義一組 LARGEINT 值和標籤。

</dd> <dt>

**lpLabeledSystemTimeTable**
</dt> <dd>

[標記 \_ SYSTEMTIME](labeled-systemtime.md)結構陣列的指標，這些結構會定義一組系統值和標籤。

</dd> <dt>

**lpLabeledBit**
</dt> <dd>

[標記的 \_ 位](labeled-bit.md)結構陣列的指標，該陣列會定義一組標記的位配對。 每個位都可以針對每個狀態指定兩個標籤 (0 或 1) 位。

</dd> <dt>

**lpVoidTable**
</dt> <dd>

值陣列的指標。

</dd> </dl>

## <a name="remarks"></a>備註

**Set** 結構是用來定義一組比較資料，網路監視器可以用來解讀通訊協定封包中的屬性值。 當需要比較資料集時，會在 [PROPERTYINFO](propertyinfo.md)結構的 **lpSet** 成員中指定 **set** 結構的指標。

剖析器 DLL 可以提供設定的值和標籤。 您在 **集合** 結構中選取之 **聯集的** 成員會指向定義集合每個成員的結構陣列。

-   值集

    當您想要網路監視器使用在通訊協定封包中找到的值來包含內建或非內建的指標時，就會使用值集。 例如，如果指定了 DWORD 集合，網路監視器會顯示在通訊協定封包中找到之每個 DWORD 值的標籤，指出 DWORD 是或未在集合中指定。

    設定的值可以根據 BYTE、WORD、DWORD、LARGEINT 和 SYSTEMTIME 資料類型。

-   標籤集合

    當您想要網路監視器顯示使用者定義的標籤，而不是集合中指定的屬性值時，會使用標籤集合。

    標籤集可以根據位元組、字組、DWORD、LARGEINT、SYSTEMTIME 和位標籤配對來設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[標示為 \_ 位](labeled-bit.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




