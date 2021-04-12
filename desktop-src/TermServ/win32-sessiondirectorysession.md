---
title: Win32_SessionDirectorySession 類別
description: 提供屬性，以用來查看遠端桌面連線代理人 (RD 連線代理人) 會話的屬性。
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession 類別遠端桌面服務
- Win32_SessionDirectorySession 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384149"
---
# <a name="win32_sessiondirectorysession-class"></a><span data-ttu-id="1a6c7-105">Win32 \_ SessionDirectorySession 類別</span><span class="sxs-lookup"><span data-stu-id="1a6c7-105">Win32\_SessionDirectorySession class</span></span>

<span data-ttu-id="1a6c7-106">提供屬性，以用來查看遠端桌面連線代理人 (RD 連線代理人) 會話的屬性。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) session.</span></span>

> [!Note]  
> <span data-ttu-id="1a6c7-107">在 Windows Server 2008 R2 中，終端機服務會話代理人 (TS 會話代理人) 的名稱已變更為 RD 連線代理人。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="1a6c7-108">除非另有說明，否則這些屬性適用于所有支援的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1a6c7-109">語法</span><span class="sxs-lookup"><span data-stu-id="1a6c7-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a><span data-ttu-id="1a6c7-110">成員</span><span class="sxs-lookup"><span data-stu-id="1a6c7-110">Members</span></span>

<span data-ttu-id="1a6c7-111">**Win32 \_ SessionDirectorySession** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1a6c7-111">The **Win32\_SessionDirectorySession** class has these types of members:</span></span>

-   [<span data-ttu-id="1a6c7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1a6c7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a6c7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1a6c7-113">Properties</span></span>

<span data-ttu-id="1a6c7-114">**Win32 \_ SessionDirectorySession** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-114">The **Win32\_SessionDirectorySession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a6c7-115">**ApplicationType**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-115">**ApplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-118">應用程式已開始使用此會話。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-118">Application started with this session.</span></span> <span data-ttu-id="1a6c7-119">這與 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)的 **StartProgram** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-119">This is the same as the **StartProgram** property of [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-120">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-120">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-121">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-123">會話的色彩深度，以每圖元的位數來測量。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-123">Color depth of the session, measured in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-124">**Createtimefilterend**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-124">**CreateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-125">資料類型： **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-125">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-127">建立會話的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-127">Date and time the session was created.</span></span> <span data-ttu-id="1a6c7-128">當會話中斷連接並重新連接時，不會重設此值。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-128">This value is not reset when a session is disconnected and reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-129">**DisconnectTime**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-129">**DisconnectTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-130">資料類型： **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-130">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-132">會話中斷連線的日期和時間 (如果適用) 。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-132">Date and time the session was disconnected (if applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-133">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-133">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-136">登入此會話之使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-136">Domain name of the user logged on to this session.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-137">**ResolutionHeight**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-137">**ResolutionHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-140">此會話的會話高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-140">Height of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-141">**ResolutionWidth**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-141">**ResolutionWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-144">此會話的會話寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-144">Width of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-145">**Microsoft.sqlserver.management.smo.wmi.serveripaddress<**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-145">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-148">此會話的 RD 連線代理人伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-148">IP address of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-149">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-149">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a6c7-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-153">此會話的 RD 連線代理人伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-153">Name of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-154">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-154">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-155">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-157">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a6c7-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-158">此會話的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-158">Session ID for this session.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-159">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-159">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-162">此會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-162">State of this session.</span></span>

<dt>

<span data-ttu-id="1a6c7-163">0</span><span class="sxs-lookup"><span data-stu-id="1a6c7-163">0</span></span>
</dt> <dd>

<span data-ttu-id="1a6c7-164">會話為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-164">The session is active.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-165">1</span><span class="sxs-lookup"><span data-stu-id="1a6c7-165">1</span></span>
</dt> <dd>

<span data-ttu-id="1a6c7-166">會話已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-166">The session is disconnected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a6c7-167">**TSProtocol**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-167">**TSProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-170">此會話的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-170">Protocol for this session.</span></span>

<dt>

<span data-ttu-id="1a6c7-171">0</span><span class="sxs-lookup"><span data-stu-id="1a6c7-171">0</span></span>
</dt> <dd>

<span data-ttu-id="1a6c7-172">此會話正在實體主控台上執行。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-172">This session is running on a physical console.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-173">1</span><span class="sxs-lookup"><span data-stu-id="1a6c7-173">1</span></span>
</dt> <dd>

<span data-ttu-id="1a6c7-174">此會話會使用專屬的協力廠商通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-174">A proprietary third-party protocol is used for this session.</span></span>

</dd> <dt>

<span data-ttu-id="1a6c7-175">2</span><span class="sxs-lookup"><span data-stu-id="1a6c7-175">2</span></span>
</dt> <dd>

<span data-ttu-id="1a6c7-176">此會話會使用遠端桌面通訊協定 (RDP) 。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-176">Remote Desktop Protocol (RDP) is used for this session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a6c7-177">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-177">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a6c7-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a6c7-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a6c7-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a6c7-180">登入此會話之使用者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-180">User name of the user logged on to this session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a6c7-181">備註</span><span class="sxs-lookup"><span data-stu-id="1a6c7-181">Remarks</span></span>

<span data-ttu-id="1a6c7-182">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-182">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1a6c7-183">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-183">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1a6c7-184">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-184">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1a6c7-185">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="1a6c7-185">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6c7-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a6c7-186">Requirements</span></span>



| <span data-ttu-id="1a6c7-187">需求</span><span class="sxs-lookup"><span data-stu-id="1a6c7-187">Requirement</span></span> | <span data-ttu-id="1a6c7-188">值</span><span class="sxs-lookup"><span data-stu-id="1a6c7-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6c7-189">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a6c7-189">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6c7-190">都不支援</span><span class="sxs-lookup"><span data-stu-id="1a6c7-190">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1a6c7-191">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a6c7-191">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6c7-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a6c7-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1a6c7-193">命名空間</span><span class="sxs-lookup"><span data-stu-id="1a6c7-193">Namespace</span></span><br/>                | <span data-ttu-id="1a6c7-194">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1a6c7-194">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="1a6c7-195">MOF</span><span class="sxs-lookup"><span data-stu-id="1a6c7-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a6c7-196"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a6c7-196"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a6c7-197">DLL</span><span class="sxs-lookup"><span data-stu-id="1a6c7-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a6c7-198"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a6c7-198"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6c7-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a6c7-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6c7-200">**Win32 \_ SessionDirectoryCluster**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-200">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="1a6c7-201">**Win32 \_ SessionDirectoryServer**</span><span class="sxs-lookup"><span data-stu-id="1a6c7-201">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> </dl>

 

