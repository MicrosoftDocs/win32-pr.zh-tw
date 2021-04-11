---
title: MDM_Policy_Config01_Licensing02 類別
description: MDM \_ Policy \_ Config01 \_ Licensing02 類別代表可用的授權原則。
ms.assetid: 7ec186e9-626e-4361-88fd-665b947ca23d
keywords:
- MDM_Policy_Config01_Licensing02 類別
- MDM_Policy_Config01_Licensing02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Licensing02
- MDM_Policy_Config01_Licensing02.InstanceID
- MDM_Policy_Config01_Licensing02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d654facc7ec3ba08d1f5b0f31497545945cc73d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934358"
---
# <a name="mdm_policy_config01_licensing02-class"></a><span data-ttu-id="eb2de-105">MDM \_ 原則 \_ Config01 \_ Licensing02 類別</span><span class="sxs-lookup"><span data-stu-id="eb2de-105">MDM\_Policy\_Config01\_Licensing02 class</span></span>

<span data-ttu-id="eb2de-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="eb2de-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eb2de-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="eb2de-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eb2de-108">**MDM \_ Policy \_ Config01 \_ Licensing02** 類別代表可用的授權原則。</span><span class="sxs-lookup"><span data-stu-id="eb2de-108">The **MDM\_Policy\_Config01\_Licensing02** class represents the licensing policies available.</span></span>

<span data-ttu-id="eb2de-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb2de-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2de-110">語法</span><span class="sxs-lookup"><span data-stu-id="eb2de-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Licensing02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsEntitlementReactivation;
  sint32 DisallowKMSClientOnlineAVSValidation;
};
```

## <a name="members"></a><span data-ttu-id="eb2de-111">成員</span><span class="sxs-lookup"><span data-stu-id="eb2de-111">Members</span></span>

<span data-ttu-id="eb2de-112">**MDM \_ Policy \_ Config01 \_ Licensing02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eb2de-112">The **MDM\_Policy\_Config01\_Licensing02** class has these types of members:</span></span>

-   [<span data-ttu-id="eb2de-113">屬性</span><span class="sxs-lookup"><span data-stu-id="eb2de-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb2de-114">屬性</span><span class="sxs-lookup"><span data-stu-id="eb2de-114">Properties</span></span>

<span data-ttu-id="eb2de-115">**MDM \_ Policy \_ Config01 \_ Licensing02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eb2de-115">The **MDM\_Policy\_Config01\_Licensing02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="eb2de-116">AllowWindowsEntitlementReactivation</span><span class="sxs-lookup"><span data-stu-id="eb2de-116">AllowWindowsEntitlementReactivation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-allowwindowsentitlementreactivation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb2de-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="eb2de-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb2de-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eb2de-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="eb2de-119">DisallowKMSClientOnlineAVSValidation</span><span class="sxs-lookup"><span data-stu-id="eb2de-119">DisallowKMSClientOnlineAVSValidation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-disallowkmsclientonlineavsvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb2de-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="eb2de-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb2de-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eb2de-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eb2de-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eb2de-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb2de-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb2de-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb2de-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb2de-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb2de-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb2de-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb2de-126">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb2de-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="eb2de-127">針對此類別，字串為「授權」。</span><span class="sxs-lookup"><span data-stu-id="eb2de-127">For this class, the string is "Licensing".</span></span>

</dd> <dt>

<span data-ttu-id="eb2de-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="eb2de-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb2de-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb2de-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb2de-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb2de-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb2de-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="eb2de-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="eb2de-132">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="eb2de-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="eb2de-133">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="eb2de-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb2de-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb2de-134">Requirements</span></span>



| <span data-ttu-id="eb2de-135">需求</span><span class="sxs-lookup"><span data-stu-id="eb2de-135">Requirement</span></span> | <span data-ttu-id="eb2de-136">值</span><span class="sxs-lookup"><span data-stu-id="eb2de-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2de-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb2de-137">Minimum supported client</span></span><br/> | <span data-ttu-id="eb2de-138">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb2de-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="eb2de-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb2de-139">Minimum supported server</span></span><br/> | <span data-ttu-id="eb2de-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="eb2de-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="eb2de-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="eb2de-141">Namespace</span></span><br/>                | <span data-ttu-id="eb2de-142">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="eb2de-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="eb2de-143">MOF</span><span class="sxs-lookup"><span data-stu-id="eb2de-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb2de-144"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb2de-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="eb2de-145">DLL</span><span class="sxs-lookup"><span data-stu-id="eb2de-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb2de-146"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb2de-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

