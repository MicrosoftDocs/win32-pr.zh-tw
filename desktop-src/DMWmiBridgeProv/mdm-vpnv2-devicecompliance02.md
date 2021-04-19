---
title: MDM_VPNv2_DeviceCompliance02 類別
description: 保留供日後使用。 |MDM_VPNv2_DeviceCompliance02 類別
ms.assetid: f84f4812-3083-46c4-a60c-919ec92c844f
keywords:
- MDM_VPNv2_DeviceCompliance02 類別
- MDM_VPNv2_DeviceCompliance02 類別，描述
topic_type:
- apiref
api_name:
- MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02.InstanceID
- MDM_VPNv2_DeviceCompliance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a454a5cce3a40066c7cf14a60bdeeb81dcabab9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993846"
---
# <a name="mdm_vpnv2_devicecompliance02-class"></a><span data-ttu-id="19edc-106">MDM \_ >vpnv2 \_ DeviceCompliance02 類別</span><span class="sxs-lookup"><span data-stu-id="19edc-106">MDM\_VPNv2\_DeviceCompliance02 class</span></span>

<span data-ttu-id="19edc-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="19edc-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="19edc-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="19edc-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="19edc-109">保留供日後使用</span><span class="sxs-lookup"><span data-stu-id="19edc-109">Reserved for Future Use</span></span>

<span data-ttu-id="19edc-110">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="19edc-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19edc-111">語法</span><span class="sxs-lookup"><span data-stu-id="19edc-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DeviceCompliance02
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
};
```

## <a name="members"></a><span data-ttu-id="19edc-112">成員</span><span class="sxs-lookup"><span data-stu-id="19edc-112">Members</span></span>

<span data-ttu-id="19edc-113">**MDM \_ >vpnv2 \_ DeviceCompliance02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="19edc-113">The **MDM\_VPNv2\_DeviceCompliance02** class has these types of members:</span></span>

-   [<span data-ttu-id="19edc-114">屬性</span><span class="sxs-lookup"><span data-stu-id="19edc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19edc-115">屬性</span><span class="sxs-lookup"><span data-stu-id="19edc-115">Properties</span></span>

<span data-ttu-id="19edc-116">**MDM \_ >vpnv2 \_ DeviceCompliance02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="19edc-116">The **MDM\_VPNv2\_DeviceCompliance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="19edc-117">Enabled</span><span class="sxs-lookup"><span data-stu-id="19edc-117">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="19edc-118">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="19edc-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="19edc-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19edc-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="19edc-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="19edc-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19edc-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19edc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19edc-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19edc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19edc-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19edc-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19edc-124">在 Windows 10 1607 版中新增。</span><span class="sxs-lookup"><span data-stu-id="19edc-124">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="19edc-125">DeviceCompliance 下的節點可以用來啟用 VPN 的 AAD 型條件式存取。</span><span class="sxs-lookup"><span data-stu-id="19edc-125">Nodes under DeviceCompliance can be used to enable AAD-based Conditional Access for VPN.</span></span>

</dd> <dt>

<span data-ttu-id="19edc-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="19edc-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19edc-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19edc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19edc-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="19edc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19edc-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="19edc-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="19edc-130">在 Windows 10 1607 版中新增。</span><span class="sxs-lookup"><span data-stu-id="19edc-130">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="19edc-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="19edc-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="19edc-132">針對此類別，字串為 "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="19edc-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19edc-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="19edc-133">Requirements</span></span>



| <span data-ttu-id="19edc-134">需求</span><span class="sxs-lookup"><span data-stu-id="19edc-134">Requirement</span></span> | <span data-ttu-id="19edc-135">值</span><span class="sxs-lookup"><span data-stu-id="19edc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19edc-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19edc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="19edc-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19edc-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19edc-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19edc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="19edc-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="19edc-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="19edc-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="19edc-140">Namespace</span></span><br/>                | <span data-ttu-id="19edc-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="19edc-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="19edc-142">MOF</span><span class="sxs-lookup"><span data-stu-id="19edc-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19edc-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="19edc-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="19edc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="19edc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19edc-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19edc-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19edc-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19edc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19edc-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="19edc-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

