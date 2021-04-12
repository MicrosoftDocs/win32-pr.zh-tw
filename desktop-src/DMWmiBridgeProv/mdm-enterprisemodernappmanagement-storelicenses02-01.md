---
title: MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別
description: MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 類別可用來管理 store 應用程式的授權。
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a4549ba473afaf76bea3f23ec65aacf301121a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025319"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="a0453-105">MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 類別</span><span class="sxs-lookup"><span data-stu-id="a0453-105">MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="a0453-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a0453-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a0453-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a0453-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a0453-108">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** 類別可用來管理 store 應用程式的授權。</span><span class="sxs-lookup"><span data-stu-id="a0453-108">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class is used to manage licenses for store apps.</span></span>

<span data-ttu-id="a0453-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a0453-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0453-110">語法</span><span class="sxs-lookup"><span data-stu-id="a0453-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a><span data-ttu-id="a0453-111">成員</span><span class="sxs-lookup"><span data-stu-id="a0453-111">Members</span></span>

<span data-ttu-id="a0453-112">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a0453-112">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="a0453-113">方法</span><span class="sxs-lookup"><span data-stu-id="a0453-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0453-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a0453-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0453-115">方法</span><span class="sxs-lookup"><span data-stu-id="a0453-115">Methods</span></span>

<span data-ttu-id="a0453-116">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a0453-116">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these methods.</span></span>



| <span data-ttu-id="a0453-117">方法</span><span class="sxs-lookup"><span data-stu-id="a0453-117">Method</span></span>                                                                                                              | <span data-ttu-id="a0453-118">描述</span><span class="sxs-lookup"><span data-stu-id="a0453-118">Description</span></span>                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="a0453-119">**AddLicenseMethod**</span><span class="sxs-lookup"><span data-stu-id="a0453-119">**AddLicenseMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | <span data-ttu-id="a0453-120">新增授權的方法。</span><span class="sxs-lookup"><span data-stu-id="a0453-120">Method for adding a license.</span></span><br/>                 |
| [<span data-ttu-id="a0453-121">**GetLicenseFromStoreMethod**</span><span class="sxs-lookup"><span data-stu-id="a0453-121">**GetLicenseFromStoreMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | <span data-ttu-id="a0453-122">從存放區取得授權的方法。</span><span class="sxs-lookup"><span data-stu-id="a0453-122">Method for getting a license from the store.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a0453-123">屬性</span><span class="sxs-lookup"><span data-stu-id="a0453-123">Properties</span></span>

<span data-ttu-id="a0453-124">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a0453-124">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0453-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a0453-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0453-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0453-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0453-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0453-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0453-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0453-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a0453-129">選擇性節點。</span><span class="sxs-lookup"><span data-stu-id="a0453-129">Optional node.</span></span> <span data-ttu-id="a0453-130">存放區已安裝應用程式的授權識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0453-130">License ID for a store installed app.</span></span> <span data-ttu-id="a0453-131">授權識別碼通常是應用程式的 PFN。</span><span class="sxs-lookup"><span data-stu-id="a0453-131">The license ID is generally the PFN of the app.</span></span>

<span data-ttu-id="a0453-132">支援的作業為 [新增]、[取得] 和 [刪除]。</span><span class="sxs-lookup"><span data-stu-id="a0453-132">Supported operations are Add, Get, and Delete.</span></span>

</dd> <dt>

[<span data-ttu-id="a0453-133">LicenseCategory</span><span class="sxs-lookup"><span data-stu-id="a0453-133">LicenseCategory</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0453-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0453-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0453-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0453-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0453-136">LicenseUsage</span><span class="sxs-lookup"><span data-stu-id="a0453-136">LicenseUsage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0453-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0453-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0453-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0453-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0453-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a0453-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0453-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0453-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0453-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0453-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0453-142">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0453-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a0453-143">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a0453-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="a0453-144">此類別的字串為 "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span><span class="sxs-lookup"><span data-stu-id="a0453-144">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span></span>

</dd> <dt>

[<span data-ttu-id="a0453-145">RequesterID</span><span class="sxs-lookup"><span data-stu-id="a0453-145">RequesterID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0453-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a0453-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0453-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0453-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0453-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0453-148">Requirements</span></span>



| <span data-ttu-id="a0453-149">需求</span><span class="sxs-lookup"><span data-stu-id="a0453-149">Requirement</span></span> | <span data-ttu-id="a0453-150">值</span><span class="sxs-lookup"><span data-stu-id="a0453-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0453-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0453-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a0453-152">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0453-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0453-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0453-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a0453-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="a0453-154">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a0453-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="a0453-155">Namespace</span></span><br/>                | <span data-ttu-id="a0453-156">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a0453-156">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a0453-157">MOF</span><span class="sxs-lookup"><span data-stu-id="a0453-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0453-158"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0453-158"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0453-159">DLL</span><span class="sxs-lookup"><span data-stu-id="a0453-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0453-160"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0453-160"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0453-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0453-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0453-162">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a0453-162">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

