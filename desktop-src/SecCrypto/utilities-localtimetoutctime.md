---
description: 將電腦的當地時間轉換成國際標準時間 (格林尼治平均時間) 。
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: LocalTimeToUTCTime 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 03efb6cdfbea712f2fbca194073b89bcee66975481c1a7c0fdc2d7bd385eb652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971019"
---
# <a name="utilitieslocaltimetoutctime-method"></a>LocalTimeToUTCTime 方法

\[**LocalTimeToUTCTime** 方法可用於 [需求] 區段中指定的作業系統。\]

**LocalTimeToUTCTime** 方法會將電腦的當地時間轉換成國際標準時間 (格林尼治平均時間) 。

## <a name="syntax"></a>語法


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*LocalTime* \[在\]
</dt> <dd>

要轉換成國際標準時間的當地時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

對應到指定之本地時間的國際標準時間。

## <a name="remarks"></a>備註

當系統在內部使用國際標準時間時，應用程式通常會顯示本地時間，也就是電腦本地時區的日期和時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**公用程式**](utilities.md)
</dt> </dl>

 

 




