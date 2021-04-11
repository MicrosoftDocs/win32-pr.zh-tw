---
title: MDM_Policy_Result01_Cellular02 類別
description: MDM \_ Policy \_ Result01 \_ Cellular02 類別代表行動電話原則。
ms.assetid: df2b2461-5e4e-4b28-87f1-5ca348409192
keywords:
- MDM_Policy_Result01_Cellular02 類別
- MDM_Policy_Result01_Cellular02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Cellular02
- MDM_Policy_Result01_Cellular02.InstanceID
- MDM_Policy_Result01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2a8b9178ecd4d69b0c313eb7fdcb826e944317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094071"
---
# <a name="mdm_policy_result01_cellular02-class"></a><span data-ttu-id="aed78-105">MDM \_ 原則 \_ Result01 \_ Cellular02 類別</span><span class="sxs-lookup"><span data-stu-id="aed78-105">MDM\_Policy\_Result01\_Cellular02 class</span></span>

<span data-ttu-id="aed78-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="aed78-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aed78-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="aed78-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aed78-108">MDM \_ Policy \_ Result01 \_ Cellular02 類別代表行動電話原則。</span><span class="sxs-lookup"><span data-stu-id="aed78-108">the MDM\_Policy\_Result01\_Cellular02 class represents the cellular policies.</span></span>

<span data-ttu-id="aed78-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aed78-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed78-110">語法</span><span class="sxs-lookup"><span data-stu-id="aed78-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Cellular02
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

## <a name="members"></a><span data-ttu-id="aed78-111">成員</span><span class="sxs-lookup"><span data-stu-id="aed78-111">Members</span></span>

<span data-ttu-id="aed78-112">**MDM \_ Policy \_ Result01 \_ Cellular02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aed78-112">The **MDM\_Policy\_Result01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="aed78-113">屬性</span><span class="sxs-lookup"><span data-stu-id="aed78-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aed78-114">屬性</span><span class="sxs-lookup"><span data-stu-id="aed78-114">Properties</span></span>

<span data-ttu-id="aed78-115">**MDM \_ Policy \_ Result01 \_ Cellular02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aed78-115">The **MDM\_Policy\_Result01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aed78-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aed78-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aed78-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aed78-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aed78-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aed78-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aed78-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aed78-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aed78-120">LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="aed78-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aed78-121">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="aed78-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="aed78-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aed78-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aed78-123">LetAppsAccessCellularData \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="aed78-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aed78-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aed78-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aed78-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aed78-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aed78-126">LetAppsAccessCellularData \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="aed78-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aed78-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aed78-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aed78-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aed78-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aed78-129">LetAppsAccessCellularData \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="aed78-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aed78-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aed78-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aed78-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aed78-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aed78-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="aed78-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aed78-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aed78-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aed78-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aed78-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aed78-135">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aed78-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aed78-136">ShowAppCellularAccessUI</span><span class="sxs-lookup"><span data-stu-id="aed78-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aed78-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aed78-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aed78-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aed78-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aed78-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="aed78-139">Requirements</span></span>



| <span data-ttu-id="aed78-140">需求</span><span class="sxs-lookup"><span data-stu-id="aed78-140">Requirement</span></span> | <span data-ttu-id="aed78-141">值</span><span class="sxs-lookup"><span data-stu-id="aed78-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aed78-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aed78-142">Minimum supported client</span></span><br/> | <span data-ttu-id="aed78-143">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aed78-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aed78-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aed78-144">Minimum supported server</span></span><br/> | <span data-ttu-id="aed78-145">都不支援</span><span class="sxs-lookup"><span data-stu-id="aed78-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="aed78-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="aed78-146">Namespace</span></span><br/>                | <span data-ttu-id="aed78-147">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="aed78-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="aed78-148">MOF</span><span class="sxs-lookup"><span data-stu-id="aed78-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aed78-149"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="aed78-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aed78-150">DLL</span><span class="sxs-lookup"><span data-stu-id="aed78-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aed78-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aed78-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

