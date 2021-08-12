---
description: 定義原生 Wifi 自動設定服務所使用的 WLAN 設定檔。
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: WLAN_profile 架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91bd1a5d04bcc265f2b9ba7c0533bb0beb4e2c861f01c8b5e286d59f8b4bcfc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619065"
---
# <a name="wlan_profile-schema"></a>WLAN \_ 設定檔架構

WLAN \_ 設定檔架構會定義原生 Wifi 自動設定服務所使用的 wlan 設定檔。

自動設定服務會接受來自群組原則代理程式的無線設定檔、指令碼介面 (**netsh**) 、使用者介面，或從 USB flash 設定介面。

從這些系統之一收到的設定檔會對應至 WLAN \_ 設定檔架構，並儲存在設定檔存放區中。 您可以使用 netsh 命令或使用 API 元素（例如 [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)），從設定檔存放區匯出設定檔。

WLAN 設定檔的根項目是 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) 元素。 每個設定檔都只會有一個根項目。 **WLANProfile** 元素位於命名空間中 `https://www.microsoft.com/networking/WLAN/profile/v1` 。

若要查看範例 WLAN 設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。

-   [WLAN \_ 設定檔架構元素](wlan-profileschema-elements.md)
-   [WLAN \_ 設定檔架構簡單類型](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[無線區域網路 (wlan) 的 Netsh 命令 ](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
