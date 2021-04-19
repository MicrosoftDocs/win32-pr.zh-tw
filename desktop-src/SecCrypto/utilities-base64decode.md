---
description: 從 base64 解碼字串。
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Base64Decode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993343"
---
# <a name="utilitiesbase64decode-method"></a>Base64Decode 方法

\[**Base64Decode** 方法可用於 [需求] 區段中指定的作業系統。\]

**Base64Decode** 方法會從 base64 解碼字串。

## <a name="syntax"></a>語法


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*EncodedString* \[在\]
</dt> <dd>

要解碼的 base64 編碼字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

解碼的字串。

## <a name="remarks"></a>備註

Base64 編碼是用來傳輸二進位資料的配置。 Base64 以24位群組的形式處理資料，將此資料對應到四個編碼的字元。 Base64 編碼有時稱為「3對4編碼」。 24位群組的每6位都是用來做為對應表的索引， (base64 字母) 來取得編碼資料的字元。 編碼的資料行長度限制為76個字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**公用程式**](utilities.md)
</dt> </dl>

 

 




