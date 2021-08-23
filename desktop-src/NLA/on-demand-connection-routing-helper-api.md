---
title: 隨選連接路由協助程式 API 參考
description: 下列主題提供隨選連接路由協助程式的詳細資料。
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e046c1add8703e6603d925d2c80b03aab8d7eae3a352825e56ec907f3adb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685578"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a>隨選連接路由協助程式 API 參考

下列主題提供隨選連接路由協助程式的詳細資料。



| 參考                                                                          | 描述                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnDemandGetRoutingHint**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | 查閱路由要求快取中的目的地，如果找到相符的，則會傳回對應的介面識別碼。<br/>                                               |
| [**OnDemandRegisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | 註冊，以在修改路由要求快取時收到通知。<br/>                                                                                               |
| [**OnDemandUnregisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | 取消註冊通知並清除資源。<br/>                                                                                                             |
| [**網路 \_ 介面 \_ 內容**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | 屬於 [**NET \_ interface \_ coNtext \_ TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) 結構一部分的介面內容。<br/>                                       |
| [**NET \_ 介面 \_ 內容 \_ 表**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | [**NET \_ 介面 \_ 內容**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)結構的資料表。<br/>                                                                                |
| [**GetInterfaceCoNtextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | 此函式會針對指定的主機名稱和連接設定檔篩選器，抓取介面內容表。<br/>                                                         |
| [**FreeInterfaceCoNtextTable**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | 此函式會釋出使用 [**GetInterfaceCoNtextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) 函數抓取的介面內容資料表。<br/> |



 

 

 





