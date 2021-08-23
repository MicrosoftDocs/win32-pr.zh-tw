---
description: 由於作業系統的基礎架構差異，Windows xp service pack 3 (SP3) 以及 Windows XP service pack 2 (SP2 的無線區域網路 API) 僅支援 WLAN \_ 設定檔架構和 OneX 架構參考資料中所述的元素子集。
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: 無線設定檔相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36db0ecea6f85341d904603c99308ec10e79cee20d7567160cd3beee3b13c35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684568"
---
# <a name="wireless-profile-compatibility"></a>無線設定檔相容性

由於作業系統的基礎架構差異，Windows xp service pack 3 (SP3) 以及 Windows XP service pack 2 (SP2 的無線區域網路 API) 僅支援[WLAN \_ 設定檔架構](wlan-profileschema-schema.md)和[OneX 架構](onexschema-schema.md)參考資料中所述的元素子集。

所有符合 Windows XP 含 SP3 以及適用于 Windows XP SP2 需求的無線區域網路 API 的設定檔，也可以在 Windows Vista 和 Windows Server 2008 上使用。

## <a name="wlan_profile-support"></a>WLAN \_ 設定檔支援

\_Windows XP SP3 或適用于 Windows XP SP2 的無線區域網路 API 不支援下列 WLAN 設定檔元素：

-    (IHV) 的連線能力
-   IHV (WLANProfile) 
-   OUI (OUIHeader) 
-   phyType (連接) 
-   PMKCacheMode (安全性) 
-   PMKCacheSize (安全性) 
-   PMKCacheTTL (安全性) 
-   preAuthMode (安全性) 
-   preAuthThrottle (安全性) 
-    (IHV) 安全性
-   輸入 (OUIHeader) 
-   useMSOneX (IHV) 

下錶針對 \_ Windows xp 含 SP2 的 Windows XP 和適用于 xp 的無線區域網路 API，顯示具有限制值的 WLAN 設定檔元素：



| 元素                                                                               | 條件約束                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WLANProfile) 名稱 (**](wlan-profileschema-name-wlanprofile-element.md)             | 當設定檔儲存在設定檔存放區中時，會忽略 name 元素。 設定檔的名稱會自動衍生自網路的 SSID。 在基礎結構網路設定檔中，設定檔的名稱是網路的 SSID。 針對臨機操作網路設定檔，設定檔的名稱是臨機操作網路的 SSID，後面接著 `-adhoc` 。 |
| [**protected (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | 的值必須為 FALSE。                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | 限制為一個子 [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) 元素。                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>OneX 支援

Windows xp （含 SP3）和適用于 Windows XP SP2 的無線區域網路 API 都只支援 [**EAPConfig**](onexschema-eapconfig-onex-element.md)元素。 如果設定檔中有其他的 OneX 元素，將會予以忽略。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於原生 Wifi API](about-the-native-wifi-api.md)
</dt> <dt>

[Windows XP 上的原生 Wifi API 支援](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



