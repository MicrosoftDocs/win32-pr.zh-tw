---
title: Win32_TSGatewayConnection 類別
description: 代表從用戶端電腦到遠端桌面閘道 (RD 閘道) server 的連接。
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnection 類別遠端桌面服務
- Win32_TSGatewayConnection 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105833"
---
# <a name="win32_tsgatewayconnection-class"></a><span data-ttu-id="5b281-105">Win32 \_ TSGatewayConnection 類別</span><span class="sxs-lookup"><span data-stu-id="5b281-105">Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="5b281-106">代表從用戶端電腦到遠端桌面閘道 (RD 閘道) server 的連接。</span><span class="sxs-lookup"><span data-stu-id="5b281-106">Represents a connection from a client computer to a Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b281-107">語法</span><span class="sxs-lookup"><span data-stu-id="5b281-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="5b281-108">成員</span><span class="sxs-lookup"><span data-stu-id="5b281-108">Members</span></span>

<span data-ttu-id="5b281-109">**Win32 \_ TSGatewayConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5b281-109">The **Win32\_TSGatewayConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="5b281-110">方法</span><span class="sxs-lookup"><span data-stu-id="5b281-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5b281-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5b281-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5b281-112">方法</span><span class="sxs-lookup"><span data-stu-id="5b281-112">Methods</span></span>

<span data-ttu-id="5b281-113">**Win32 \_ TSGatewayConnection** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5b281-113">The **Win32\_TSGatewayConnection** class has these methods.</span></span>



| <span data-ttu-id="5b281-114">方法</span><span class="sxs-lookup"><span data-stu-id="5b281-114">Method</span></span>                                                                     | <span data-ttu-id="5b281-115">描述</span><span class="sxs-lookup"><span data-stu-id="5b281-115">Description</span></span>                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b281-116">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="5b281-116">**CheckStatus**</span></span>](checkstatus-win32-tsgatewayconnection.md)               | <span data-ttu-id="5b281-117">檢查 RD 閘道伺服器連接的狀態，以及是否已設定目標伺服器進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="5b281-117">Checks the status of an RD Gateway server connection, and whether the target server is configured for load balancing.</span></span><br/> |
| [<span data-ttu-id="5b281-118">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="5b281-118">**Disconnect**</span></span>](disconnect-win32-tsgatewayconnection.md)                 | <span data-ttu-id="5b281-119">結束連接。</span><span class="sxs-lookup"><span data-stu-id="5b281-119">Ends the connection.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="5b281-120">**DisconnectProtocol**</span><span class="sxs-lookup"><span data-stu-id="5b281-120">**DisconnectProtocol**</span></span>](disconnectprotocol-win32-tsgatewayconnection.md) | <span data-ttu-id="5b281-121">結束使用指定之通訊協定的所有連接。</span><span class="sxs-lookup"><span data-stu-id="5b281-121">Ends all connections that use the specified protocol.</span></span><br/>                                                                 |
| [<span data-ttu-id="5b281-122">**DisconnectUser**</span><span class="sxs-lookup"><span data-stu-id="5b281-122">**DisconnectUser**</span></span>](disconnectuser-win32-tsgatewayconnection.md)         | <span data-ttu-id="5b281-123">結束指定之使用者的所有連接。</span><span class="sxs-lookup"><span data-stu-id="5b281-123">Ends all connections of the specified user.</span></span><br/>                                                                           |



 

### <a name="properties"></a><span data-ttu-id="5b281-124">屬性</span><span class="sxs-lookup"><span data-stu-id="5b281-124">Properties</span></span>

<span data-ttu-id="5b281-125">**Win32 \_ TSGatewayConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5b281-125">The **Win32\_TSGatewayConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b281-126">**ChannelId**</span><span class="sxs-lookup"><span data-stu-id="5b281-126">**ChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-127">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5b281-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-129">通道識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b281-129">Channel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-130">**ClientAddress**</span><span class="sxs-lookup"><span data-stu-id="5b281-130">**ClientAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-133">用戶端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5b281-133">Client IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-134">**ConnectedPort**</span><span class="sxs-lookup"><span data-stu-id="5b281-134">**ConnectedPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5b281-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-137">連接的資源上使用者所連線的埠。</span><span class="sxs-lookup"><span data-stu-id="5b281-137">Port on the connected resource to which the user is connected.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-138">**ConnectedResource**</span><span class="sxs-lookup"><span data-stu-id="5b281-138">**ConnectedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-141">用戶端所連線之電腦 (或叢集) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b281-141">Name of the computer (or cluster) to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-142">**ConnectedTime**</span><span class="sxs-lookup"><span data-stu-id="5b281-142">**ConnectedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-145">建立連接時的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="5b281-145">The time stamp for when the connection was established.</span></span> <span data-ttu-id="5b281-146">當連接重設時，會重設此時間，即使它會自動重新連線。</span><span class="sxs-lookup"><span data-stu-id="5b281-146">This time is reset when the connection is reset, even if it is automatically reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-147">**ConnectionDuration**</span><span class="sxs-lookup"><span data-stu-id="5b281-147">**ConnectionDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-150">自連線時間以來經過的時間。</span><span class="sxs-lookup"><span data-stu-id="5b281-150">The time that has elapsed since the connected time.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-151">**ConnectionKey**</span><span class="sxs-lookup"><span data-stu-id="5b281-151">**ConnectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b281-154">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5b281-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5b281-155">格式為 "tunnelId： channelID" 的連接識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b281-155">Connection identifier in the format "tunnelId:channelID".</span></span>

