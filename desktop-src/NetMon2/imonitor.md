---
description: IMonitor 介面提供控制監視作業的方法。 監視器控制服務會呼叫這些方法 (MCSVC) 。
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: 'IMonitor 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848367"
---
# <a name="imonitor-interface"></a>IMonitor 介面

**IMonitor** 介面提供控制監視作業的方法。 [*監視器控制服務*](m.md)會呼叫這些方法 (MCSVC) 。

## <a name="members"></a>成員

**IMonitor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMonitor** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMonitor** 介面具有這些方法。



| 方法                                        | 描述                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**DoConfigure**](imonitor-doconfigure.md)   | 更新監視設定。<br/>                                                                           |
| [**DoInitialize**](imonitor-doinitialize.md) | 初始化監視器。<br/>                                                                                   |
| [**OnFrames**](imonitor-onframes.md)         | 指出框架事件的狀態。<br/>                                                                   |
| [**OnStart**](imonitor-onstart.md)           | 表示已成功設定監視，且資料捕捉即將開始。<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | 表示 NPP 狀態事件。<br/>                                                                           |
| [**S**](imonitor-onstop.md)             | 表示資料捕獲完成。<br/>                                                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

