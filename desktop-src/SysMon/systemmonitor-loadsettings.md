---
title: SystemMonitor. LoadSettings 方法
description: 將 HTML 範本檔案中的計數器加入至系統監視器。
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- LoadSettings 方法 SysMon
- LoadSettings 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，LoadSettings 方法
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384709"
---
# <a name="systemmonitorloadsettings-method"></a>SystemMonitor. LoadSettings 方法

將 HTML 範本檔案中的計數器加入至系統監視器。

## <a name="syntax"></a>語法


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*SettingsFileName* \[在\]
</dt> <dd>

HTML 字串，指定要加入至系統監視器的計數器。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

若要將系統監視器中的目前計數器儲存至 HTML 檔案，請呼叫 [**SystemMonitor**](systemmonitor-saveas.md) 方法。

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

 

 





