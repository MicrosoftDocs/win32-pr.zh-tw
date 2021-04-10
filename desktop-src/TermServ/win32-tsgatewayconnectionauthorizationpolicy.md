---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別
description: 描述 (RD \ 160; 的遠端桌面連線授權原則。端點) 。 RD \ 160;CAPs 可用來判斷是否允許使用者連接到遠端桌面閘道 (RD 閘道) server。
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27384ec3a5f17c3e41fe0ceccf0ee1f7f9d08044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843460"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="4fa94-106">Win32 \_ TSGatewayConnectionAuthorizationPolicy 類別</span><span class="sxs-lookup"><span data-stu-id="4fa94-106">Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="4fa94-107">描述 (RD CAP) 的遠端桌面連線授權原則。</span><span class="sxs-lookup"><span data-stu-id="4fa94-107">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="4fa94-108">RD Cap 用來判斷是否允許使用者連線至遠端桌面閘道 (RD 閘道) server。</span><span class="sxs-lookup"><span data-stu-id="4fa94-108">RD CAPs are used to determine whether a user is allowed to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa94-109">語法</span><span class="sxs-lookup"><span data-stu-id="4fa94-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a><span data-ttu-id="4fa94-110">成員</span><span class="sxs-lookup"><span data-stu-id="4fa94-110">Members</span></span>

<span data-ttu-id="4fa94-111">**Win32 \_ TSGatewayConnectionAuthorizationPolicy** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4fa94-111">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="4fa94-112">方法</span><span class="sxs-lookup"><span data-stu-id="4fa94-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4fa94-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4fa94-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4fa94-114">方法</span><span class="sxs-lookup"><span data-stu-id="4fa94-114">Methods</span></span>

