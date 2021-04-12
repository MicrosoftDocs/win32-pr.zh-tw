---
title: MDM_VPNv2_AppTriggerList02_App04 類別
description: MDM \_ VPNv2AppTriggerList02 \_ App04 類別描述設定為觸發 VPN 的應用程式清單。
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- MDM_VPNv2_AppTriggerList02_App04 類別
- MDM_VPNv2_AppTriggerList02_App04 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62685ea94b99e843625e87e7c653a2ff19ab737d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104166"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a><span data-ttu-id="fd5c7-105">MDM \_ >vpnv2 \_ AppTriggerList02 \_ App04 類別</span><span class="sxs-lookup"><span data-stu-id="fd5c7-105">MDM\_VPNv2\_AppTriggerList02\_App04 class</span></span>

<span data-ttu-id="fd5c7-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="fd5c7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd5c7-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="fd5c7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fd5c7-108">**MDM \_ VPNv2AppTriggerList02 \_ App04** 類別描述設定為觸發 VPN 的應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="fd5c7-108">The **MDM\_VPNv2AppTriggerList02\_App04** class describes a list of applications set to trigger the VPN.</span></span>

<span data-ttu-id="fd5c7-109">如果有任何這些應用程式啟動，而且 VPN 設定檔目前為使用中設定檔，則會觸發此 VPN 設定檔以進行連線。</span><span class="sxs-lookup"><span data-stu-id="fd5c7-109">If any of these apps are launched and the VPN profile is currently the active profile, this VPN profile will be triggered to connect.</span></span>

<span data-ttu-id="fd5c7-110">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd5c7-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd5c7-111">語法</span><span class="sxs-lookup"><span data-stu-id="fd5c7-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="fd5c7-112">成員</span><span class="sxs-lookup"><span data-stu-id="fd5c7-112">Members</span></span>

<span data-ttu-id="fd5c7-113">**MDM \_ >vpnv2 \_ AppTriggerList02 \_ App04** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fd5c7-113">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="fd5c7-114">屬性</span><span class="sxs-lookup"><span data-stu-id="fd5c7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd5c7-115">屬性</span><span class="sxs-lookup"><span data-stu-id="fd5c7-115">Properties</span></span>

<span data-ttu-id="fd5c7-116">**MDM \_ >vpnv2 \_ AppTriggerList02 \_ App04** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fd5c7-116">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fd5c7-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="fd5c7-117">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5c7-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd5c7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5c7-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd5c7-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fd5c7-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fd5c7-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5c7-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd5c7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5c7-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd5c7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5c7-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd5c7-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd5c7-124">資料列識別碼底下的應用程式節點。</span><span class="sxs-lookup"><span data-stu-id="fd5c7-124">App Node under the Row Id.</span></span>

</dd> <dt>

<span data-ttu-id="fd5c7-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fd5c7-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5c7-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd5c7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5c7-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fd5c7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd5c7-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd5c7-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd5c7-129">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="fd5c7-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="fd5c7-130">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span><span class="sxs-lookup"><span data-stu-id="fd5c7-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span></span>

</dd> <dt>

[<span data-ttu-id="fd5c7-131">型別</span><span class="sxs-lookup"><span data-stu-id="fd5c7-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd5c7-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd5c7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd5c7-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd5c7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd5c7-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd5c7-134">Requirements</span></span>



| <span data-ttu-id="fd5c7-135">需求</span><span class="sxs-lookup"><span data-stu-id="fd5c7-135">Requirement</span></span> | <span data-ttu-id="fd5c7-136">值</span><span class="sxs-lookup"><span data-stu-id="fd5c7-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5c7-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd5c7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fd5c7-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd5c7-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd5c7-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd5c7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fd5c7-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="fd5c7-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fd5c7-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="fd5c7-141">Namespace</span></span><br/>                | <span data-ttu-id="fd5c7-142">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="fd5c7-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fd5c7-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fd5c7-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd5c7-144"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd5c7-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd5c7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fd5c7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd5c7-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd5c7-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd5c7-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd5c7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd5c7-148">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="fd5c7-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

