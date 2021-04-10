---
title: Win32_TSGatewayServer 類別的 Import 方法
description: 將指定的設定匯入遠端桌面閘道 (RD 閘道) server。
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- 匯入方法遠端桌面服務
- 匯入方法遠端桌面服務，Win32_TSGatewayServer 類別
- Win32_TSGatewayServer 類別遠端桌面服務，匯入方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934586"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="93e5f-106">Win32 TSGatewayServer 類別的 Import 方法 \_</span><span class="sxs-lookup"><span data-stu-id="93e5f-106">Import method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="93e5f-107">將指定的設定匯入遠端桌面閘道 (RD 閘道) server。</span><span class="sxs-lookup"><span data-stu-id="93e5f-107">Imports a given configuration to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e5f-108">語法</span><span class="sxs-lookup"><span data-stu-id="93e5f-108">Syntax</span></span>


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a><span data-ttu-id="93e5f-109">參數</span><span class="sxs-lookup"><span data-stu-id="93e5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e5f-110">*ImportType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93e5f-110">*ImportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e5f-111">要匯入的內容。</span><span class="sxs-lookup"><span data-stu-id="93e5f-111">The content to import.</span></span> <span data-ttu-id="93e5f-112">在 *ImportType* 參數中設定對應的位，以設定匯入類型。</span><span class="sxs-lookup"><span data-stu-id="93e5f-112">Set the import type by setting the corresponding bits in the *ImportType* parameter.</span></span> <span data-ttu-id="93e5f-113">您可以設定多個匯入類型。</span><span class="sxs-lookup"><span data-stu-id="93e5f-113">You can set multiple import types.</span></span> <span data-ttu-id="93e5f-114">例如，如果設定0位，將會匯入遠端桌面服務的連線授權原則 (RD Cap) 。</span><span class="sxs-lookup"><span data-stu-id="93e5f-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be imported.</span></span> <span data-ttu-id="93e5f-115">如果設定0和第2位，則會匯入 RD Cap 和遠端桌面服務資源授權原則 (RD Rap) 。</span><span class="sxs-lookup"><span data-stu-id="93e5f-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be imported.</span></span>

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span data-ttu-id="93e5f-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>匯 **入所有 CAPs** (1) </span><span class="sxs-lookup"><span data-stu-id="93e5f-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Import all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="93e5f-117">匯入所有 RD Cap。</span><span class="sxs-lookup"><span data-stu-id="93e5f-117">Import all RD CAPs.</span></span>

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="93e5f-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>匯 **入所有 Radius 伺服器** (2) </span><span class="sxs-lookup"><span data-stu-id="93e5f-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Import all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="93e5f-119">) 伺服器 (的 NPS 匯入所有網路原則伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="93e5f-119">Import a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span data-ttu-id="93e5f-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>匯 **入所有 rap** (4) </span><span class="sxs-lookup"><span data-stu-id="93e5f-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Import all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93e5f-121">匯入所有 RD Rap。</span><span class="sxs-lookup"><span data-stu-id="93e5f-121">Import all RD RAPs.</span></span>

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span data-ttu-id="93e5f-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>匯 **入所有 RGs** (8) </span><span class="sxs-lookup"><span data-stu-id="93e5f-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Import all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="93e5f-123">匯入所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="93e5f-123">Import all resource groups.</span></span>

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="93e5f-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>匯 **入所有負載平衡伺服器** (16) </span><span class="sxs-lookup"><span data-stu-id="93e5f-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Import all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="93e5f-125">匯入所有負載平衡伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="93e5f-125">Import a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="93e5f-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>將 **所有伺服器設定匯入** (32) </span><span class="sxs-lookup"><span data-stu-id="93e5f-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Import all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="93e5f-127">匯入所有 RD 閘道相關的伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="93e5f-127">Import all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="93e5f-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>匯 **入所有健康原則** (64) </span><span class="sxs-lookup"><span data-stu-id="93e5f-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Import all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="93e5f-129">匯入所有健康狀態原則。</span><span class="sxs-lookup"><span data-stu-id="93e5f-129">Import all health policies.</span></span>

<span data-ttu-id="93e5f-130">\* \* Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2 和 Windows Server 2008： \* \*</span><span class="sxs-lookup"><span data-stu-id="93e5f-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="93e5f-131">Windows Server 2016 之前不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="93e5f-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="93e5f-132">*XmlString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93e5f-132">*XmlString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e5f-133">以 XML 字串形式設定的設定。</span><span class="sxs-lookup"><span data-stu-id="93e5f-133">The configuration as an XML string.</span></span>

</dd> <dt>

<span data-ttu-id="93e5f-134">*MergeOrReplace* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93e5f-134">*MergeOrReplace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e5f-135">指出當發生衝突時，是否要合併或取代資料。</span><span class="sxs-lookup"><span data-stu-id="93e5f-135">Indicates whether to merge or replace data when a conflict occurs.</span></span>

> [!Note]  
> <span data-ttu-id="93e5f-136">尚未實行合併。</span><span class="sxs-lookup"><span data-stu-id="93e5f-136">Merge is not yet implemented.</span></span> <span data-ttu-id="93e5f-137">因此，會忽略此參數值。</span><span class="sxs-lookup"><span data-stu-id="93e5f-137">Therefore, this parameter value is ignored.</span></span>

 

</dd> <dt>

<span data-ttu-id="93e5f-138">*LogString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93e5f-138">*LogString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93e5f-139">匯入作業期間所產生的記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="93e5f-139">The log information that is generated during the import operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93e5f-140">備註</span><span class="sxs-lookup"><span data-stu-id="93e5f-140">Remarks</span></span>

<span data-ttu-id="93e5f-141">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="93e5f-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="93e5f-142">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="93e5f-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93e5f-143">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="93e5f-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="93e5f-144">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="93e5f-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93e5f-145">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="93e5f-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="93e5f-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="93e5f-146">Requirements</span></span>



| <span data-ttu-id="93e5f-147">需求</span><span class="sxs-lookup"><span data-stu-id="93e5f-147">Requirement</span></span> | <span data-ttu-id="93e5f-148">值</span><span class="sxs-lookup"><span data-stu-id="93e5f-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e5f-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93e5f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="93e5f-150">都不支援</span><span class="sxs-lookup"><span data-stu-id="93e5f-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="93e5f-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93e5f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="93e5f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93e5f-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="93e5f-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="93e5f-153">Namespace</span></span><br/>                | <span data-ttu-id="93e5f-154">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="93e5f-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="93e5f-155">MOF</span><span class="sxs-lookup"><span data-stu-id="93e5f-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93e5f-156"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="93e5f-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="93e5f-157">DLL</span><span class="sxs-lookup"><span data-stu-id="93e5f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93e5f-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93e5f-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="93e5f-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93e5f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e5f-160">**Win32 \_ TSGatewayServer**</span><span class="sxs-lookup"><span data-stu-id="93e5f-160">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