<span data-ttu-id="4fa94-115">**Win32 \_ TSGatewayConnectionAuthorizationPolicy** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4fa94-115">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="4fa94-116">方法</span><span class="sxs-lookup"><span data-stu-id="4fa94-116">Method</span></span>                                                                                                                | <span data-ttu-id="4fa94-117">描述</span><span class="sxs-lookup"><span data-stu-id="4fa94-117">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4fa94-118">**AddComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="4fa94-118">**AddComputerGroupNames**</span></span>](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="4fa94-119">將指定的電腦群組名加入至 **ComputerGroupNames** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-119">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span><br/>                                                                                      |
| [<span data-ttu-id="4fa94-120">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="4fa94-120">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="4fa94-121">將指定的使用者組名加入至 **UserGroupNames** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-121">Adds the specified user group names to the **UserGroupNames** property.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4fa94-122">**建立**</span><span class="sxs-lookup"><span data-stu-id="4fa94-122">**Create**</span></span>](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="4fa94-123">建立 RD CAP。</span><span class="sxs-lookup"><span data-stu-id="4fa94-123">Creates an RD CAP.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="4fa94-124">**刪除**</span><span class="sxs-lookup"><span data-stu-id="4fa94-124">**Delete**</span></span>](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="4fa94-125">刪除目前的 RD CAP。</span><span class="sxs-lookup"><span data-stu-id="4fa94-125">Deletes the current RD CAP.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="4fa94-126">**DisableClipboard**</span><span class="sxs-lookup"><span data-stu-id="4fa94-126">**DisableClipboard**</span></span>](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | <span data-ttu-id="4fa94-127">設定 **ClipboardDisabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-127">Sets the **ClipboardDisabled** property.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="4fa94-128">**DisableDiskDrives**</span><span class="sxs-lookup"><span data-stu-id="4fa94-128">**DisableDiskDrives**</span></span>](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="4fa94-129">設定 **DiskDrivesDisabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-129">Sets the **DiskDrivesDisabled** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="4fa94-130">**DisablePlugAndPlayDevices**</span><span class="sxs-lookup"><span data-stu-id="4fa94-130">**DisablePlugAndPlayDevices**</span></span>](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | <span data-ttu-id="4fa94-131">設定 **PlugAndPlayDevicesDisabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-131">Sets the **PlugAndPlayDevicesDisabled** property.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="4fa94-132">**DisablePrinters**</span><span class="sxs-lookup"><span data-stu-id="4fa94-132">**DisablePrinters**</span></span>](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | <span data-ttu-id="4fa94-133">設定 **PrintersDisabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-133">Sets the **PrintersDisabled** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="4fa94-134">**DisableSerialPorts**</span><span class="sxs-lookup"><span data-stu-id="4fa94-134">**DisableSerialPorts**</span></span>](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="4fa94-135">設定 **SerialPortsDisabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-135">Sets the **SerialPortsDisabled** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="4fa94-136">**EnableAllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="4fa94-136">**EnableAllowOnlySDRServers**</span></span>](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | <span data-ttu-id="4fa94-137">用來切換 **AllowOnlySDRServers** 屬性</span><span class="sxs-lookup"><span data-stu-id="4fa94-137">Used to toggle the **AllowOnlySDRServers** property</span></span><br/> <span data-ttu-id="4fa94-138">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="4fa94-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                  |
| [<span data-ttu-id="4fa94-139">**MoveDown**</span><span class="sxs-lookup"><span data-stu-id="4fa94-139">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | <span data-ttu-id="4fa94-140">將目前 RD CAP 在清單中向下移動一個位置。</span><span class="sxs-lookup"><span data-stu-id="4fa94-140">Moves the current RD CAP one position down in the list.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="4fa94-141">**上移**</span><span class="sxs-lookup"><span data-stu-id="4fa94-141">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="4fa94-142">將目前 RD CAP 在清單中向上移動一個位置。</span><span class="sxs-lookup"><span data-stu-id="4fa94-142">Moves the current RD CAP one position up in the list.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="4fa94-143">**RemoveComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="4fa94-143">**RemoveComputerGroupNames**</span></span>](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="4fa94-144">從 **ComputerGroupNames** 屬性中移除指定的電腦群組名。</span><span class="sxs-lookup"><span data-stu-id="4fa94-144">Removes the specified computer group names from the **ComputerGroupNames** property.</span></span><br/>                                                                                 |
| [<span data-ttu-id="4fa94-145">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="4fa94-145">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | <span data-ttu-id="4fa94-146">從 **UserGroupNames** 屬性中移除指定的使用者組名。</span><span class="sxs-lookup"><span data-stu-id="4fa94-146">Removes specified user group names from the **UserGroupNames** property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="4fa94-147">**SetComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="4fa94-147">**SetComputerGroupNames**</span></span>](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | <span data-ttu-id="4fa94-148">設定 **ComputerGroupNames** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-148">Sets the **ComputerGroupNames** property.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="4fa94-149">**SetCookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="4fa94-149">**SetCookieAuthenticationAllowed**</span></span>](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | <span data-ttu-id="4fa94-150">設定 **CookieAuthenticationAllowed** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-150">Sets the **CookieAuthenticationAllowed** property.</span></span><br/> <span data-ttu-id="4fa94-151">**Windows Server 2008：** 無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="4fa94-151">**Windows Server 2008:** This method is not available.</span></span><br/>                                                 |
| [<span data-ttu-id="4fa94-152">**SetDeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="4fa94-152">**SetDeviceRedirectionType**</span></span>](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | <span data-ttu-id="4fa94-153">設定 **DeviceRedirectionType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-153">Sets the **DeviceRedirectionType** property.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="4fa94-154">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="4fa94-154">**SetEnabled**</span></span>](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | <span data-ttu-id="4fa94-155">啟用或停用目前的 RD CAP。</span><span class="sxs-lookup"><span data-stu-id="4fa94-155">Enables or disables the current RD CAP.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="4fa94-156">**SetIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="4fa94-156">**SetIdleTimeout**</span></span>](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | <span data-ttu-id="4fa94-157">設定 **IdleTimeout** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-157">Sets the **IdleTimeout** property.</span></span><br/> <span data-ttu-id="4fa94-158">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="4fa94-158">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                   |
| [<span data-ttu-id="4fa94-159">**SetName**</span><span class="sxs-lookup"><span data-stu-id="4fa94-159">**SetName**</span></span>](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | <span data-ttu-id="4fa94-160">為此 RD CAP 設定新的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fa94-160">Sets a new name for this RD CAP.</span></span> <span data-ttu-id="4fa94-161">這個方法會確保名稱是唯一的。</span><span class="sxs-lookup"><span data-stu-id="4fa94-161">This method ensures that names will be unique.</span></span><br/>                                                                                      |
| [<span data-ttu-id="4fa94-162">**SetPasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="4fa94-162">**SetPasswordAllowed**</span></span>](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="4fa94-163">設定 **PasswordAllowed** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-163">Sets the **PasswordAllowed** property.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="4fa94-164">**SetSecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="4fa94-164">**SetSecureIdAllowed**</span></span>](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | <span data-ttu-id="4fa94-165">設定 **SecureIdAllowed** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-165">Sets the **SecureIdAllowed** property.</span></span><br/> <span data-ttu-id="4fa94-166">**Windows Server 2008：** 這個方法會保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="4fa94-166">**Windows Server 2008:** This method is reserved for future use.</span></span><br/>                                                   |
| [<span data-ttu-id="4fa94-167">**SetSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="4fa94-167">**SetSessionTimeout**</span></span>](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="4fa94-168">設定 **SessionTimeout** 和 **SessionTimeoutAction** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-168">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span><br/> <span data-ttu-id="4fa94-169">**Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="4fa94-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/> |
| [<span data-ttu-id="4fa94-170">**SetSmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="4fa94-170">**SetSmartcardAllowed**</span></span>](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | <span data-ttu-id="4fa94-171">設定 **SmartcardAllowed** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-171">Sets the **SmartcardAllowed** property.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="4fa94-172">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="4fa94-172">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | <span data-ttu-id="4fa94-173">設定 **UserGroupNames** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-173">Sets the **UserGroupNames** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="4fa94-174">**更新**</span><span class="sxs-lookup"><span data-stu-id="4fa94-174">**Update**</span></span>](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | <span data-ttu-id="4fa94-175">更新目前的 RD CAP。</span><span class="sxs-lookup"><span data-stu-id="4fa94-175">Updates the current RD CAP.</span></span><br/>                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="4fa94-176">屬性</span><span class="sxs-lookup"><span data-stu-id="4fa94-176">Properties</span></span>

<span data-ttu-id="4fa94-177">**Win32 \_ TSGatewayConnectionAuthorizationPolicy** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-177">The **Win32\_TSGatewayConnectionAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fa94-178">**AllowOnlySDRServers**</span><span class="sxs-lookup"><span data-stu-id="4fa94-178">**AllowOnlySDRServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-179">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-181">指出連接是否只允許安全的裝置重新導向 (SDR) RDS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4fa94-181">Indicates whether connections allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="4fa94-182">您可以使用 [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-182">This property can be set using the [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) method.</span></span>

<span data-ttu-id="4fa94-183">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="4fa94-183">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-184">**ClipboardDisabled**</span><span class="sxs-lookup"><span data-stu-id="4fa94-184">**ClipboardDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-185">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-187">指出是否將停用剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="4fa94-187">Indicates if clipboard redirection will be disabled.</span></span> <span data-ttu-id="4fa94-188">只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。</span><span class="sxs-lookup"><span data-stu-id="4fa94-188">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-189">**ComputerGroupNames**</span><span class="sxs-lookup"><span data-stu-id="4fa94-189">**ComputerGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fa94-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-192">分號分隔的電腦群組名清單。</span><span class="sxs-lookup"><span data-stu-id="4fa94-192">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="4fa94-193">這個值可以是空的。</span><span class="sxs-lookup"><span data-stu-id="4fa94-193">This value can be empty.</span></span> <span data-ttu-id="4fa94-194">名稱的格式為 *網域 \\ ComputerGroupName*。</span><span class="sxs-lookup"><span data-stu-id="4fa94-194">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="4fa94-195">如果指定了值，用戶端電腦必須屬於其中一個電腦群組，使用者才能存取 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="4fa94-195">If a value is specified, then the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-196">**CookieAuthenticationAllowed**</span><span class="sxs-lookup"><span data-stu-id="4fa94-196">**CookieAuthenticationAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-197">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-199">指出是否可以使用 cookie 驗證連接到 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="4fa94-199">Indicates if cookie authentication can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="4fa94-200">您可以使用 [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-200">This property can be set by using the [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="4fa94-201">**Windows Server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-201">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-202">**DeviceRedirectionType**</span><span class="sxs-lookup"><span data-stu-id="4fa94-202">**DeviceRedirectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-203">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4fa94-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-205">指定將會重新導向的裝置。</span><span class="sxs-lookup"><span data-stu-id="4fa94-205">Specifies which devices will be redirected.</span></span>

<dt>

<span data-ttu-id="4fa94-206">0</span><span class="sxs-lookup"><span data-stu-id="4fa94-206">0</span></span>
</dt> <dd>

<span data-ttu-id="4fa94-207">將會重新導向所有裝置。</span><span class="sxs-lookup"><span data-stu-id="4fa94-207">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-208">1</span><span class="sxs-lookup"><span data-stu-id="4fa94-208">1</span></span>
</dt> <dd>

<span data-ttu-id="4fa94-209">將不會重新導向任何裝置。</span><span class="sxs-lookup"><span data-stu-id="4fa94-209">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-210">2</span><span class="sxs-lookup"><span data-stu-id="4fa94-210">2</span></span>
</dt> <dd>

<span data-ttu-id="4fa94-211">將不會重新導向指定的裝置。</span><span class="sxs-lookup"><span data-stu-id="4fa94-211">Specified devices will not be redirected.</span></span> <span data-ttu-id="4fa94-212">**DiskDrivesDisabled**、 **PrintersDisabled**、 **SerialPortsDisabled**、 **ClipboardDisabled** 和 **PlugAndPlayDevicesDisabled** 屬性控制哪些裝置將不會被重新導向。</span><span class="sxs-lookup"><span data-stu-id="4fa94-212">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4fa94-213">**DiskDrivesDisabled**</span><span class="sxs-lookup"><span data-stu-id="4fa94-213">**DiskDrivesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-214">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-216">指出是否將停用磁片磁碟機重新導向。</span><span class="sxs-lookup"><span data-stu-id="4fa94-216">Indicates if disk drive redirection will be disabled.</span></span> <span data-ttu-id="4fa94-217">只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。</span><span class="sxs-lookup"><span data-stu-id="4fa94-217">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-218">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="4fa94-218">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-219">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-221">指出此 RD CAP 是否將用來評估使用者的授權。</span><span class="sxs-lookup"><span data-stu-id="4fa94-221">Indicates whether this RD CAP will be used to evaluate a user for authorization.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-222">**HasNapAttributes**</span><span class="sxs-lookup"><span data-stu-id="4fa94-222">**HasNapAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-223">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-225">指出 RD CAP 是否 (NAP) 屬性使用網路存取保護。</span><span class="sxs-lookup"><span data-stu-id="4fa94-225">Indicates if the RD CAP uses Network Access Protection (NAP) attributes.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-226">**IdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="4fa94-226">**IdleTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-227">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4fa94-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-229">閒置的超時值（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="4fa94-229">The idle timeout value, in minutes.</span></span> <span data-ttu-id="4fa94-230">值為0表示沒有任何超時時間。</span><span class="sxs-lookup"><span data-stu-id="4fa94-230">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="4fa94-231">您可以使用 [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-231">This property can be set by using the [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="4fa94-232">**Windows Server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-232">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-233">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4fa94-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fa94-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-236">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4fa94-236">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-237">RD CAP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fa94-237">Name of the RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-238">**順序**</span><span class="sxs-lookup"><span data-stu-id="4fa94-238">**Order**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-239">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4fa94-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-241">RD CAP 的評估順序。</span><span class="sxs-lookup"><span data-stu-id="4fa94-241">Evaluation order of the RD CAP.</span></span> <span data-ttu-id="4fa94-242">第一個評估 RD CAP 的值為 "1"。</span><span class="sxs-lookup"><span data-stu-id="4fa94-242">The first RD CAP evaluated has a value of "1".</span></span> <span data-ttu-id="4fa94-243">呼叫 [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md)、 [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)、[**上移**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)或 [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)方法時，可以變更 **Order** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-243">The **Order** property can be changed when the [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md), or [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-244">**PasswordAllowed**</span><span class="sxs-lookup"><span data-stu-id="4fa94-244">**PasswordAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-245">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-247">指出是否可以使用密碼連接到 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="4fa94-247">Indicates if a password can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="4fa94-248">您可以使用 [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-248">This property can be changed by using the [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-249">**PlugAndPlayDevicesDisabled**</span><span class="sxs-lookup"><span data-stu-id="4fa94-249">**PlugAndPlayDevicesDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-250">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-252">指出是否將停用隨插即用裝置的重新導向。</span><span class="sxs-lookup"><span data-stu-id="4fa94-252">Indicates if redirection of Plug and Play devices will be disabled.</span></span> <span data-ttu-id="4fa94-253">只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。</span><span class="sxs-lookup"><span data-stu-id="4fa94-253">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-254">**PrintersDisabled**</span><span class="sxs-lookup"><span data-stu-id="4fa94-254">**PrintersDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-255">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-257">指出是否將停用印表機重新導向。</span><span class="sxs-lookup"><span data-stu-id="4fa94-257">Indicates if printer redirection will be disabled.</span></span> <span data-ttu-id="4fa94-258">只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。</span><span class="sxs-lookup"><span data-stu-id="4fa94-258">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-259">**SecureIdAllowed**</span><span class="sxs-lookup"><span data-stu-id="4fa94-259">**SecureIdAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-260">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-260">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-262">指出是否可以使用安全識別碼來連接 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="4fa94-262">Indicates if a secure identifier can be used to connect to the RD Gateway server.</span></span>

<span data-ttu-id="4fa94-263">**Windows Server 2008：** 未使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-263">**Windows Server 2008:** This property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-264">**SerialPortsDisabled**</span><span class="sxs-lookup"><span data-stu-id="4fa94-264">**SerialPortsDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-265">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-267">指出是否將停用序列埠重新導向。</span><span class="sxs-lookup"><span data-stu-id="4fa94-267">Indicates if serial port redirection will be disabled.</span></span> <span data-ttu-id="4fa94-268">只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。</span><span class="sxs-lookup"><span data-stu-id="4fa94-268">This property has an effect only if the **DeviceRedirectionType** property has a value of "2".</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-269">**SessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="4fa94-269">**SessionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-270">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4fa94-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-272">會話超時值（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="4fa94-272">The session timeout value, in minutes.</span></span> <span data-ttu-id="4fa94-273">值為0表示沒有任何超時時間。</span><span class="sxs-lookup"><span data-stu-id="4fa94-273">A value of 0 means there is no timeout.</span></span> <span data-ttu-id="4fa94-274">您可以使用 [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-274">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="4fa94-275">**Windows Server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-275">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-276">**SessionTimeoutAction**</span><span class="sxs-lookup"><span data-stu-id="4fa94-276">**SessionTimeoutAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-277">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4fa94-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-279">指定會話超時時要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="4fa94-279">Specifies the action to be taken in the case of a session timeout.</span></span> <span data-ttu-id="4fa94-280">您可以使用 [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-280">This property can be set by using the [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

<span data-ttu-id="4fa94-281">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4fa94-281">This can be one of the following values.</span></span>

<span data-ttu-id="4fa94-282">**Windows Server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-282">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="4fa94-283">0</span><span class="sxs-lookup"><span data-stu-id="4fa94-283">0</span></span>
</dt> <dd>

<span data-ttu-id="4fa94-284">中斷會話的連線。</span><span class="sxs-lookup"><span data-stu-id="4fa94-284">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-285">1</span><span class="sxs-lookup"><span data-stu-id="4fa94-285">1</span></span>
</dt> <dd>

<span data-ttu-id="4fa94-286">嘗試重新授權會話。</span><span class="sxs-lookup"><span data-stu-id="4fa94-286">Attempt to re-authorize the session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4fa94-287">**SmartcardAllowed**</span><span class="sxs-lookup"><span data-stu-id="4fa94-287">**SmartcardAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-288">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fa94-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-290">指出是否可以使用智慧卡來連接 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="4fa94-290">Indicates if a smart card can be used to connect to the RD Gateway server.</span></span> <span data-ttu-id="4fa94-291">您可以使用 [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa94-291">This property can be changed by using the [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="4fa94-292">**UserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="4fa94-292">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fa94-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fa94-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fa94-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa94-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fa94-295">分號分隔的使用者組名清單。</span><span class="sxs-lookup"><span data-stu-id="4fa94-295">List of semicolon-separated user group names.</span></span> <span data-ttu-id="4fa94-296">名稱的格式為 *網域 \\ UserGroupName*。</span><span class="sxs-lookup"><span data-stu-id="4fa94-296">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="4fa94-297">如果使用者隸屬于這些使用者群組中的任何一項，則會允許使用者存取 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="4fa94-297">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fa94-298">備註</span><span class="sxs-lookup"><span data-stu-id="4fa94-298">Remarks</span></span>

<span data-ttu-id="4fa94-299">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="4fa94-299">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="4fa94-300">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4fa94-300">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4fa94-301">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4fa94-301">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4fa94-302">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4fa94-302">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4fa94-303">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="4fa94-303">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa94-304">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fa94-304">Requirements</span></span>



| <span data-ttu-id="4fa94-305">需求</span><span class="sxs-lookup"><span data-stu-id="4fa94-305">Requirement</span></span> | <span data-ttu-id="4fa94-306">值</span><span class="sxs-lookup"><span data-stu-id="4fa94-306">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa94-307">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fa94-307">Minimum supported client</span></span><br/> | <span data-ttu-id="4fa94-308">都不支援</span><span class="sxs-lookup"><span data-stu-id="4fa94-308">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4fa94-309">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fa94-309">Minimum supported server</span></span><br/> | <span data-ttu-id="4fa94-310">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fa94-310">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4fa94-311">命名空間</span><span class="sxs-lookup"><span data-stu-id="4fa94-311">Namespace</span></span><br/>                | <span data-ttu-id="4fa94-312">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="4fa94-312">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4fa94-313">MOF</span><span class="sxs-lookup"><span data-stu-id="4fa94-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fa94-314"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fa94-314"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fa94-315">DLL</span><span class="sxs-lookup"><span data-stu-id="4fa94-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fa94-316"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fa94-316"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4fa94-317">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fa94-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa94-318">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="4fa94-318">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="4fa94-319">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="4fa94-319">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="4fa94-320">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="4fa94-320">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="4fa94-321">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="4fa94-321">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="4fa94-322">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="4fa94-322">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="4fa94-323">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="4fa94-323">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

