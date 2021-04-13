---
title: SystemMonitor. GetLogViewRange 方法
description: 抓取用來從記錄檔中取出計數器值的開始日期。
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- GetLogViewRange 方法 SysMon
- GetLogViewRange 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，GetLogViewRange 方法
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508588"
---
# <a name="systemmonitorgetlogviewrange-method"></a>SystemMonitor. GetLogViewRange 方法

抓取用來從記錄檔中取出計數器值的開始日期。

## <a name="syntax"></a>語法


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartTime* \[擴展\]
</dt> <dd>

用來從記錄檔中取出計數器值的開始日期。

</dd> <dt>

*StopTime* \[擴展\]
</dt> <dd>

用來從記錄檔中取出計數器值的結束日期。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

SYSMON 會從開始和停止日期內的記錄檔抓取計數器值（含）。

使用這個方法與存取 [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) 和 [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) 屬性相同。

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

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





