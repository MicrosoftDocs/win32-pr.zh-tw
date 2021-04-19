---
title: MDM_Firewall_PrivateProfile02 類別
description: MDM \_ 防火牆 \_ PrivateProfile02 類別可用來設定 Windows Defender 防火牆設定。
ms.assetid: 9d25c181-e9a8-4f63-b276-b22676842667
keywords:
- MDM_Firewall_PrivateProfile02 類別
- MDM_Firewall_PrivateProfile02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Firewall_PrivateProfile02
- MDM_Firewall_PrivateProfile02.InstanceID
- MDM_Firewall_PrivateProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57812ef7c8550937b009e4ff4855321983391585
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969156"
---
# <a name="mdm_firewall_privateprofile02-class"></a><span data-ttu-id="2d6df-105">MDM \_ 防火牆 \_ PrivateProfile02 類別</span><span class="sxs-lookup"><span data-stu-id="2d6df-105">MDM\_Firewall\_PrivateProfile02 class</span></span>

<span data-ttu-id="2d6df-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="2d6df-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2d6df-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="2d6df-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2d6df-108">MDM \_ 防火牆 \_ PrivateProfile02 類別可用來設定 Windows Defender 防火牆設定。</span><span class="sxs-lookup"><span data-stu-id="2d6df-108">The MDM\_Firewall\_PrivateProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="2d6df-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2d6df-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d6df-110">語法</span><span class="sxs-lookup"><span data-stu-id="2d6df-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PrivateProfile02
{
  string InstanceID;
  string ParentID;
  sint32 EnableFirewall;
  sint32 DisableStealthMode;
  sint32 Shielded;
  sint32 DisableUnicastResponsesToMulticastBroadcast;
  sint32 DisableInboundNotifications;
  sint32 AuthAppsAllowUserPrefMerge;
  sint32 GlobalPortsAllowUserPrefMerge;
  sint32 AllowLocalPolicyMerge;
  sint32 AllowLocalIpsecPolicyMerge;
  sint32 DefaultOutboundAction;
  sint32 DefaultInboundAction;
  sint32 DisableStealthModeIpsecSecuredPacketExemption;
};
```

## <a name="members"></a><span data-ttu-id="2d6df-111">成員</span><span class="sxs-lookup"><span data-stu-id="2d6df-111">Members</span></span>

<span data-ttu-id="2d6df-112">**MDM \_ 防火牆 \_ PrivateProfile02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2d6df-112">The **MDM\_Firewall\_PrivateProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="2d6df-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2d6df-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d6df-114">屬性</span><span class="sxs-lookup"><span data-stu-id="2d6df-114">Properties</span></span>

<span data-ttu-id="2d6df-115">**MDM \_ 防火牆 \_ PrivateProfile02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2d6df-115">The **MDM\_Firewall\_PrivateProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2d6df-116">AllowLocalIpsecPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="2d6df-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-119">AllowLocalPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="2d6df-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-122">AuthAppsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="2d6df-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-125">DefaultInboundAction</span><span class="sxs-lookup"><span data-stu-id="2d6df-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-128">DefaultOutboundAction</span><span class="sxs-lookup"><span data-stu-id="2d6df-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-131">DisableInboundNotifications</span><span class="sxs-lookup"><span data-stu-id="2d6df-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-134">DisableStealthMode</span><span class="sxs-lookup"><span data-stu-id="2d6df-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-137">DisableStealthModeIpsecSecuredPacketExemption</span><span class="sxs-lookup"><span data-stu-id="2d6df-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-140">DisableUnicastResponsesToMulticastBroadcast</span><span class="sxs-lookup"><span data-stu-id="2d6df-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-143">EnableFirewall</span><span class="sxs-lookup"><span data-stu-id="2d6df-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-146">GlobalPortsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="2d6df-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d6df-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2d6df-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d6df-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d6df-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2d6df-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d6df-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2d6df-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d6df-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d6df-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-156">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2d6df-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2d6df-157">受防護</span><span class="sxs-lookup"><span data-stu-id="2d6df-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d6df-158">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d6df-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d6df-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2d6df-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d6df-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d6df-160">Requirements</span></span>



| <span data-ttu-id="2d6df-161">需求</span><span class="sxs-lookup"><span data-stu-id="2d6df-161">Requirement</span></span> | <span data-ttu-id="2d6df-162">值</span><span class="sxs-lookup"><span data-stu-id="2d6df-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d6df-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d6df-163">Minimum supported client</span></span><br/> | <span data-ttu-id="2d6df-164">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d6df-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2d6df-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d6df-165">Minimum supported server</span></span><br/> | <span data-ttu-id="2d6df-166">都不支援</span><span class="sxs-lookup"><span data-stu-id="2d6df-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="2d6df-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="2d6df-167">Namespace</span></span><br/>                | <span data-ttu-id="2d6df-168">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2d6df-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="2d6df-169">MOF</span><span class="sxs-lookup"><span data-stu-id="2d6df-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d6df-170"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d6df-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d6df-171">DLL</span><span class="sxs-lookup"><span data-stu-id="2d6df-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d6df-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d6df-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

