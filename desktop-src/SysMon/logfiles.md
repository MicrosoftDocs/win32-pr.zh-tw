---
title: LogFiles 物件 (Isysmon.h)
description: 您可以使用這個類別來管理一個或多個包含效能計數器資料之記錄檔的集合。若要取出這個物件，請呼叫 SystemMonitor。
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- 記錄檔物件 SysMon
- 記錄檔物件 SysMon，描述
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a0890acdf656c807ae3bcb275012bd56a4711a114547f750f04fd8d875fc68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883146"
---
# <a name="logfiles-object"></a>記錄檔物件

您可以使用這個類別來管理一個或多個包含效能計數器資料之記錄檔的集合。

若要取出這個物件，請呼叫 [**SystemMonitor。**](systemmonitor-logfiles.md)

## <a name="members"></a>成員

記錄 **檔物件具有** 下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

記錄 **檔物件有** 這些方法。



| 方法                                          | 描述                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**添加**](systemmonitor-logfiles-add.md)       | 將 [**LogFileItem**](logfileitem.md) 實例加入至集合。<br/>      |
| [**移除**](systemmonitor-logfiles-remove.md) | 從集合中移除 [**LogFileItem**](logfileitem.md) 實例。<br/> |



 

### <a name="properties"></a>屬性

記錄 **檔物件具有** 這些屬性。



| 屬性                                                 | 描述                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**計數**](systemmonitor-logfiles-count.md)<br/> | 抓取集合中 [**LogFileItem**](logfileitem.md) 實例的數目。<br/>  |
| [**項目**](systemmonitor-logfiles-item.md)<br/>   | 從集合中抓取指定的 [**LogFileItem**](logfileitem.md) 實例。<br/> |



 

## <a name="remarks"></a>備註

若要讓 SYSMON 顯示記錄檔中的效能計數器，請將 [**SystemMonitor DataSourceType**](systemmonitor-datasourcetype.md) 為 [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)。 將記錄檔加入至集合之後，請使用 [**計數器**](counters.md) 集合來指定您要從記錄檔讀取的計數器資料。 請注意，如果 **SystemMonitor DataSourceType** 設定為 **DataSourceTypeConstants.sysmonLogFiles**，則每次您將記錄檔或計數器新增至各自的集合時，SYSMON 將會重新取樣記錄檔。

**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)的值設定為 [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)，您就無法將記錄檔加入 [**記錄檔集合**](systemmonitor-logfiles.md)。 首先，將 **SystemMonitor** 設定為 **DataSourceTypeConstants.sysmonNullDataSource**、新增您的記錄檔和計數器，然後將 **SystemMonitor DataSourceType** 設定為 **DataSourceTypeConstants.sysmonLogFiles**。

[**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md)和 [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md)屬性會指定從記錄檔到圖形的取樣值範圍。 SYSMON 圖形的記錄檔中只會有一個資料檢視 (圖表視圖不會像繪製電腦目前的活動) 一樣地滾動。 如果取樣的資料超過可在單一圖表上顯示的資料，SYSMON 會將取樣的資料壓縮 (每個圖形化點都代表多個取樣值的平均值，) 以符合圖形上記錄檔中的所有取樣資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Isysmon。h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





