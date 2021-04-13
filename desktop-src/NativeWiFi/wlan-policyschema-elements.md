---
description: 原生 Wifi 無線區域網路 (WLAN) 原則設定檔是由下列架構元素所組成。
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy 架構元素
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511183"
---
# <a name="wlan_policy-schema-elements"></a>WLAN \_ 原則架構元素

原生 Wifi 無線區域網路 (WLAN) 原則設定檔是由下列架構元素所組成。 所有命名的元素都位於命名空間中 `https://www.microsoft.com/networking/WLAN/policy/v1` 。

下列清單以專案在設定檔中出現的順序顯示已定義的元素。 強制執行元素的順序。 並非所有專案都在每個設定檔中，因為有些元素是選擇性的。

這份清單不會顯示所有可能出現在設定檔中的元素，因為可以在 **xs：任何** 插入點中加入元素。

-   [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
    -   [**WLANPolicy) 名稱 (**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**描述 (WLANPolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableAutoConfig (globalFlags)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showDeniedNetwork (globalFlags)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**allowEveryoneToCreateAllUserProfiles (globalFlags)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**允許清單 (networkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**network (允許清單)**](wlan-policyschema-network-allowlist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**封鎖清單 (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**network (封鎖清單)**](wlan-policyschema-network-blocklist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyAllIBSS (networkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyAllESS (networkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**profileList (WLANPolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



