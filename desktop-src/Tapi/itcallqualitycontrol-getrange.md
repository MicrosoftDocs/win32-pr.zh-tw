---
description: GetRange 方法會取得指定之呼叫品質屬性的有效值範圍。
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'ITCallQualityControl：： GetRange 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978708"
---
# <a name="itcallqualitycontrolgetrange-method"></a>ITCallQualityControl：： GetRange 方法

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。 RTC 用戶端 API 提供類似的功能。\]

**GetRange** 方法會取得指定之 [呼叫品質屬性](callqualityproperty.md)的有效值範圍。

## <a name="syntax"></a>語法


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

[**CallQualityProperty**](callqualityproperty.md)列舉的成員。

</dd> <dt>

*plMin* \[擴展\]
</dt> <dd>

輸入屬性的最小有效值。

</dd> <dt>

*plMax* \[擴展\]
</dt> <dd>

輸入屬性的最大有效值。

</dd> <dt>

*plSteppingDelta* \[擴展\]
</dt> <dd>

可以增加或減少屬性值的遞增量。

</dd> <dt>

*plDefault* \[擴展\]
</dt> <dd>

*Property* 參數的預設值。

</dd> <dt>

*plFlags* \[擴展\]
</dt> <dd>

[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出 *屬性* 值的控制方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITCallQualityControl**](itcallqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**CallQualityProperty**](callqualityproperty.md)
</dt> </dl>

 

 




