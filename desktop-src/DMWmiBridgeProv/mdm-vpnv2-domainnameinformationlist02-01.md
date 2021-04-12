---
title: MDM_VPNv2_DomainNameInformationList02_01 類別
description: MDM \_ >vpnv2 \_ DomainNameInformationList02 \_ 01 類別描述的名稱解析原則表 (NRPT) VPN 設定檔的規則。
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- MDM_VPNv2_DomainNameInformationList02_01 類別
- MDM_VPNv2_DomainNameInformationList02_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934940"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a><span data-ttu-id="77010-105">MDM \_ >vpnv2 \_ DomainNameInformationList02 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="77010-105">MDM\_VPNv2\_DomainNameInformationList02\_01 class</span></span>

<span data-ttu-id="77010-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="77010-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="77010-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="77010-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="77010-108">**MDM \_ >vpnv2 \_ DomainNameInformationList02 \_ 01** 類別描述的名稱解析原則表 (NRPT) VPN 設定檔的規則。</span><span class="sxs-lookup"><span data-stu-id="77010-108">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class describes the Name Resolution Policy Table (NRPT) rules for the VPN profile.</span></span>

<span data-ttu-id="77010-109">名稱解析原則表 (NRPT) 是儲存在 Windows 登錄中的命名空間和對應設定的表格，可決定發出查詢和處理回應時的 DNS 用戶端行為。</span><span class="sxs-lookup"><span data-stu-id="77010-109">The Name Resolution Policy Table (NRPT) is a table of namespaces and corresponding settings stored in the Windows registry that determines the DNS client behavior when issuing queries and processing responses.</span></span> <span data-ttu-id="77010-110">NRPT 中的每個資料列都代表 DNS 用戶端發出查詢之部分命名空間的規則。</span><span class="sxs-lookup"><span data-stu-id="77010-110">Each row in the NRPT represents a rule for a portion of the namespace for which the DNS client issues queries.</span></span> <span data-ttu-id="77010-111">在發出名稱解析查詢之前，DNS 用戶端會查閱 NRPT，以判斷是否必須在查詢中設定任何其他旗標。</span><span class="sxs-lookup"><span data-stu-id="77010-111">Before issuing name resolution queries, the DNS client consults the NRPT to determine if any additional flags must be set in the query.</span></span> <span data-ttu-id="77010-112">收到回應之後，用戶端會再次諮詢 NRPT，以檢查是否有任何特殊的處理或原則需求。</span><span class="sxs-lookup"><span data-stu-id="77010-112">After receiving the response, the client again consults the NRPT to check for any special processing or policy requirements.</span></span> <span data-ttu-id="77010-113">如果沒有 NRPT，用戶端會根據在介面上設定的 DNS 伺服器和尾碼來操作。</span><span class="sxs-lookup"><span data-stu-id="77010-113">In the absence of the NRPT, the client operates based on the DNS servers and suffixes set on the interface.</span></span>

<span data-ttu-id="77010-114">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="77010-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="77010-115">語法</span><span class="sxs-lookup"><span data-stu-id="77010-115">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="77010-116">成員</span><span class="sxs-lookup"><span data-stu-id="77010-116">Members</span></span>

<span data-ttu-id="77010-117">**MDM \_ >vpnv2 \_ DomainNameInformationList02 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="77010-117">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="77010-118">屬性</span><span class="sxs-lookup"><span data-stu-id="77010-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77010-119">屬性</span><span class="sxs-lookup"><span data-stu-id="77010-119">Properties</span></span>

<span data-ttu-id="77010-120">**MDM \_ >vpnv2 \_ DomainNameInformationList02 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="77010-120">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="77010-121">DnsServers</span><span class="sxs-lookup"><span data-stu-id="77010-121">DnsServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77010-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="77010-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77010-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="77010-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="77010-124">DomainName</span><span class="sxs-lookup"><span data-stu-id="77010-124">DomainName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77010-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="77010-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77010-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="77010-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="77010-127">DomainNameType</span><span class="sxs-lookup"><span data-stu-id="77010-127">DomainNameType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77010-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="77010-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77010-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="77010-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="77010-130">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="77010-130">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77010-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="77010-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77010-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="77010-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77010-133">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77010-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77010-134">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="77010-134">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="77010-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="77010-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77010-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="77010-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77010-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="77010-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="77010-138">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="77010-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="77010-139">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="77010-139">Describes the full path to the parent node.</span></span> <span data-ttu-id="77010-140">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="77010-140">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="77010-141">WebProxyServers</span><span class="sxs-lookup"><span data-stu-id="77010-141">WebProxyServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="77010-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="77010-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77010-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="77010-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77010-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="77010-144">Requirements</span></span>



| <span data-ttu-id="77010-145">需求</span><span class="sxs-lookup"><span data-stu-id="77010-145">Requirement</span></span> | <span data-ttu-id="77010-146">值</span><span class="sxs-lookup"><span data-stu-id="77010-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77010-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77010-147">Minimum supported client</span></span><br/> | <span data-ttu-id="77010-148">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77010-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77010-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77010-149">Minimum supported server</span></span><br/> | <span data-ttu-id="77010-150">都不支援</span><span class="sxs-lookup"><span data-stu-id="77010-150">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="77010-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="77010-151">Namespace</span></span><br/>                | <span data-ttu-id="77010-152">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="77010-152">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="77010-153">MOF</span><span class="sxs-lookup"><span data-stu-id="77010-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77010-154"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="77010-154"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="77010-155">DLL</span><span class="sxs-lookup"><span data-stu-id="77010-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77010-156"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77010-156"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77010-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77010-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77010-158">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="77010-158">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

