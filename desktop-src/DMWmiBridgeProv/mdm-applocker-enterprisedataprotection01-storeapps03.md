---
title: MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 類別
description: MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03 類別會捕捉允許處理企業資料的 Windows 應用程式清單。 應該與/Vendor/MSFT/Policy/ConfigSource/DataProtection 中的設定一起使用。
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 類別
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 類別，描述
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240f641e542bbbe0c71fd686e2d9df3908b9bab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935053"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a><span data-ttu-id="6c39b-106">MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03 類別</span><span class="sxs-lookup"><span data-stu-id="6c39b-106">MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03 class</span></span>

<span data-ttu-id="6c39b-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="6c39b-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6c39b-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="6c39b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6c39b-109">**MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** 類別會捕捉允許處理企業資料的 Windows 應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="6c39b-109">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class captures the list of Windows apps that are allowed to handle enterprise data.</span></span> <span data-ttu-id="6c39b-110">應該與/Vendor/MSFT/Policy/ConfigSource/DataProtection 中的設定一起使用。</span><span class="sxs-lookup"><span data-stu-id="6c39b-110">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="6c39b-111">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6c39b-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c39b-112">語法</span><span class="sxs-lookup"><span data-stu-id="6c39b-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="6c39b-113">成員</span><span class="sxs-lookup"><span data-stu-id="6c39b-113">Members</span></span>

<span data-ttu-id="6c39b-114">**MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6c39b-114">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="6c39b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="6c39b-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c39b-116">屬性</span><span class="sxs-lookup"><span data-stu-id="6c39b-116">Properties</span></span>

<span data-ttu-id="6c39b-117">**MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ StoreApps03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6c39b-117">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c39b-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6c39b-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c39b-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c39b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c39b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c39b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c39b-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6c39b-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6c39b-122">定義從 Windows 市集中執行應用程式的限制。</span><span class="sxs-lookup"><span data-stu-id="6c39b-122">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="6c39b-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6c39b-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c39b-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c39b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c39b-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6c39b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c39b-126">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6c39b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6c39b-127">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="6c39b-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="6c39b-128">針對此類別，字串為 "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*群組*"</span><span class="sxs-lookup"><span data-stu-id="6c39b-128">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="6c39b-129">**原則**</span><span class="sxs-lookup"><span data-stu-id="6c39b-129">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c39b-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c39b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c39b-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6c39b-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c39b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c39b-132">Requirements</span></span>



| <span data-ttu-id="6c39b-133">需求</span><span class="sxs-lookup"><span data-stu-id="6c39b-133">Requirement</span></span> | <span data-ttu-id="6c39b-134">值</span><span class="sxs-lookup"><span data-stu-id="6c39b-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c39b-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c39b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6c39b-136">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c39b-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c39b-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c39b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6c39b-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="6c39b-138">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6c39b-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c39b-139">Namespace</span></span><br/>                | <span data-ttu-id="6c39b-140">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="6c39b-140">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="6c39b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6c39b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c39b-142"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c39b-142"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c39b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6c39b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c39b-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c39b-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c39b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c39b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c39b-146">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="6c39b-146">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

