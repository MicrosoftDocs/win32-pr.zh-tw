---
title: SystemMonitor.BatchingLock 方法
description: 鎖定系統監視器，以防止它從新加入的計數器或記錄檔取樣計數器資料。
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- BatchingLock 方法 SysMon
- BatchingLock 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，BatchingLock 方法
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965911"
---
# <a name="systemmonitorbatchinglock-method"></a>SystemMonitor.BatchingLock 方法

鎖定系統監視器，以防止它從新加入的計數器或記錄檔取樣計數器資料。

## <a name="syntax"></a>語法


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*鎖定* \[在\]
</dt> <dd>

設定為 True 可鎖定系統監視器，以防止它從新加入的計數器或記錄檔取樣計數器資料。 設定為 False 以移除鎖定。

</dd> <dt>

*batchReason* \[在\]
</dt> <dd>

識別您要鎖定之資料的來源。 鎖定和解除鎖定資源時，請使用相同的原因值。 如需可能的值，請參閱 [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) 列舉。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

您必須呼叫這個方法兩次，一次是鎖定來源 (True) 和一次，以 (False) 解除鎖定來源。

您只能放置一個鎖定。 例如，如果您設定 SysmonBatchAddFiles 的鎖定，然後使用 SysmonBatchAddCounters 做為原因來進行第二次呼叫，則第二個呼叫會移除第一個呼叫所放置的鎖定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





