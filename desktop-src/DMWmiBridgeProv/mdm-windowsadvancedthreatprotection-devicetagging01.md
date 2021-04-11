---
title: MDM_WindowsAdvancedThreatProtection_DeviceTagging01 類別
description: MDM \_ WindowsAdvancedThreatProtection \_ DeviceTagging01 類別用來上架、判斷設定和健康狀態，以及下架 Windows Defender Advanced 威脅防護的端點。
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01 類別
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01 類別，描述
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104945"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a><span data-ttu-id="c13f1-105">MDM \_ WindowsAdvancedThreatProtection \_ DeviceTagging01 類別</span><span class="sxs-lookup"><span data-stu-id="c13f1-105">MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class</span></span>

<span data-ttu-id="c13f1-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="c13f1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c13f1-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="c13f1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c13f1-108">MDM \_ WindowsAdvancedThreatProtection \_ DeviceTagging01 類別用來上架、判斷設定和健康狀態，以及下架 Windows Defender Advanced 威脅防護的端點。</span><span class="sxs-lookup"><span data-stu-id="c13f1-108">The MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class is used to onboard, determine configuration and health status, and offboard endpoints for Windows Defender Advanced Threat Protection.</span></span>

<span data-ttu-id="c13f1-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c13f1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c13f1-110">語法</span><span class="sxs-lookup"><span data-stu-id="c13f1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a><span data-ttu-id="c13f1-111">成員</span><span class="sxs-lookup"><span data-stu-id="c13f1-111">Members</span></span>

<span data-ttu-id="c13f1-112">**MDM \_ WindowsAdvancedThreatProtection \_ DeviceTagging01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c13f1-112">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these types of members:</span></span>

-   [<span data-ttu-id="c13f1-113">屬性</span><span class="sxs-lookup"><span data-stu-id="c13f1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c13f1-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c13f1-114">Properties</span></span>

<span data-ttu-id="c13f1-115">**MDM \_ WindowsAdvancedThreatProtection \_ DeviceTagging01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c13f1-115">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c13f1-116">重要性</span><span class="sxs-lookup"><span data-stu-id="c13f1-116">Criticality</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13f1-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c13f1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c13f1-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c13f1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c13f1-119">群組</span><span class="sxs-lookup"><span data-stu-id="c13f1-119">Group</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13f1-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c13f1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c13f1-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c13f1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c13f1-122">**IdMethod**</span><span class="sxs-lookup"><span data-stu-id="c13f1-122">**IdMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13f1-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="c13f1-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c13f1-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c13f1-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c13f1-125">TBD</span><span class="sxs-lookup"><span data-stu-id="c13f1-125">TBD</span></span>

</dd> <dt>

<span data-ttu-id="c13f1-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c13f1-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13f1-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c13f1-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c13f1-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c13f1-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c13f1-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c13f1-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c13f1-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c13f1-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c13f1-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c13f1-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c13f1-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c13f1-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c13f1-133">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c13f1-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c13f1-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="c13f1-134">Requirements</span></span>



| <span data-ttu-id="c13f1-135">需求</span><span class="sxs-lookup"><span data-stu-id="c13f1-135">Requirement</span></span> | <span data-ttu-id="c13f1-136">值</span><span class="sxs-lookup"><span data-stu-id="c13f1-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c13f1-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c13f1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c13f1-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c13f1-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c13f1-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c13f1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c13f1-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="c13f1-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="c13f1-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="c13f1-141">Namespace</span></span><br/>                | <span data-ttu-id="c13f1-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c13f1-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="c13f1-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c13f1-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c13f1-144"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c13f1-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="c13f1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c13f1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c13f1-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c13f1-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

