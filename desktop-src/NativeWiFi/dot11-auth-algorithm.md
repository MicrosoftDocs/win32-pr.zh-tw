---
description: 定義無線區域網路驗證演算法。
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: 'DOT11_AUTH_ALGORITHM 列舉 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971869"
---
# <a name="dot11_auth_algorithm-enumeration"></a><span data-ttu-id="18fc9-103">DOT11 \_ AUTH \_ 演算法列舉</span><span class="sxs-lookup"><span data-stu-id="18fc9-103">DOT11\_AUTH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="18fc9-104">**DOT11 \_ AUTH \_ 演算法** 列舉型別定義了無線區域網路驗證演算法。</span><span class="sxs-lookup"><span data-stu-id="18fc9-104">The **DOT11\_AUTH\_ALGORITHM** enumerated type defines a wireless LAN authentication algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="18fc9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18fc9-105">Syntax</span></span>


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="18fc9-106">常數</span><span class="sxs-lookup"><span data-stu-id="18fc9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="18fc9-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="18fc9-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11\_AUTH\_ALGO\_80211\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-108">指定 IEEE 802.11 開放式系統驗證演算法。</span><span class="sxs-lookup"><span data-stu-id="18fc9-108">Specifies an IEEE 802.11 Open System authentication algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="18fc9-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ 共用 \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="18fc9-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11\_AUTH\_ALGO\_80211\_SHARED\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-110">指定802.11 共用金鑰驗證演算法，此演算法需要使用預先共用的有線對等隱私權 (WEP) 金鑰進行802.11 驗證。</span><span class="sxs-lookup"><span data-stu-id="18fc9-110">Specifies an 802.11 Shared Key authentication algorithm that requires the use of a pre-shared Wired Equivalent Privacy (WEP) key for the 802.11 authentication.</span></span>

</dd> <dt>

<span data-ttu-id="18fc9-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA**</span><span class="sxs-lookup"><span data-stu-id="18fc9-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11\_AUTH\_ALGO\_WPA**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-112"> (WPA) 演算法指定 Wi-Fi 保護的存取。</span><span class="sxs-lookup"><span data-stu-id="18fc9-112">Specifies a Wi-Fi Protected Access (WPA) algorithm.</span></span> <span data-ttu-id="18fc9-113">IEEE 802.1 X 埠驗證是由要求者、驗證器和驗證服務器所執行。</span><span class="sxs-lookup"><span data-stu-id="18fc9-113">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="18fc9-114">加密金鑰是透過驗證程式進行動態衍生。</span><span class="sxs-lookup"><span data-stu-id="18fc9-114">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="18fc9-115">此演算法只對 dot11 \_ bss \_ 類型基礎結構的 bss 類型有效 \_ 。</span><span class="sxs-lookup"><span data-stu-id="18fc9-115">This algorithm is valid only for BSS types of dot11\_BSS\_type\_infrastructure.</span></span>

<span data-ttu-id="18fc9-116">啟用 WPA 演算法時，802.11 站只會與存取點相關聯，而該存取點的指標或探查回應會包含類型 1 (802.1 X) 在 WPA 資訊元素 (IE) 內的驗證套件。</span><span class="sxs-lookup"><span data-stu-id="18fc9-116">When the WPA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the WPA information element (IE).</span></span>

</dd> <dt>

<span data-ttu-id="18fc9-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="18fc9-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11\_AUTH\_ALGO\_WPA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-118">指定使用預先共用金鑰 (PSK) 的 WPA 演算法。</span><span class="sxs-lookup"><span data-stu-id="18fc9-118">Specifies a WPA algorithm that uses preshared keys (PSK).</span></span> <span data-ttu-id="18fc9-119">「IEEE 802.1 X 埠驗證」是由要求者和驗證者執行。</span><span class="sxs-lookup"><span data-stu-id="18fc9-119">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="18fc9-120">加密金鑰是透過在要求者和驗證者上使用的預先共用金鑰來動態衍生。</span><span class="sxs-lookup"><span data-stu-id="18fc9-120">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="18fc9-121">此演算法只對 **dot11 \_ bss \_ 類型 \_ 基礎結構** 的 bss 類型有效。</span><span class="sxs-lookup"><span data-stu-id="18fc9-121">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="18fc9-122">啟用 WPA PSK 演算法時，802.11 工作站只會與存取點相關聯，該存取點的指標或探查回應會包含類型2的驗證套件， (預先共用金鑰) 在 WPA IE 內。</span><span class="sxs-lookup"><span data-stu-id="18fc9-122">When the WPA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2 (preshared key) within the WPA IE.</span></span>

</dd> <dt>

