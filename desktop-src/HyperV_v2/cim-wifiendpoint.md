---
description: 代表無線通訊端點，其相關聯的介面裝置與 IEEE 802.11 無線區域網路連線時，可以傳送和接收資料框架。
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: CIM_WiFiEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiEndpoint
- CIM_WiFiEndpoint.LANID
- CIM_WiFiEndpoint.ProtocolIFType
- CIM_WiFiEndpoint.EncryptionMethod
- CIM_WiFiEndpoint.OtherEncryptionMethod
- CIM_WiFiEndpoint.AuthenticationMethod
- CIM_WiFiEndpoint.OtherAuthenticationMethod
- CIM_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- CIM_WiFiEndpoint.AccessPointAddress
- CIM_WiFiEndpoint.BSSType
- CIM_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e09d040f9d4530bee4347528d704cfe2e9403b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988340"
---
# <a name="cim_wifiendpoint-class"></a><span data-ttu-id="810c8-103">CIM \_ WiFiEndpoint 類別</span><span class="sxs-lookup"><span data-stu-id="810c8-103">CIM\_WiFiEndpoint class</span></span>

<span data-ttu-id="810c8-104">代表無線通訊端點，其相關聯的介面裝置與 IEEE 802.11 無線區域網路連線時，可以傳送和接收資料框架。</span><span class="sxs-lookup"><span data-stu-id="810c8-104">Represents a wireless communication endpoint, which can send and receive data frames when its associated interface device is connected with an IEEE 802.11 wireless LAN.</span></span>

