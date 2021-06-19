---
description: 使用預先共用金鑰進行網路驗證。 此範例設定檔會使用以個人模式執行的 Wi-Fi Protected Access security (WPA-Personal) 。
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: WPA-Personal 設定檔範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334076d4b0cf10372ed845265a1fff652f0879b9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395023"
---
# <a name="wpa-personal-profile-sample"></a>WPA-Personal 設定檔範例

此範例設定檔會使用預先共用金鑰進行網路驗證。 金鑰會與用戶端和存取點共用。 此範例設定檔設定為使用在個人模式中執行的 Wi-Fi 保護的存取安全性 (WPA-Personal) 。 時態性金鑰完整性通訊協定 (TKIP) 用於加密。

**安裝了無線局域網路服務的 windows 7 和 Windows Server 2008 R2：** 變更會在已安裝無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行，以將無線網路效能優化。 當無線局域網路設定檔中未設定此元素時， [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 的預設設定已變更。 在安裝了無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上，預設設定會變更為 "false"。 Windows Server 2008 和 Windows Vista 上的預設設定為 "true"。 如需詳細資訊，請參閱 [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 架構元素的描述。

Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：**[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素的 [**name**](wlan-profileschema-name-wlanprofile-element.md)子系會被忽略。 設定檔的名稱（儲存在設定檔存放區中）是衍生自 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)元素的 [**名稱**](wlan-profileschema-name-ssid-element.md)子系。

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAPSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAPSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

此範例設定檔已省略共用金鑰。 如果您嘗試使用此範例設定檔連接到網路，系統會提示您輸入共用金鑰。 您可以將 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)子項目新增至緊接在 [**authEncryption**](wlan-profileschema-authencryption-security-element.md)元素後面的 [**安全性**](wlan-profileschema-security-msm-element.md)元素，以避免這個提示。

下列程式碼片段顯示 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素，其中包含未加密的金鑰。 在 `<!-- insert key here -->` 設定檔中使用此程式碼片段之前，您必須將批註取代為實際未加密的金鑰。

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[無線設定檔範例](wireless-profile-samples.md)
</dt> </dl>

 

 



