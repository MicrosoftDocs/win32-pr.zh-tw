---
title: 記錄檔。新增方法
description: 將記錄檔加入至集合。
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- 新增方法 SysMon
- 新增方法 SysMon，記錄檔類別
- 記錄檔類別 SysMon，加入方法
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103829"
---
# <a name="logfilesadd-method"></a>記錄檔。新增方法

將記錄檔加入至集合。

## <a name="syntax"></a>語法


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑名稱* \[在\]
</dt> <dd>

記錄檔的路徑。 您可以將路徑指定為絕對路徑、相對路徑或 UNC 路徑。 記錄檔副檔名必須是 .csv、tsv 或 .blg。

</dd> </dl>

## <a name="remarks"></a>備註

您必須使用 Logman.exe 工具或 Perfmon MMC 嵌入式管理單元來產生您新增至此集合的記錄檔。 針對 Perfmon，計數器記錄檔位於 **效能記錄檔及警示** 下。 如需有關使用 Logman.exe 或 Perfmon 的詳細資訊，請在 **說明及支援中心** 中分別搜尋 Logman 或使用效能。

**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)的值設定為 [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)，您就無法將記錄檔加入 [**記錄檔集合**](systemmonitor-logfiles.md)。 首先，將 **SystemMonitor** 設定為 **DataSourceTypeConstants.sysmonNullDataSource**、新增您的記錄檔和計數器，然後將 **SystemMonitor DataSourceType** 設定為 **DataSourceTypeConstants.sysmonLogFiles**。

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

 

 