<span data-ttu-id="18fc9-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ NONE**</span><span class="sxs-lookup"><span data-stu-id="18fc9-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11\_AUTH\_ALGO\_WPA\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-124">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="18fc9-124">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="18fc9-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA**</span><span class="sxs-lookup"><span data-stu-id="18fc9-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11\_AUTH\_ALGO\_RSNA**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-126">指定 802.11 i 穩固的安全性網路關聯 (RSNA) 演算法。</span><span class="sxs-lookup"><span data-stu-id="18fc9-126">Specifies an 802.11i Robust Security Network Association (RSNA) algorithm.</span></span> <span data-ttu-id="18fc9-127">WPA2 就是其中一種演算法。</span><span class="sxs-lookup"><span data-stu-id="18fc9-127">WPA2 is one such algorithm.</span></span> <span data-ttu-id="18fc9-128">IEEE 802.1 X 埠驗證是由要求者、驗證器和驗證服務器所執行。</span><span class="sxs-lookup"><span data-stu-id="18fc9-128">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="18fc9-129">加密金鑰是透過驗證程式進行動態衍生。</span><span class="sxs-lookup"><span data-stu-id="18fc9-129">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="18fc9-130">此演算法只對 **dot11 \_ bss \_ 類型 \_ 基礎結構** 的 bss 類型有效。</span><span class="sxs-lookup"><span data-stu-id="18fc9-130">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="18fc9-131">啟用 RSNA 演算法時，802.11 站只會與一個存取點相關聯，該存取點的指標或探查回應會包含 RSN IE 內類型 1 (802.1 X) 的驗證套件。</span><span class="sxs-lookup"><span data-stu-id="18fc9-131">When the RSNA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="18fc9-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="18fc9-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11\_AUTH\_ALGO\_RSNA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-133">指定使用 PSK 的 802.11 i RSNA 演算法。</span><span class="sxs-lookup"><span data-stu-id="18fc9-133">Specifies an 802.11i RSNA algorithm that uses PSK.</span></span> <span data-ttu-id="18fc9-134">「IEEE 802.1 X 埠驗證」是由要求者和驗證者執行。</span><span class="sxs-lookup"><span data-stu-id="18fc9-134">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="18fc9-135">加密金鑰是透過在要求者和驗證者上使用的預先共用金鑰來動態衍生。</span><span class="sxs-lookup"><span data-stu-id="18fc9-135">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="18fc9-136">此演算法只對 **dot11 \_ bss \_ 類型 \_ 基礎結構** 的 bss 類型有效。</span><span class="sxs-lookup"><span data-stu-id="18fc9-136">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="18fc9-137">當啟用 RSNA PSK 演算法時，802.11 站只會與存取點產生關聯，而該存取點的指標或探查回應會包含類型2的驗證套件， (預先共用金鑰) 在 RSN IE 內。</span><span class="sxs-lookup"><span data-stu-id="18fc9-137">When the RSNA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2(preshared key) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="18fc9-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ START**</span><span class="sxs-lookup"><span data-stu-id="18fc9-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11\_AUTH\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-139">表示範圍的開頭，此範圍會指定由 IHV 開發的專屬驗證演算法。</span><span class="sxs-lookup"><span data-stu-id="18fc9-139">Indicates the start of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="18fc9-140">只有當微型埠驅動程式是在可延伸工作站 (ExtSTA) 模式下運作時， **DOT11 \_ AUTH \_ ALGO \_ IHV \_ 啟動** 列舉值才有效。</span><span class="sxs-lookup"><span data-stu-id="18fc9-140">The **DOT11\_AUTH\_ALGO\_IHV\_START** enumerator is valid only when the miniport driver is operating in Extensible Station (ExtSTA) mode.</span></span>

</dd> <dt>

<span data-ttu-id="18fc9-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ END**</span><span class="sxs-lookup"><span data-stu-id="18fc9-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11\_AUTH\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="18fc9-142">表示範圍的結尾，此範圍會指定由 IHV 開發的專屬驗證演算法。</span><span class="sxs-lookup"><span data-stu-id="18fc9-142">Indicates the end of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="18fc9-143">只有當微型埠驅動程式是以 ExtSTA 模式運作時， **DOT11 \_ AUTH \_ ALGO \_ IHV \_ END** 列舉值才有效。</span><span class="sxs-lookup"><span data-stu-id="18fc9-143">The **DOT11\_AUTH\_ALGO\_IHV\_END** enumerator is valid only when the miniport driver is operating in ExtSTA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18fc9-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="18fc9-144">Requirements</span></span>



| <span data-ttu-id="18fc9-145">需求</span><span class="sxs-lookup"><span data-stu-id="18fc9-145">Requirement</span></span> | <span data-ttu-id="18fc9-146">值</span><span class="sxs-lookup"><span data-stu-id="18fc9-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18fc9-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18fc9-147">Minimum supported client</span></span><br/> | <span data-ttu-id="18fc9-148">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18fc9-148">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18fc9-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18fc9-149">Minimum supported server</span></span><br/> | <span data-ttu-id="18fc9-150">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18fc9-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="18fc9-151">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="18fc9-151">Redistributable</span></span><br/>          | <span data-ttu-id="18fc9-152">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="18fc9-152">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="18fc9-153">標頭</span><span class="sxs-lookup"><span data-stu-id="18fc9-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="18fc9-154"><dt>Wlantypes (包含 Windot11) </dt></span><span class="sxs-lookup"><span data-stu-id="18fc9-154"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18fc9-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18fc9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18fc9-156">**DOT11 \_ AUTH \_ CIPHER \_ 配對**</span><span class="sxs-lookup"><span data-stu-id="18fc9-156">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="18fc9-157">**可用的 WLAN \_ \_ 網路**</span><span class="sxs-lookup"><span data-stu-id="18fc9-157">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="18fc9-158">**WLAN \_ 安全性 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="18fc9-158">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




