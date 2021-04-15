---
title: Win32_TSGatewayServerSettings 類別
description: 提供方法和屬性來查看和設定遠端桌面閘道 (RD 閘道) 伺服器設定。
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings 類別遠端桌面服務
- Win32_TSGatewayServerSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466705"
---
# <a name="win32_tsgatewayserversettings-class"></a><span data-ttu-id="e2367-105">Win32 \_ TSGatewayServerSettings 類別</span><span class="sxs-lookup"><span data-stu-id="e2367-105">Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="e2367-106">提供方法和屬性來查看和設定遠端桌面閘道 (RD 閘道) 伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="e2367-106">Provides methods and properties to view and configure Remote Desktop Gateway (RD Gateway) server settings.</span></span> <span data-ttu-id="e2367-107">系統管理員可以使用這個類別來設定一組通訊協定、一組將寫入事件記錄檔的事件，以及透過 RD 閘道的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="e2367-107">An administrator can use this class to configure a set of protocols, the set of events that will be written to the event log, and the maximum number of connections through RD Gateway.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2367-108">語法</span><span class="sxs-lookup"><span data-stu-id="e2367-108">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a><span data-ttu-id="e2367-109">成員</span><span class="sxs-lookup"><span data-stu-id="e2367-109">Members</span></span>

<span data-ttu-id="e2367-110">**Win32 \_ TSGatewayServerSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e2367-110">The **Win32\_TSGatewayServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="e2367-111">方法</span><span class="sxs-lookup"><span data-stu-id="e2367-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2367-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e2367-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2367-113">方法</span><span class="sxs-lookup"><span data-stu-id="e2367-113">Methods</span></span>

<span data-ttu-id="e2367-114">**Win32 \_ TSGatewayServerSettings** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-114">The **Win32\_TSGatewayServerSettings** class has these methods.</span></span>



