---
description: 由於作業系統的基礎架構差異，Windows XP Service Pack 3 (SP3) 和適用于 Windows XP Service Pack 2 (SP2 的無線區域網路 API) 僅支援 WLAN \_ 設定檔架構和 OneX 架構參考資料中所述的元素子集。
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: 無線設定檔相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513488"
---
# <a name="wireless-profile-compatibility"></a><span data-ttu-id="c2578-103">無線設定檔相容性</span><span class="sxs-lookup"><span data-stu-id="c2578-103">Wireless Profile Compatibility</span></span>

<span data-ttu-id="c2578-104">由於作業系統的基礎架構差異，Windows XP Service Pack 3 (SP3) 和適用于 Windows XP Service Pack 2 (SP2 的無線區域網路 API) 僅支援 [WLAN \_ 設定檔架構](wlan-profileschema-schema.md) 和 [OneX 架構](onexschema-schema.md) 參考資料中所述的元素子集。</span><span class="sxs-lookup"><span data-stu-id="c2578-104">Because of underlying architectural differences in the operating system, Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) support only a subset of the elements described in the [WLAN\_profile Schema](wlan-profileschema-schema.md) and [OneX Schema](onexschema-schema.md) reference material.</span></span>

<span data-ttu-id="c2578-105">所有符合 Windows XP 含 SP3 的設定檔，以及適用于 Windows XP SP2 的無線區域網路 API 需求，也可以在 Windows Vista 和 Windows Server 2008 上使用。</span><span class="sxs-lookup"><span data-stu-id="c2578-105">All profiles that conform to Windows XP with SP3 and Wireless LAN API for Windows XP with SP2 requirements can also be used on Windows Vista and Windows Server 2008.</span></span>

## <a name="wlan_profile-support"></a><span data-ttu-id="c2578-106">WLAN \_ 設定檔支援</span><span class="sxs-lookup"><span data-stu-id="c2578-106">WLAN\_profile Support</span></span>

<span data-ttu-id="c2578-107">Windows \_ xp 含 SP3 或適用于 WINDOWS XP SP2 的無線區域網路 API 不支援下列 WLAN 設定檔元素：</span><span class="sxs-lookup"><span data-stu-id="c2578-107">The following WLAN\_profile elements are not supported in Windows XP with SP3 or Wireless LAN API for Windows XP with SP2:</span></span>

-   <span data-ttu-id="c2578-108"> (IHV) 的連線能力</span><span class="sxs-lookup"><span data-stu-id="c2578-108">connectivity (IHV)</span></span>
-   <span data-ttu-id="c2578-109">IHV (WLANProfile) </span><span class="sxs-lookup"><span data-stu-id="c2578-109">IHV (WLANProfile)</span></span>
-   <span data-ttu-id="c2578-110">OUI (OUIHeader) </span><span class="sxs-lookup"><span data-stu-id="c2578-110">OUI (OUIHeader)</span></span>
-   <span data-ttu-id="c2578-111">phyType (連接) </span><span class="sxs-lookup"><span data-stu-id="c2578-111">phyType (connectivity)</span></span>
-   <span data-ttu-id="c2578-112">PMKCacheMode (安全性) </span><span class="sxs-lookup"><span data-stu-id="c2578-112">PMKCacheMode (security)</span></span>
-   <span data-ttu-id="c2578-113">PMKCacheSize (安全性) </span><span class="sxs-lookup"><span data-stu-id="c2578-113">PMKCacheSize (security)</span></span>
-   <span data-ttu-id="c2578-114">PMKCacheTTL (安全性) </span><span class="sxs-lookup"><span data-stu-id="c2578-114">PMKCacheTTL (security)</span></span>
-   <span data-ttu-id="c2578-115">preAuthMode (安全性) </span><span class="sxs-lookup"><span data-stu-id="c2578-115">preAuthMode (security)</span></span>
-   <span data-ttu-id="c2578-116">preAuthThrottle (安全性) </span><span class="sxs-lookup"><span data-stu-id="c2578-116">preAuthThrottle (security)</span></span>
-   <span data-ttu-id="c2578-117"> (IHV) 安全性</span><span class="sxs-lookup"><span data-stu-id="c2578-117">security (IHV)</span></span>
-   <span data-ttu-id="c2578-118">輸入 (OUIHeader) </span><span class="sxs-lookup"><span data-stu-id="c2578-118">type (OUIHeader)</span></span>
-   <span data-ttu-id="c2578-119">useMSOneX (IHV) </span><span class="sxs-lookup"><span data-stu-id="c2578-119">useMSOneX (IHV)</span></span>

<span data-ttu-id="c2578-120">下表顯示具有 windows xp \_ （含 SP3）的受限制值的 WLAN 設定檔元素，以及適用于 WINDOWS XP SP2 的無線區域網路 API：</span><span class="sxs-lookup"><span data-stu-id="c2578-120">The following table shows WLAN\_profile elements with constrained values for Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>



| <span data-ttu-id="c2578-121">元素</span><span class="sxs-lookup"><span data-stu-id="c2578-121">Element</span></span>                                                                               | <span data-ttu-id="c2578-122">條件約束</span><span class="sxs-lookup"><span data-stu-id="c2578-122">Constraint</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2578-123">**WLANProfile) 名稱 (**</span><span class="sxs-lookup"><span data-stu-id="c2578-123">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)             | <span data-ttu-id="c2578-124">當設定檔儲存在設定檔存放區中時，會忽略 name 元素。</span><span class="sxs-lookup"><span data-stu-id="c2578-124">The name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="c2578-125">設定檔的名稱會自動衍生自網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="c2578-125">The name of the profile is derived automatically from the SSID of the network.</span></span> <span data-ttu-id="c2578-126">在基礎結構網路設定檔中，設定檔的名稱是網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="c2578-126">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="c2578-127">針對臨機操作網路設定檔，設定檔的名稱是臨機操作網路的 SSID，後面接著 `-adhoc` 。</span><span class="sxs-lookup"><span data-stu-id="c2578-127">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> |
| [<span data-ttu-id="c2578-128">**protected (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="c2578-128">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)       | <span data-ttu-id="c2578-129">的值必須為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="c2578-129">Must have a value of FALSE.</span></span>                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="c2578-130">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="c2578-130">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md) | <span data-ttu-id="c2578-131">限制為一個子 [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="c2578-131">Restricted to one child [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a><span data-ttu-id="c2578-132">OneX 支援</span><span class="sxs-lookup"><span data-stu-id="c2578-132">OneX Support</span></span>

<span data-ttu-id="c2578-133">Windows xp （含 SP3）和適用于 Windows XP SP2 的無線區域網路 API 只支援 [**EAPConfig**](onexschema-eapconfig-onex-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="c2578-133">Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="c2578-134">如果設定檔中有其他的 OneX 元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="c2578-134">Other OneX elements, if present in a profile, will be ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2578-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2578-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2578-136">關於原生 Wifi API</span><span class="sxs-lookup"><span data-stu-id="c2578-136">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="c2578-137">Windows XP 上的原生 Wifi API 支援</span><span class="sxs-lookup"><span data-stu-id="c2578-137">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



