---
title: MDM_Firewall_FirewallRules02_01 類別
description: MDM \_ Firewall \_ FirewallRules02 \_ 01 類別是用來設定 Windows Defender 防火牆設定。
ms.assetid: b09cbd98-152e-486c-acb5-4e1d83e5f8e2
keywords:
- MDM_Firewall_FirewallRules02_01 類別
- MDM_Firewall_FirewallRules02_01 類別，描述
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_Firewall_FirewallRules02_01
- MDM_Firewall_FirewallRules02_01.InstanceID
- MDM_Firewall_FirewallRules02_01.ParentID
- MDM_Firewall_FirewallRules02_01.IcmpTypesAndCodes
- MDM_Firewall_FirewallRules02_01.FriendlyName
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 494be18ece91e7a1776780542f988b80cb822e42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094283"
---
# <a name="mdm_firewall_firewallrules02_01-class"></a><span data-ttu-id="a027e-105">MDM \_ Firewall \_ FirewallRules02 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="a027e-105">MDM\_Firewall\_FirewallRules02\_01 class</span></span>

<span data-ttu-id="a027e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a027e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a027e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a027e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a027e-108">MDM \_ Firewall \_ FirewallRules02 \_ 01 類別是用來設定 Windows Defender 防火牆設定。</span><span class="sxs-lookup"><span data-stu-id="a027e-108">The MDM\_Firewall\_FirewallRules02\_01 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="a027e-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a027e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a027e-110">語法</span><span class="sxs-lookup"><span data-stu-id="a027e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_FirewallRules02_01
{
  string  InstanceID;
  string  ParentID;
  sint32  Protocol;
  string  LocalPortRanges;
  string  RemotePortRanges;
  string  LocalAddressRanges;
  string  RemoteAddressRanges;
  string  Description;
  boolean Enabled;
  sint32  Profiles;
  string  Direction;
  string  InterfaceTypes;
  string  IcmpTypesAndCodes;
  boolean EdgeTraversal;
  string  LocalUserAuthorizedList;
  string  Status;
  string  FriendlyName;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="a027e-111">成員</span><span class="sxs-lookup"><span data-stu-id="a027e-111">Members</span></span>

<span data-ttu-id="a027e-112">**MDM \_ Firewall \_ FirewallRules02 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a027e-112">The **MDM\_Firewall\_FirewallRules02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="a027e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a027e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a027e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a027e-114">Properties</span></span>

<span data-ttu-id="a027e-115">**MDM \_ Firewall \_ FirewallRules02 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a027e-115">The **MDM\_Firewall\_FirewallRules02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a027e-116">說明</span><span class="sxs-lookup"><span data-stu-id="a027e-116">Description</span></span>](/windows/client-management/mdm/firewall-csp#description)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a027e-119">[方向]</span><span class="sxs-lookup"><span data-stu-id="a027e-119">[Direction](/windows/client-management/mdm/firewall-csp#direction)</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-122">EdgeTraversal</span><span class="sxs-lookup"><span data-stu-id="a027e-122">EdgeTraversal</span></span>](/windows/client-management/mdm/firewall-csp#edgetraversal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-123">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a027e-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-125">Enabled</span><span class="sxs-lookup"><span data-stu-id="a027e-125">Enabled</span></span>](/windows/client-management/mdm/firewall-csp#enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a027e-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a027e-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="a027e-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a027e-131">TBD</span><span class="sxs-lookup"><span data-stu-id="a027e-131">TBD</span></span>

</dd> <dt>

<span data-ttu-id="a027e-132">**IcmpTypesAndCodes**</span><span class="sxs-lookup"><span data-stu-id="a027e-132">**IcmpTypesAndCodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a027e-135">TBD</span><span class="sxs-lookup"><span data-stu-id="a027e-135">TBD</span></span>

</dd> <dt>

<span data-ttu-id="a027e-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a027e-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a027e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a027e-139">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a027e-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-140">InterfaceTypes</span><span class="sxs-lookup"><span data-stu-id="a027e-140">InterfaceTypes</span></span>](/windows/client-management/mdm/firewall-csp#interfacetypes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-143">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="a027e-143">LocalAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-146">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="a027e-146">LocalPortRanges</span></span>](/windows/client-management/mdm/firewall-csp#localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-149">LocalUserAuthorizedList</span><span class="sxs-lookup"><span data-stu-id="a027e-149">LocalUserAuthorizedList</span></span>](/windows/client-management/mdm/firewall-csp#localuserauthorizedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-152">名稱</span><span class="sxs-lookup"><span data-stu-id="a027e-152">Name</span></span>](/windows/client-management/mdm/firewall-csp#name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a027e-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a027e-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a027e-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a027e-158">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a027e-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-159">設定檔</span><span class="sxs-lookup"><span data-stu-id="a027e-159">Profiles</span></span>](/windows/client-management/mdm/firewall-csp#profiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-160">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a027e-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-161">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-162">通訊協定</span><span class="sxs-lookup"><span data-stu-id="a027e-162">Protocol</span></span>](/windows/client-management/mdm/firewall-csp#protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-163">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a027e-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-164">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-165">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="a027e-165">RemoteAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-167">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-168">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="a027e-168">RemotePortRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a027e-171">狀態</span><span class="sxs-lookup"><span data-stu-id="a027e-171">Status</span></span>](/windows/client-management/mdm/firewall-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a027e-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a027e-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a027e-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a027e-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a027e-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="a027e-174">Requirements</span></span>



| <span data-ttu-id="a027e-175">需求</span><span class="sxs-lookup"><span data-stu-id="a027e-175">Requirement</span></span> | <span data-ttu-id="a027e-176">值</span><span class="sxs-lookup"><span data-stu-id="a027e-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a027e-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a027e-177">Minimum supported client</span></span><br/> | <span data-ttu-id="a027e-178">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a027e-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a027e-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a027e-179">Minimum supported server</span></span><br/> | <span data-ttu-id="a027e-180">都不支援</span><span class="sxs-lookup"><span data-stu-id="a027e-180">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a027e-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="a027e-181">Namespace</span></span><br/>                | <span data-ttu-id="a027e-182">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a027e-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="a027e-183">MOF</span><span class="sxs-lookup"><span data-stu-id="a027e-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a027e-184"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a027e-184"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="a027e-185">DLL</span><span class="sxs-lookup"><span data-stu-id="a027e-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a027e-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a027e-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

