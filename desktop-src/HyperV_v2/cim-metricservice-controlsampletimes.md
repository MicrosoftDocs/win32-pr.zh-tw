---
description: 允許啟動時間點度量收集的規格，並指定定期資料收集的慣用取樣間隔時間。
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: CIM_MetricService 類別的 ControlSampleTimes 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979178"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a>CIM MetricService 類別的 ControlSampleTimes 方法 \_

允許啟動時間點度量收集的規格，並指定定期資料收集的慣用取樣間隔時間。

每次啟動其他計量的取樣時，都可以使用這個方法所指定的設定。

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

CIM 用戶端可以藉由取出相關的 BaseMetricDefinition 實例並檢查 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)的內容，來檢查計量提供者是否接受要求的取樣間隔時間。**SampleInterval** 屬性。

</dd> <dt>

*RestartGathering* \[在\]
</dt> <dd>

**TRUE** 表示要求收集與度量服務相關聯的所有計量，並使用此方法呼叫重新開機。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

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

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




