---
title: Win32_TSGatewayServer 類別的 Export 方法
description: 以 XML 字串形式傳回遠端桌面閘道 (RD 閘道) 伺服器設定。
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Export 方法遠端桌面服務
- Export 方法遠端桌面服務，Win32_TSGatewayServer 類別
- Win32_TSGatewayServer 類別遠端桌面服務，Export 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935138"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="4bb17-106">Win32 TSGatewayServer 類別的 Export 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4bb17-106">Export method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="4bb17-107">以 XML 字串形式傳回遠端桌面閘道 (RD 閘道) 伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="4bb17-107">Returns the Remote Desktop Gateway (RD Gateway) server configuration as an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb17-108">語法</span><span class="sxs-lookup"><span data-stu-id="4bb17-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a><span data-ttu-id="4bb17-109">參數</span><span class="sxs-lookup"><span data-stu-id="4bb17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bb17-110">*ExportType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bb17-110">*ExportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb17-111">要匯出的內容。</span><span class="sxs-lookup"><span data-stu-id="4bb17-111">The content to export.</span></span> <span data-ttu-id="4bb17-112">設定匯出類型，方法是在 *ExportType* 參數中設定對應的位。</span><span class="sxs-lookup"><span data-stu-id="4bb17-112">Set the export type by setting the corresponding bits in the *ExportType* parameter.</span></span> <span data-ttu-id="4bb17-113">您可以設定多個匯出類型。</span><span class="sxs-lookup"><span data-stu-id="4bb17-113">You can set multiple export types.</span></span> <span data-ttu-id="4bb17-114">例如，如果設定0位，則會匯出 (RD Cap) 的遠端桌面服務連線授權原則。</span><span class="sxs-lookup"><span data-stu-id="4bb17-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be exported.</span></span> <span data-ttu-id="4bb17-115">如果設定0和第2位，則會匯出 RD Cap 和遠端桌面服務資源授權原則 (RD Rap) 。</span><span class="sxs-lookup"><span data-stu-id="4bb17-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be exported.</span></span>

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span data-ttu-id="4bb17-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**匯出所有 CAPs** (1) </span><span class="sxs-lookup"><span data-stu-id="4bb17-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Export all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4bb17-117">匯出所有 RD Cap。</span><span class="sxs-lookup"><span data-stu-id="4bb17-117">Export all RD CAPs.</span></span>

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="4bb17-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>將 **所有 Radius 伺服器匯出** (2) </span><span class="sxs-lookup"><span data-stu-id="4bb17-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Export all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4bb17-119">將所有網路原則伺服器的清單匯出 (NPS) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4bb17-119">Export a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span data-ttu-id="4bb17-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>將 **所有 Rap 匯出** (4) </span><span class="sxs-lookup"><span data-stu-id="4bb17-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Export all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4bb17-121">匯出所有 RD Rap。</span><span class="sxs-lookup"><span data-stu-id="4bb17-121">Export all RD RAPs.</span></span>

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span data-ttu-id="4bb17-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>將 **所有 RGs 匯出** (8) </span><span class="sxs-lookup"><span data-stu-id="4bb17-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Export all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4bb17-123">匯出所有資源群組。</span><span class="sxs-lookup"><span data-stu-id="4bb17-123">Export all resource groups.</span></span>

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="4bb17-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>將 **所有負載平衡伺服器匯出** (16) </span><span class="sxs-lookup"><span data-stu-id="4bb17-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Export all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="4bb17-125">匯出所有負載平衡伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="4bb17-125">Export a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="4bb17-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>將 **所有伺服器設定匯出** (32) </span><span class="sxs-lookup"><span data-stu-id="4bb17-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Export all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="4bb17-127">匯出所有 RD 閘道相關的伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="4bb17-127">Export all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="4bb17-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>將 **所有健康原則匯出** (64) </span><span class="sxs-lookup"><span data-stu-id="4bb17-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Export all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="4bb17-129">匯出所有健康情況原則。</span><span class="sxs-lookup"><span data-stu-id="4bb17-129">Export all health policies.</span></span>

<span data-ttu-id="4bb17-130">\* \* Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2 和 Windows Server 2008： \* \*</span><span class="sxs-lookup"><span data-stu-id="4bb17-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="4bb17-131">Windows Server 2016 之前不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="4bb17-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4bb17-132">*XmlString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4bb17-132">*XmlString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb17-133">XML 字串。</span><span class="sxs-lookup"><span data-stu-id="4bb17-133">The XML string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bb17-134">備註</span><span class="sxs-lookup"><span data-stu-id="4bb17-134">Remarks</span></span>

<span data-ttu-id="4bb17-135">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="4bb17-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4bb17-136">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4bb17-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4bb17-137">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4bb17-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4bb17-138">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4bb17-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4bb17-139">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="4bb17-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb17-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bb17-140">Requirements</span></span>



| <span data-ttu-id="4bb17-141">需求</span><span class="sxs-lookup"><span data-stu-id="4bb17-141">Requirement</span></span> | <span data-ttu-id="4bb17-142">值</span><span class="sxs-lookup"><span data-stu-id="4bb17-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb17-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bb17-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb17-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="4bb17-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4bb17-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bb17-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb17-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bb17-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4bb17-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="4bb17-147">Namespace</span></span><br/>                | <span data-ttu-id="4bb17-148">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="4bb17-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4bb17-149">MOF</span><span class="sxs-lookup"><span data-stu-id="4bb17-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bb17-150"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bb17-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bb17-151">DLL</span><span class="sxs-lookup"><span data-stu-id="4bb17-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bb17-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bb17-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4bb17-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bb17-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb17-154">**Win32 \_ TSGatewayServer**</span><span class="sxs-lookup"><span data-stu-id="4bb17-154">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

