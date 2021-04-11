---
title: SystemMonitor 方法
description: 將計數器資料 Relogs 至新的檔案。 您也可以使用這個方法來指定新的檔案類型，並減少記錄檔中包含的樣本數目。
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- 重新 SysMon 方法
- 重新 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，重新的方法
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094367"
---
# <a name="systemmonitorrelog-method"></a>SystemMonitor 方法

將計數器資料 Relogs 至新的檔案。 您也可以使用這個方法來指定新的檔案類型，並減少記錄檔中包含的樣本數目。

## <a name="syntax"></a>語法


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* \[在\]
</dt> <dd>

記錄檔的檔案路徑。 您可以將路徑指定為絕對路徑、相對路徑或 UNC 路徑。 記錄檔副檔名必須是 .blg、tsv 或 .csv。 如果路徑中的資料夾不存在，SYSMON 會加以建立。 如果檔案存在，則會覆寫檔案。 SYSMON 會從父目錄套用預設 Acl。

</dd> <dt>

*類型類型* \[在\]
</dt> <dd>

儲存至記錄檔的計數器資料格式。 您可以指定 [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)、 **SysmonFileType.sysMonFileCsv** 或 **SysmonFileType.sysmonFileTsv**。

</dd> <dt>

*篩選* \[在\]
</dt> <dd>

舊記錄檔中要儲存至新記錄檔的樣本數。 指定1，將舊檔案中的每個範例儲存至新檔案。 指定2以從舊檔案的每個範例中儲存一個。 指定3以從舊檔案的每三個樣本中儲存一份。 依此類推。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會使用 [**SystemMonitor**](systemmonitor-logfiles.md) .log 集合中包含的記錄檔來重新記錄計數器資料。

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

[**SystemMonitor**](systemmonitor-saveas.md)
</dt> </dl>

 

 





