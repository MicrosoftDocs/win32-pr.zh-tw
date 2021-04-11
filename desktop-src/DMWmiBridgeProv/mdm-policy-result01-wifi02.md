---
title: MDM_Policy_Result01_WiFi02 類別
description: MDM \_ Policy \_ Result01 \_ WiFi02 類別代表可用的 Wi-Fi 原則。
ms.assetid: 074C4428-401D-4564-B7AC-45C2221EEC3A
keywords:
- MDM_Policy_Result01_WiFi02 類別
- MDM_Policy_Result01_WiFi02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WiFi02
- MDM_Policy_Result01_WiFi02.InstanceID
- MDM_Policy_Result01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff9e0349f7a18da3320fab333d5b5fd36715999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933949"
---
# <a name="mdm_policy_result01_wifi02-class"></a><span data-ttu-id="9f587-105">MDM \_ 原則 \_ Result01 \_ WiFi02 類別</span><span class="sxs-lookup"><span data-stu-id="9f587-105">MDM\_Policy\_Result01\_WiFi02 class</span></span>

<span data-ttu-id="9f587-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="9f587-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9f587-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="9f587-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9f587-108">**MDM \_ Policy \_ Result01 \_ WiFi02** 類別代表可用的 Wi-Fi 原則。</span><span class="sxs-lookup"><span data-stu-id="9f587-108">The **MDM\_Policy\_Result01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="9f587-109">這些原則會決定允許的 Wi-Fi 設定。</span><span class="sxs-lookup"><span data-stu-id="9f587-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="9f587-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9f587-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f587-111">語法</span><span class="sxs-lookup"><span data-stu-id="9f587-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WiFi02
{
  string InstanceID;
  string ParentID;
  sint32 AllowInternetSharing;
  sint32 AllowWiFi;
  sint32 AllowWiFiDirect;
  sint32 AllowManualWiFiConfiguration;
  sint32 AllowAutoConnectToWiFiSenseHotspots;
  sint32 WLANScanMode;
};
```

## <a name="members"></a><span data-ttu-id="9f587-112">成員</span><span class="sxs-lookup"><span data-stu-id="9f587-112">Members</span></span>

<span data-ttu-id="9f587-113">**MDM \_ Policy \_ Result01 \_ WiFi02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9f587-113">The **MDM\_Policy\_Result01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="9f587-114">屬性</span><span class="sxs-lookup"><span data-stu-id="9f587-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f587-115">屬性</span><span class="sxs-lookup"><span data-stu-id="9f587-115">Properties</span></span>

<span data-ttu-id="9f587-116">**MDM \_ Policy \_ Result01 \_ WiFi02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9f587-116">The **MDM\_Policy\_Result01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9f587-117">AllowAutoConnectToWiFiSenseHotspots</span><span class="sxs-lookup"><span data-stu-id="9f587-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f587-118">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f587-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f587-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f587-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f587-120">AllowInternetSharing</span><span class="sxs-lookup"><span data-stu-id="9f587-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f587-121">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f587-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f587-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f587-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f587-123">AllowManualWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f587-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f587-124">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f587-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f587-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f587-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f587-126">AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="9f587-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f587-127">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f587-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f587-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f587-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f587-129">AllowWiFiDirect</span><span class="sxs-lookup"><span data-stu-id="9f587-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f587-130">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f587-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f587-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f587-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f587-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9f587-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f587-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9f587-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f587-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9f587-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f587-135">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f587-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f587-136">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f587-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="9f587-137">此類別的字串為 "WiFi"。</span><span class="sxs-lookup"><span data-stu-id="9f587-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="9f587-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9f587-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f587-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9f587-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f587-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9f587-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f587-141">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f587-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f587-142">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9f587-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="9f587-143">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="9f587-143">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="9f587-144">WLANScanMode</span><span class="sxs-lookup"><span data-stu-id="9f587-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f587-145">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f587-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f587-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f587-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f587-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f587-147">Requirements</span></span>



| <span data-ttu-id="9f587-148">需求</span><span class="sxs-lookup"><span data-stu-id="9f587-148">Requirement</span></span> | <span data-ttu-id="9f587-149">值</span><span class="sxs-lookup"><span data-stu-id="9f587-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f587-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f587-150">Minimum supported client</span></span><br/> | <span data-ttu-id="9f587-151">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f587-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f587-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f587-152">Minimum supported server</span></span><br/> | <span data-ttu-id="9f587-153">都不支援</span><span class="sxs-lookup"><span data-stu-id="9f587-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9f587-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="9f587-154">Namespace</span></span><br/>                | <span data-ttu-id="9f587-155">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="9f587-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9f587-156">MOF</span><span class="sxs-lookup"><span data-stu-id="9f587-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f587-157"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f587-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f587-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9f587-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f587-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f587-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f587-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f587-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f587-161">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="9f587-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

