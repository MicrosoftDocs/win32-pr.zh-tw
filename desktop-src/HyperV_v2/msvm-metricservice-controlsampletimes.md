---
description: 設定控制項取樣時間。
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Msvm_MetricService 類別的 ControlSampleTimes 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ea13050c2c8e52d5786a97b3b749f10e48a73c4ecf1274e0415967ad25c9d9ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521478"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a>Msvm MetricService 類別的 ControlSampleTimes 方法 \_

設定控制項取樣時間。

## <a name="syntax"></a>語法


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartSampleTime* \[在\]
</dt> <dd>

開始計量取樣的時間點。

99990101000000.000000 + 000 的值應該指出在下一次同步處理至全小時時，應開始取樣。 當午夜模數取樣間隔（以秒為單位）等於0之後，取樣會同步處理至全小時。

</dd> <dt>

*PreferredSampleInterval* \[在\]
</dt> <dd>

慣用的取樣間隔時間。 若要取得相關計量，建議您選擇取樣間隔，方法是3600模數取樣間隔時間（秒）等於0。

CIM 計量服務的責任是要決定是否接受要求的取樣間隔時間。

CIM 用戶端可以藉由取出相關的 BaseMetricDefinition 實例並檢查 "CIM \_ BaseMetricDefinition. SampleInterval" 屬性的內容，來檢查計量提供者是否接受要求的取樣間隔時間。

</dd> <dt>

*RestartGathering* \[在\]
</dt> <dd>

布林值，當設為 TRUE 時，要求收集與計量服務相關聯的所有計量都會透過此方法呼叫重新開機。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值：

<dl> <dt>

**成功** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**失敗** (2) 
</dt> <dt>

**方法保留** ( .。。) 
</dt> <dt>

**廠商特定** (32768. 65535) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




