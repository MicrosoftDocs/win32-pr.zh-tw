---
title: MDM_Policy_Config01_Cellular02 類別
description: MDM \_ Policy \_ Config01 Cellular02 類別會設定 \_ 行動電話原則。
ms.assetid: e5926a21-a375-4d1c-8b37-7fe7f7532c50
keywords:
- MDM_Policy_Config01_Cellular02 類別
- MDM_Policy_Config01_Cellular02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cellular02
- MDM_Policy_Config01_Cellular02.InstanceID
- MDM_Policy_Config01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1b6d9163723299b144368d9d2b73a12ccc7a91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094264"
---
# <a name="mdm_policy_config01_cellular02-class"></a><span data-ttu-id="bd8f0-105">MDM \_ 原則 \_ Config01 \_ Cellular02 類別</span><span class="sxs-lookup"><span data-stu-id="bd8f0-105">MDM\_Policy\_Config01\_Cellular02 class</span></span>

<span data-ttu-id="bd8f0-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="bd8f0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bd8f0-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="bd8f0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bd8f0-108">MDM \_ Policy \_ Config01 Cellular02 類別會設定 \_ 行動電話原則。</span><span class="sxs-lookup"><span data-stu-id="bd8f0-108">The MDM\_Policy\_Config01\_Cellular02 class configures the cellular policies.</span></span>

<span data-ttu-id="bd8f0-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd8f0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd8f0-110">語法</span><span class="sxs-lookup"><span data-stu-id="bd8f0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cellular02
{
  string InstanceID;
  string ParentID;
  string LetAppsAccessCellularData_UserInControlOfTheseApps;
  string LetAppsAccessCellularData_ForceDenyTheseApps;
  string LetAppsAccessCellularData_ForceAllowTheseApps;
  sint32 LetAppsAccessCellularData;
  string ShowAppCellularAccessUI;
};
```

## <a name="members"></a><span data-ttu-id="bd8f0-111">成員</span><span class="sxs-lookup"><span data-stu-id="bd8f0-111">Members</span></span>

<span data-ttu-id="bd8f0-112">**MDM \_ Policy \_ Config01 \_ Cellular02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bd8f0-112">The **MDM\_Policy\_Config01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="bd8f0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bd8f0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd8f0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="bd8f0-114">Properties</span></span>

<span data-ttu-id="bd8f0-115">**MDM \_ Policy \_ Config01 \_ Cellular02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bd8f0-115">The **MDM\_Policy\_Config01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd8f0-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd8f0-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd8f0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bd8f0-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bd8f0-120">LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="bd8f0-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd8f0-121">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bd8f0-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bd8f0-123">LetAppsAccessCellularData \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="bd8f0-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd8f0-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bd8f0-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bd8f0-126">LetAppsAccessCellularData \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="bd8f0-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd8f0-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bd8f0-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bd8f0-129">LetAppsAccessCellularData \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="bd8f0-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd8f0-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bd8f0-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bd8f0-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd8f0-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="bd8f0-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-135">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bd8f0-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bd8f0-136">ShowAppCellularAccessUI</span><span class="sxs-lookup"><span data-stu-id="bd8f0-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd8f0-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bd8f0-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd8f0-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bd8f0-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd8f0-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd8f0-139">Requirements</span></span>



| <span data-ttu-id="bd8f0-140">需求</span><span class="sxs-lookup"><span data-stu-id="bd8f0-140">Requirement</span></span> | <span data-ttu-id="bd8f0-141">值</span><span class="sxs-lookup"><span data-stu-id="bd8f0-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd8f0-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd8f0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="bd8f0-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd8f0-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd8f0-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd8f0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="bd8f0-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="bd8f0-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bd8f0-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="bd8f0-146">Namespace</span></span><br/>                | <span data-ttu-id="bd8f0-147">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bd8f0-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bd8f0-148">MOF</span><span class="sxs-lookup"><span data-stu-id="bd8f0-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd8f0-149"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f0-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd8f0-150">DLL</span><span class="sxs-lookup"><span data-stu-id="bd8f0-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd8f0-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f0-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