| <span data-ttu-id="e2367-115">方法</span><span class="sxs-lookup"><span data-stu-id="e2367-115">Method</span></span>                                                                                                                                             | <span data-ttu-id="e2367-116">描述</span><span class="sxs-lookup"><span data-stu-id="e2367-116">Description</span></span>                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2367-117">**設定**</span><span class="sxs-lookup"><span data-stu-id="e2367-117">**Configure**</span></span>](configure-win32-tsgatewayserversettings.md)                                                                                       | <span data-ttu-id="e2367-118">設定 RD 閘道服務所需的 IIS 和 RPC 設定。</span><span class="sxs-lookup"><span data-stu-id="e2367-118">Configures the IIS and RPC settings required by the RD Gateway service.</span></span><br/> <span data-ttu-id="e2367-119">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-119">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                               |
| [<span data-ttu-id="e2367-120">**EnableCentralCAP**</span><span class="sxs-lookup"><span data-stu-id="e2367-120">**EnableCentralCAP**</span></span>](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="e2367-121">啟用或停用 **CentralCAPEnabled** 屬性，此屬性會控制是否使用中央遠端桌面連線授權原則 (RD CAP) 伺服器來控制這部伺服器的連線授權原則。</span><span class="sxs-lookup"><span data-stu-id="e2367-121">Enables or disables the **CentralCAPEnabled** property, which controls whether central Remote Desktop connection authorization policy (RD CAP) servers are used for controlling connection authorization policies for this server.</span></span><br/>                    |
| [<span data-ttu-id="e2367-122">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="e2367-122">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="e2367-123">啟用或停用指定事件種類的記錄。</span><span class="sxs-lookup"><span data-stu-id="e2367-123">Enables or disables logging of the specified event type.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="e2367-124">**EnableOnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="e2367-124">**EnableOnlyConsentCapableClients**</span></span>](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | <span data-ttu-id="e2367-125">設定 **OnlyConsentCapableClients** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-125">Sets the **OnlyConsentCapableClients** property.</span></span><br/> <span data-ttu-id="e2367-126">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-126">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="e2367-127">**EnableRequestSOH**</span><span class="sxs-lookup"><span data-stu-id="e2367-127">**EnableRequestSOH**</span></span>](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | <span data-ttu-id="e2367-128">從 Windows Server 2016 開始不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-128">This method is not supported starting with Windows Server 2016.</span></span><br/> <span data-ttu-id="e2367-129">**Windows server 2012 r2、Windows server 2012、Windows server 2008 R2 和 Windows server 2008：** 啟用或停用健康狀態聲明 (SoH) 的要求。</span><span class="sxs-lookup"><span data-stu-id="e2367-129">**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:** Enables or disables requests for a Statement of Health (SoH).</span></span><br/> <br/> |
| [<span data-ttu-id="e2367-130">**EnableTransport**</span><span class="sxs-lookup"><span data-stu-id="e2367-130">**EnableTransport**</span></span>](enabletransport-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="e2367-131">啟用或停用指定的傳輸。</span><span class="sxs-lookup"><span data-stu-id="e2367-131">Enables or disables the specified transport.</span></span><br/> <span data-ttu-id="e2367-132">**Windows server 2008 R2 和 Windows server 2008：** Windows Server 2012 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-132">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e2367-133">**EnumAuthenticationPlugins**</span><span class="sxs-lookup"><span data-stu-id="e2367-133">**EnumAuthenticationPlugins**</span></span>](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | <span data-ttu-id="e2367-134">列舉所有已註冊的驗證外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e2367-134">Enumerates all registered authentication plug-ins.</span></span><br/> <span data-ttu-id="e2367-135">**Windows Server 2008：** 無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-135">**Windows Server 2008:** This method is not available.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="e2367-136">**EnumAuthorizationPlugins**</span><span class="sxs-lookup"><span data-stu-id="e2367-136">**EnumAuthorizationPlugins**</span></span>](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="e2367-137">列舉所有已註冊的授權外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e2367-137">Enumerates all registered authorization plug-ins.</span></span><br/> <span data-ttu-id="e2367-138">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="e2367-139">**GetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="e2367-139">**GetIPAndPort**</span></span>](getipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="e2367-140">取得指定傳輸的接聽 IP 位址和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="e2367-140">Obtains the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="e2367-141">**Windows server 2008 R2 和 Windows server 2008：** Windows Server 2012 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-141">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                 |
| [<span data-ttu-id="e2367-142">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="e2367-142">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="e2367-143">傳回指定之記錄事件索引的記錄事件名稱。</span><span class="sxs-lookup"><span data-stu-id="e2367-143">Returns the log event name for the specified log event index.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="e2367-144">**GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="e2367-144">**GetProtocolName**</span></span>](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="e2367-145">傳回指定之通訊協定索引的通訊協定名稱。</span><span class="sxs-lookup"><span data-stu-id="e2367-145">Returns the protocol name for the specified protocol index.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="e2367-146">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="e2367-146">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="e2367-147">指出是否已啟用指定的事件記錄檔類型。</span><span class="sxs-lookup"><span data-stu-id="e2367-147">Indicates whether the specified event log type is enabled.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="e2367-148">**IsTransportEnabled**</span><span class="sxs-lookup"><span data-stu-id="e2367-148">**IsTransportEnabled**</span></span>](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="e2367-149">判斷指定的傳輸是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="e2367-149">Determines whether the specified transport is enabled.</span></span><br/> <span data-ttu-id="e2367-150">**Windows server 2008 R2 和 Windows server 2008：** Windows Server 2012 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-150">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                        |
| [<span data-ttu-id="e2367-151">**QueryCertCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e2367-151">**QueryCertContext**</span></span>](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | <span data-ttu-id="e2367-152">指出是否已安裝指定的憑證。</span><span class="sxs-lookup"><span data-stu-id="e2367-152">Indicates whether the specified certificate is installed.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="e2367-153">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="e2367-153">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | <span data-ttu-id="e2367-154">回收 IIS 中的 RPC 應用程式集區。</span><span class="sxs-lookup"><span data-stu-id="e2367-154">Recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="e2367-155">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-155">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="e2367-156">**RefreshCertCoNtext**</span><span class="sxs-lookup"><span data-stu-id="e2367-156">**RefreshCertContext**</span></span>](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | <span data-ttu-id="e2367-157">重新整理 RD 閘道伺服器所使用的憑證。</span><span class="sxs-lookup"><span data-stu-id="e2367-157">Refreshes the certificate that is used by the RD Gateway server.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="e2367-158">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="e2367-158">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | <span data-ttu-id="e2367-159">設定 RD 閘道伺服器的目前驗證外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e2367-159">Sets the current authentication plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="e2367-160">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-160">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="e2367-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="e2367-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span></span>](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | <span data-ttu-id="e2367-162">設定 RD 閘道伺服器的目前驗證外掛程式，並在 IIS 中回收 RPC 應用程式集區。</span><span class="sxs-lookup"><span data-stu-id="e2367-162">Sets the current authentication plug-in for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="e2367-163">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-163">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                      |
| [<span data-ttu-id="e2367-164">**SetAuthorizationPlugin**</span><span class="sxs-lookup"><span data-stu-id="e2367-164">**SetAuthorizationPlugin**</span></span>](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | <span data-ttu-id="e2367-165">設定 RD 閘道伺服器目前的授權外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e2367-165">Sets the current authorization plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="e2367-166">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-166">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                     |
| [<span data-ttu-id="e2367-167">**SetCertificate**</span><span class="sxs-lookup"><span data-stu-id="e2367-167">**SetCertificate**</span></span>](setcertificate-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="e2367-168">在 IIS 中設定埠443的 HTTPS 系結憑證雜湊。</span><span class="sxs-lookup"><span data-stu-id="e2367-168">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span><br/> <span data-ttu-id="e2367-169">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                       |
| [<span data-ttu-id="e2367-170">**SetCertificateACL**</span><span class="sxs-lookup"><span data-stu-id="e2367-170">**SetCertificateACL**</span></span>](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="e2367-171">設定此伺服器 (Acl) 的憑證存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="e2367-171">Sets the certificate access control lists (ACLs) for this server.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="e2367-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="e2367-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span></span>](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | <span data-ttu-id="e2367-173">設定 RD 閘道伺服器目前的驗證和授權外掛程式，並在 IIS 中回收 RPC 應用程式集區。</span><span class="sxs-lookup"><span data-stu-id="e2367-173">Sets the current authentication and authorization plug-ins for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="e2367-174">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-174">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                   |
| [<span data-ttu-id="e2367-175">**SetEnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="e2367-175">**SetEnforceChannelBinding**</span></span>](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="e2367-176">設定 **EnforceChannelBinding** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-176">Sets the **EnforceChannelBinding** property.</span></span><br/> <span data-ttu-id="e2367-177">**Windows server 2008 R2 和 Windows server 2008：** Windows Server 2012 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-177">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e2367-178">**SetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="e2367-178">**SetIPAndPort**</span></span>](setipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="e2367-179">設定指定傳輸的接聽 IP 位址和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="e2367-179">Sets the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="e2367-180">**Windows server 2008 R2 和 Windows server 2008：** Windows Server 2012 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-180">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                    |
| [<span data-ttu-id="e2367-181">**SetMaxConnections**</span><span class="sxs-lookup"><span data-stu-id="e2367-181">**SetMaxConnections**</span></span>](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="e2367-182">設定允許的最大連接數 RD 閘道。</span><span class="sxs-lookup"><span data-stu-id="e2367-182">Sets the maximum number of allowed connections through RD Gateway.</span></span> <span data-ttu-id="e2367-183">這個方法會變更 **MaxConnections** 和 **UnlimitedConnections** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-183">This method changes the **MaxConnections** and **UnlimitedConnections** properties.</span></span><br/>                                                                                                |
| [<span data-ttu-id="e2367-184">**SetSslBridging**</span><span class="sxs-lookup"><span data-stu-id="e2367-184">**SetSslBridging**</span></span>](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="e2367-185">設定 RD 閘道伺服器所使用的 SSL 橋接類型。</span><span class="sxs-lookup"><span data-stu-id="e2367-185">Sets the type of SSL bridging to be used by the RD Gateway server.</span></span><br/> <span data-ttu-id="e2367-186">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-186">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="e2367-187">**TSGRemoveAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="e2367-187">**TSGRemoveAdminMsg**</span></span>](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="e2367-188">移除閘道伺服器的系統管理訊息。</span><span class="sxs-lookup"><span data-stu-id="e2367-188">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="e2367-189">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-189">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="e2367-190">**TSGRemoveConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="e2367-190">**TSGRemoveConsentMsg**</span></span>](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | <span data-ttu-id="e2367-191">移除閘道伺服器的系統管理訊息。</span><span class="sxs-lookup"><span data-stu-id="e2367-191">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="e2367-192">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-192">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="e2367-193">**TSGStoreAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="e2367-193">**TSGStoreAdminMsg**</span></span>](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="e2367-194">更新閘道伺服器的系統管理訊息。</span><span class="sxs-lookup"><span data-stu-id="e2367-194">Updates the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="e2367-195">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-195">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="e2367-196">**TSGStoreConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="e2367-196">**TSGStoreConsentMsg**</span></span>](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="e2367-197">更新閘道伺服器的同意訊息。</span><span class="sxs-lookup"><span data-stu-id="e2367-197">Updates the consent message for the gateway server.</span></span><br/> <span data-ttu-id="e2367-198">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e2367-198">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="e2367-199">屬性</span><span class="sxs-lookup"><span data-stu-id="e2367-199">Properties</span></span>

<span data-ttu-id="e2367-200">**Win32 \_ TSGatewayServerSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-200">The **Win32\_TSGatewayServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2367-201">**adminMessageEndTime**</span><span class="sxs-lookup"><span data-stu-id="e2367-201">**adminMessageEndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-204">系統管理訊息的結束時間。</span><span class="sxs-lookup"><span data-stu-id="e2367-204">The administrative message end time.</span></span>

<span data-ttu-id="e2367-205">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-205">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-206">**adminMessageStartTime**</span><span class="sxs-lookup"><span data-stu-id="e2367-206">**adminMessageStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-209">管理訊息開始時間。</span><span class="sxs-lookup"><span data-stu-id="e2367-209">The administrative message start time.</span></span>

<span data-ttu-id="e2367-210">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-210">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-211">**adminMessageText**</span><span class="sxs-lookup"><span data-stu-id="e2367-211">**adminMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-212">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-214">系統管理郵件內文。</span><span class="sxs-lookup"><span data-stu-id="e2367-214">The administrative message text.</span></span>

<span data-ttu-id="e2367-215">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-215">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-216">**AuthenticationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="e2367-216">**AuthenticationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-219">目前驗證外掛程式的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="e2367-219">The CLSID of the current authentication plug-in.</span></span>

<span data-ttu-id="e2367-220">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-220">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-221">**AuthenticationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="e2367-221">**AuthenticationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-224">目前驗證外掛程式的描述。</span><span class="sxs-lookup"><span data-stu-id="e2367-224">The description of the current authentication plug-in.</span></span>

<span data-ttu-id="e2367-225">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-225">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-226">**AuthenticationPluginName**</span><span class="sxs-lookup"><span data-stu-id="e2367-226">**AuthenticationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-229">目前驗證外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2367-229">The name of the current authentication plug-in.</span></span>

<span data-ttu-id="e2367-230">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-230">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-231">**AuthorizationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="e2367-231">**AuthorizationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-234">目前授權外掛程式的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="e2367-234">The CLSID of the current authorization plug-in.</span></span>

<span data-ttu-id="e2367-235">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-235">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-236">**AuthorizationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="e2367-236">**AuthorizationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-239">目前授權外掛程式的描述。</span><span class="sxs-lookup"><span data-stu-id="e2367-239">The description of the current authorization plug-in.</span></span>

<span data-ttu-id="e2367-240">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-240">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-241">**AuthorizationPluginName**</span><span class="sxs-lookup"><span data-stu-id="e2367-241">**AuthorizationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-244">目前授權外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2367-244">The name of the current authorization plug-in.</span></span>

<span data-ttu-id="e2367-245">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-245">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-246">**CentralCAPEnabled**</span><span class="sxs-lookup"><span data-stu-id="e2367-246">**CentralCAPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-247">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2367-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-249">指定是否使用中央 RD CAP 伺服器來控制這部伺服器。</span><span class="sxs-lookup"><span data-stu-id="e2367-249">Specifies whether central RD CAP servers are used for controlling this server.</span></span> <span data-ttu-id="e2367-250">您可以藉由呼叫 [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) 方法來變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-250">This property can be changed by calling the [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-251">**CertHash**</span><span class="sxs-lookup"><span data-stu-id="e2367-251">**CertHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-252">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="e2367-252">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e2367-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-254">在 IIS 中為埠443上的 HTTPS 系結指定憑證雜湊。</span><span class="sxs-lookup"><span data-stu-id="e2367-254">Specifies the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

<span data-ttu-id="e2367-255">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-255">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-256">**consentMessageText**</span><span class="sxs-lookup"><span data-stu-id="e2367-256">**consentMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-259">同意郵件內文。</span><span class="sxs-lookup"><span data-stu-id="e2367-259">The consent message text.</span></span>

<span data-ttu-id="e2367-260">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-260">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-261">**EnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="e2367-261">**EnforceChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-262">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2367-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-264">指出是否針對 HTTP 傳輸強制執行通道系結。</span><span class="sxs-lookup"><span data-stu-id="e2367-264">Indicates if channel binding is enforced for the HTTP transport.</span></span> <span data-ttu-id="e2367-265">您可以使用 [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) 方法來變更這個屬性值。</span><span class="sxs-lookup"><span data-stu-id="e2367-265">This property value can be changed by using the [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) method.</span></span>

<span data-ttu-id="e2367-266">**Windows server 2008 R2 和 Windows server 2008：** 此屬性在 Windows Server 2012 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-266">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available before Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-267">**IsConfigured**</span><span class="sxs-lookup"><span data-stu-id="e2367-267">**IsConfigured**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-268">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2367-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-270">指定是否設定 RD 閘道服務所需的 IIS 和 RPC 設定。</span><span class="sxs-lookup"><span data-stu-id="e2367-270">Specifies if IIS and RPC settings required by the RD Gateway service are configured.</span></span>

<span data-ttu-id="e2367-271">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-271">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-272">**MaxConnections**</span><span class="sxs-lookup"><span data-stu-id="e2367-272">**MaxConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-273">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2367-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2367-275">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e2367-275">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e2367-276">傳回透過 RD 閘道允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="e2367-276">Returns the maximum number of connections that are allowed through RD Gateway.</span></span> <span data-ttu-id="e2367-277">您可以使用 [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-277">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-278">**MaximumAllowedConnectionsBySku**</span><span class="sxs-lookup"><span data-stu-id="e2367-278">**MaximumAllowedConnectionsBySku**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-279">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2367-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-281">庫存單位 (SKU) 允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="e2367-281">Maximum number of connections that the stock-keeping unit (SKU) allows.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-282">**MaxLogEvents**</span><span class="sxs-lookup"><span data-stu-id="e2367-282">**MaxLogEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-283">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2367-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-285">傳回記錄事件的最大數目。</span><span class="sxs-lookup"><span data-stu-id="e2367-285">Returns the maximum number of log events.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-286">**MaxProtocols**</span><span class="sxs-lookup"><span data-stu-id="e2367-286">**MaxProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-287">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2367-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-289">RD 閘道支援的通訊協定數目。</span><span class="sxs-lookup"><span data-stu-id="e2367-289">Number of protocols supported by RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-290">**OnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="e2367-290">**OnlyConsentCapableClients**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-291">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2367-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-293">指定是否只允許用戶端能夠同意訊息連接到 RD 閘道。</span><span class="sxs-lookup"><span data-stu-id="e2367-293">Specifies if only clients capable of consent messages are allowed to connect to the RD Gateway.</span></span>

<span data-ttu-id="e2367-294">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-294">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="e2367-295">零</span><span class="sxs-lookup"><span data-stu-id="e2367-295">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="e2367-296">只有同意訊息可供用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="e2367-296">Only consent message capable clients can connect.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-297">零</span><span class="sxs-lookup"><span data-stu-id="e2367-297">zero</span></span>
</dt> <dd>

<span data-ttu-id="e2367-298">未同意訊息的用戶端也可以連接。</span><span class="sxs-lookup"><span data-stu-id="e2367-298">Clients that are not consent message capable can also connect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e2367-299">**RequestSOH**</span><span class="sxs-lookup"><span data-stu-id="e2367-299">**RequestSOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-300">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2367-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-302">從 Windows Server 2016 開始不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-302">This property is not supported starting with Windows Server 2016.</span></span>

<span data-ttu-id="e2367-303">\* \* Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2 和 Windows Server 2008： \* \*</span><span class="sxs-lookup"><span data-stu-id="e2367-303">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="e2367-304">指定伺服器是否必須要求來自用戶端的健全狀況聲明 (SoH) 。</span><span class="sxs-lookup"><span data-stu-id="e2367-304">Specifies whether the server must request a Statement of Health (SoH) from the client.</span></span> <span data-ttu-id="e2367-305">您可以使用 [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) 方法來變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-305">This property can be changed by using the [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-306">**SkuName**</span><span class="sxs-lookup"><span data-stu-id="e2367-306">**SkuName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e2367-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-309">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2367-309">Name of the SKU.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-310">**SslBridging**</span><span class="sxs-lookup"><span data-stu-id="e2367-310">**SslBridging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-311">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e2367-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-313">指定 RD 閘道伺服器所使用的 SSL 橋接類型。</span><span class="sxs-lookup"><span data-stu-id="e2367-313">Specifies which type of SSL bridging to be used by the RD Gateway server.</span></span> <span data-ttu-id="e2367-314">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e2367-314">This can be one of the following values.</span></span>

<span data-ttu-id="e2367-315">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="e2367-315">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="e2367-316">0</span><span class="sxs-lookup"><span data-stu-id="e2367-316">0</span></span>
</dt> <dd>

<span data-ttu-id="e2367-317">無 SSL 橋接。</span><span class="sxs-lookup"><span data-stu-id="e2367-317">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-318">1</span><span class="sxs-lookup"><span data-stu-id="e2367-318">1</span></span>
</dt> <dd>

<span data-ttu-id="e2367-319">HTTPS 至 HTTP 橋接。</span><span class="sxs-lookup"><span data-stu-id="e2367-319">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="e2367-320">2</span><span class="sxs-lookup"><span data-stu-id="e2367-320">2</span></span>
</dt> <dd>

<span data-ttu-id="e2367-321">HTTPS 至 HTTPS 橋接。</span><span class="sxs-lookup"><span data-stu-id="e2367-321">HTTPS to HTTPS bridging.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e2367-322">**UnlimitedConnections**</span><span class="sxs-lookup"><span data-stu-id="e2367-322">**UnlimitedConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2367-323">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e2367-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2367-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e2367-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2367-325">指出是否允許透過 RD 閘道的連接數目不限。</span><span class="sxs-lookup"><span data-stu-id="e2367-325">Indicates whether an unlimited number of connections are allowed through RD Gateway.</span></span> <span data-ttu-id="e2367-326">您可以使用 [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e2367-326">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2367-327">備註</span><span class="sxs-lookup"><span data-stu-id="e2367-327">Remarks</span></span>

<span data-ttu-id="e2367-328">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="e2367-328">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="e2367-329">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e2367-329">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e2367-330">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e2367-330">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e2367-331">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e2367-331">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e2367-332">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e2367-332">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2367-333">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2367-333">Requirements</span></span>



| <span data-ttu-id="e2367-334">需求</span><span class="sxs-lookup"><span data-stu-id="e2367-334">Requirement</span></span> | <span data-ttu-id="e2367-335">值</span><span class="sxs-lookup"><span data-stu-id="e2367-335">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2367-336">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2367-336">Minimum supported client</span></span><br/> | <span data-ttu-id="e2367-337">都不支援</span><span class="sxs-lookup"><span data-stu-id="e2367-337">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e2367-338">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2367-338">Minimum supported server</span></span><br/> | <span data-ttu-id="e2367-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2367-339">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e2367-340">命名空間</span><span class="sxs-lookup"><span data-stu-id="e2367-340">Namespace</span></span><br/>                | <span data-ttu-id="e2367-341">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e2367-341">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e2367-342">MOF</span><span class="sxs-lookup"><span data-stu-id="e2367-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2367-343"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2367-343"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2367-344">DLL</span><span class="sxs-lookup"><span data-stu-id="e2367-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2367-345"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2367-345"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e2367-346">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2367-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2367-347">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="e2367-347">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="e2367-348">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2367-348">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="e2367-349">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="e2367-349">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="e2367-350">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="e2367-350">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="e2367-351">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2367-351">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="e2367-352">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="e2367-352">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

