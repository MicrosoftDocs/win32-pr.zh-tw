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
# <a name="wlan_profile-schema-elements"></a><span data-ttu-id="8ad48-103">WLAN \_ 設定檔架構元素</span><span class="sxs-lookup"><span data-stu-id="8ad48-103">WLAN\_profile Schema Elements</span></span>

<span data-ttu-id="8ad48-104">WLAN \_ 設定檔架構會定義下列元素。</span><span class="sxs-lookup"><span data-stu-id="8ad48-104">The WLAN\_profile schema defines the following elements.</span></span> <span data-ttu-id="8ad48-105">`https://www.microsoft.com/networking/WLAN/profile/v1`除了命名空間中的 [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md)之外，大部分的元素都位於命名空間中 `https://www.microsoft.com/networking/WLAN/profile/v2` 。</span><span class="sxs-lookup"><span data-stu-id="8ad48-105">Most elements are in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`, except for [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), which is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v2`.</span></span>

<span data-ttu-id="8ad48-106">下列清單以專案在設定檔中出現的順序顯示已定義的元素。</span><span class="sxs-lookup"><span data-stu-id="8ad48-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="8ad48-107">強制執行元素的順序。</span><span class="sxs-lookup"><span data-stu-id="8ad48-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="8ad48-108">並非所有專案都在每個設定檔中，因為有些元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8ad48-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="8ad48-109">這份清單不會顯示所有可能出現在無線設定檔中的元素，因為可以在 **xs：任何** 插入點中新增元素。</span><span class="sxs-lookup"><span data-stu-id="8ad48-109">This list does not show all possible elements that can appear in a wireless profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="8ad48-110">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="8ad48-110">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
    -   [<span data-ttu-id="8ad48-111">**WLANProfile) 名稱 (**</span><span class="sxs-lookup"><span data-stu-id="8ad48-111">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)
    -   [<span data-ttu-id="8ad48-112">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-112">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [<span data-ttu-id="8ad48-113">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-113">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [<span data-ttu-id="8ad48-114">**(SSID 的十六進位)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-114">**hex (SSID)**</span></span>](wlan-profileschema-hex-ssid-element.md)
            -   [<span data-ttu-id="8ad48-115">**(SSID 的名稱)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-115">**name (SSID)**</span></span>](wlan-profileschema-name-ssid-element.md)
        -   [<span data-ttu-id="8ad48-116">**非廣播 (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-116">**nonBroadcast (SSIDConfig)**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [<span data-ttu-id="8ad48-117">**Hotspot2 (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-117">**Hotspot2 (WLANProfile)**</span></span>](wlan-profileschema-hotspot2-element.md)
        -   [<span data-ttu-id="8ad48-118">**DomainName (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-118">**DomainName (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-domainname-element.md)
        -   [<span data-ttu-id="8ad48-119">**NAIRealm (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-119">**NAIRealm (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [<span data-ttu-id="8ad48-120">**Network3GPP (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-120">**Network3GPP (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [<span data-ttu-id="8ad48-121">**RoamingConsortium (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-121">**RoamingConsortium (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [<span data-ttu-id="8ad48-122">**connectionType (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-122">**connectionType (WLANProfile)**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [<span data-ttu-id="8ad48-123">**connectionMode (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-123">**connectionMode (WLANProfile)**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [<span data-ttu-id="8ad48-124">**autoSwitch (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-124">**autoSwitch (WLANProfile)**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [<span data-ttu-id="8ad48-125">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
        -   [<span data-ttu-id="8ad48-126">**(MSM) 的連線能力**</span><span class="sxs-lookup"><span data-stu-id="8ad48-126">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
            -   [<span data-ttu-id="8ad48-127">**phyType (連接)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-127">**phyType (connectivity)**</span></span>](wlan-profileschema-phytype-connectivity-element.md)
        -   [<span data-ttu-id="8ad48-128">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="8ad48-128">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
            -   [<span data-ttu-id="8ad48-129">**authEncryption (安全性)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-129">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
                -   [<span data-ttu-id="8ad48-130">**驗證 (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-130">**authentication (authEncryption)**</span></span>](wlan-profileschema-authentication-authencryption-element.md)
                -   [<span data-ttu-id="8ad48-131">**加密 (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-131">**encryption (authEncryption)**</span></span>](wlan-profileschema-encryption-authencryption-element.md)
                -   [<span data-ttu-id="8ad48-132">**useOneX (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-132">**useOneX (authEncryption)**</span></span>](wlan-profileschema-useonex-authencryption-element.md)
                -   [<span data-ttu-id="8ad48-133">**FIPSMode (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-133">**FIPSMode (authEncryption)**</span></span>](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [<span data-ttu-id="8ad48-134">**sharedKey (安全性)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-134">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
                -   [<span data-ttu-id="8ad48-135">**keyType (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-135">**keyType (sharedKey)**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)
                -   [<span data-ttu-id="8ad48-136">**protected (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-136">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)
                -   [<span data-ttu-id="8ad48-137">**keyMaterial (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-137">**keyMaterial (sharedKey)**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [<span data-ttu-id="8ad48-138">**索引鍵索引 (安全性)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-138">**keyIndex (security)**</span></span>](wlan-profileschema-keyindex-security-element.md)
            -   [<span data-ttu-id="8ad48-139">**PMKCacheMode (安全性)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-139">**PMKCacheMode (security)**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)
            -   [<span data-ttu-id="8ad48-140">**PMKCacheTTL (安全性)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-140">**PMKCacheTTL (security)**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)
            -   [<span data-ttu-id="8ad48-141">**PMKCacheSize (安全性)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-141">**PMKCacheSize (security)**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)
            -   [<span data-ttu-id="8ad48-142">**preAuthMode (安全性)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-142">**preAuthMode (security)**</span></span>](wlan-profileschema-preauthmode-security-element.md)
            -   [<span data-ttu-id="8ad48-143">**preAuthThrottle (安全性)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-143">**preAuthThrottle (security)**</span></span>](wlan-profileschema-preauththrottle-security-element.md)
    -   [<span data-ttu-id="8ad48-144">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-144">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [<span data-ttu-id="8ad48-145">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-145">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
            -   [<span data-ttu-id="8ad48-146">**OUI (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-146">**OUI (OUIHeader)**</span></span>](wlan-profileschema-oui-ouiheader-element.md)
            -   [<span data-ttu-id="8ad48-147">**輸入 (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-147">**type (OUIHeader)**</span></span>](wlan-profileschema-type-ouiheader-element.md)
        -   [<span data-ttu-id="8ad48-148">**(IHV) 的連線能力**</span><span class="sxs-lookup"><span data-stu-id="8ad48-148">**connectivity (IHV)**</span></span>](wlan-profileschema-connectivity-ihv-element.md)
        -   [<span data-ttu-id="8ad48-149">**(IHV) 安全性**</span><span class="sxs-lookup"><span data-stu-id="8ad48-149">**security (IHV)**</span></span>](wlan-profileschema-security-ihv-element.md)
        -   [<span data-ttu-id="8ad48-150">**useMSOneX (IHV)**</span><span class="sxs-lookup"><span data-stu-id="8ad48-150">**useMSOneX (IHV)**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)

 

 



