---
title: 使用 Teredo 搭配 IP Helper
description: 網際網路通訊協定協助程式 (IP 協助程式) API 是由應用程式使用，以收集和提供有關本機電腦網路設定的重要資訊。
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e977dd585f9759a4eef93daca55e0ff95abdc98085393577afabb4ae6e5908ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990798"
---
# <a name="using-teredo-with-ip-helper"></a>使用 Teredo 搭配 IP Helper

應用程式會使用 [網際網路通訊協定](/windows/desktop/IpHlp/about-ip-helper) 協助程式 (IP 協助程式) API 來收集和提供有關本機電腦網路設定的重要資訊。 在 Windows Vista 平臺上操作時，此資訊會包含指派給 Teredo 介面的動態 UDP 通訊埠，以及可能會發生在指定埠上的變更。

IP 協助程式 API 會利用下列函式來加速使用 Teredo 介面：

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 