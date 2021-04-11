---
title: MDM_EnterpriseModernAppManagement_AppManagement01 類別
description: MDM \_ EnterpriseModernAppManagement \_ AppManagement01 類別會啟動 Windows Update 掃描，並報告上次的掃描錯誤。
ms.assetid: f579a7c9-2e98-4e34-b45b-db8a4d553c57
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01 類別
- MDM_EnterpriseModernAppManagement_AppManagement01 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1f2a3739fe16d4a13e409d7d152645d4653336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187292"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="1e516-105">MDM \_ EnterpriseModernAppManagement \_ AppManagement01 類別</span><span class="sxs-lookup"><span data-stu-id="1e516-105">MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="1e516-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="1e516-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1e516-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="1e516-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1e516-108">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01** 類別會啟動 Windows Update 掃描，並報告上次的掃描錯誤。</span><span class="sxs-lookup"><span data-stu-id="1e516-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class starts the Windows Update scan and reports the last scan error.</span></span>

<span data-ttu-id="1e516-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1e516-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e516-110">語法</span><span class="sxs-lookup"><span data-stu-id="1e516-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01
{
  string InstanceID;
  string ParentID;
  sint32 LastScanError;
  string AppInventoryQuery;
  string AppInventoryResults;
  string RemovePackage;
};
```

## <a name="members"></a><span data-ttu-id="1e516-111">成員</span><span class="sxs-lookup"><span data-stu-id="1e516-111">Members</span></span>

<span data-ttu-id="1e516-112">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1e516-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these types of members:</span></span>

-   [<span data-ttu-id="1e516-113">方法</span><span class="sxs-lookup"><span data-stu-id="1e516-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="1e516-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1e516-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1e516-115">方法</span><span class="sxs-lookup"><span data-stu-id="1e516-115">Methods</span></span>

<span data-ttu-id="1e516-116">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1e516-116">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these methods.</span></span>



| <span data-ttu-id="1e516-117">方法</span><span class="sxs-lookup"><span data-stu-id="1e516-117">Method</span></span>                                                                                               | <span data-ttu-id="1e516-118">描述</span><span class="sxs-lookup"><span data-stu-id="1e516-118">Description</span></span>                                             |
|:-----------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="1e516-119">**RemovePackageMethod**</span><span class="sxs-lookup"><span data-stu-id="1e516-119">**RemovePackageMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-removepackagemethod.md) | <span data-ttu-id="1e516-120">移除封裝的方法。</span><span class="sxs-lookup"><span data-stu-id="1e516-120">Method for removing packages.</span></span><br/>                |
| [<span data-ttu-id="1e516-121">**UpdateScanMethod**</span><span class="sxs-lookup"><span data-stu-id="1e516-121">**UpdateScanMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-updatescanmethod.md)       | <span data-ttu-id="1e516-122">開始 Windows Update 掃描的方法。</span><span class="sxs-lookup"><span data-stu-id="1e516-122">Method for starting the Windows Update scan.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1e516-123">屬性</span><span class="sxs-lookup"><span data-stu-id="1e516-123">Properties</span></span>

<span data-ttu-id="1e516-124">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1e516-124">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1e516-125">AppInventoryQuery</span><span class="sxs-lookup"><span data-stu-id="1e516-125">AppInventoryQuery</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryquery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e516-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1e516-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e516-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1e516-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e516-128">AppInventoryResults</span><span class="sxs-lookup"><span data-stu-id="1e516-128">AppInventoryResults</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryresults)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e516-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1e516-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e516-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1e516-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e516-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e516-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e516-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1e516-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e516-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1e516-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e516-134">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e516-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e516-135">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e516-135">Identifies the name of the parent node.</span></span> <span data-ttu-id="1e516-136">此類別的字串為 "AppManagement"。</span><span class="sxs-lookup"><span data-stu-id="1e516-136">For this class, the string is "AppManagement".</span></span>

</dd> <dt>

[<span data-ttu-id="1e516-137">LastScanError</span><span class="sxs-lookup"><span data-stu-id="1e516-137">LastScanError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-lastscanerror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e516-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1e516-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e516-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1e516-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e516-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1e516-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e516-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1e516-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e516-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1e516-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e516-143">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e516-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e516-144">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1e516-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="1e516-145">此類別的字串為 "./Vendor/MSFT/EnterpriseModernAppManagement/"</span><span class="sxs-lookup"><span data-stu-id="1e516-145">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/"</span></span>

</dd> <dt>

[<span data-ttu-id="1e516-146">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="1e516-146">RemovePackage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-removepackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e516-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1e516-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e516-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1e516-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e516-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e516-149">Requirements</span></span>



| <span data-ttu-id="1e516-150">需求</span><span class="sxs-lookup"><span data-stu-id="1e516-150">Requirement</span></span> | <span data-ttu-id="1e516-151">值</span><span class="sxs-lookup"><span data-stu-id="1e516-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e516-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e516-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1e516-153">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e516-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e516-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e516-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1e516-155">都不支援</span><span class="sxs-lookup"><span data-stu-id="1e516-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1e516-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="1e516-156">Namespace</span></span><br/>                | <span data-ttu-id="1e516-157">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1e516-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1e516-158">MOF</span><span class="sxs-lookup"><span data-stu-id="1e516-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e516-159"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e516-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e516-160">DLL</span><span class="sxs-lookup"><span data-stu-id="1e516-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e516-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e516-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e516-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e516-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e516-163">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="1e516-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

