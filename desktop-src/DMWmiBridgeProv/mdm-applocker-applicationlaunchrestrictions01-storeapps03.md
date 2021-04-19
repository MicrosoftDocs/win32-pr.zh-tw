---
title: MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03 類別
description: MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03 類別可讓您指定允許或不允許企業資料保護的 EXE 應用程式。
ms.assetid: de5ceaea-589a-4ed7-8dd6-eb9477d68e0e
keywords:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03 類別
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03 類別，描述
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c58610c10e672a6fbc1406b2d022b8ce211871
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966107"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_storeapps03-class"></a><span data-ttu-id="e4403-105">MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03 類別</span><span class="sxs-lookup"><span data-stu-id="e4403-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03 class</span></span>

<span data-ttu-id="e4403-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="e4403-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e4403-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="e4403-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e4403-108">**MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** 類別可讓您指定允許或不允許企業資料保護的 EXE 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e4403-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class allows you to specify which EXE applications are allowed or disallowed for Enterprise Data Protection.</span></span>

<span data-ttu-id="e4403-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e4403-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4403-110">語法</span><span class="sxs-lookup"><span data-stu-id="e4403-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="e4403-111">成員</span><span class="sxs-lookup"><span data-stu-id="e4403-111">Members</span></span>

<span data-ttu-id="e4403-112">**MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e4403-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="e4403-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e4403-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4403-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e4403-114">Properties</span></span>

<span data-ttu-id="e4403-115">**MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ StoreApps03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e4403-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e4403-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="e4403-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4403-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4403-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4403-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e4403-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e4403-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e4403-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4403-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4403-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4403-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4403-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4403-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e4403-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e4403-123">定義從 Windows 市集中執行應用程式的限制。</span><span class="sxs-lookup"><span data-stu-id="e4403-123">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="e4403-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e4403-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4403-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4403-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4403-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4403-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4403-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e4403-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e4403-128">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e4403-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="e4403-129">針對此類別，字串為 "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*群組*"</span><span class="sxs-lookup"><span data-stu-id="e4403-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="e4403-130">**原則**</span><span class="sxs-lookup"><span data-stu-id="e4403-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4403-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4403-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4403-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e4403-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4403-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4403-133">Requirements</span></span>



| <span data-ttu-id="e4403-134">需求</span><span class="sxs-lookup"><span data-stu-id="e4403-134">Requirement</span></span> | <span data-ttu-id="e4403-135">值</span><span class="sxs-lookup"><span data-stu-id="e4403-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4403-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4403-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e4403-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4403-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4403-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4403-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e4403-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="e4403-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e4403-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="e4403-140">Namespace</span></span><br/>                | <span data-ttu-id="e4403-141">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="e4403-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e4403-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e4403-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4403-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4403-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4403-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e4403-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4403-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4403-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4403-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4403-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4403-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="e4403-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

