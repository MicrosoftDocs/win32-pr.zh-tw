---
title: MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03 類別
description: MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03 類別可讓您指定允許哪些 EXE 應用程式啟動。
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03 類別
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03 類別，描述
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843420"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a><span data-ttu-id="2924e-105">MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03 類別</span><span class="sxs-lookup"><span data-stu-id="2924e-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03 class</span></span>

<span data-ttu-id="2924e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="2924e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2924e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="2924e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2924e-108">**MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** 類別可讓您指定允許哪些 EXE 應用程式啟動。</span><span class="sxs-lookup"><span data-stu-id="2924e-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class allows you to specify which EXE applications are allowed to launch.</span></span>

<span data-ttu-id="2924e-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2924e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2924e-110">語法</span><span class="sxs-lookup"><span data-stu-id="2924e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="2924e-111">成員</span><span class="sxs-lookup"><span data-stu-id="2924e-111">Members</span></span>

<span data-ttu-id="2924e-112">**MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2924e-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="2924e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2924e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2924e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="2924e-114">Properties</span></span>

<span data-ttu-id="2924e-115">**MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ EXE03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2924e-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2924e-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="2924e-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2924e-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2924e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2924e-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2924e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2924e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2924e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2924e-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2924e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2924e-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2924e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2924e-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2924e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2924e-123">定義啟動可執行應用程式的限制。</span><span class="sxs-lookup"><span data-stu-id="2924e-123">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

[<span data-ttu-id="2924e-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="2924e-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2924e-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2924e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2924e-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2924e-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2924e-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2924e-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2924e-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2924e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2924e-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2924e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2924e-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2924e-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2924e-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2924e-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="2924e-132">針對此類別，字串為 "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*群組*"</span><span class="sxs-lookup"><span data-stu-id="2924e-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="2924e-133">**原則**</span><span class="sxs-lookup"><span data-stu-id="2924e-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2924e-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2924e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2924e-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2924e-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2924e-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="2924e-136">Requirements</span></span>



| <span data-ttu-id="2924e-137">需求</span><span class="sxs-lookup"><span data-stu-id="2924e-137">Requirement</span></span> | <span data-ttu-id="2924e-138">值</span><span class="sxs-lookup"><span data-stu-id="2924e-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2924e-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2924e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2924e-140">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2924e-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2924e-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2924e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2924e-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="2924e-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2924e-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="2924e-143">Namespace</span></span><br/>                | <span data-ttu-id="2924e-144">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="2924e-144">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="2924e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="2924e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2924e-146"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="2924e-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2924e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2924e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2924e-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2924e-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2924e-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2924e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2924e-150">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="2924e-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

