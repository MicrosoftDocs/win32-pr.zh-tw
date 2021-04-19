---
description: 以 base64 編碼字串。
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Base64Encode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994656"
---
# <a name="utilitiesbase64encode-method"></a>Base64Encode 方法

\[**Base64Encode** 方法可用於 [需求] 區段中指定的作業系統。\]

**Base64Encode** 方法會將字串編碼為 base64。

## <a name="syntax"></a>語法


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*SrcString* \[在\]
</dt> <dd>

要以 base64 編碼的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

Base64 編碼的字串。

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

 

 




