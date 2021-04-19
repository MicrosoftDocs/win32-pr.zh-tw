---
description: 使用下列函式，以確保應用程式會收到特定網路事件的通知。
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: 接收網路事件的通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970403"
---
# <a name="receiving-notification-of-network-events"></a>接收網路事件的通知

使用下列函式，以確保應用程式會收到特定網路事件的通知。

使用 [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) 函式來要求在本機電腦上的 IP 位址和介面之間的對應中發生之任何變更的通知。

同樣地， [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) 函式可讓應用程式要求 IP 路由表中發生之任何變更的通知。

這些函數所提供的通知不會指定變更的內容;他們只會指定變更的內容。 使用其他 IP Helper 函式（例如 [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 和 [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute)）來判斷變更的確切本質。

 

 



