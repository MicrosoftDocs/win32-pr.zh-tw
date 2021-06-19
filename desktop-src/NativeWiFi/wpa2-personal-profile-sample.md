---
description: 使用預先共用金鑰進行網路驗證。 此範例設定檔會使用以個人模式執行的 Wi-Fi Protected Access 2 安全性 (WPA2-Personal) 。
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: WPA2-Personal 設定檔範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e0df238b83a27155e640d56fc81ed5606a76e3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394863"
---
# <a name="wpa2-personal-profile-sample"></a><span data-ttu-id="2919a-104">WPA2-Personal 設定檔範例</span><span class="sxs-lookup"><span data-stu-id="2919a-104">WPA2-Personal Profile Sample</span></span>

<span data-ttu-id="2919a-105">此範例設定檔會使用預先共用金鑰進行網路驗證。</span><span class="sxs-lookup"><span data-stu-id="2919a-105">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="2919a-106">金鑰會與用戶端和存取點共用。</span><span class="sxs-lookup"><span data-stu-id="2919a-106">The key is shared with the client and the access point.</span></span> <span data-ttu-id="2919a-107">此範例設定檔設定為使用在個人模式中執行的 Wi-Fi Protected Access 2 安全性 (WPA2-Personal) 。</span><span class="sxs-lookup"><span data-stu-id="2919a-107">This sample profile is configured to use Wi-Fi Protected Access 2 security running in Personal mode (WPA2-Personal).</span></span> <span data-ttu-id="2919a-108">進階加密標準 (AES) 加密類型。</span><span class="sxs-lookup"><span data-stu-id="2919a-108">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="2919a-109">**安裝了無線局域網路服務的 windows 7 和 Windows Server 2008 R2：** 變更會在已安裝無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行，以將無線網路效能優化。</span><span class="sxs-lookup"><span data-stu-id="2919a-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="2919a-110">當無線局域網路設定檔中未設定此元素時， [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 的預設設定已變更。</span><span class="sxs-lookup"><span data-stu-id="2919a-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="2919a-111">在安裝了無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上，預設設定會變更為 "false"。</span><span class="sxs-lookup"><span data-stu-id="2919a-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="2919a-112">Windows Server 2008 和 Windows Vista 上的預設設定為 "true"。</span><span class="sxs-lookup"><span data-stu-id="2919a-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="2919a-113">如需詳細資訊，請參閱 [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) 架構元素的描述。</span><span class="sxs-lookup"><span data-stu-id="2919a-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="2919a-114">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：**[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素的 [**name**](wlan-profileschema-name-wlanprofile-element.md)子系會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2919a-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="2919a-115">設定檔的名稱（儲存在設定檔存放區中）是衍生自 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)元素的 [**名稱**](wlan-profileschema-name-ssid-element.md)子系。</span><span class="sxs-lookup"><span data-stu-id="2919a-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2PSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2PSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2PSK</authentication>
                <encryption>AES</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

<span data-ttu-id="2919a-116">此範例設定檔已省略共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="2919a-116">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="2919a-117">如果您嘗試使用此範例設定檔連接到網路，系統會提示您輸入共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="2919a-117">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="2919a-118">您可以將 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)子項目新增至緊接在 [**authEncryption**](wlan-profileschema-authencryption-security-element.md)元素後面的 [**安全性**](wlan-profileschema-security-msm-element.md)元素，以避免這個提示。</span><span class="sxs-lookup"><span data-stu-id="2919a-118">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="2919a-119">下列程式碼片段顯示 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素，其中包含未加密的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2919a-119">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="2919a-120">在 `<!-- insert key here -->` 設定檔中使用此程式碼片段之前，您必須將批註取代為實際未加密的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2919a-120">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="2919a-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="2919a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2919a-122">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="2919a-122">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



