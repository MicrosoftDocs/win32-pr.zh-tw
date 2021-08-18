---
description: 由瀏覽器所執行。 公開方法，以管理哪些監視包含多個監視器系統上 Windows 的工作列。
title: IMultiMonitorDockingSite 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: a5a17e8206af8f0821833f4b2ea250606de29b6fbe74b7a29ced6c5b5dc13ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458218"
---
# <a name="imultimonitordockingsite-interface"></a>IMultiMonitorDockingSite 介面

由瀏覽器所執行。 公開方法，以管理哪些監視包含多個監視器系統上 Windows 的工作列。

## <a name="members"></a>成員

**IMultiMonitorDockingSite** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IMultiMonitorDockingSite** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMultiMonitorDockingSite** 介面具有這些方法。



| 方法                                                            | 描述                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetMonitor**](imultimonitordockingsite-getmonitor.md)         | 取得目前的預設監視器。<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | 確認監視器正在使用中且可供使用。<br/>                              |
| [**SetMonitor**](imultimonitordockingsite-setmonitor.md)         | 變更用於多個監視器系統上停駐工具列的監視器。<br/> |



 

## <a name="remarks"></a>備註

您通常不會執行 **IMultiMonitorDockingSite** 介面。 Shell 瀏覽器會執行這個介面，以支援多個監視器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                   |



 

 
