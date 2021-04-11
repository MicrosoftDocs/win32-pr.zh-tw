---
title: MDM_PassportForWork_Policies02 類別
description: MDM \_ PassportForWork Policies02 類別會布建 \_ Windows Hello 企業版。
ms.assetid: 362fe819-a68a-4433-8b43-201d9678a8da
keywords:
- MDM_PassportForWork_Policies02 類別
- MDM_PassportForWork_Policies02 類別，描述
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Policies02
- MDM_PassportForWork_Policies02.InstanceID
- MDM_PassportForWork_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf407289f93f5ecff0e57ebf7b7fa8d9844183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934182"
---
# <a name="mdm_passportforwork_policies02-class"></a><span data-ttu-id="46f67-105">MDM \_ PassportForWork \_ Policies02 類別</span><span class="sxs-lookup"><span data-stu-id="46f67-105">MDM\_PassportForWork\_Policies02 class</span></span>

<span data-ttu-id="46f67-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="46f67-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="46f67-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="46f67-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="46f67-108">**MDM \_ PassportForWork \_ Policies02** 類別會布建 Windows Hello 企業版。</span><span class="sxs-lookup"><span data-stu-id="46f67-108">The **MDM\_PassportForWork\_Policies02** class provisions Windows Hello for Business.</span></span>

<span data-ttu-id="46f67-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="46f67-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f67-110">語法</span><span class="sxs-lookup"><span data-stu-id="46f67-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UsePassportForWork;
  boolean RequireSecurityDevice;
};
```

## <a name="members"></a><span data-ttu-id="46f67-111">成員</span><span class="sxs-lookup"><span data-stu-id="46f67-111">Members</span></span>

<span data-ttu-id="46f67-112">**MDM \_ PassportForWork \_ Policies02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="46f67-112">The **MDM\_PassportForWork\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="46f67-113">屬性</span><span class="sxs-lookup"><span data-stu-id="46f67-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46f67-114">屬性</span><span class="sxs-lookup"><span data-stu-id="46f67-114">Properties</span></span>

<span data-ttu-id="46f67-115">**MDM \_ PassportForWork \_ Policies02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="46f67-115">The **MDM\_PassportForWork\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46f67-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="46f67-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f67-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46f67-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46f67-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46f67-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46f67-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46f67-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46f67-120">Windows Hello 企業版原則的根節點。</span><span class="sxs-lookup"><span data-stu-id="46f67-120">Root node for Windows Hello for Business policies.</span></span>

</dd> <dt>

<span data-ttu-id="46f67-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="46f67-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f67-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="46f67-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46f67-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="46f67-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46f67-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46f67-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46f67-125">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="46f67-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="46f67-126">此類別的字串為 "./Vendor/MSFT/PassPortForWork/*TenantID*"</span><span class="sxs-lookup"><span data-stu-id="46f67-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*"</span></span>

</dd> <dt>

[<span data-ttu-id="46f67-127">RequireSecurityDevice</span><span class="sxs-lookup"><span data-stu-id="46f67-127">RequireSecurityDevice</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-requiresecuritydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f67-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="46f67-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46f67-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="46f67-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46f67-130">UsePassportForWork</span><span class="sxs-lookup"><span data-stu-id="46f67-130">UsePassportForWork</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-usepassportforwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f67-131">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="46f67-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46f67-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="46f67-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46f67-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="46f67-133">Requirements</span></span>



| <span data-ttu-id="46f67-134">需求</span><span class="sxs-lookup"><span data-stu-id="46f67-134">Requirement</span></span> | <span data-ttu-id="46f67-135">值</span><span class="sxs-lookup"><span data-stu-id="46f67-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f67-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46f67-136">Minimum supported client</span></span><br/> | <span data-ttu-id="46f67-137">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46f67-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46f67-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46f67-138">Minimum supported server</span></span><br/> | <span data-ttu-id="46f67-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="46f67-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="46f67-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="46f67-140">Namespace</span></span><br/>                | <span data-ttu-id="46f67-141">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="46f67-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="46f67-142">MOF</span><span class="sxs-lookup"><span data-stu-id="46f67-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46f67-143"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="46f67-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="46f67-144">DLL</span><span class="sxs-lookup"><span data-stu-id="46f67-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46f67-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46f67-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f67-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46f67-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f67-147">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="46f67-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

