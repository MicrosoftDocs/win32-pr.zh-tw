---
title: SystemMonitor. SaveAs 方法
description: 將圖形視圖中的計數器值儲存至記錄檔。
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- SaveAs 方法 SysMon
- SaveAs 方法 SysMon、SystemMonitor 物件
- SystemMonitor 物件 SysMon，SaveAs 方法
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf1590b5fdb9f4cdd8bbd52d4349b2423fb1b9883054c24cb5ffb4ac6b52dd2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954986"
---
# <a name="systemmonitorsaveas-method"></a>SystemMonitor. SaveAs 方法

將圖形視圖中的計數器值儲存至記錄檔。

## <a name="syntax"></a>語法


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

記錄檔的檔案路徑。 您可以將路徑指定為絕對路徑、相對路徑或 UNC 路徑。 記錄檔的副檔名必須是 tsv 或 .htm。 如果路徑中的資料夾不存在，SYSMON 會加以建立。 如果檔案存在，則會覆寫檔案。 SYSMON 會從父目錄套用預設 Acl。

</dd> <dt>

*類型類型* \[在\]
</dt> <dd>

儲存至記錄檔的計數器資料格式。 您可以指定 [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) 或 **SysmonFileType.sysmonFileTsv**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

只有儲存的資料點實際數目 (儲存在圖形視圖中可見的計數器資料，請參閱 [**SystemMonitor DataPointCount**](systemmonitor-datapointcount.md)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor**](systemmonitor-relog.md)
</dt> </dl>

 

 