</dd> <dt>

<span data-ttu-id="5b281-156">**FullUserName**</span><span class="sxs-lookup"><span data-stu-id="5b281-156">**FullUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-159">已連線使用者的完整使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="5b281-159">Full user name of the connected user.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-160">**IdleTime**</span><span class="sxs-lookup"><span data-stu-id="5b281-160">**IdleTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-163">連接的閒置時間。</span><span class="sxs-lookup"><span data-stu-id="5b281-163">Idle time of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-164">**NumberOfKilobytesReceived**</span><span class="sxs-lookup"><span data-stu-id="5b281-164">**NumberOfKilobytesReceived**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-165">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5b281-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-167">RD 閘道伺服器從用戶端電腦收到的 kb 數。</span><span class="sxs-lookup"><span data-stu-id="5b281-167">Number of kilobytes received from the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-168">**NumberOfKilobytesSent**</span><span class="sxs-lookup"><span data-stu-id="5b281-168">**NumberOfKilobytesSent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-169">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5b281-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-171">RD 閘道伺服器傳送給用戶端電腦的 kb 數。</span><span class="sxs-lookup"><span data-stu-id="5b281-171">Number of kilobytes sent to the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-172">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="5b281-172">**ProtocolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-175">用來連接 RD 閘道伺服器的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5b281-175">Protocol that is used to connect to the RD Gateway server.</span></span>

<dt>

<span data-ttu-id="5b281-176">RDP</span><span class="sxs-lookup"><span data-stu-id="5b281-176">"RDP"</span></span>
</dt> <dd>

<span data-ttu-id="5b281-177">RD 閘道伺服器的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5b281-177">The protocol for the RD Gateway server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b281-178">**TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="5b281-178">**TransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-179">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5b281-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-181">指定連接的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="5b281-181">Specifies the transport type for the connection.</span></span> <span data-ttu-id="5b281-182">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="5b281-182">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="5b281-183">0</span><span class="sxs-lookup"><span data-stu-id="5b281-183">0</span></span>
</dt> <dd>

<span data-ttu-id="5b281-184">RPC over HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="5b281-184">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-185">1</span><span class="sxs-lookup"><span data-stu-id="5b281-185">1</span></span>
</dt> <dd>

<span data-ttu-id="5b281-186">HTTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="5b281-186">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-187">2</span><span class="sxs-lookup"><span data-stu-id="5b281-187">2</span></span>
</dt> <dd>

<span data-ttu-id="5b281-188">UDP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="5b281-188">UDP transport.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5b281-189">**TunnelId**</span><span class="sxs-lookup"><span data-stu-id="5b281-189">**TunnelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-190">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5b281-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-192">通道識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b281-192">Tunnel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5b281-193">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="5b281-193">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b281-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5b281-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b281-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5b281-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5b281-196">連接到 RD 閘道伺服器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="5b281-196">User name connected to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b281-197">備註</span><span class="sxs-lookup"><span data-stu-id="5b281-197">Remarks</span></span>

<span data-ttu-id="5b281-198">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="5b281-198">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="5b281-199">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="5b281-199">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5b281-200">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5b281-200">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5b281-201">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="5b281-201">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5b281-202">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="5b281-202">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b281-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b281-203">Requirements</span></span>



| <span data-ttu-id="5b281-204">需求</span><span class="sxs-lookup"><span data-stu-id="5b281-204">Requirement</span></span> | <span data-ttu-id="5b281-205">值</span><span class="sxs-lookup"><span data-stu-id="5b281-205">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b281-206">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b281-206">Minimum supported client</span></span><br/> | <span data-ttu-id="5b281-207">都不支援</span><span class="sxs-lookup"><span data-stu-id="5b281-207">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5b281-208">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b281-208">Minimum supported server</span></span><br/> | <span data-ttu-id="5b281-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b281-209">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5b281-210">命名空間</span><span class="sxs-lookup"><span data-stu-id="5b281-210">Namespace</span></span><br/>                | <span data-ttu-id="5b281-211">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5b281-211">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5b281-212">MOF</span><span class="sxs-lookup"><span data-stu-id="5b281-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b281-213"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b281-213"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b281-214">DLL</span><span class="sxs-lookup"><span data-stu-id="5b281-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b281-215"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b281-215"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5b281-216">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b281-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b281-217">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="5b281-217">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="5b281-218">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="5b281-218">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="5b281-219">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="5b281-219">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="5b281-220">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="5b281-220">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="5b281-221">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="5b281-221">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="5b281-222">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="5b281-222">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

