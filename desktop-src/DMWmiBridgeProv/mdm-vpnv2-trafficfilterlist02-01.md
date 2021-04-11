---
title: MDM_VPNv2_TrafficFilterList02_01 類別
description: MDM \_ >vpnv2 \_ TrafficFilterList02 \_ 01 類別包含規則的選擇性清單。 只有符合這些規則的流量可以透過 VPN 介面傳送。
ms.assetid: 3cffe96d-7454-43a1-aa5b-33e820369e7e
keywords:
- MDM_VPNv2_TrafficFilterList02_01 類別
- MDM_VPNv2_TrafficFilterList02_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_01
- MDM_VPNv2_TrafficFilterList02_01.InstanceID
- MDM_VPNv2_TrafficFilterList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3005026a85aa118a4122e073579fcb06389a9fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104957"
---
# <a name="mdm_vpnv2_trafficfilterlist02_01-class"></a><span data-ttu-id="3c1eb-106">MDM \_ >vpnv2 \_ TrafficFilterList02 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="3c1eb-106">MDM\_VPNv2\_TrafficFilterList02\_01 class</span></span>

<span data-ttu-id="3c1eb-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="3c1eb-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3c1eb-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="3c1eb-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3c1eb-109">**MDM \_ >vpnv2 \_ TrafficFilterList02 \_ 01** 類別包含規則的選擇性清單。</span><span class="sxs-lookup"><span data-stu-id="3c1eb-109">The **MDM\_VPNv2\_TrafficFilterList02\_01** class contains an optional list of rules.</span></span> <span data-ttu-id="3c1eb-110">只有符合這些規則的流量可以透過 VPN 介面傳送。</span><span class="sxs-lookup"><span data-stu-id="3c1eb-110">Only traffic that matches these rules can be sent via the VPN Interface.</span></span>

<span data-ttu-id="3c1eb-111">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3c1eb-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1eb-112">語法</span><span class="sxs-lookup"><span data-stu-id="3c1eb-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_01
{
  string InstanceID;
  string ParentID;
  string Claims;
  sint32 Protocol;
  string LocalPortRanges;
  string RemotePortRanges;
  string LocalAddressRanges;
  string RemoteAddressRanges;
  string RoutingPolicyType;
};
```

## <a name="members"></a><span data-ttu-id="3c1eb-113">成員</span><span class="sxs-lookup"><span data-stu-id="3c1eb-113">Members</span></span>

<span data-ttu-id="3c1eb-114">**MDM \_ >vpnv2 \_ TrafficFilterList02 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3c1eb-114">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="3c1eb-115">屬性</span><span class="sxs-lookup"><span data-stu-id="3c1eb-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c1eb-116">屬性</span><span class="sxs-lookup"><span data-stu-id="3c1eb-116">Properties</span></span>

<span data-ttu-id="3c1eb-117">**MDM \_ >vpnv2 \_ TrafficFilterList02 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3c1eb-117">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3c1eb-118">宣告</span><span class="sxs-lookup"><span data-stu-id="3c1eb-118">Claims</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-claims)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c1eb-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c1eb-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c1eb-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c1eb-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c1eb-125">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c1eb-125">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="3c1eb-126">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="3c1eb-126">LocalAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c1eb-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c1eb-129">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="3c1eb-129">LocalPortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c1eb-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c1eb-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c1eb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-135">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3c1eb-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3c1eb-136">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="3c1eb-136">Describes the full path to the parent node.</span></span> <span data-ttu-id="3c1eb-137">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span><span class="sxs-lookup"><span data-stu-id="3c1eb-137">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span></span>

</dd> <dt>

[<span data-ttu-id="3c1eb-138">通訊協定</span><span class="sxs-lookup"><span data-stu-id="3c1eb-138">Protocol</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-139">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c1eb-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c1eb-141">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="3c1eb-141">RemoteAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c1eb-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c1eb-144">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="3c1eb-144">RemotePortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c1eb-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3c1eb-147">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="3c1eb-147">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c1eb-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c1eb-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c1eb-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c1eb-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c1eb-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c1eb-150">Requirements</span></span>



| <span data-ttu-id="3c1eb-151">需求</span><span class="sxs-lookup"><span data-stu-id="3c1eb-151">Requirement</span></span> | <span data-ttu-id="3c1eb-152">值</span><span class="sxs-lookup"><span data-stu-id="3c1eb-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c1eb-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c1eb-153">Minimum supported client</span></span><br/> | <span data-ttu-id="3c1eb-154">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c1eb-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c1eb-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c1eb-155">Minimum supported server</span></span><br/> | <span data-ttu-id="3c1eb-156">都不支援</span><span class="sxs-lookup"><span data-stu-id="3c1eb-156">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3c1eb-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="3c1eb-157">Namespace</span></span><br/>                | <span data-ttu-id="3c1eb-158">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="3c1eb-158">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3c1eb-159">MOF</span><span class="sxs-lookup"><span data-stu-id="3c1eb-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c1eb-160"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c1eb-160"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c1eb-161">DLL</span><span class="sxs-lookup"><span data-stu-id="3c1eb-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c1eb-162"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c1eb-162"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c1eb-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c1eb-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1eb-164">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="3c1eb-164">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

