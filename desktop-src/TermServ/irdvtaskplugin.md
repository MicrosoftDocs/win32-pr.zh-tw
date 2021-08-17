---
title: IRDVTaskPlugin 介面
description: IRDVTaskPlugin 介面是由虛擬機器更新工作代理程式所執行，可讓工作代理程式管理虛擬機器的系統更新。
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- IRDVTaskPlugin 介面遠端桌面服務
- IRDVTaskPlugin 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe76f0b0b92286d5a4b7db5126706fd55bdb6f580c11fda1dcaa55a47be4678c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129167"
---
# <a name="irdvtaskplugin-interface"></a>IRDVTaskPlugin 介面

**IRDVTaskPlugin** 介面是由虛擬機器更新工作 *代理程式* 所執行，可讓工作代理程式管理虛擬機器的系統更新。 此介面是由主機系統所執行的 *觸發程式代理程式* 所使用。

## <a name="members"></a>成員

**IRDVTaskPlugin** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IRDVTaskPlugin** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IRDVTaskPlugin** 介面具有這些方法。



| 方法                                          | 描述                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**初始化**](irdvtaskplugin-initialize.md) | 呼叫以初始化工作代理程式。<br/>                    |
| [**StartTask**](irdvtaskplugin-starttask.md)   | 呼叫以啟動虛擬機器上的更新工作。<br/> |
| [**終止**](irdvtaskplugin-terminate.md)   | 在工作代理程式關閉時呼叫。<br/>          |



 

### <a name="properties"></a>屬性

**IRDVTaskPlugin** 介面具有這些屬性。



| 屬性                                                   | 存取類型          | 描述                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | 唯讀<br/> | 包含工作代理程式的顯示名稱。<br/> |



 

## <a name="remarks"></a>備註

當虛擬機器已排程進行系統更新時，就會在虛擬機器上執行工作代理程式。 當呼叫 [**StartTask**](irdvtaskplugin-starttask.md) 方法時，工作代理程式會更新虛擬機器。

若要註冊工作代理程式，請將下列機碼新增至虛擬機器的登錄：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\ **Task** \\ **外掛程式** \\ **TaskAgentName**

在此登錄機碼底下，新增下列值：



| 名稱                     | 類型                      | 描述                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **CLSID**<br/>     | **REG \_ SZ**<br/>    | 表示工作代理程式 **CLSID** 的字串。<br/>          |
| **IsEnabled**<br/> | **REG \_ DWORD**<br/> | 如果工作代理程式已停用，則為 0; 如果工作代理程式已啟用，則為1。<br/> |



 

> [!Note]  
> 您可以註冊一個以上的工作代理程式，但只會使用一個工作代理程式。 如果啟用多個工作代理程式，則只會使用找到的第一個工作代理程式。

 

雖然下列需求中所識別的作業系統支援這個介面，但只有在虛擬機器裝載于 Windows Server 2012 時，才會使用此介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------|
| 最低支援的用戶端<br/> | Windows 7 Enterprise<br/>   |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/> |



 

