---
description: WLAN \_ 設定檔架構會定義下列元素。
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: WLAN_profile 架構元素
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690831"
---
# <a name="wlan_profile-schema-elements"></a>WLAN \_ 設定檔架構元素

WLAN \_ 設定檔架構會定義下列元素。 `https://www.microsoft.com/networking/WLAN/profile/v1`除了命名空間中的 [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md)之外，大部分的元素都位於命名空間中 `https://www.microsoft.com/networking/WLAN/profile/v2` 。

下列清單以專案在設定檔中出現的順序顯示已定義的元素。 強制執行元素的順序。 並非所有專案都在每個設定檔中，因為有些元素是選擇性的。

這份清單不會顯示所有可能出現在無線設定檔中的元素，因為可以在 **xs：任何** 插入點中新增元素。

-   [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
    -   [**WLANProfile) 名稱 (**](wlan-profileschema-name-wlanprofile-element.md)
    -   [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [**(SSID 的十六進位)**](wlan-profileschema-hex-ssid-element.md)
            -   [**(SSID 的名稱)**](wlan-profileschema-name-ssid-element.md)
        -   [**非廣播 (SSIDConfig)**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [**Hotspot2 (WLANProfile)**](wlan-profileschema-hotspot2-element.md)
        -   [**DomainName (Hotspot2)**](wlan-profileschema-hotspot2-domainname-element.md)
        -   [**NAIRealm (Hotspot2)**](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [**Network3GPP (Hotspot2)**](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [**RoamingConsortium (Hotspot2)**](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [**connectionType (WLANProfile)**](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [**connectionMode (WLANProfile)**](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [**autoSwitch (WLANProfile)**](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
        -   [**(MSM) 的連線能力**](wlan-profileschema-connectivity-msm-element.md)
            -   [**phyType (連接)**](wlan-profileschema-phytype-connectivity-element.md)
        -   [**(MSM) 的安全性**](wlan-profileschema-security-msm-element.md)
            -   [**authEncryption (安全性)**](wlan-profileschema-authencryption-security-element.md)
                -   [**驗證 (authEncryption)**](wlan-profileschema-authentication-authencryption-element.md)
                -   [**加密 (authEncryption)**](wlan-profileschema-encryption-authencryption-element.md)
                -   [**useOneX (authEncryption)**](wlan-profileschema-useonex-authencryption-element.md)
                -   [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [**sharedKey (安全性)**](wlan-profileschema-sharedkey-security-element.md)
                -   [**keyType (sharedKey)**](wlan-profileschema-keytype-sharedkey-element.md)
                -   [**protected (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)
                -   [**keyMaterial (sharedKey)**](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [**索引鍵索引 (安全性)**](wlan-profileschema-keyindex-security-element.md)
            -   [**PMKCacheMode (安全性)**](wlan-profileschema-pmkcachemode-security-element.md)
            -   [**PMKCacheTTL (安全性)**](wlan-profileschema-pmkcachettl-security-element.md)
            -   [**PMKCacheSize (安全性)**](wlan-profileschema-pmkcachesize-security-element.md)
            -   [**preAuthMode (安全性)**](wlan-profileschema-preauthmode-security-element.md)
            -   [**preAuthThrottle (安全性)**](wlan-profileschema-preauththrottle-security-element.md)
    -   [**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
            -   [**OUI (OUIHeader)**](wlan-profileschema-oui-ouiheader-element.md)
            -   [**輸入 (OUIHeader)**](wlan-profileschema-type-ouiheader-element.md)
        -   [**(IHV) 的連線能力**](wlan-profileschema-connectivity-ihv-element.md)
        -   [**(IHV) 安全性**](wlan-profileschema-security-ihv-element.md)
        -   [**useMSOneX (IHV)**](wlan-profileschema-usemsonex-ihv-element.md)

 

 



