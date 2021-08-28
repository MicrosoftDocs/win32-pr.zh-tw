---
description: 指定 NMCOLUMNVARIANT 結構的成員。
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: 'NMCOLUMNTYPE 列舉 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5e3877a15a55ac1d942a068843173e2771202047691f3df96601fe4b9de3152a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799498"
---
# <a name="nmcolumntype-enumeration"></a>NMCOLUMNTYPE 列舉

**NMCOLUMNTYPE** 列舉會指定 [**NMCOLUMNVARIANT**](nmcolumnvariant.md)結構的成員。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE \_ UINT8**
</dt> <dd>

8位不帶正負號的整數。

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE \_ SINT8**
</dt> <dd>

8位帶正負號的整數。

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE \_ UINT16**
</dt> <dd>

16位不帶正負號的整數。

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE \_ SINT16**
</dt> <dd>

16位帶正負號的整數。

</dd> <dt>

<span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE \_ UINT32**
</dt> <dd>

32位不帶正負號的整數。

</dd> <dt>

<span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE \_ SINT32**
</dt> <dd>

32 位元帶正負號的整數。

</dd> <dt>

<span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE \_ FLOAT64**
</dt> <dd>

64位浮點數。

</dd> <dt>

<span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**NMCOLUMNTYPE \_ 框架**
</dt> <dd>

畫面格編號。

</dd> <dt>

<span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE \_ YESNO**
</dt> <dd>

「是」或「否」。

</dd> <dt>

<span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE \_ ONOFF**
</dt> <dd>

「開啟」或「關閉」

</dd> <dt>

<span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE \_ TRUEFALSE**
</dt> <dd>

"True" 或 "False"。

</dd> <dt>

<span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE \_ MACADDR**
</dt> <dd>

MAC 位址。

</dd> <dt>

<span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE \_ IPXADDR**
</dt> <dd>

IPX 位址。

</dd> <dt>

<span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE \_ IPADDR**
</dt> <dd>

IP 位址。

</dd> <dt>

<span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE \_ VARTIME**
</dt> <dd>

變異時間。

</dd> <dt>

<span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**NMCOLUMNTYPE \_ 字串**
</dt> <dd>

字串的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




