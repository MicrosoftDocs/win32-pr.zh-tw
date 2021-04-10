---
title: Win32_SessionDirectoryServer 類別
description: 提供屬性，以用來查看遠端桌面連線代理人 (RD 連線代理人) server 的屬性。
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer 類別遠端桌面服務
- Win32_SessionDirectoryServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934233"
---
# <a name="win32_sessiondirectoryserver-class"></a><span data-ttu-id="78ad9-105">Win32 \_ SessionDirectoryServer 類別</span><span class="sxs-lookup"><span data-stu-id="78ad9-105">Win32\_SessionDirectoryServer class</span></span>

<span data-ttu-id="78ad9-106">提供屬性，以用來查看遠端桌面連線代理人 (RD 連線代理人) server 的屬性。</span><span class="sxs-lookup"><span data-stu-id="78ad9-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) server.</span></span>

> [!Note]  
> <span data-ttu-id="78ad9-107">在 Windows Server 2008 R2 中，終端機服務會話代理人 (TS 會話代理人) 的名稱已變更為 RD 連線代理人。</span><span class="sxs-lookup"><span data-stu-id="78ad9-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="78ad9-108">除非另有說明，否則這些屬性適用于所有支援的作業系統。</span><span class="sxs-lookup"><span data-stu-id="78ad9-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="78ad9-109">語法</span><span class="sxs-lookup"><span data-stu-id="78ad9-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a><span data-ttu-id="78ad9-110">成員</span><span class="sxs-lookup"><span data-stu-id="78ad9-110">Members</span></span>

<span data-ttu-id="78ad9-111">**Win32 \_ SessionDirectoryServer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="78ad9-111">The **Win32\_SessionDirectoryServer** class has these types of members:</span></span>

