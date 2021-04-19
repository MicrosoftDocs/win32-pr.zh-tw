---
description: 用來連線到不會廣播其網路名稱或 SSID 的網路。
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: 非廣播設定檔範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989391"
---
# <a name="non-broadcast-profile-sample"></a><span data-ttu-id="2f63b-103">非廣播設定檔範例</span><span class="sxs-lookup"><span data-stu-id="2f63b-103">Non-Broadcast Profile Sample</span></span>

<span data-ttu-id="2f63b-104">非廣播設定檔範例可以用來連線到未廣播其網路名稱或 SSID 的網路。</span><span class="sxs-lookup"><span data-stu-id="2f63b-104">The non-broadcast profile sample can be used to connect to networks which do not broadcast their network name or SSID.</span></span>

<span data-ttu-id="2f63b-105">此範例設定檔設定為使用在個人模式中執行的 Wi-Fi 保護的存取安全性 (WPA-Personal) 。</span><span class="sxs-lookup"><span data-stu-id="2f63b-105">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="2f63b-106">時態性金鑰完整性通訊協定 (TKIP) 用於加密。</span><span class="sxs-lookup"><span data-stu-id="2f63b-106">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span> <span data-ttu-id="2f63b-107">使用其他安全性和加密類型的設定檔也可以設定為非廣播設定檔。</span><span class="sxs-lookup"><span data-stu-id="2f63b-107">Profiles that use other security and cipher types can also be configured as non-broadcast profiles.</span></span>

<span data-ttu-id="2f63b-108">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：**[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素的 [**name**](wlan-profileschema-name-wlanprofile-element.md)子系會被忽略。</span><span class="sxs-lookup"><span data-stu-id="2f63b-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="2f63b-109">設定檔的名稱（儲存在設定檔存放區中）是衍生自 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)元素的 [**名稱**](wlan-profileschema-name-ssid-element.md)子系。</span><span class="sxs-lookup"><span data-stu-id="2f63b-109">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleNonBroadcast</name>
    <SSIDConfig>
        <SSID>
            <name>SampleNonBroadcast</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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

<span data-ttu-id="2f63b-110">此範例設定檔已省略共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f63b-110">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="2f63b-111">如果您嘗試使用此範例設定檔連接到網路，系統會提示您輸入共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f63b-111">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="2f63b-112">您可以將 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)子項目新增至緊接在 [**authEncryption**](wlan-profileschema-authencryption-security-element.md)元素後面的 [**安全性**](wlan-profileschema-security-msm-element.md)元素，以避免這個提示。</span><span class="sxs-lookup"><span data-stu-id="2f63b-112">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="2f63b-113">下列程式碼片段顯示 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素，其中包含未加密的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f63b-113">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="2f63b-114">在 `<!-- insert key here -->` 設定檔中使用此程式碼片段之前，您必須將批註取代為實際未加密的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f63b-114">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="2f63b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f63b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f63b-116">無線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="2f63b-116">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



