---
description: 由瀏覽器所執行。 公開管理哪些監視在多個監視器系統上包含 Windows 工作列的方法。
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
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991822"
---
# <a name="imultimonitordockingsite-interface"></a>IMultiMonitorDockingSite 介面

由瀏覽器所執行。 公開管理哪些監視在多個監視器系統上包含 Windows 工作列的方法。

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
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                   |



 

 
