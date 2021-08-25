---
description: 在事件檢視器的上方窗格中提供一條線，作為所有可能插入資料行之資料的容器。
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: 'NMCOLUMNVARIANT 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 814b419909591e45c07b3ed499072ec4871cdeb1f4c5a355277a03d0623d264c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890018"
---
# <a name="nmcolumnvariant-structure"></a>NMCOLUMNVARIANT 結構

**NMCOLUMNVARIANT** 結構會在事件檢視器的上方窗格中提供一條線，作為所有可能插入資料行之資料的容器。

## <a name="syntax"></a>語法


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a>成員

<dl> <dt>

**類型**
</dt> <dd>

[**NMCOLUMNTYPE**](nmcolumntype.md)列舉型別中的值。

</dd> <dt>

**值**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

8位不帶正負號的整數值。

</dd> <dt>

**Sint8Val**
</dt> <dd>

8位帶正負號的整數值。

</dd> <dt>

**Uint16Val**
</dt> <dd>

16位不帶正負號的整數值。

</dd> <dt>

**Sint16Val**
</dt> <dd>

16位帶正負號的整數值。

</dd> <dt>

**Uint32Val**
</dt> <dd>

32位不帶正負號的整數值。

</dd> <dt>

**Sint32Val**
</dt> <dd>

32位帶正負號的整數值。

</dd> <dt>

**Float64Val**
</dt> <dd>

64位浮點值。

</dd> <dt>

**FrameVal**
</dt> <dd>

畫面格編號。

</dd> <dt>

**YesNoVal**
</dt> <dd>

顯示 [是] 或 [否]。

</dd> <dt>

**OnOffVal**
</dt> <dd>

顯示為開啟或關閉。

</dd> <dt>

**TrueFalseVal**
</dt> <dd>

顯示 True 或 False。

</dd> <dt>

**MACAddrVal**
</dt> <dd>

MAC 位址。

</dd> <dt>

**IPXAddrVal**
</dt> <dd>

IPX 位址。

</dd> <dt>

**IPAddrVal**
</dt> <dd>

IP 位址。

</dd> <dt>

**VarTimeVal**
</dt> <dd>

變異時間。 使用 **VariantTimetoSystemTime** 轉換為系統時間。

</dd> <dt>

**pStringVal**
</dt> <dd>

字串的指標。

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NMCOLUMNTYPE**](nmcolumntype.md)
</dt> </dl>

 

 




