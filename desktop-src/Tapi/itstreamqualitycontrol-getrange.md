---
description: GetRange 方法會取得指定之資料流程品質屬性的有效值範圍。
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'ITStreamQualityControl：： GetRange 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13d07b848ef3be744f40ec1ba4bb4a73514f88204fa1918db661e00d36019ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774468"
---
# <a name="itstreamqualitycontrolgetrange-method"></a>ITStreamQualityControl：： GetRange 方法

\[此方法無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**GetRange** 方法會取得指定之 [**資料流程品質屬性**](streamqualityproperty.md)的有效值範圍。

## <a name="syntax"></a>語法


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

[**StreamQualityProperty**](streamqualityproperty.md)列舉的成員。

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

[**ITStreamQualityControl**](itstreamqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**StreamQualityProperty**](streamqualityproperty.md)
</dt> </dl>

 

 




