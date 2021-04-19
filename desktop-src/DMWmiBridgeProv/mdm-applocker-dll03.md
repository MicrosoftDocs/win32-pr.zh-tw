---
title: MDM_AppLocker_DLL03 類別
description: MDM \_ AppLocker \_ DLL03 類別會定義處理 DLL 檔案的原則限制。
ms.assetid: 956b2ec0-f8a8-41d1-a571-01e73c4cebf9
keywords:
- MDM_AppLocker_DLL03 類別
- MDM_AppLocker_DLL03 類別，描述
topic_type:
- apiref
api_name:
- MDM_AppLocker_DLL03
- MDM_AppLocker_DLL03.InstanceID
- MDM_AppLocker_DLL03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c332a7d606b21ed9641c3c25f10a011cf7bea6e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969213"
---
# <a name="mdm_applocker_dll03-class"></a><span data-ttu-id="78e87-105">MDM \_ AppLocker \_ DLL03 類別</span><span class="sxs-lookup"><span data-stu-id="78e87-105">MDM\_AppLocker\_DLL03 class</span></span>

<span data-ttu-id="78e87-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="78e87-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="78e87-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="78e87-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="78e87-108">**MDM \_ AppLocker \_ DLL03** 類別會定義處理 DLL 檔案的原則限制。</span><span class="sxs-lookup"><span data-stu-id="78e87-108">The **MDM\_AppLocker\_DLL03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="78e87-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="78e87-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e87-110">語法</span><span class="sxs-lookup"><span data-stu-id="78e87-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_DLL03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="78e87-111">成員</span><span class="sxs-lookup"><span data-stu-id="78e87-111">Members</span></span>

<span data-ttu-id="78e87-112">**MDM \_ AppLocker \_ DLL03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="78e87-112">The **MDM\_AppLocker\_DLL03** class has these types of members:</span></span>

-   [<span data-ttu-id="78e87-113">屬性</span><span class="sxs-lookup"><span data-stu-id="78e87-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78e87-114">屬性</span><span class="sxs-lookup"><span data-stu-id="78e87-114">Properties</span></span>

<span data-ttu-id="78e87-115">**MDM \_ AppLocker \_ DLL03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="78e87-115">The **MDM\_AppLocker\_DLL03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="78e87-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="78e87-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78e87-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78e87-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78e87-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="78e87-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78e87-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="78e87-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78e87-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78e87-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78e87-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78e87-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78e87-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="78e87-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="78e87-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="78e87-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="78e87-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="78e87-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78e87-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78e87-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78e87-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="78e87-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78e87-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="78e87-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78e87-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78e87-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78e87-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78e87-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78e87-130">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="78e87-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="78e87-131">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="78e87-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="78e87-132">此類別的字串為 "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="78e87-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="78e87-133">**原則**</span><span class="sxs-lookup"><span data-stu-id="78e87-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="78e87-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78e87-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78e87-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="78e87-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78e87-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="78e87-136">Requirements</span></span>



| <span data-ttu-id="78e87-137">需求</span><span class="sxs-lookup"><span data-stu-id="78e87-137">Requirement</span></span> | <span data-ttu-id="78e87-138">值</span><span class="sxs-lookup"><span data-stu-id="78e87-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e87-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78e87-139">Minimum supported client</span></span><br/> | <span data-ttu-id="78e87-140">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78e87-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78e87-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78e87-141">Minimum supported server</span></span><br/> | <span data-ttu-id="78e87-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="78e87-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="78e87-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="78e87-143">Namespace</span></span><br/>                | <span data-ttu-id="78e87-144">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="78e87-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="78e87-145">MOF</span><span class="sxs-lookup"><span data-stu-id="78e87-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78e87-146"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="78e87-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="78e87-147">DLL</span><span class="sxs-lookup"><span data-stu-id="78e87-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78e87-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78e87-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78e87-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78e87-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e87-150">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="78e87-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