-   [<span data-ttu-id="78ad9-112">屬性</span><span class="sxs-lookup"><span data-stu-id="78ad9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78ad9-113">屬性</span><span class="sxs-lookup"><span data-stu-id="78ad9-113">Properties</span></span>

<span data-ttu-id="78ad9-114">**Win32 \_ SessionDirectoryServer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="78ad9-114">The **Win32\_SessionDirectoryServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78ad9-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="78ad9-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78ad9-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78ad9-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78ad9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78ad9-118">包含伺服器之伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="78ad9-118">Name of the farm that includes the server.</span></span>

</dd> <dt>

<span data-ttu-id="78ad9-119">**LoadIndicator**</span><span class="sxs-lookup"><span data-stu-id="78ad9-119">**LoadIndicator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78ad9-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="78ad9-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78ad9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78ad9-122">表示使用預設負載平衡演算法時 RD 工作階段主機伺服器負載的相對數位。</span><span class="sxs-lookup"><span data-stu-id="78ad9-122">A relative number that represents the RD Session Host server load when the default load-balancing algorithm is used.</span></span> <span data-ttu-id="78ad9-123">*LoadIndicator* 屬性值是根據會話的數目、暫止的重新導向要求數目，以及伺服器加權值。</span><span class="sxs-lookup"><span data-stu-id="78ad9-123">The *LoadIndicator* property value is based on the number of sessions, the number of pending redirection requests, and the server weight value.</span></span>

</dd> <dt>

<span data-ttu-id="78ad9-124">**NumberOfSessions**</span><span class="sxs-lookup"><span data-stu-id="78ad9-124">**NumberOfSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78ad9-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="78ad9-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78ad9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78ad9-127">RD 連線代理人伺服器中的會話數目。</span><span class="sxs-lookup"><span data-stu-id="78ad9-127">Number of sessions in the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="78ad9-128">**NumPendRedir**</span><span class="sxs-lookup"><span data-stu-id="78ad9-128">**NumPendRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78ad9-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="78ad9-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78ad9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78ad9-131">暫止重新導向要求的數目。</span><span class="sxs-lookup"><span data-stu-id="78ad9-131">Number of pending redirection requests.</span></span>

</dd> <dt>

<span data-ttu-id="78ad9-132">**Microsoft.sqlserver.management.smo.wmi.serveripaddress<**</span><span class="sxs-lookup"><span data-stu-id="78ad9-132">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78ad9-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78ad9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78ad9-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78ad9-135">RD 連線代理人伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="78ad9-135">IP address of the RD Connection Broker server.</span></span> <span data-ttu-id="78ad9-136">如果伺服器同時設定為 IPv4 和 IPv6 位址，這將會包含 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="78ad9-136">If the server is configured for both IPv4 and IPv6 addresses, this will contain the IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="78ad9-137">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="78ad9-137">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78ad9-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78ad9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78ad9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-140">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="78ad9-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="78ad9-141">RD 連線代理人伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="78ad9-141">Name of the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="78ad9-142">**ServerWeight**</span><span class="sxs-lookup"><span data-stu-id="78ad9-142">**ServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78ad9-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="78ad9-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78ad9-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78ad9-145">伺服器權數值，用於負載平衡。</span><span class="sxs-lookup"><span data-stu-id="78ad9-145">Server weight value, used in load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="78ad9-146">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="78ad9-146">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78ad9-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="78ad9-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78ad9-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78ad9-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78ad9-149">RD 連線代理人伺服器的單一會話模式設定。</span><span class="sxs-lookup"><span data-stu-id="78ad9-149">Single session mode setting of the RD Connection Broker server.</span></span>

<dt>

<span data-ttu-id="78ad9-150">0</span><span class="sxs-lookup"><span data-stu-id="78ad9-150">0</span></span>
</dt> <dd>

<span data-ttu-id="78ad9-151">伺服器陣列不在單一會話模式中。</span><span class="sxs-lookup"><span data-stu-id="78ad9-151">The farm is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="78ad9-152">1</span><span class="sxs-lookup"><span data-stu-id="78ad9-152">1</span></span>
</dt> <dd>

<span data-ttu-id="78ad9-153">中的伺服器陣列處於單一會話模式。</span><span class="sxs-lookup"><span data-stu-id="78ad9-153">The farm in is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78ad9-154">備註</span><span class="sxs-lookup"><span data-stu-id="78ad9-154">Remarks</span></span>

<span data-ttu-id="78ad9-155">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="78ad9-155">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="78ad9-156">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="78ad9-156">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="78ad9-157">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="78ad9-157">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="78ad9-158">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="78ad9-158">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="78ad9-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="78ad9-159">Requirements</span></span>



| <span data-ttu-id="78ad9-160">需求</span><span class="sxs-lookup"><span data-stu-id="78ad9-160">Requirement</span></span> | <span data-ttu-id="78ad9-161">值</span><span class="sxs-lookup"><span data-stu-id="78ad9-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78ad9-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78ad9-162">Minimum supported client</span></span><br/> | <span data-ttu-id="78ad9-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="78ad9-163">None supported</span></span><br/>                                                              |
| <span data-ttu-id="78ad9-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78ad9-164">Minimum supported server</span></span><br/> | <span data-ttu-id="78ad9-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78ad9-165">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="78ad9-166">命名空間</span><span class="sxs-lookup"><span data-stu-id="78ad9-166">Namespace</span></span><br/>                | <span data-ttu-id="78ad9-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="78ad9-167">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="78ad9-168">MOF</span><span class="sxs-lookup"><span data-stu-id="78ad9-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78ad9-169"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="78ad9-169"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="78ad9-170">DLL</span><span class="sxs-lookup"><span data-stu-id="78ad9-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78ad9-171"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78ad9-171"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78ad9-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78ad9-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ad9-173">**Win32 \_ SessionDirectoryCluster**</span><span class="sxs-lookup"><span data-stu-id="78ad9-173">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="78ad9-174">**Win32 \_ SessionDirectorySession**</span><span class="sxs-lookup"><span data-stu-id="78ad9-174">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

