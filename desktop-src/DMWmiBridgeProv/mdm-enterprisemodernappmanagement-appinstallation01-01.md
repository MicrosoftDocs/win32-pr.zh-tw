---
title: MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別
description: MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 類別可用來從 Windows 存放區或裝載位置安裝應用程式。
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cd3fc5478e73df5276fdc9d6a1d66c9649dd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934772"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="738af-105">MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="738af-105">MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="738af-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="738af-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="738af-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="738af-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="738af-108">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** 類別可用來從 Windows 存放區或裝載位置安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="738af-108">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class is used to install apps from the Windows Store or a hosted location.</span></span>

<span data-ttu-id="738af-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="738af-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="738af-110">語法</span><span class="sxs-lookup"><span data-stu-id="738af-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a><span data-ttu-id="738af-111">成員</span><span class="sxs-lookup"><span data-stu-id="738af-111">Members</span></span>

<span data-ttu-id="738af-112">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="738af-112">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="738af-113">方法</span><span class="sxs-lookup"><span data-stu-id="738af-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="738af-114">屬性</span><span class="sxs-lookup"><span data-stu-id="738af-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="738af-115">方法</span><span class="sxs-lookup"><span data-stu-id="738af-115">Methods</span></span>

<span data-ttu-id="738af-116">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="738af-116">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these methods.</span></span>



| <span data-ttu-id="738af-117">方法</span><span class="sxs-lookup"><span data-stu-id="738af-117">Method</span></span>                                                                                                    | <span data-ttu-id="738af-118">描述</span><span class="sxs-lookup"><span data-stu-id="738af-118">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="738af-119">**HostedInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="738af-119">**HostedInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | <span data-ttu-id="738af-120">從託管位置執行應用程式套件安裝的方法 (這可以是本機磁片磁碟機、UNC 或 HTTPs 資料來源) 。</span><span class="sxs-lookup"><span data-stu-id="738af-120">Method to perform an install of an app package from a hosted location (this can be a local drive, a UNC, or https data source).</span></span><br/> |
| [<span data-ttu-id="738af-121">**StoreInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="738af-121">**StoreInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | <span data-ttu-id="738af-122">從 Windows 市集中執行應用程式和授權安裝的方法。</span><span class="sxs-lookup"><span data-stu-id="738af-122">Method to perform an install of an app and a license from the Windows Store.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="738af-123">屬性</span><span class="sxs-lookup"><span data-stu-id="738af-123">Properties</span></span>

<span data-ttu-id="738af-124">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="738af-124">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="738af-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="738af-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="738af-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="738af-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="738af-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="738af-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="738af-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="738af-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="738af-129">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="738af-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="738af-130">此類別的字串為 "AppInstallation"。</span><span class="sxs-lookup"><span data-stu-id="738af-130">For this class, the string is "AppInstallation".</span></span>

</dd> <dt>

[<span data-ttu-id="738af-131">LastError</span><span class="sxs-lookup"><span data-stu-id="738af-131">LastError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="738af-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="738af-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="738af-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="738af-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="738af-134">LastErrorDesc</span><span class="sxs-lookup"><span data-stu-id="738af-134">LastErrorDesc</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="738af-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="738af-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="738af-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="738af-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="738af-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="738af-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="738af-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="738af-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="738af-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="738af-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="738af-140">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="738af-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="738af-141">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="738af-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="738af-142">此類別的字串為 "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span><span class="sxs-lookup"><span data-stu-id="738af-142">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span></span>

</dd> <dt>

[<span data-ttu-id="738af-143">ProgressStatus</span><span class="sxs-lookup"><span data-stu-id="738af-143">ProgressStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="738af-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="738af-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="738af-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="738af-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="738af-146">狀態</span><span class="sxs-lookup"><span data-stu-id="738af-146">Status</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="738af-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="738af-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="738af-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="738af-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="738af-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="738af-149">Requirements</span></span>



| <span data-ttu-id="738af-150">需求</span><span class="sxs-lookup"><span data-stu-id="738af-150">Requirement</span></span> | <span data-ttu-id="738af-151">值</span><span class="sxs-lookup"><span data-stu-id="738af-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="738af-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="738af-152">Minimum supported client</span></span><br/> | <span data-ttu-id="738af-153">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="738af-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="738af-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="738af-154">Minimum supported server</span></span><br/> | <span data-ttu-id="738af-155">都不支援</span><span class="sxs-lookup"><span data-stu-id="738af-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="738af-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="738af-156">Namespace</span></span><br/>                | <span data-ttu-id="738af-157">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="738af-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="738af-158">MOF</span><span class="sxs-lookup"><span data-stu-id="738af-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="738af-159"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="738af-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="738af-160">DLL</span><span class="sxs-lookup"><span data-stu-id="738af-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="738af-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="738af-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="738af-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="738af-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738af-163">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="738af-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

