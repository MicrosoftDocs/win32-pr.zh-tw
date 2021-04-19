---
title: MDM_WindowsAdvancedThreatProtection 類別
description: MDM \_ WindowsAdvancedThreatProtection 類別是用來上架及下架 Windows Defender Advanced 威脅防護 (WDATP) 的端點。
ms.assetid: 7a95253e-6d13-4c1b-b78d-c56c6378f7c3
keywords:
- MDM_WindowsAdvancedThreatProtection 類別
- MDM_WindowsAdvancedThreatProtection 類別，描述
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection.InstanceID
- MDM_WindowsAdvancedThreatProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369406a3c8bcf982aeb18b4bbb53c1af4983e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969995"
---
# <a name="mdm_windowsadvancedthreatprotection-class"></a><span data-ttu-id="a22bd-105">MDM \_ WindowsAdvancedThreatProtection 類別</span><span class="sxs-lookup"><span data-stu-id="a22bd-105">MDM\_WindowsAdvancedThreatProtection class</span></span>

<span data-ttu-id="a22bd-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a22bd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a22bd-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a22bd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a22bd-108">**MDM \_ WindowsAdvancedThreatProtection** 類別是用來上架及下架 Windows Defender Advanced 威脅防護 (WDATP) 的端點。</span><span class="sxs-lookup"><span data-stu-id="a22bd-108">The **MDM\_WindowsAdvancedThreatProtection** class is used to onboard and offboard endpoints for Windows Defender Advanced Threat Protection (WDATP).</span></span>

<span data-ttu-id="a22bd-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a22bd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22bd-110">語法</span><span class="sxs-lookup"><span data-stu-id="a22bd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection
{
  string InstanceID;
  string ParentID;
  string Onboarding;
  string Offboarding;
};
```

## <a name="members"></a><span data-ttu-id="a22bd-111">成員</span><span class="sxs-lookup"><span data-stu-id="a22bd-111">Members</span></span>

<span data-ttu-id="a22bd-112">**MDM \_ WindowsAdvancedThreatProtection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a22bd-112">The **MDM\_WindowsAdvancedThreatProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="a22bd-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a22bd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a22bd-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a22bd-114">Properties</span></span>

<span data-ttu-id="a22bd-115">**MDM \_ WindowsAdvancedThreatProtection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a22bd-115">The **MDM\_WindowsAdvancedThreatProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a22bd-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a22bd-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22bd-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a22bd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22bd-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a22bd-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22bd-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a22bd-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a22bd-120">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a22bd-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="a22bd-121">此類別的字串為 "WindowsAdvancedThreatProtection"。</span><span class="sxs-lookup"><span data-stu-id="a22bd-121">For this class, the string is "WindowsAdvancedThreatProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="a22bd-122">下線</span><span class="sxs-lookup"><span data-stu-id="a22bd-122">Offboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#offboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22bd-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a22bd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22bd-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a22bd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a22bd-125">入門訓練</span><span class="sxs-lookup"><span data-stu-id="a22bd-125">Onboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22bd-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a22bd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22bd-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a22bd-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a22bd-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a22bd-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22bd-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a22bd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a22bd-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a22bd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22bd-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a22bd-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a22bd-132">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a22bd-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="a22bd-133">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="a22bd-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a22bd-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="a22bd-134">Requirements</span></span>



| <span data-ttu-id="a22bd-135">需求</span><span class="sxs-lookup"><span data-stu-id="a22bd-135">Requirement</span></span> | <span data-ttu-id="a22bd-136">值</span><span class="sxs-lookup"><span data-stu-id="a22bd-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a22bd-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a22bd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a22bd-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a22bd-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a22bd-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a22bd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a22bd-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="a22bd-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a22bd-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="a22bd-141">Namespace</span></span><br/>                | <span data-ttu-id="a22bd-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a22bd-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="a22bd-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a22bd-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a22bd-144"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a22bd-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="a22bd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a22bd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22bd-146"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22bd-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22bd-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a22bd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22bd-148">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a22bd-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

