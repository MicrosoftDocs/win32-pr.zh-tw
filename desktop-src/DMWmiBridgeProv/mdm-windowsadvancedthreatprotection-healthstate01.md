---
title: MDM_WindowsAdvancedThreatProtection_HealthState01 類別
description: MDM \_ WindowsAdvancedThreatProtection \_ HealthState01 類別用來判斷 Windows Defender Advanced 威脅防護 (WDATP) 端點的健全狀況狀態。
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- MDM_WindowsAdvancedThreatProtection_HealthState01 類別
- MDM_WindowsAdvancedThreatProtection_HealthState01 類別，描述
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934765"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a><span data-ttu-id="e94ad-105">MDM \_ WindowsAdvancedThreatProtection \_ HealthState01 類別</span><span class="sxs-lookup"><span data-stu-id="e94ad-105">MDM\_WindowsAdvancedThreatProtection\_HealthState01 class</span></span>

<span data-ttu-id="e94ad-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e94ad-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e94ad-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e94ad-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e94ad-108">**MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** 類別用來判斷 Windows Defender ADVANCED 威脅防護 (WDATP) 端點的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="e94ad-108">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class is used to determine the health status of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="e94ad-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e94ad-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e94ad-110">語法</span><span class="sxs-lookup"><span data-stu-id="e94ad-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a><span data-ttu-id="e94ad-111">成員</span><span class="sxs-lookup"><span data-stu-id="e94ad-111">Members</span></span>

<span data-ttu-id="e94ad-112">**MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e94ad-112">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these types of members:</span></span>

-   [<span data-ttu-id="e94ad-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e94ad-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e94ad-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e94ad-114">Properties</span></span>

<span data-ttu-id="e94ad-115">**MDM \_ WindowsAdvancedThreatProtection \_ HealthState01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e94ad-115">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e94ad-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e94ad-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e94ad-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e94ad-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e94ad-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e94ad-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e94ad-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e94ad-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e94ad-120">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="e94ad-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="e94ad-121">此類別的字串為 "HealthState"。</span><span class="sxs-lookup"><span data-stu-id="e94ad-121">For this class, the string is "HealthState".</span></span>

</dd> <dt>

[<span data-ttu-id="e94ad-122">LastConnected</span><span class="sxs-lookup"><span data-stu-id="e94ad-122">LastConnected</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e94ad-123">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e94ad-123">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e94ad-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e94ad-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e94ad-125">OnboardingState</span><span class="sxs-lookup"><span data-stu-id="e94ad-125">OnboardingState</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e94ad-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="e94ad-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e94ad-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e94ad-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e94ad-128">OrgId</span><span class="sxs-lookup"><span data-stu-id="e94ad-128">OrgId</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e94ad-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e94ad-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e94ad-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e94ad-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e94ad-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e94ad-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e94ad-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e94ad-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e94ad-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e94ad-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e94ad-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e94ad-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e94ad-135">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e94ad-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="e94ad-136">此類別的字串為 "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span><span class="sxs-lookup"><span data-stu-id="e94ad-136">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="e94ad-137">SenseIsRunning</span><span class="sxs-lookup"><span data-stu-id="e94ad-137">SenseIsRunning</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e94ad-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e94ad-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e94ad-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e94ad-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e94ad-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="e94ad-140">Requirements</span></span>



| <span data-ttu-id="e94ad-141">需求</span><span class="sxs-lookup"><span data-stu-id="e94ad-141">Requirement</span></span> | <span data-ttu-id="e94ad-142">值</span><span class="sxs-lookup"><span data-stu-id="e94ad-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e94ad-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e94ad-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e94ad-144">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e94ad-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e94ad-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e94ad-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e94ad-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="e94ad-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="e94ad-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="e94ad-147">Namespace</span></span><br/>                | <span data-ttu-id="e94ad-148">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="e94ad-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="e94ad-149">MOF</span><span class="sxs-lookup"><span data-stu-id="e94ad-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e94ad-150"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e94ad-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="e94ad-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e94ad-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e94ad-152"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e94ad-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e94ad-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e94ad-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e94ad-154">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="e94ad-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

