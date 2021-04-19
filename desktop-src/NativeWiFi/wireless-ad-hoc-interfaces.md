---
description: 無線臨機操作程式設計介面是由下列介面所組成。
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: 無線特定介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982316"
---
# <a name="wireless-ad-hoc-interfaces"></a>無線特定介面

無線臨機操作程式設計介面是由下列介面所組成。



| 介面名稱                                                                       | 描述                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | 代表 (NIC) 的無線網路介面卡。                                                    |
| [**IDot11AdHocInterfaceNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | 定義 [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)支援的通知。           |
| [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | 建立及管理802.11 臨機操作網路。                                                            |
| [**IDot11AdHocManagerNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | 定義 [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) 介面所支援的通知。 |
| [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | 代表連接範圍內的可用特定網路目的地。                            |
| [**IDot11AdHocNetworkNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | 定義 [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) 介面所支援的通知。 |
| [**IDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | 指定無線特定網路的安全性設定。                                         |
| [**IEnumDot11AdHocInterfaces**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | 表示目前可見的802.11 特定網路介面集合。                       |
| [**IEnumDot11AdHocNetworks**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | 表示目前可見的802.11 特定網路集合。                                 |
| [**IEnumDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | 表示與每個可見無線臨機操作網路相關聯的安全性設定集合。   |



 

> [!Note]  
> 未來的 Windows 版本可能無法使用臨機操作模式。 從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 [Wi-Fi Direct](about-the-wi-fi-direct-api.md) 。

 

 

 



