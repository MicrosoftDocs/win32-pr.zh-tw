---
title: SystemMonitor. SetLogViewRange 方法
description: 設定用來從記錄檔中取出計數器值的開始日期。
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- SetLogViewRange 方法 SysMon
- SetLogViewRange 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，SetLogViewRange 方法
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384241"
---
# <a name="systemmonitorsetlogviewrange-method"></a>SystemMonitor. SetLogViewRange 方法

設定用來從記錄檔中取出計數器值的開始日期。

## <a name="syntax"></a>語法


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartTime* \[在\]
</dt> <dd>

用來從記錄檔中取出計數器值的開始日期。

</dd> <dt>

*StopTime* \[在\]
</dt> <dd>

用來從記錄檔中取出計數器值的結束日期。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

SYSMON 會從開始和停止日期內的記錄檔抓取計數器值（含）。

如果您未指定開始日期，或是將開始日期設定為在記錄檔中找到的日期值範圍之外的日期值，SYSMON 會將值變更為記錄檔中找到的最早日期值。 如果開始值大於停止值，SYSMON 會將開始值變更為與停止值相同的值。

如果您未指定停止值，或將 [停用] 值設定為晚于記錄檔中所包含之最後一個日期的日期值，則 SYSMON 會將此值變更為記錄檔中找到的最新日期值。 如果停止值小於停止值，SYSMON 會將停止值變更為與開始值相同的值。

如果您指定開始和停止日期，則應該在設定 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)之前指定日期。 如果您在設定 **SystemMonitor. DataSourceType** 之後設定日期，則只會從記錄檔中取出第一個計數器值。

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

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





