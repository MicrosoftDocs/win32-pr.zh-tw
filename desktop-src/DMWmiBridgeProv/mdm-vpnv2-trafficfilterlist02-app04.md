---
title: MDM_VPNv2_TrafficFilterList02_App04 類別
description: MDM \_ TrafficFilterList02 \_ App04 類別可讓您設定透過 VPN 介面允許的應用程式。
ms.assetid: a56d004b-8fe3-4187-8aad-962f1cab8f7f
keywords:
- MDM_VPNv2_TrafficFilterList02_App04 類別
- MDM_VPNv2_TrafficFilterList02_App04 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_App04
- MDM_VPNv2_TrafficFilterList02_App04.InstanceID
- MDM_VPNv2_TrafficFilterList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b1cd3edbfec5fa270f8404983af57dba4fad31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104952"
---
# <a name="mdm_vpnv2_trafficfilterlist02_app04-class"></a><span data-ttu-id="80b31-105">MDM \_ >vpnv2 \_ TrafficFilterList02 \_ App04 類別</span><span class="sxs-lookup"><span data-stu-id="80b31-105">MDM\_VPNv2\_TrafficFilterList02\_App04 class</span></span>

<span data-ttu-id="80b31-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="80b31-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="80b31-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="80b31-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="80b31-108">**MDM \_ TrafficFilterList02 \_ App04** 類別可讓您設定透過 VPN 介面允許的應用程式。</span><span class="sxs-lookup"><span data-stu-id="80b31-108">The **MDM\_TrafficFilterList02\_App04** class provides configuration of the apps that are allowed over the VPN interface.</span></span>

<span data-ttu-id="80b31-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="80b31-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b31-110">語法</span><span class="sxs-lookup"><span data-stu-id="80b31-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="80b31-111">成員</span><span class="sxs-lookup"><span data-stu-id="80b31-111">Members</span></span>

<span data-ttu-id="80b31-112">**MDM \_ >vpnv2 \_ TrafficFilterList02 \_ App04** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="80b31-112">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="80b31-113">屬性</span><span class="sxs-lookup"><span data-stu-id="80b31-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80b31-114">屬性</span><span class="sxs-lookup"><span data-stu-id="80b31-114">Properties</span></span>

<span data-ttu-id="80b31-115">**MDM \_ >vpnv2 \_ TrafficFilterList02 \_ App04** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="80b31-115">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="80b31-116">識別碼</span><span class="sxs-lookup"><span data-stu-id="80b31-116">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80b31-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="80b31-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80b31-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="80b31-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="80b31-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="80b31-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80b31-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="80b31-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80b31-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80b31-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80b31-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80b31-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80b31-123">每個應用程式 VPN 規則。</span><span class="sxs-lookup"><span data-stu-id="80b31-123">Per app VPN rule.</span></span> <span data-ttu-id="80b31-124">這會只允許透過 VPN 介面允許指定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="80b31-124">This will allow only the apps specified to be allowed over the VPN interface.</span></span> <span data-ttu-id="80b31-125">針對此類別，字串為 "App"</span><span class="sxs-lookup"><span data-stu-id="80b31-125">For this class, the string is "App"</span></span>

</dd> <dt>

<span data-ttu-id="80b31-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="80b31-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80b31-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="80b31-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80b31-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80b31-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80b31-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80b31-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80b31-130">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="80b31-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="80b31-131">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span><span class="sxs-lookup"><span data-stu-id="80b31-131">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span></span>

</dd> <dt>

[<span data-ttu-id="80b31-132">型別</span><span class="sxs-lookup"><span data-stu-id="80b31-132">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80b31-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="80b31-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80b31-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="80b31-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80b31-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="80b31-135">Requirements</span></span>



| <span data-ttu-id="80b31-136">需求</span><span class="sxs-lookup"><span data-stu-id="80b31-136">Requirement</span></span> | <span data-ttu-id="80b31-137">值</span><span class="sxs-lookup"><span data-stu-id="80b31-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b31-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80b31-138">Minimum supported client</span></span><br/> | <span data-ttu-id="80b31-139">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80b31-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80b31-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80b31-140">Minimum supported server</span></span><br/> | <span data-ttu-id="80b31-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="80b31-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="80b31-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="80b31-142">Namespace</span></span><br/>                | <span data-ttu-id="80b31-143">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="80b31-143">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="80b31-144">MOF</span><span class="sxs-lookup"><span data-stu-id="80b31-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80b31-145"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="80b31-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="80b31-146">DLL</span><span class="sxs-lookup"><span data-stu-id="80b31-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80b31-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80b31-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b31-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80b31-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b31-149">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="80b31-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