## <a name="syntax"></a><span data-ttu-id="810c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="810c8-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Network::Wireless"), AMENDMENT]
class CIM_WiFiEndpoint : CIM_LANEndpoint
{
  string  LANID;
  uint16  ProtocolIFType = 71;
  uint16  EncryptionMethod;
  string  OtherEncryptionMethod;
  uint16  AuthenticationMethod;
  string  OtherAuthenticationMethod;
  uint16  IEEE8021xAuthenticationProtocol;
  string  AccessPointAddress;
  uint16  BSSType;
  boolean Associated;
};
```

## <a name="members"></a><span data-ttu-id="810c8-106">成員</span><span class="sxs-lookup"><span data-stu-id="810c8-106">Members</span></span>

<span data-ttu-id="810c8-107">**CIM \_ WiFiEndpoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="810c8-107">The **CIM\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="810c8-108">屬性</span><span class="sxs-lookup"><span data-stu-id="810c8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="810c8-109">屬性</span><span class="sxs-lookup"><span data-stu-id="810c8-109">Properties</span></span>

<span data-ttu-id="810c8-110">**CIM \_ WiFiEndpoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="810c8-110">The **CIM\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="810c8-111">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="810c8-111">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="810c8-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="810c8-114">與 Wi-Fi 端點相關聯之存取點的 MAC 位址;否則 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="810c8-114">The MAC address of the access point that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="810c8-115">**相關聯**</span><span class="sxs-lookup"><span data-stu-id="810c8-115">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="810c8-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="810c8-118">如果 WiFi 端點目前與存取點或用戶端工作站相關聯，則 **為 true** 。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="810c8-118">**true** if the WiFi endpoint is currently associated with an access point or client station; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="810c8-119">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="810c8-119">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-120">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="810c8-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c8-122">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "IEEE 802.11-2007 \| 8" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ WiFiEndpoint**。**EncryptionMethod**"，"**CIM \_ WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**"，"**CIM \_ WiFiEndpoint**.**OtherAuthenticationMethod**") </span><span class="sxs-lookup"><span data-stu-id="810c8-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**", "**CIM\_WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM\_WiFiEndpoint**.**OtherAuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="810c8-123">Wi-Fi 端點和網路之間使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="810c8-123">The authentication type used between the Wi-Fi endpoint and the network.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="810c8-124">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="810c8-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="810c8-125">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="810c8-125">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

<span data-ttu-id="810c8-126">**開啟 System** (2) </span><span class="sxs-lookup"><span data-stu-id="810c8-126">**Open System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

<span data-ttu-id="810c8-127">**共用金鑰** (3) </span><span class="sxs-lookup"><span data-stu-id="810c8-127">**Shared Key** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

<span data-ttu-id="810c8-128">**WPA PSK** (4) </span><span class="sxs-lookup"><span data-stu-id="810c8-128">**WPA PSK** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

<span data-ttu-id="810c8-129">**WPA IEEE 802.1 x** (5) </span><span class="sxs-lookup"><span data-stu-id="810c8-129">**WPA IEEE 802.1x** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

<span data-ttu-id="810c8-130">**WPA2 PSK** (6) </span><span class="sxs-lookup"><span data-stu-id="810c8-130">**WPA2 PSK** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

<span data-ttu-id="810c8-131">**WPA2 IEEE 802.1 x** (7) </span><span class="sxs-lookup"><span data-stu-id="810c8-131">**WPA2 IEEE 802.1x** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

<span data-ttu-id="810c8-132">**CCKM IEEE 802.1 x** (8) </span><span class="sxs-lookup"><span data-stu-id="810c8-132">**CCKM IEEE 802.1x** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="810c8-133">**DMTF 保留** (9 ... ) </span><span class="sxs-lookup"><span data-stu-id="810c8-133">**DMTF Reserved** (9..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="810c8-134">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="810c8-134">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="810c8-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c8-137">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "IEEE 802.11-2007 \| 3.16" ) </span><span class="sxs-lookup"><span data-stu-id="810c8-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")</span></span>
</dt> </dl>

<span data-ttu-id="810c8-138">基本服務設定 (BSS) 對應至實例之網路的類型。</span><span class="sxs-lookup"><span data-stu-id="810c8-138">The basic service set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="810c8-139">BSS 是由單一協調功能所控制的一組工作站。</span><span class="sxs-lookup"><span data-stu-id="810c8-139">A BSS is a set of stations controlled by a single coordination function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="810c8-140">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="810c8-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="810c8-141">**獨立** (2) </span><span class="sxs-lookup"><span data-stu-id="810c8-141">**Independent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

<span data-ttu-id="810c8-142">**基礎結構** (3) </span><span class="sxs-lookup"><span data-stu-id="810c8-142">**Infrastructure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="810c8-143">**DMTF 保留** (4.. ) </span><span class="sxs-lookup"><span data-stu-id="810c8-143">**DMTF Reserved** (4..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="810c8-144">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="810c8-144">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-145">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="810c8-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c8-147">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "IEEE 802.11-2007 \| 8" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ WiFiEndpoint**。**AuthenticationMethod**"，"**CIM \_ WiFiEndpoint**。**OtherEncryptionMethod**") </span><span class="sxs-lookup"><span data-stu-id="810c8-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**", "**CIM\_WiFiEndpoint**.**OtherEncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="810c8-148">透過 Wi-Fi 端點來傳送和接收資料時所使用的加密類型。</span><span class="sxs-lookup"><span data-stu-id="810c8-148">The encryption type used when sending and receiving data through the Wi-Fi endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="810c8-149">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="810c8-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="810c8-150">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="810c8-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

<span data-ttu-id="810c8-151">**WEP** (2) </span><span class="sxs-lookup"><span data-stu-id="810c8-151">**WEP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

<span data-ttu-id="810c8-152">**TKIP** (3) </span><span class="sxs-lookup"><span data-stu-id="810c8-152">**TKIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

<span data-ttu-id="810c8-153">**CCMP** (4) </span><span class="sxs-lookup"><span data-stu-id="810c8-153">**CCMP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="810c8-154">**無** (5) </span><span class="sxs-lookup"><span data-stu-id="810c8-154">**None** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="810c8-155">**DMTF 保留** (6.. ) </span><span class="sxs-lookup"><span data-stu-id="810c8-155">**DMTF Reserved** (6..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="810c8-156">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="810c8-156">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="810c8-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c8-159">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "RFC4017。IETF "，" RFC2716。IETF」、「draft-ietf-pppext-eap-tls。IETF」、「draft-kamath-pppext-peapv0」。IETF "、" draft-josefsson s.-pppext-eap-tls-eap-tls "、" RFC4851。IETF "，" RFC3748。IETF "，" RFC4764。IETF "，" RFC4186。IETF "，" RFC4187。IETF ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**。**AuthenticationMethod**") </span><span class="sxs-lookup"><span data-stu-id="810c8-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017.IETF", "RFC2716.IETF", "draft-ietf-pppext-eap-ttls.IETF", "draft-kamath-pppext-peapv0.IETF", "draft-josefsson-pppext-eap-tls-eap", "RFC4851.IETF", "RFC3748.IETF", "RFC4764.IETF", "RFC4186.IETF", "RFC4187.IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="810c8-160">當 **AuthenticationMethod** 包含 "7" (WPA ieee 802.1 x) 或 "8" (CCKM IEEE 802.1 x) 時，EAP (可延伸的驗證通訊協定) 類型的 Wi-Fi 端點。</span><span class="sxs-lookup"><span data-stu-id="810c8-160">The EAP (Extensible Authentication Protocol) type for the Wi-Fi endpoint when **AuthenticationMethod** contains "7" (WPA IEEE 802.1x) or "8" (CCKM IEEE 802.1x).</span></span>

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

<span data-ttu-id="810c8-161">**Eap-tls** (0) </span><span class="sxs-lookup"><span data-stu-id="810c8-161">**EAP-TLS** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

<span data-ttu-id="810c8-162">**EAP-TTLS/eap-mschapv2** (1) </span><span class="sxs-lookup"><span data-stu-id="810c8-162">**EAP-TTLS/MSCHAPv2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

<span data-ttu-id="810c8-163">**PEAPv0/EAP-eap-mschapv2** (2) </span><span class="sxs-lookup"><span data-stu-id="810c8-163">**PEAPv0/EAP-MSCHAPv2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

<span data-ttu-id="810c8-164">**PEAPv1/EAP-GTC** (3) </span><span class="sxs-lookup"><span data-stu-id="810c8-164">**PEAPv1/EAP-GTC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

<span data-ttu-id="810c8-165">**Eap-fast/eap-mschapv2** (4) </span><span class="sxs-lookup"><span data-stu-id="810c8-165">**EAP-FAST/MSCHAPv2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

<span data-ttu-id="810c8-166">**Eap-fast/GTC** (5) </span><span class="sxs-lookup"><span data-stu-id="810c8-166">**EAP-FAST/GTC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

<span data-ttu-id="810c8-167">**EAP-MD5** (6) </span><span class="sxs-lookup"><span data-stu-id="810c8-167">**EAP-MD5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

<span data-ttu-id="810c8-168">**Eap-tls** (7) </span><span class="sxs-lookup"><span data-stu-id="810c8-168">**EAP-PSK** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

<span data-ttu-id="810c8-169">**EAP-SIM** (8) </span><span class="sxs-lookup"><span data-stu-id="810c8-169">**EAP-SIM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

<span data-ttu-id="810c8-170">**EAP-也稱為** (9) </span><span class="sxs-lookup"><span data-stu-id="810c8-170">**EAP-AKA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

<span data-ttu-id="810c8-171">**Eap-fast/TLS** (10) </span><span class="sxs-lookup"><span data-stu-id="810c8-171">**EAP-FAST/TLS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="810c8-172">**DMTF 保留** (11 ) </span><span class="sxs-lookup"><span data-stu-id="810c8-172">**DMTF Reserved** (11..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="810c8-173">**LANID**</span><span class="sxs-lookup"><span data-stu-id="810c8-173">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="810c8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c8-176">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "LANID" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "IEEE 802.11-2007 \| 7.3.2.1" ) </span><span class="sxs-lookup"><span data-stu-id="810c8-176">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span></span>
</dt> </dl>

<span data-ttu-id="810c8-177">服務組識別元 (SSID) 與 Wi-Fi 端點相關聯的無線區域網路;否則 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="810c8-177">The service set identifier (SSID) of the wireless LAN that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="810c8-178">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="810c8-178">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="810c8-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c8-181">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ WiFiEndpoint**.**AuthenticationMethod**") </span><span class="sxs-lookup"><span data-stu-id="810c8-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="810c8-182">當 **AuthenticationMethod** 包含 "1" (其他) 時，Wi-Fi 端點和網路之間使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="810c8-182">The authentication type used between the Wi-Fi endpoint and the network when **AuthenticationMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="810c8-183">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="810c8-183">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="810c8-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c8-186">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ WiFiEndpoint**.**EncryptionMethod**") </span><span class="sxs-lookup"><span data-stu-id="810c8-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="810c8-187">描述當 **EncryptionMethod** 包含 "1" (其他) 時，Wi-Fi 端點的加密類型。</span><span class="sxs-lookup"><span data-stu-id="810c8-187">Describes the encryption type for the Wi-Fi endpoint when **EncryptionMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="810c8-188">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="810c8-188">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="810c8-189">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="810c8-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="810c8-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="810c8-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="810c8-191">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ProtocolIFType" ) </span><span class="sxs-lookup"><span data-stu-id="810c8-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span></span>
</dt> </dl>

<span data-ttu-id="810c8-192">此實例的分類或分類。</span><span class="sxs-lookup"><span data-stu-id="810c8-192">The category or classification of this instance.</span></span> <span data-ttu-id="810c8-193">可能的值限制為來自 DMTF 和 [IANA IFTYPE MIB](https://www.iana.org/assignments/ianaiftype-mib)的 Wi-Fi 和保留值。</span><span class="sxs-lookup"><span data-stu-id="810c8-193">The possible values are limited to the Wi-Fi and reserved values from the DMTF and [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span>

<span data-ttu-id="810c8-194">如果 **ProtocolIFType** 設為 "1" (其他) ，則應該在 **OtherTypeDescription** 屬性中提供類型資訊。</span><span class="sxs-lookup"><span data-stu-id="810c8-194">If the **ProtocolIFType** is set to "1" (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="810c8-195">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="810c8-195">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="810c8-196">**IEEE 802.11** (71) </span><span class="sxs-lookup"><span data-stu-id="810c8-196">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="810c8-197">**IANA 保留** (225. 4095) </span><span class="sxs-lookup"><span data-stu-id="810c8-197">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="810c8-198">**DMTF 保留** 的 (a334-18f799d361d1. 32767) </span><span class="sxs-lookup"><span data-stu-id="810c8-198">**DMTF Reserved** (4301..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="810c8-199">**廠商保留** (32768 ) </span><span class="sxs-lookup"><span data-stu-id="810c8-199">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="810c8-200"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="810c8-200"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="810c8-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="810c8-201">Requirements</span></span>



| <span data-ttu-id="810c8-202">需求</span><span class="sxs-lookup"><span data-stu-id="810c8-202">Requirement</span></span> | <span data-ttu-id="810c8-203">值</span><span class="sxs-lookup"><span data-stu-id="810c8-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="810c8-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="810c8-204">Minimum supported client</span></span><br/> | <span data-ttu-id="810c8-205">Windows 8</span><span class="sxs-lookup"><span data-stu-id="810c8-205">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="810c8-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="810c8-206">Minimum supported server</span></span><br/> | <span data-ttu-id="810c8-207">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="810c8-207">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="810c8-208">命名空間</span><span class="sxs-lookup"><span data-stu-id="810c8-208">Namespace</span></span><br/>                | <span data-ttu-id="810c8-209">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="810c8-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="810c8-210">MOF</span><span class="sxs-lookup"><span data-stu-id="810c8-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="810c8-211"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="810c8-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="810c8-212">DLL</span><span class="sxs-lookup"><span data-stu-id="810c8-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="810c8-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="810c8-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="810c8-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="810c8-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810c8-215">**CIM \_ LANEndpoint**</span><span class="sxs-lookup"><span data-stu-id="810c8-215">**CIM\_LANEndpoint**</span></span>](cim-lanendpoint.md)
</dt> </dl>

 

