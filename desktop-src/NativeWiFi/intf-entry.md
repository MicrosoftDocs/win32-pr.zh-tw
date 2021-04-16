---
description: 包含 RPC 用戶端所需介面的詳細資訊。
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: 'INTF_ENTRY 結構 (Wzcsapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512428"
---
# <a name="intf_entry-structure"></a><span data-ttu-id="76d89-103">INTF \_ 專案結構</span><span class="sxs-lookup"><span data-stu-id="76d89-103">INTF\_ENTRY structure</span></span>

<span data-ttu-id="76d89-104">\[**INTF \_** Windows Vista 和 Windows Server 2008 不再支援此專案。</span><span class="sxs-lookup"><span data-stu-id="76d89-104">\[**INTF\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="76d89-105">相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="76d89-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="76d89-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]</span><span class="sxs-lookup"><span data-stu-id="76d89-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="76d89-107">包含 RPC 用戶端所需介面的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="76d89-107">Contains detailed information about an interface that is required by an RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d89-108">語法</span><span class="sxs-lookup"><span data-stu-id="76d89-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a><span data-ttu-id="76d89-109">成員</span><span class="sxs-lookup"><span data-stu-id="76d89-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="76d89-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="76d89-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-111">以下列格式的 Unicode 字串形式表示之介面 GUID 的指標： "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"。</span><span class="sxs-lookup"><span data-stu-id="76d89-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> <dt>

<span data-ttu-id="76d89-112">**wszDescr**</span><span class="sxs-lookup"><span data-stu-id="76d89-112">**wszDescr**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-113">字串的指標，其中包含無線零設定服務 (WZCSVC) 取出的介面描述。</span><span class="sxs-lookup"><span data-stu-id="76d89-113">A pointer to a string that contains the interface description that is retrieved by the Wireless Zero Configuration service (WZCSVC).</span></span>

</dd> <dt>

<span data-ttu-id="76d89-114">**dwCoNtext**</span><span class="sxs-lookup"><span data-stu-id="76d89-114">**dwContext**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-115">保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="76d89-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-116">**ulMediaState**</span><span class="sxs-lookup"><span data-stu-id="76d89-116">**ulMediaState**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-117">介面目前的 NDIS 媒體連接狀態。</span><span class="sxs-lookup"><span data-stu-id="76d89-117">The current NDIS media connect state for the interface.</span></span> <span data-ttu-id="76d89-118">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="76d89-118">The following table shows the possible values.</span></span>



| <span data-ttu-id="76d89-119">值</span><span class="sxs-lookup"><span data-stu-id="76d89-119">Value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="76d89-120">意義</span><span class="sxs-lookup"><span data-stu-id="76d89-120">Meaning</span></span>                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <span data-ttu-id="76d89-121"><dt>**媒體 \_ 狀態 \_ 已連線**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-121"><dt>**MEDIA\_STATE\_CONNECTED** </dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="76d89-122">媒體已連線。</span><span class="sxs-lookup"><span data-stu-id="76d89-122">The media is connected.</span></span><br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <span data-ttu-id="76d89-123"><dt>**媒體 \_狀態已 \_ 中斷**</dt>連線 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-123"><dt>**MEDIA\_STATE\_DISCONNECTED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="76d89-124">媒體已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="76d89-124">The media is disconnected.</span></span><br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <span data-ttu-id="76d89-125"><dt>**媒體 \_\_未知狀態**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-125"><dt>**MEDIA\_STATE\_UNKNOWN**</dt> <dt>-1</dt></span></span> </dl>               | <span data-ttu-id="76d89-126">媒體狀態不明。</span><span class="sxs-lookup"><span data-stu-id="76d89-126">The media state is unknown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="76d89-127">**ulMediaType**</span><span class="sxs-lookup"><span data-stu-id="76d89-127">**ulMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-128">NIC 目前使用的 NDIS 媒體類型。</span><span class="sxs-lookup"><span data-stu-id="76d89-128">The NDIS media types that the NIC currently uses.</span></span> <span data-ttu-id="76d89-129">進行查詢時，這個成員的值會是 **NdisMedium802 \_ 3** ，如同 *Ndispnp .h* 標頭檔中所定義。</span><span class="sxs-lookup"><span data-stu-id="76d89-129">When queried, the value of this member is **NdisMedium802\_3** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-130">**ulPhysicalMediaType**</span><span class="sxs-lookup"><span data-stu-id="76d89-130">**ulPhysicalMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-131">介面的 NDIS 媒體類型。</span><span class="sxs-lookup"><span data-stu-id="76d89-131">The NDIS media type for the interface.</span></span> <span data-ttu-id="76d89-132">進行查詢時，此成員的值會 **NdisPhysicalMediumWirelessLan** 為 *Ndispnp .h* 標頭檔中所定義。</span><span class="sxs-lookup"><span data-stu-id="76d89-132">When queried, the value of this member is **NdisPhysicalMediumWirelessLan** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-133">**nInfraMode**</span><span class="sxs-lookup"><span data-stu-id="76d89-133">**nInfraMode**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-134">在介面上設定的目前802.11 基礎結構模式。</span><span class="sxs-lookup"><span data-stu-id="76d89-134">The current 802.11 Infrastructure Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-135">**nAuthMode**</span><span class="sxs-lookup"><span data-stu-id="76d89-135">**nAuthMode**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-136">在介面上設定的目前802.11 驗證模式。</span><span class="sxs-lookup"><span data-stu-id="76d89-136">The current 802.11 Authentication Mode set on the interface.</span></span>

<span data-ttu-id="76d89-137">下表根據 *NtDDNdis .h* 標頭檔中定義的 **NDIS \_ 802 \_ 11 \_ 驗證 \_ 模式** 列舉，顯示參數的可能值。</span><span class="sxs-lookup"><span data-stu-id="76d89-137">The following table shows the possible values for the parameter based on the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration defined in the *NtDDNdis.h* header file.</span></span>



| <span data-ttu-id="76d89-138">值</span><span class="sxs-lookup"><span data-stu-id="76d89-138">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="76d89-139">意義</span><span class="sxs-lookup"><span data-stu-id="76d89-139">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <span data-ttu-id="76d89-140"><dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-140"><dt>**Ndis802\_11AuthModeOpen**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="76d89-141">IEEE 802.11 開啟系統驗證。</span><span class="sxs-lookup"><span data-stu-id="76d89-141">IEEE 802.11 Open System authentication.</span></span><br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <span data-ttu-id="76d89-142"><dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-142"><dt>**Ndis802\_11AuthModeShared**</dt> <dt>2</dt></span></span> </dl>                 | <span data-ttu-id="76d89-143">IEEE 802.11 共用驗證，使用預先共用的有線對等隱私權 (WEP) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="76d89-143">IEEE 802.11 shared authentication that uses a pre-shared wired equivalent privacy (WEP) key.</span></span> <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <span data-ttu-id="76d89-144"><dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-144"><dt>**Ndis802\_11AuthModeAutoSwitch**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="76d89-145">自動切換模式。</span><span class="sxs-lookup"><span data-stu-id="76d89-145">Auto-switch mode.</span></span> <span data-ttu-id="76d89-146">使用自動切換模式時，無線網路介面卡 (NIC) 會先嘗試共用驗證模式。</span><span class="sxs-lookup"><span data-stu-id="76d89-146">When using auto-switch mode, the wireless network interface card (NIC) tries shared authentication mode first.</span></span> <span data-ttu-id="76d89-147">如果共用模式失敗，則 NIC 會嘗試使用 open 驗證模式。</span><span class="sxs-lookup"><span data-stu-id="76d89-147">If shared mode fails, the NIC attempts to use open authentication mode.</span></span> <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <span data-ttu-id="76d89-148"><dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-148"><dt>**Ndis802\_11AuthModeWPA**</dt> <dt>4</dt></span></span> </dl>                             | <span data-ttu-id="76d89-149"> (WPA 的無線保護存取) 安全性。</span><span class="sxs-lookup"><span data-stu-id="76d89-149">Wireless Protected Access(WPA) security.</span></span> <span data-ttu-id="76d89-150">驗證是透過 IEEE 802.1 X 在要求者、驗證器和驗證服務器之間執行。</span><span class="sxs-lookup"><span data-stu-id="76d89-150">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="76d89-151">加密金鑰是動態的，並且會透過驗證程式來衍生。</span><span class="sxs-lookup"><span data-stu-id="76d89-151">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <span data-ttu-id="76d89-152"><dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-152"><dt>**Ndis802\_11AuthModeWPAPSK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="76d89-153">使用預先共用金鑰的 WPA 安全性。</span><span class="sxs-lookup"><span data-stu-id="76d89-153">WPA security using a pre-shared key.</span></span> <span data-ttu-id="76d89-154">驗證是透過 IEEE 802.1 X 在要求者和驗證器之間執行。</span><span class="sxs-lookup"><span data-stu-id="76d89-154">Authentication is performed between the supplicant and authenticator over IEEE 802.1X.</span></span> <span data-ttu-id="76d89-155">加密金鑰是動態的，而且是透過要求者和驗證器所使用的預先共用金鑰所衍生。</span><span class="sxs-lookup"><span data-stu-id="76d89-155">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <span data-ttu-id="76d89-156"><dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-156"><dt>**Ndis802\_11AuthModeWPANone**</dt> <dt>6</dt></span></span> </dl>             | <span data-ttu-id="76d89-157">WPA 安全性。</span><span class="sxs-lookup"><span data-stu-id="76d89-157">WPA security.</span></span> <span data-ttu-id="76d89-158">使用未使用 IEEE 802.1 X 驗證的預先共用金鑰執行驗證。</span><span class="sxs-lookup"><span data-stu-id="76d89-158">Authentication is performed using a preshared key without IEEE 802.1X authentication.</span></span> <span data-ttu-id="76d89-159">加密金鑰是靜態的，而且是透過預先共用的金鑰來衍生。</span><span class="sxs-lookup"><span data-stu-id="76d89-159">Encryption keys are static and are derived through the preshared key.</span></span> <span data-ttu-id="76d89-160">此模式只適用于臨機操作網路類型。</span><span class="sxs-lookup"><span data-stu-id="76d89-160">This mode is applicable only to ad hoc network types.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <span data-ttu-id="76d89-161"><dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-161"><dt>**Ndis802\_11AuthModeWPA2**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="76d89-162">WPA2 安全性。</span><span class="sxs-lookup"><span data-stu-id="76d89-162">WPA2 security.</span></span> <span data-ttu-id="76d89-163">驗證是透過 IEEE 802.1 X 在要求者、驗證器和驗證服務器之間執行。</span><span class="sxs-lookup"><span data-stu-id="76d89-163">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="76d89-164">加密金鑰是動態的，並且會透過驗證程式來衍生。</span><span class="sxs-lookup"><span data-stu-id="76d89-164">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <span data-ttu-id="76d89-165"><dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-165"><dt>**Ndis802\_11AuthModeWPA2PSK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="76d89-166">指定 WPA2 安全性。</span><span class="sxs-lookup"><span data-stu-id="76d89-166">Specifies WPA2 security.</span></span> <span data-ttu-id="76d89-167">驗證是透過 IEEE 802 1X 在要求者與驗證器之間執行。</span><span class="sxs-lookup"><span data-stu-id="76d89-167">Authentication is performed between the supplicant and authenticator over IEEE 802 1X.</span></span> <span data-ttu-id="76d89-168">加密金鑰是動態的，而且是透過要求者和驗證器所使用的預先共用金鑰所衍生。</span><span class="sxs-lookup"><span data-stu-id="76d89-168">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <span data-ttu-id="76d89-169"><dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-169"><dt>**Ndis802\_11AuthModeMax**</dt> <dt>9</dt></span></span> </dl>                             | <span data-ttu-id="76d89-170">**NDIS \_ 802 \_ 11 \_ 驗證 \_ 模式** 列舉值的最大可能值。</span><span class="sxs-lookup"><span data-stu-id="76d89-170">The maximum possible value for the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration value.</span></span> <span data-ttu-id="76d89-171">這不是驗證模式的合法值。</span><span class="sxs-lookup"><span data-stu-id="76d89-171">This is not a legal value for the authentication mode.</span></span> <br/>                                                                                        |



 

</dd> <dt>

<span data-ttu-id="76d89-172">**nWepStatus**</span><span class="sxs-lookup"><span data-stu-id="76d89-172">**nWepStatus**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-173">在介面上設定的目前802.11 加密模式。</span><span class="sxs-lookup"><span data-stu-id="76d89-173">The current 802.11 Encryption Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-174">**dwCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="76d89-174">**dwCtlFlags**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-175">控制旗標的位元遮罩值，表示 WZCSVC 在介面上的運作方式。</span><span class="sxs-lookup"><span data-stu-id="76d89-175">A bitmask value of control flags that indicate how WZCSVC is operating on the interface.</span></span>

<span data-ttu-id="76d89-176">下表顯示可能的位值。</span><span class="sxs-lookup"><span data-stu-id="76d89-176">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="76d89-177">值</span><span class="sxs-lookup"><span data-stu-id="76d89-177">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="76d89-178">意義</span><span class="sxs-lookup"><span data-stu-id="76d89-178">Meaning</span></span>                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <span data-ttu-id="76d89-179"><dt>**INTFCTL \_CM \_ 遮罩**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-179"><dt>**INTFCTL\_CM\_MASK**</dt> <dt>0x0007</dt></span></span> </dl>      | <span data-ttu-id="76d89-180">網路篩選模式的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="76d89-180">A bitmask for the network filter mode.</span></span> <span data-ttu-id="76d89-181">INTFCTL \_ CM \_ MASK & dwCtlFlags 會產生類型 NDIS \_ 802 \_ 11 \_ 網路 \_ 基礎結構的值。</span><span class="sxs-lookup"><span data-stu-id="76d89-181">INTFCTL\_CM\_MASK & dwCtlFlags result in a value of the type NDIS\_802\_11\_NETWORK\_INFRASTRUCTURE.</span></span> <span data-ttu-id="76d89-182">產生的值會指出 WZCSVC 只會連線到基礎結構網路、臨機操作網路，或連線至這兩種網路類型。</span><span class="sxs-lookup"><span data-stu-id="76d89-182">The resulting value indicates whether WZCSVC connects only to infrastructure networks, adhoc networks, or to both types of networks.</span></span><br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <span data-ttu-id="76d89-183"><dt>**INTFCTL \_啟用**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-183"><dt>**INTFCTL\_ENABLED**</dt> <dt>0x8000</dt></span></span> </dl>       | <span data-ttu-id="76d89-184">指出 WZCSVC 是否應設定介面。</span><span class="sxs-lookup"><span data-stu-id="76d89-184">Indicates whether WZCSVC should configure the interface.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <span data-ttu-id="76d89-185"><dt>**INTFCTL \_回退**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-185"><dt>**INTFCTL\_FALLBACK**</dt> <dt>0x4000</dt></span></span> </dl>    | <span data-ttu-id="76d89-186">如果無法使用慣用網路，此值會指出 WZCSVC 是否應該自動設定要與任何可用網路相關聯的 NIC。</span><span class="sxs-lookup"><span data-stu-id="76d89-186">If a preferred network is not available, this value indicates whether WZCSVC should automatically configure the NIC to associate to any available network.</span></span><br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <span data-ttu-id="76d89-187"><dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-187"><dt>**INTFCTL\_OIDSSUPP** </dt> <dt>0x2000</dt></span></span> </dl> | <span data-ttu-id="76d89-188">指出 NIC 驅動程式是否支援 WZCSVC 運作所需的所有 802.11 Oid。</span><span class="sxs-lookup"><span data-stu-id="76d89-188">Indicates whether the NIC driver supports all the 802.11 OIDs required by WZCSVC to function.</span></span><br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <span data-ttu-id="76d89-189"><dt> **INTFCTL \_ VOLATILE**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-189"><dt>**INTFCTL\_VOLATILE** </dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="76d89-190">指出此介面的服務參數是否應該保留在登錄中。</span><span class="sxs-lookup"><span data-stu-id="76d89-190">Indicates whether the service parameters for this interface should be retained in the registry.</span></span> <br/> <span data-ttu-id="76d89-191">如果設定了這個值，這些參數就會是暫時性的，不應該保留在登錄中。</span><span class="sxs-lookup"><span data-stu-id="76d89-191">If this value is set, then these parameters are volatile and should not be retained in the registry.</span></span><br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <span data-ttu-id="76d89-192"><dt> **INTFCTL \_ 原則**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-192"><dt>**INTFCTL\_POLICY** </dt> <dt>0x0800</dt></span></span> </dl>       | <span data-ttu-id="76d89-193">指出此介面的服務參數是否由群組原則推送。</span><span class="sxs-lookup"><span data-stu-id="76d89-193">Indicates whether the service parameters for this interface are pushed by a group policy.</span></span><br/> <span data-ttu-id="76d89-194">如果設定此值，則會依群組原則將服務參數推送至本機電腦。</span><span class="sxs-lookup"><span data-stu-id="76d89-194">If this value is set, then the service parameters are pushed to the local computer by group policy.</span></span><br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <span data-ttu-id="76d89-195"><dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-195"><dt>**INTFCTL\_8021XSUPP**</dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="76d89-196">指出是否已啟用 802.1 X 支援。</span><span class="sxs-lookup"><span data-stu-id="76d89-196">Indicates whether 802.1X support is enabled.</span></span><br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="76d89-197">**dwDynFlags**</span><span class="sxs-lookup"><span data-stu-id="76d89-197">**dwDynFlags**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-198">動態旗標的位元遮罩，可控制介面上動態 (非持續性和非靜態) 行為。</span><span class="sxs-lookup"><span data-stu-id="76d89-198">A bitmask of dynamic flags that control the dynamic (non-persistent and non-static) behavior on the interface.</span></span>

<span data-ttu-id="76d89-199">這些位有助於以 WZCSVC 在介面上的運作方式觸發動態、暫時的變更。</span><span class="sxs-lookup"><span data-stu-id="76d89-199">These bits are useful to trigger dynamic, temporary changes in the way the WZCSVC acts on the interface.</span></span> <span data-ttu-id="76d89-200">這些位都不會保存在登錄中，因此這些設定將不會在系統重新開機或裝置停用和啟用順序時存活。</span><span class="sxs-lookup"><span data-stu-id="76d89-200">None of these bits are persisted in the registry, so the settings won't survive a system restart or a device disable and enable sequence.</span></span>

<span data-ttu-id="76d89-201">下表顯示可能的位值。</span><span class="sxs-lookup"><span data-stu-id="76d89-201">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="76d89-202">值</span><span class="sxs-lookup"><span data-stu-id="76d89-202">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="76d89-203">意義</span><span class="sxs-lookup"><span data-stu-id="76d89-203">Meaning</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <span data-ttu-id="76d89-204"><dt>**INTFDYN \_NOSCAN**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-204"><dt>**INTFDYN\_NOSCAN**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="76d89-205">指出 WZCSVC 不應要求介面進行主動掃描，但改為在 NIC 驅動程式中使用快取的值。</span><span class="sxs-lookup"><span data-stu-id="76d89-205">Indicates that the WZCSVC should not request the interface conduct an active scan, but instead use the cached values in the NIC driver.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="76d89-206">**dwCapabilities**</span><span class="sxs-lookup"><span data-stu-id="76d89-206">**dwCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-207">指定驅動程式功能。</span><span class="sxs-lookup"><span data-stu-id="76d89-207">Specifies the driver capabilities.</span></span>



| <span data-ttu-id="76d89-208">值</span><span class="sxs-lookup"><span data-stu-id="76d89-208">Value</span></span>                                                                                                                                                                                                                                                         | <span data-ttu-id="76d89-209">意義</span><span class="sxs-lookup"><span data-stu-id="76d89-209">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <span data-ttu-id="76d89-210"><dt>**INTFCAP \_最大 \_ 密碼 \_ 遮罩**</dt> <dt>0x000000ff</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-210"><dt>**INTFCAP\_MAX\_CIPHER\_MASK**</dt> <dt>0x000000ff</dt></span></span> </dl> | <span data-ttu-id="76d89-211">此成員的較低順序位可用來指出支援的最大加密。</span><span class="sxs-lookup"><span data-stu-id="76d89-211">The lower order bits of this member are used to indicate the maximum encryption that is supported.</span></span> <span data-ttu-id="76d89-212">可能的值是 Windows SDK 中所包含的 *NtDDNdis .h* 標頭檔中， **NDIS \_ 802 \_ 11 \_ WEP \_ 狀態** 結構中所定義的一些列舉值。</span><span class="sxs-lookup"><span data-stu-id="76d89-212">The possible values are some of the enumeration values defined in the **NDIS\_802\_11\_WEP\_STATUS** structure in the *NtDDNdis.h* header file included in the Windows SDK.</span></span><br/> <span data-ttu-id="76d89-213">Ndis802 \_ 11Encryption1Enabled 值 (2) 表示支援 WEP。</span><span class="sxs-lookup"><span data-stu-id="76d89-213">The Ndis802\_11Encryption1Enabled value (2) indicates that WEP is supported.</span></span> <span data-ttu-id="76d89-214">不支援 TKIP 和 AES，而且傳輸金鑰可能或可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="76d89-214">TKIP and AES are not supported, and a transmit key may or may not be available.</span></span> <br/> <span data-ttu-id="76d89-215">Ndis802 \_ 11Encryption2Enabled 值 (9) 指出支援 TKIP 和 WEP。</span><span class="sxs-lookup"><span data-stu-id="76d89-215">The Ndis802\_11Encryption2Enabled value (9) indicates that TKIP and WEP are supported.</span></span> <span data-ttu-id="76d89-216">AES 不受支援，且有可用的傳輸金鑰。</span><span class="sxs-lookup"><span data-stu-id="76d89-216">AES is not supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="76d89-217">Ndis802 \_ 11Encryption3Enabled 值 (11) 指出支援 AES、TKIP 和 WEP，且有可用的傳輸金鑰。</span><span class="sxs-lookup"><span data-stu-id="76d89-217">The Ndis802\_11Encryption3Enabled value (11) indicates that AES, TKIP, and WEP are supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="76d89-218">Ndis802 \_ 11EncryptionNotSupported (8) 指出不支援 WEP 金鑰。</span><span class="sxs-lookup"><span data-stu-id="76d89-218">The Ndis802\_11EncryptionNotSupported (8) indicates Indicates that the WEP key is not supported.</span></span> <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <span data-ttu-id="76d89-219"><dt>**INTFCAP \_SSN**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-219"><dt>**INTFCAP\_SSN**</dt> <dt>0x00000100</dt></span></span> </dl>                                       | <span data-ttu-id="76d89-220">指出支援簡單的安全網路 (SSN) 這是 802.11 i 的子集。</span><span class="sxs-lookup"><span data-stu-id="76d89-220">Indicates support for Simple Secure Network (SSN) which is a subset of 802.11i.</span></span> <br/> <span data-ttu-id="76d89-221">SSN 會定期變更加密金鑰，而非 WEP (有線對等的隱私權) 標準（使用靜態金鑰）。</span><span class="sxs-lookup"><span data-stu-id="76d89-221">SSN changes the encryption key periodically, as opposed to the WEP (Wired Equivalent Privacy) standard, which uses a static key.</span></span> <span data-ttu-id="76d89-222">為了讓 SSN 能夠運作，最大支援的密碼至少應該是 TKIP。</span><span class="sxs-lookup"><span data-stu-id="76d89-222">In order for SSN to work, the maximum supported cipher should be at least TKIP.</span></span> <span data-ttu-id="76d89-223">SSN 是由一家廠商協會在2002中開發，做為在 IEEE 802.11 i 標準完成時改善無線區域網路安全性的過渡方法。</span><span class="sxs-lookup"><span data-stu-id="76d89-223">SSN was developed by a consortium of vendors in 2002 as an interim approach to improve wireless LAN security while the IEEE 802.11i standard was being completed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <span data-ttu-id="76d89-224"><dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-224"><dt>**INTFCAP\_80211I**</dt> <dt>0x00000200</dt></span></span> </dl>                              | <span data-ttu-id="76d89-225">指出 IEEE 802.11 i 標準的支援。</span><span class="sxs-lookup"><span data-stu-id="76d89-225">Indicates support for the IEEE 802.11i standard.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="76d89-226">**rdNicCapabilities**</span><span class="sxs-lookup"><span data-stu-id="76d89-226">**rdNicCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-227">適用于 802.11 i 的一組功能。</span><span class="sxs-lookup"><span data-stu-id="76d89-227">A set of capabilities for 802.11i.</span></span>

<span data-ttu-id="76d89-228">[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdNicCapabilities** 的資料，並在 *dwInflags* 參數中傳遞 **INTF \_ 功能** 旗標。</span><span class="sxs-lookup"><span data-stu-id="76d89-228">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdNicCapabilities** data when called with the **INTF\_CAPABILITIES** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="76d89-229">如果函式呼叫成功，**原始 \_ 資料** 結構的 **.pdata** 成員就會包含 **INTF \_ 80211 \_ 功能** 結構。</span><span class="sxs-lookup"><span data-stu-id="76d89-229">If the function call is successful, the **pData** member of the **RAW\_DATA** structure contains an **INTF\_80211\_CAPABILITY** structure.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-230">**rdSSID**</span><span class="sxs-lookup"><span data-stu-id="76d89-230">**rdSSID**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-231">包含目前在介面上設定之 802.11 SSID 的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="76d89-231">Binary data containing the 802.11 SSID currently configured on the interface.</span></span>

<span data-ttu-id="76d89-232">[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdSSID** 的資料，並在 *dwInflags* 參數中傳遞 **INTF 的 \_ SSID** 旗標。</span><span class="sxs-lookup"><span data-stu-id="76d89-232">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdSSID** data when called with the **INTF\_SSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="76d89-233">如果函式呼叫成功，**原始 \_ 資料** 結構 **的 DwDataLen** 成員會包含 **Ndis \_ 802 \_ 11 \_ ssid** 結構的 **>ssidlength** 成員，而 **原始 \_ 資料** 結構的 **.pdata** 成員則包含 **ndis \_ 802 \_ 11 \_ ssid** 結構的 **ssid** 成員。</span><span class="sxs-lookup"><span data-stu-id="76d89-233">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the **SsidLength** member of a **NDIS\_802\_11\_SSID** structure and the **pData** member of the **RAW\_DATA** structure contains the **Ssid** member of a **NDIS\_802\_11\_SSID** structure.</span></span>

<span data-ttu-id="76d89-234">**NDIS \_ 802 \_ 11 \_ SSID** 結構定義于 *Ntddndis .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="76d89-234">The **NDIS\_802\_11\_SSID** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-235">**rdBSSID**</span><span class="sxs-lookup"><span data-stu-id="76d89-235">**rdBSSID**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-236">包含在介面上設定 802.11 BSSID 的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="76d89-236">Binary data containing the 802.11 BSSID configured on the interface.</span></span>

<span data-ttu-id="76d89-237">[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdBSSID** 的資料，並在 *dwInflags* 參數中傳遞 **INTF \_ BSSID** 旗標。</span><span class="sxs-lookup"><span data-stu-id="76d89-237">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSID** data when called with the **INTF\_BSSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="76d89-238">如果函式呼叫成功，**原始 \_ 資料** 結構的 **DwDataLen** 成員會包含 **ndis \_ 802 \_ 11 \_ mac \_ 位址** 結構的大小，而 **原始 \_ 資料** 結構的 **.pdata** 成員則包含 **ndis \_ 802 \_ 11 \_ mac \_ 位址** 結構。</span><span class="sxs-lookup"><span data-stu-id="76d89-238">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the size of an **NDIS\_802\_11\_MAC\_ADDRESS** structure and the **pData** member of the **RAW\_DATA** structure contains the **NDIS\_802\_11\_MAC\_ADDRESS** structure.</span></span>

<span data-ttu-id="76d89-239">**NDIS \_ 802 \_ 11 \_ MAC \_ 位址** 結構定義于 *Ntddndis .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="76d89-239">The **NDIS\_802\_11\_MAC\_ADDRESS** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-240">**rdBSSIDList**</span><span class="sxs-lookup"><span data-stu-id="76d89-240">**rdBSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-241">二進位資料，其中包含 WZCSVC 最後一次取出的 BSSIDs 清單。</span><span class="sxs-lookup"><span data-stu-id="76d89-241">Binary data that contains the list of BSSIDs that was last retrieved by WZCSVC.</span></span>

<span data-ttu-id="76d89-242">[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdBSSIDList** 的資料，並在 *dwInflags* 參數中傳遞 **INTF \_ BSSIDLIST** 旗標。</span><span class="sxs-lookup"><span data-stu-id="76d89-242">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSIDList** data when called with the **INTF\_BSSIDLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="76d89-243">如果函式呼叫成功，**原始 \_ 資料** 結構的 **dwDataLen** 成員就會包含緩衝區的長度以及傳回的資料，而 **原始 \_ 資料** 結構的 **.pdata** 成員會包含 **WZC \_ 802 \_ 11 \_ CONFIG \_ LIST** 結構。</span><span class="sxs-lookup"><span data-stu-id="76d89-243">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-244">**rdStSSIDList**</span><span class="sxs-lookup"><span data-stu-id="76d89-244">**rdStSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-245">包含針對此介面設定之慣用網路清單的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="76d89-245">Binary data that contains the list of preferred networks configured for this interface.</span></span>

<span data-ttu-id="76d89-246">[**WZCQueryInterface**](wzcqueryinterface.md)函式會在呼叫時傳回 **rdStSSIDList** 的資料，並在 *dwInflags* 參數中傳遞 **INTF \_ PREFLIST** 旗標。</span><span class="sxs-lookup"><span data-stu-id="76d89-246">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdStSSIDList** data when called with the **INTF\_PREFLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="76d89-247">如果函式呼叫成功，**原始 \_ 資料** 結構的 **dwDataLen** 成員就會包含緩衝區的長度以及傳回的資料，而 **原始 \_ 資料** 結構的 **.pdata** 成員會包含 **WZC \_ 802 \_ 11 \_ CONFIG \_ LIST** 結構。</span><span class="sxs-lookup"><span data-stu-id="76d89-247">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

<span data-ttu-id="76d89-248">如果其中一個慣用的網路目前已連線，則網路的 **WZC \_ WLAN \_** 設定結構的 **dwCtlFlags** 成員會將 **WZCCTL \_ 媒體 \_ 連線** (0x0400) 位組。</span><span class="sxs-lookup"><span data-stu-id="76d89-248">If one of the preferred networks is currently connected, the **dwCtlFlags** member of the **WZC\_WLAN\_CONFIG** structure for the network will have the **WZCCTL\_MEDIA\_CONNECTED** (0x0400) bit set.</span></span>

</dd> <dt>

<span data-ttu-id="76d89-249">**rdCtrlData**</span><span class="sxs-lookup"><span data-stu-id="76d89-249">**rdCtrlData**</span></span>
</dt> <dd>

<span data-ttu-id="76d89-250">在介面上設定其他參數時，與其他控制項旗標搭配使用的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="76d89-250">Binary data used with other control flags, when setting additional parameters on the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76d89-251">備註</span><span class="sxs-lookup"><span data-stu-id="76d89-251">Remarks</span></span>

<span data-ttu-id="76d89-252">[**WZCQueryInterface**](wzcqueryinterface.md)和 [**WZCRefreshInterface**](wzcrefreshinterface.md)函數會使用 **INTF \_ 專案** 結構。</span><span class="sxs-lookup"><span data-stu-id="76d89-252">The **INTF\_ENTRY** structure is used by the [**WZCQueryInterface**](wzcqueryinterface.md) and [**WZCRefreshInterface**](wzcrefreshinterface.md) functions.</span></span>

<span data-ttu-id="76d89-253">**原始 \_ 資料** 結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="76d89-253">The **RAW\_DATA** structure is defined as follows:</span></span>


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



<span data-ttu-id="76d89-254">*.Pdata* 成員指向二進位資料。</span><span class="sxs-lookup"><span data-stu-id="76d89-254">The *pData* member points to binary data.</span></span> <span data-ttu-id="76d89-255">*DwDataLen* 指出 *.pdata* 所指向的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="76d89-255">The *dwDataLen* indicates the number of bytes pointed by *pData*.</span></span>

> [!Note]  
> <span data-ttu-id="76d89-256">Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="76d89-256">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="76d89-257">規格需求</span><span class="sxs-lookup"><span data-stu-id="76d89-257">Requirements</span></span>



| <span data-ttu-id="76d89-258">需求</span><span class="sxs-lookup"><span data-stu-id="76d89-258">Requirement</span></span> | <span data-ttu-id="76d89-259">值</span><span class="sxs-lookup"><span data-stu-id="76d89-259">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76d89-260">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76d89-260">Minimum supported client</span></span><br/> | <span data-ttu-id="76d89-261">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76d89-261">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76d89-262">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76d89-262">Minimum supported server</span></span><br/> | <span data-ttu-id="76d89-263">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76d89-263">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76d89-264">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="76d89-264">End of client support</span></span><br/>    | <span data-ttu-id="76d89-265">Windows XP （含 SP3）</span><span class="sxs-lookup"><span data-stu-id="76d89-265">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="76d89-266">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="76d89-266">End of server support</span></span><br/>    | <span data-ttu-id="76d89-267">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76d89-267">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="76d89-268">標頭</span><span class="sxs-lookup"><span data-stu-id="76d89-268">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d89-269"><dt>Wzcsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="76d89-269"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d89-270">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76d89-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d89-271">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="76d89-271">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="76d89-272">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="76d89-272">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="76d89-273">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="76d89-273">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 




