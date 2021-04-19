---
title: '計數器集合 (Isysmon .h) '
description: 您可以使用這個類別來管理 CounterItem 物件的集合。 若要取出這個物件，請呼叫 SystemMonitor。
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- 計數器集合 SysMon
- 計數器集合 SysMon，描述
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966944"
---
# <a name="counters-collection"></a>計數器集合

您可以使用這個類別來管理 [**CounterItem**](counteritem.md) 物件的集合。

若要取出這個物件，請呼叫 [**SystemMonitor。**](systemmonitor-counters.md)

## <a name="members"></a>成員

**計數器** 集合有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**計數器** 集合具有這些方法。



| 方法                            | 描述                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [**添加**](counters-add.md)       | 將 [**CounterItem**](counteritem.md) 實例加入至集合。<br/>      |
| [**移除**](counters-remove.md) | 從集合中移除 [**CounterItem**](counteritem.md) 實例。<br/> |



 

### <a name="properties"></a>屬性

**計數器** 集合具有這些屬性。



| 屬性                                   | 描述                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**計數**](counters-count.md)<br/> | 抓取集合中 [**CounterItem**](counteritem.md) 實例的數目。<br/>  |
| [**項目**](counters-item.md)<br/>   | 從集合中抓取指定的 [**CounterItem**](counteritem.md) 實例。<br/> |



 

## <a name="remarks"></a>備註

**計數器** 物件是 [**SystemMonitor**](systemmonitor.md)物件的預設屬性。

將您想要繪製的計數器加入至此集合。 SYSMON 會根據您指定的 [**資料來源**](systemmonitor-datasourcetype.md) ，從系統或記錄檔抓取計數器值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Isysmon。h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





