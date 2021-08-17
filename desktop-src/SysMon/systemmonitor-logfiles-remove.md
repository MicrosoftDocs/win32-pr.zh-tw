---
title: 記錄檔. Remove 方法
description: 從集合中移除指定的 LogFileItem 實例。
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- 移除方法 SysMon
- Remove 方法 SysMon，記錄檔類別
- 記錄檔類別 SysMon、移除方法
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c12c0bae91df3baf421638665a5587612e6d1404c3300cf02b0308b7bef7d016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955430"
---
# <a name="logfilesremove-method"></a>記錄檔. Remove 方法

從集合中移除指定的 [**LogFileItem**](logfileitem.md) 實例。

## <a name="syntax"></a>語法


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要從集合中移除之記錄檔的整數索引。 索引是以一為基礎。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)的值設定為 sysmonLogFiles，您就無法從 [**記錄檔集合**](systemmonitor-logfiles.md)中移除記錄檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





