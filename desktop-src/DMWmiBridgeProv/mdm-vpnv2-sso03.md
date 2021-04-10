---
title: MDM_VPNv2_Sso03 類別
description: 在 \_ \_ 裝置合規性的情況下，您可以使用 MDM >vpnv2 Sso03 類別來選取與 VPN 驗證憑證不同的憑證來進行 Kerberos 驗證。
ms.assetid: 179b6b69-1319-4310-aebc-f61550af6c77
keywords:
- MDM_VPNv2_Sso03 類別
- MDM_VPNv2_Sso03 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03.InstanceID
- MDM_VPNv2_Sso03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5f3f10d365e1405981e206963cd98f0b7f803c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934768"
---
# <a name="mdm_vpnv2_sso03-class"></a><span data-ttu-id="fa8f5-105">MDM \_ >vpnv2 \_ Sso03 類別</span><span class="sxs-lookup"><span data-stu-id="fa8f5-105">MDM\_VPNv2\_Sso03 class</span></span>

<span data-ttu-id="fa8f5-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="fa8f5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fa8f5-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="fa8f5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fa8f5-108">在裝置合規性的情況下，您可以使用 **MDM \_ >vpnv2 \_ Sso03** 類別來選取與 VPN 驗證憑證不同的憑證來進行 Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="fa8f5-108">The **MDM\_VPNv2\_Sso03** class can be used to select a certificate different from the VPN Authentication certificate for the Kerberos Authentication in the case of Device Compliance.</span></span>

<span data-ttu-id="fa8f5-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8f5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8f5-110">語法</span><span class="sxs-lookup"><span data-stu-id="fa8f5-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Sso03
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
  string  IssuerHash;
  string  Eku;
};
```

## <a name="members"></a><span data-ttu-id="fa8f5-111">成員</span><span class="sxs-lookup"><span data-stu-id="fa8f5-111">Members</span></span>

<span data-ttu-id="fa8f5-112">**MDM \_ >vpnv2 \_ Sso03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fa8f5-112">The **MDM\_VPNv2\_Sso03** class has these types of members:</span></span>

-   [<span data-ttu-id="fa8f5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fa8f5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa8f5-114">屬性</span><span class="sxs-lookup"><span data-stu-id="fa8f5-114">Properties</span></span>

<span data-ttu-id="fa8f5-115">**MDM \_ >vpnv2 \_ Sso03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8f5-115">The **MDM\_VPNv2\_Sso03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fa8f5-116">Eku</span><span class="sxs-lookup"><span data-stu-id="fa8f5-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8f5-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8f5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8f5-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fa8f5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fa8f5-119">Enabled</span><span class="sxs-lookup"><span data-stu-id="fa8f5-119">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8f5-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fa8f5-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa8f5-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fa8f5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fa8f5-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fa8f5-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8f5-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8f5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8f5-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8f5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8f5-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa8f5-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa8f5-126">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa8f5-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="fa8f5-127">IssuerHash</span><span class="sxs-lookup"><span data-stu-id="fa8f5-127">IssuerHash</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-issuerhash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8f5-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8f5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8f5-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fa8f5-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fa8f5-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fa8f5-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8f5-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8f5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8f5-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8f5-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8f5-133">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa8f5-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa8f5-134">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="fa8f5-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="fa8f5-135">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span><span class="sxs-lookup"><span data-stu-id="fa8f5-135">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa8f5-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa8f5-136">Requirements</span></span>



| <span data-ttu-id="fa8f5-137">需求</span><span class="sxs-lookup"><span data-stu-id="fa8f5-137">Requirement</span></span> | <span data-ttu-id="fa8f5-138">值</span><span class="sxs-lookup"><span data-stu-id="fa8f5-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8f5-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa8f5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fa8f5-140">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa8f5-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa8f5-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa8f5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fa8f5-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="fa8f5-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fa8f5-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa8f5-143">Namespace</span></span><br/>                | <span data-ttu-id="fa8f5-144">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="fa8f5-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fa8f5-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fa8f5-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa8f5-146"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa8f5-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa8f5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fa8f5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa8f5-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa8f5-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa8f5-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa8f5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8f5-150">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="fa8f5-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

