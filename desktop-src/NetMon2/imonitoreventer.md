---
description: IMonitorEventer 介面提供提交事件以及配置和釋放監視資源的方法。
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: 'IMonitorEventer 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847937"
---
# <a name="imonitoreventer-interface"></a>IMonitorEventer 介面

**IMonitorEventer** 介面提供提交事件以及配置和釋放監視資源的方法。

## <a name="members"></a>成員

**IMonitorEventer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMonitorEventer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMonitorEventer** 介面具有這些方法。



| 方法                                                 | 描述                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**FreeEventData**](imonitoreventer-freeeventdata.md) | 釋出配置給監視資料的空間。<br/> |
| [**GetEventData**](imonitoreventer-geteventdata.md)   | 配置監視器資料的空間。<br/>       |
| [**SendNMEvent**](imonitoreventer-sendnmevent.md)     | 將事件提交至 WMI。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

