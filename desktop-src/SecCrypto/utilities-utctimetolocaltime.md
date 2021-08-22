---
description: 將國際標準時間 (格林尼治平均時間) 轉換為電腦的當地時間。
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: UTCTimeToLocalTime 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c1ad7236564fff2f9a3814beda9bedacbf96fbc9ca2678546304ee108891bea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005146"
---
# <a name="utilitiesutctimetolocaltime-method"></a>UTCTimeToLocalTime 方法

\[**UTCTimeToLocalTime** 方法可用於 [需求] 區段中指定的作業系統。\]

**UTCTimeToLocalTime** 方法會將國際標準時間的 (格林威治標準時間) 轉換為電腦的當地時間。

## <a name="syntax"></a>語法


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*UTCTime* \[在\]
</dt> <dd>

要轉換為電腦本地時間的國際標準時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

對應至指定之國際標準時間的當地時間。

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

 

 




