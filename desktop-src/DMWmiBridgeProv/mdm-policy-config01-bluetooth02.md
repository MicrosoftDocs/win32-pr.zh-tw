---
title: MDM_Policy_Config01_Bluetooth02 類別
description: MDM \_ Policy \_ Config01 \_ Bluetooth02 類別代表可用的藍牙管理原則。
ms.assetid: 8544c8df-a57b-4e21-87ee-f819aeddc071
keywords:
- MDM_Policy_Config01_Bluetooth02 類別
- MDM_Policy_Config01_Bluetooth02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Bluetooth02
- MDM_Policy_Config01_Bluetooth02.InstanceID
- MDM_Policy_Config01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceeea1cd099fa00d6138a0ff1d37123725f0be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094267"
---
# <a name="mdm_policy_config01_bluetooth02-class"></a><span data-ttu-id="7b72e-105">MDM \_ 原則 \_ Config01 \_ Bluetooth02 類別</span><span class="sxs-lookup"><span data-stu-id="7b72e-105">MDM\_Policy\_Config01\_Bluetooth02 class</span></span>

<span data-ttu-id="7b72e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="7b72e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7b72e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="7b72e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7b72e-108">**MDM \_ Policy \_ Config01 \_ Bluetooth02** 類別代表可用的藍牙管理原則。</span><span class="sxs-lookup"><span data-stu-id="7b72e-108">The **MDM\_Policy\_Config01\_Bluetooth02** class represents the Bluetooth management policies available.</span></span>

<span data-ttu-id="7b72e-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b72e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b72e-110">語法</span><span class="sxs-lookup"><span data-stu-id="7b72e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Bluetooth02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiscoverableMode;
  string LocalDeviceName;
  sint32 AllowAdvertising;
  string ServicesAllowedList;
  sint32 AllowPrepairing;
};
```

## <a name="members"></a><span data-ttu-id="7b72e-111">成員</span><span class="sxs-lookup"><span data-stu-id="7b72e-111">Members</span></span>

<span data-ttu-id="7b72e-112">**MDM \_ Policy \_ Config01 \_ Bluetooth02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7b72e-112">The **MDM\_Policy\_Config01\_Bluetooth02** class has these types of members:</span></span>

-   [<span data-ttu-id="7b72e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7b72e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b72e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7b72e-114">Properties</span></span>

<span data-ttu-id="7b72e-115">**MDM \_ Policy \_ Config01 \_ Bluetooth02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7b72e-115">The **MDM\_Policy\_Config01\_Bluetooth02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7b72e-116">AllowAdvertising</span><span class="sxs-lookup"><span data-stu-id="7b72e-116">AllowAdvertising</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b72e-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7b72e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b72e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7b72e-119">AllowDiscoverableMode</span><span class="sxs-lookup"><span data-stu-id="7b72e-119">AllowDiscoverableMode</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b72e-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7b72e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b72e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7b72e-122">AllowPrepairing</span><span class="sxs-lookup"><span data-stu-id="7b72e-122">AllowPrepairing</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b72e-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="7b72e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b72e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b72e-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7b72e-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b72e-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b72e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b72e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b72e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b72e-129">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b72e-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="7b72e-130">此類別的字串為 "Bluetooth"。</span><span class="sxs-lookup"><span data-stu-id="7b72e-130">For this class, the string is "Bluetooth".</span></span>

</dd> <dt>

[<span data-ttu-id="7b72e-131">LocalDeviceName</span><span class="sxs-lookup"><span data-stu-id="7b72e-131">LocalDeviceName</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b72e-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b72e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b72e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b72e-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7b72e-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b72e-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b72e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7b72e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-137">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b72e-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b72e-138">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="7b72e-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="7b72e-139">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="7b72e-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="7b72e-140">ServicesAllowedList</span><span class="sxs-lookup"><span data-stu-id="7b72e-140">ServicesAllowedList</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b72e-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7b72e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b72e-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7b72e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b72e-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b72e-143">Requirements</span></span>



| <span data-ttu-id="7b72e-144">需求</span><span class="sxs-lookup"><span data-stu-id="7b72e-144">Requirement</span></span> | <span data-ttu-id="7b72e-145">值</span><span class="sxs-lookup"><span data-stu-id="7b72e-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b72e-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b72e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7b72e-147">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b72e-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b72e-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b72e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7b72e-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="7b72e-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7b72e-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="7b72e-150">Namespace</span></span><br/>                | <span data-ttu-id="7b72e-151">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="7b72e-151">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="7b72e-152">MOF</span><span class="sxs-lookup"><span data-stu-id="7b72e-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b72e-153"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b72e-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b72e-154">DLL</span><span class="sxs-lookup"><span data-stu-id="7b72e-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b72e-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b72e-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b72e-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b72e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b72e-157">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="7b72e-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

