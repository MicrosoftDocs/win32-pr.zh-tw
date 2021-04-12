---
title: MDM_WindowsAdvancedThreatProtection_Configuration01 類別
description: MDM \_ WindowsAdvancedThreatProtection \_ Configuration01 類別用來判斷 Windows Defender Advanced 威脅防護 (WDATP) 端點的設定。
ms.assetid: b4b2ff02-3836-4044-b8fa-d3405f433d8c
keywords:
- MDM_WindowsAdvancedThreatProtection_Configuration01 類別
- MDM_WindowsAdvancedThreatProtection_Configuration01 類別，描述
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_Configuration01
- MDM_WindowsAdvancedThreatProtection_Configuration01.InstanceID
- MDM_WindowsAdvancedThreatProtection_Configuration01.ParentID
- MDM_WindowsAdvancedThreatProtection_Configuration01.GroupIds
api_type:
- DllExport
api_location:
- Mofs\DMWmiBridgeProv.dll
ms.openlocfilehash: c6cd6689a66735790c381ac307a443c08464a379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509007"
---
# <a name="mdm_windowsadvancedthreatprotection_configuration01-class"></a><span data-ttu-id="5991e-105">MDM \_ WindowsAdvancedThreatProtection \_ Configuration01 類別</span><span class="sxs-lookup"><span data-stu-id="5991e-105">MDM\_WindowsAdvancedThreatProtection\_Configuration01 class</span></span>

<span data-ttu-id="5991e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="5991e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5991e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="5991e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5991e-108">**MDM \_ WindowsAdvancedThreatProtection \_ Configuration01** 類別用來判斷 Windows Defender ADVANCED 威脅防護 (WDATP) 端點的設定。</span><span class="sxs-lookup"><span data-stu-id="5991e-108">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class is used to determine the configuration of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="5991e-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5991e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5991e-110">語法</span><span class="sxs-lookup"><span data-stu-id="5991e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_Configuration01
{
  string InstanceID;
  string ParentID;
  sint32 SampleSharing;
  string GroupIds;
  sint32 TelemetryReportingFrequency;
};
```

## <a name="members"></a><span data-ttu-id="5991e-111">成員</span><span class="sxs-lookup"><span data-stu-id="5991e-111">Members</span></span>

<span data-ttu-id="5991e-112">**MDM \_ WindowsAdvancedThreatProtection \_ Configuration01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5991e-112">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these types of members:</span></span>

-   [<span data-ttu-id="5991e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5991e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5991e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5991e-114">Properties</span></span>

<span data-ttu-id="5991e-115">**MDM \_ WindowsAdvancedThreatProtection \_ Configuration01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5991e-115">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5991e-116">**GroupIds**</span><span class="sxs-lookup"><span data-stu-id="5991e-116">**GroupIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5991e-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5991e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5991e-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5991e-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5991e-119">TBD</span><span class="sxs-lookup"><span data-stu-id="5991e-119">TBD</span></span>

</dd> <dt>

<span data-ttu-id="5991e-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5991e-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5991e-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5991e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5991e-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5991e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5991e-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5991e-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5991e-124">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5991e-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="5991e-125">此類別的字串為 "Configuration"。</span><span class="sxs-lookup"><span data-stu-id="5991e-125">For this class, the string is "Configuration".</span></span>

</dd> <dt>

<span data-ttu-id="5991e-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5991e-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5991e-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5991e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5991e-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5991e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5991e-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5991e-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5991e-130">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5991e-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="5991e-131">此類別的字串為 "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span><span class="sxs-lookup"><span data-stu-id="5991e-131">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="5991e-132">SampleSharing</span><span class="sxs-lookup"><span data-stu-id="5991e-132">SampleSharing</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-samplesharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5991e-133">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5991e-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5991e-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5991e-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5991e-135">TelemetryReportingFrequency</span><span class="sxs-lookup"><span data-stu-id="5991e-135">TelemetryReportingFrequency</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-telemetryreportingfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5991e-136">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5991e-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5991e-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5991e-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5991e-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="5991e-138">Requirements</span></span>



| <span data-ttu-id="5991e-139">需求</span><span class="sxs-lookup"><span data-stu-id="5991e-139">Requirement</span></span> | <span data-ttu-id="5991e-140">值</span><span class="sxs-lookup"><span data-stu-id="5991e-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5991e-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5991e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5991e-142">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5991e-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5991e-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5991e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5991e-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="5991e-144">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="5991e-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="5991e-145">Namespace</span></span><br/>                | <span data-ttu-id="5991e-146">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="5991e-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="5991e-147">MOF</span><span class="sxs-lookup"><span data-stu-id="5991e-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5991e-148"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5991e-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="5991e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5991e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5991e-150"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5991e-150"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5991e-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5991e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5991e-152">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="5991e-152">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

