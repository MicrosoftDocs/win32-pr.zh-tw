---
title: SystemMonitor. ScaleToFit 方法
description: 調整計數器值以納入圖形中。
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- ScaleToFit 方法 SysMon
- ScaleToFit 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，ScaleToFit 方法
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685810"
---
# <a name="systemmonitorscaletofit-method"></a>SystemMonitor. ScaleToFit 方法

調整計數器值以納入圖形中。

## <a name="syntax"></a>語法


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*selectedCountersOnly* \[在\]
</dt> <dd>

True 表示只調整選取的計數器;否則，則為 false 以調整所有計數器。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此方法會清除圖表視圖。 如果資料來源是記錄檔，SYSMON 就會使用針對每個計數器指定的縮放比例來重繪圖形，或在資料來源為即時活動時開始繪製新計數器值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem.ScaleFactor**](counteritem-scalefactor.md)
</dt> <dt>

[**CounterItem。已選取**](counteritem-selected.md)
</dt> </dl>

 

 





