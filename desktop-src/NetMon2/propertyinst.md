---
description: PROPERTYINST 結構會在一段可辨識的資料中定義屬性的實例。 當屬性附加至 capture 時，網路監視器會配置並填入 PROPERTYINST 結構。
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: 'PROPERTYINST 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977042"
---
# <a name="propertyinst-structure"></a>PROPERTYINST 結構

**PROPERTYINST** 結構會在一段可辨識的資料中定義屬性的實例。 當屬性附加至 capture 時，網路監視器會配置並填入 **PROPERTYINST** 結構。

## <a name="syntax"></a>語法


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a>成員

<dl> <dt>

**lpPropertyInfo**
</dt> <dd>

定義屬性之 [PROPERTYINFO](propertyinfo.md) 結構的指標。

</dd> <dt>

**szPropertyText**
</dt> <dd>

在網路監視器 UI 的詳細資料窗格中顯示之字串的指標。

</dd> <dt>

**lpData**
</dt> <dd>

屬性之資料開頭的指標。 剖析器會決定屬性資料的開始位置。

</dd> <dt>

**lpByte**
</dt> <dd>

**位元組** 資料的指標。

</dd> <dt>

**lpWord**
</dt> <dd>

**文字** 資料的指標。

</dd> <dt>

**lpDword**
</dt> <dd>

**DWORD** 資料的指標。

</dd> <dt>

**lpLargeInt**
</dt> <dd>

[**LARGEINT**](largeint.md)資料的指標。

</dd> <dt>

**lpSysTime**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)資料的指標。

</dd> <dt>

**lpPropertyInstEx**
</dt> <dd>

[PROPERTYINSTEX](propertyinstex.md)結構的指標。 只有在呼叫 [AttachPropertyInstanceEx](attachpropertyinstanceex.md)時，才會使用 **lpPropertyInstEx** 成員。

如果使用 **lpPropertyInstEx** ，您必須將 **DataLength** 成員設定為0xffff。

</dd> <dt>

**DataLength**
</dt> <dd>

這個屬性實例的資料長度。 如果 **lpPropertyInstEx** 成員指向 [**PROPERTYINSTEX**](propertyinstex.md) 結構，則必須將 **DataLength** 設定為0xffff。

</dd> <dt>

**Level**
</dt> <dd>

層級資訊。

</dd> <dt>

**HelpID**
</dt> <dd>

說明檔內容識別碼。

</dd> <dt>

**IFlags**
</dt> <dd>

錯誤條件旗標。

</dd> </dl>

## <a name="remarks"></a>備註

**PROPERTYINST** 結構會定義附加屬性的實例。 剖析器會透過數個 helper 函數來存取 **PROPERTYINST** 結構。 例如，當呼叫 [**FormatPropertyInstance**](formatpropertyinstance.md)函數來格式化屬性的資料時，它會修改 **PROPERTYINST** 結構的 **szPropertyText** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> </dl>

 

