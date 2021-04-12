---
title: MDM_AppLocker_Script03 類別
description: MDM \_ AppLocker \_ Script03 類別會定義處理 DLL 檔案的原則限制。
ms.assetid: 61fada02-7245-4825-945c-b41e9eff8e74
keywords:
- MDM_AppLocker_Script03 類別
- MDM_AppLocker_Script03 類別，描述
topic_type:
- apiref
api_name:
- MDM_AppLocker_Script03
- MDM_AppLocker_Script03.InstanceID
- MDM_AppLocker_Script03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402efedb1e15a0ea0df3dea654328de4ba0ddd86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025466"
---
# <a name="mdm_applocker_script03-class"></a><span data-ttu-id="38666-105">MDM \_ AppLocker \_ Script03 類別</span><span class="sxs-lookup"><span data-stu-id="38666-105">MDM\_AppLocker\_Script03 class</span></span>

<span data-ttu-id="38666-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="38666-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="38666-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="38666-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="38666-108">**MDM \_ AppLocker \_ Script03** 類別會定義處理 DLL 檔案的原則限制。</span><span class="sxs-lookup"><span data-stu-id="38666-108">The **MDM\_AppLocker\_Script03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="38666-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="38666-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38666-110">語法</span><span class="sxs-lookup"><span data-stu-id="38666-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_Script03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="38666-111">成員</span><span class="sxs-lookup"><span data-stu-id="38666-111">Members</span></span>

<span data-ttu-id="38666-112">**MDM \_ AppLocker \_ Script03** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="38666-112">The **MDM\_AppLocker\_Script03** class has these types of members:</span></span>

-   [<span data-ttu-id="38666-113">屬性</span><span class="sxs-lookup"><span data-stu-id="38666-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38666-114">屬性</span><span class="sxs-lookup"><span data-stu-id="38666-114">Properties</span></span>

<span data-ttu-id="38666-115">**MDM \_ AppLocker \_ Script03** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="38666-115">The **MDM\_AppLocker\_Script03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="38666-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="38666-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="38666-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38666-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38666-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38666-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="38666-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="38666-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38666-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38666-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38666-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="38666-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38666-122">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="38666-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="38666-123">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="38666-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="38666-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="38666-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38666-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38666-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38666-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="38666-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38666-127">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="38666-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="38666-128">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="38666-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="38666-129">此類別的字串為 "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span><span class="sxs-lookup"><span data-stu-id="38666-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="38666-130">**原則**</span><span class="sxs-lookup"><span data-stu-id="38666-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="38666-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="38666-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38666-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="38666-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38666-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="38666-133">Requirements</span></span>



| <span data-ttu-id="38666-134">需求</span><span class="sxs-lookup"><span data-stu-id="38666-134">Requirement</span></span> | <span data-ttu-id="38666-135">值</span><span class="sxs-lookup"><span data-stu-id="38666-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38666-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38666-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38666-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38666-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38666-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38666-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38666-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="38666-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="38666-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="38666-140">Namespace</span></span><br/>                | <span data-ttu-id="38666-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="38666-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="38666-142">MOF</span><span class="sxs-lookup"><span data-stu-id="38666-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38666-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="38666-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="38666-144">DLL</span><span class="sxs-lookup"><span data-stu-id="38666-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38666-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38666-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38666-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38666-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38666-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="38666-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

