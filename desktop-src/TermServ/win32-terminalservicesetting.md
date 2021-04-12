---
title: Win32_TerminalServiceSetting 類別
description: 代表遠端桌面工作階段主機 (RD 工作階段主機) server 的設定。
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceSetting 類別遠端桌面服務
- Win32_TerminalServiceSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317423"
---
# <a name="win32_terminalservicesetting-class"></a><span data-ttu-id="0e261-105">Win32 \_ TerminalServiceSetting 類別</span><span class="sxs-lookup"><span data-stu-id="0e261-105">Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="0e261-106">**Win32 \_ TerminalServiceSetting** WMI 類別代表遠端桌面工作階段主機 (RD 工作階段主機) server 的設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-106">The **Win32\_TerminalServiceSetting** WMI class represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="0e261-107">設定包括 RD 工作階段主機伺服器模式、授權、Active Desktop、許可權、刪除暫存資料夾，以及會話的臨時目錄等功能。</span><span class="sxs-lookup"><span data-stu-id="0e261-107">Settings include capabilities such as RD Session Host server mode, licensing, Active Desktop, permissions, deletion of temporary folders, and temporary directories for sessions.</span></span>

<span data-ttu-id="0e261-108">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-108">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="0e261-109">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="0e261-109">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e261-110">語法</span><span class="sxs-lookup"><span data-stu-id="0e261-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a><span data-ttu-id="0e261-111">成員</span><span class="sxs-lookup"><span data-stu-id="0e261-111">Members</span></span>

<span data-ttu-id="0e261-112">**Win32 \_ TerminalServiceSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0e261-112">The **Win32\_TerminalServiceSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0e261-113">方法</span><span class="sxs-lookup"><span data-stu-id="0e261-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e261-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0e261-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e261-115">方法</span><span class="sxs-lookup"><span data-stu-id="0e261-115">Methods</span></span>

<span data-ttu-id="0e261-116">**Win32 \_ TerminalServiceSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0e261-116">The **Win32\_TerminalServiceSetting** class has these methods.</span></span>



| <span data-ttu-id="0e261-117">方法</span><span class="sxs-lookup"><span data-stu-id="0e261-117">Method</span></span>                                                                                                                | <span data-ttu-id="0e261-118">描述</span><span class="sxs-lookup"><span data-stu-id="0e261-118">Description</span></span>                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e261-119">**AddDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="0e261-119">**AddDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | <span data-ttu-id="0e261-120">在企業中設定新的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-120">Configures a new license server in the enterprise.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="0e261-121">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e261-121">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | <span data-ttu-id="0e261-122">將指定的授權伺服器新增至指定授權伺服器清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="0e261-122">Adds the given license server to the end of the list of specified license servers.</span></span><br/>                                                                                  |
| [<span data-ttu-id="0e261-123">**CanAccessLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="0e261-123">**CanAccessLicenseServer**</span></span>](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | <span data-ttu-id="0e261-124">判斷 RD 工作階段主機伺服器是否允許從遠端桌面授權伺服器 (RDS Cal) 要求遠端桌面服務用戶端存取授權。</span><span class="sxs-lookup"><span data-stu-id="0e261-124">Determines whether the RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="0e261-125">**ChangeMode**</span><span class="sxs-lookup"><span data-stu-id="0e261-125">**ChangeMode**</span></span>](win32-terminalservicesetting-changemode.md)                                                         | <span data-ttu-id="0e261-126">設定遠端桌面授權伺服器的授權類型。</span><span class="sxs-lookup"><span data-stu-id="0e261-126">Sets the licensing type of the Remote Desktop license server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="0e261-127">**CreateWinstation**</span><span class="sxs-lookup"><span data-stu-id="0e261-127">**CreateWinstation**</span></span>](createwinstation-win32-terminalservicesetting.md)                                             | <span data-ttu-id="0e261-128">根據接聽程式名稱和 NIC 的唯一組合，建立新的接聽程式堆疊。</span><span class="sxs-lookup"><span data-stu-id="0e261-128">Creates a new listener stack based on the unique combination of listener name and NIC.</span></span><br/>                                                                              |
| [<span data-ttu-id="0e261-129">**DeleteDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="0e261-129">**DeleteDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | <span data-ttu-id="0e261-130">從企業刪除指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-130">Deletes the specified license server from the enterprise.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="0e261-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e261-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | <span data-ttu-id="0e261-132">從指定的授權伺服器清單中移除所有授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-132">Removes all license servers from the list of specified license servers.</span></span><br/>                                                                                             |
| [<span data-ttu-id="0e261-133">**FindLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="0e261-133">**FindLicenseServers**</span></span>](findlicenseservers-win32-terminalservicesetting.md)                                         | <span data-ttu-id="0e261-134">列舉所有的遠端桌面授權伺服器和探索方法。</span><span class="sxs-lookup"><span data-stu-id="0e261-134">Enumerates all of the Remote Desktop license servers and the method of discovery.</span></span><br/>                                                                                   |
| [<span data-ttu-id="0e261-135">**GetDomain**</span><span class="sxs-lookup"><span data-stu-id="0e261-135">**GetDomain**</span></span>](getdomain-win32-terminalservicesetting.md)                                                           | <span data-ttu-id="0e261-136">抓取 RD 工作階段主機伺服器為其成員之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e261-136">Retrieves the name of the domain that the RD Session Host server is a member of.</span></span><br/>                                                                                    |
| [<span data-ttu-id="0e261-137">**GetGracePeriodDays**</span><span class="sxs-lookup"><span data-stu-id="0e261-137">**GetGracePeriodDays**</span></span>](getgraceperioddays-win32-terminalservicesetting.md)                                         | <span data-ttu-id="0e261-138">抓取 RD 工作階段主機伺服器 RD 授權寬限期內剩餘的天數。</span><span class="sxs-lookup"><span data-stu-id="0e261-138">Retrieves the number of days that are remaining in the RD Licensing grace period for an RD Session Host server.</span></span><br/>                                                     |
| [<span data-ttu-id="0e261-139">**GetRegisteredLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e261-139">**GetRegisteredLicenseServerList**</span></span>](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | <span data-ttu-id="0e261-140">取得已註冊授權伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="0e261-140">Gets the list of registered license servers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="0e261-141">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e261-141">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="0e261-142">抓取指定授權伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="0e261-142">Retrieves the list of specified license servers.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="0e261-143">**GetTSLanaIds**</span><span class="sxs-lookup"><span data-stu-id="0e261-143">**GetTSLanaIds**</span></span>](gettslanaids-win32-terminalservicesetting.md)                                                     | <span data-ttu-id="0e261-144">取得遠端桌面服務網路介面卡的識別碼和描述。</span><span class="sxs-lookup"><span data-stu-id="0e261-144">Gets the IDs and descriptions of Remote Desktop Services network adapters.</span></span><br/>                                                                                          |
| [<span data-ttu-id="0e261-145">**GetTStoLSConnectivityStatus**</span><span class="sxs-lookup"><span data-stu-id="0e261-145">**GetTStoLSConnectivityStatus**</span></span>](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | <span data-ttu-id="0e261-146">判斷遠端桌面服務與授權伺服器之間的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="0e261-146">Determines the connectivity status between Remote Desktop Services and a license server.</span></span><br/>                                                                            |
| [<span data-ttu-id="0e261-147">**GetWinstationDriverNames**</span><span class="sxs-lookup"><span data-stu-id="0e261-147">**GetWinstationDriverNames**</span></span>](getwinstationdrivernames-win32-terminalservicesetting.md)                             | <span data-ttu-id="0e261-148">抓取 Winstation 驅動程式名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="0e261-148">Retrieves a list of Winstation driver names.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="0e261-149">**PingLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="0e261-149">**PingLicenseServer**</span></span>](pinglicenseserver-win32-terminalservicesetting.md)                                           | <span data-ttu-id="0e261-150">Ping 授權伺服器以判斷它是否為有效的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-150">Pings the license server to determine whether it is a valid license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="0e261-151">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e261-151">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | <span data-ttu-id="0e261-152">從指定的授權伺服器清單中移除指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-152">Removes the given license server from the list of specified license servers.</span></span><br/>                                                                                        |
| [<span data-ttu-id="0e261-153">**SetAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="0e261-153">**SetAllowTSConnections**</span></span>](win32-terminalservicesetting-setallowtsconnections.md)                                   | <span data-ttu-id="0e261-154">設定 **AllowTSConnections** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-154">Sets the **AllowTSConnections** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="0e261-155">**SetDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="0e261-155">**SetDisableForcibleLogoff**</span></span>](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | <span data-ttu-id="0e261-156">設定 **DisableForcibleLogoff** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-156">Sets the **DisableForcibleLogoff** property.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="0e261-157">**SetFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="0e261-157">**SetFallbackPrintDriverType**</span></span>](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | <span data-ttu-id="0e261-158">設定 **FallbackPrintDriverType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-158">Sets the **FallbackPrintDriverType** property.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="0e261-159">**SetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="0e261-159">**SetHomeDirectory**</span></span>](win32-terminalservicesetting-sethomedirectory.md)                                             | <span data-ttu-id="0e261-160">設定 **HomeDirectory** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-160">Sets the **HomeDirectory** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="0e261-161">**SetPolicyPropertyName**</span><span class="sxs-lookup"><span data-stu-id="0e261-161">**SetPolicyPropertyName**</span></span>](win32-terminalservicesetting-setpolicypropertyname.md)                                   | <span data-ttu-id="0e261-162">設定下列其中一個屬性： **DeleteTempFolders** 或 **UseTempFolders**。</span><span class="sxs-lookup"><span data-stu-id="0e261-162">Sets one of the following properties: **DeleteTempFolders** or **UseTempFolders**.</span></span><br/>                                                                                  |
| [<span data-ttu-id="0e261-163">**SetPrimaryLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="0e261-163">**SetPrimaryLicenseServer**</span></span>](setprimarylicenseserver-win32-terminalservicesetting.md)                               | <span data-ttu-id="0e261-164">將指定的授權伺服器設定為指定授權伺服器清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="0e261-164">Sets the given license server as the first entry in the list of specified license servers.</span></span><br/>                                                                          |
| [<span data-ttu-id="0e261-165">**SetProfilePath**</span><span class="sxs-lookup"><span data-stu-id="0e261-165">**SetProfilePath**</span></span>](win32-terminalservicesetting-setprofilepath.md)                                                 | <span data-ttu-id="0e261-166">設定 **ProfilePath** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-166">Sets the **ProfilePath** property.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="0e261-167">**SetSingleSession**</span><span class="sxs-lookup"><span data-stu-id="0e261-167">**SetSingleSession**</span></span>](win32-terminalservicesetting-setsinglesession.md)                                             | <span data-ttu-id="0e261-168">設定 **SingleSession** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-168">Sets the **SingleSession** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="0e261-169">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="0e261-169">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="0e261-170">更新指定授權伺服器的清單，並取代任何現有的指定授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-170">Updates the list of specified license servers, replacing any existing specified license servers.</span></span><br/>                                                                    |
| [<span data-ttu-id="0e261-171">**SetTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="0e261-171">**SetTimeZoneRedirection**</span></span>](win32-terminalservicesetting-settimezoneredirection.md)                                 | <span data-ttu-id="0e261-172">設定 **TimeZoneRedirection** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-172">Sets the **TimeZoneRedirection** property.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="0e261-173">**UpdateDirectConnectLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="0e261-173">**UpdateDirectConnectLicenseServer**</span></span>](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | <span data-ttu-id="0e261-174">更新探索授權伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="0e261-174">Updates the list of discovery license servers.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="0e261-175">屬性</span><span class="sxs-lookup"><span data-stu-id="0e261-175">Properties</span></span>

<span data-ttu-id="0e261-176">**Win32 \_ TerminalServiceSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-176">The **Win32\_TerminalServiceSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e261-177">**ActiveDesktop**</span><span class="sxs-lookup"><span data-stu-id="0e261-177">**ActiveDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-178">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-179">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-180">指定每個使用者會話中是否允許 Active Desktop。</span><span class="sxs-lookup"><span data-stu-id="0e261-180">Specifies whether Active Desktop is allowed in each user session.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0e261-181"><span id="TRUE"></span><span id="true"></span>**TRUE** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-181"><span id="TRUE"></span><span id="true"></span>**TRUE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-182">每個使用者會話中都不允許 Active Desktop。</span><span class="sxs-lookup"><span data-stu-id="0e261-182">Active Desktop is not allowed in each user session.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0e261-183"><span id="FALSE"></span><span id="false"></span>**FALSE** (1) </span><span class="sxs-lookup"><span data-stu-id="0e261-183"><span id="FALSE"></span><span id="false"></span>**FALSE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-184">每個使用者會話中都允許 Active Desktop。</span><span class="sxs-lookup"><span data-stu-id="0e261-184">Active Desktop is allowed in each user session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-185">**AllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="0e261-185">**AllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-186">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-188">指定是否允許新的遠端桌面服務連接。</span><span class="sxs-lookup"><span data-stu-id="0e261-188">Specifies whether new Remote Desktop Services connections are allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0e261-189"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-189"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-190">不允許新的連接。</span><span class="sxs-lookup"><span data-stu-id="0e261-190">New connections are not allowed.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0e261-191"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="0e261-191"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-192">允許新的連接。</span><span class="sxs-lookup"><span data-stu-id="0e261-192">New connections are allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-193">**標題**</span><span class="sxs-lookup"><span data-stu-id="0e261-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e261-196">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0e261-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e261-197">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="0e261-197">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0e261-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0e261-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e261-199">**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="0e261-199">**DeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-200">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-202">指定是否要在結束時刪除臨時目錄。</span><span class="sxs-lookup"><span data-stu-id="0e261-202">Specifies whether temporary directories are deleted on exit.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0e261-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-204">停用臨時目錄的刪除。</span><span class="sxs-lookup"><span data-stu-id="0e261-204">Deletion of temporary directories is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0e261-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="0e261-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-206">已啟用刪除臨時目錄。</span><span class="sxs-lookup"><span data-stu-id="0e261-206">Deletion of temporary directories is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-207">**說明**</span><span class="sxs-lookup"><span data-stu-id="0e261-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-210">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0e261-210">Description of the object.</span></span>

<span data-ttu-id="0e261-211">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0e261-211">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e261-212">**DirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="0e261-212">**DirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e261-215">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e261-215">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e261-216">無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-216">This property is not available.</span></span>

<span data-ttu-id="0e261-217">**Windows Server 2008：** 列舉授權伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="0e261-217">**Windows Server 2008:** Enumerates the list of license servers.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-218">**DisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="0e261-218">**DisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-219">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-221">判斷登入主控台的系統管理員是否可以強制登出。</span><span class="sxs-lookup"><span data-stu-id="0e261-221">Determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span data-ttu-id="0e261-222">0</span><span class="sxs-lookup"><span data-stu-id="0e261-222">0</span></span>
</dt> <dd>

<span data-ttu-id="0e261-223">系統管理員可以強制登出。</span><span class="sxs-lookup"><span data-stu-id="0e261-223">Administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-224">1</span><span class="sxs-lookup"><span data-stu-id="0e261-224">1</span></span>
</dt> <dd>

<span data-ttu-id="0e261-225">系統管理員無法強制登出。</span><span class="sxs-lookup"><span data-stu-id="0e261-225">Administrator cannot be forcibly logged off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-226">**EnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="0e261-226">**EnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-227">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-228">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-229">指定是否要允許遠端桌面連線用戶端在網路連結暫時遺失時，自動重新連線到 RD 工作階段主機伺服器上的會話。</span><span class="sxs-lookup"><span data-stu-id="0e261-229">Specifies whether to allow Remote Desktop connection clients to automatically reconnect to sessions on an RD Session Host server if the network link is temporarily lost.</span></span>

<dt>

<span data-ttu-id="0e261-230">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-230">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-231">自動重新連接已停用。</span><span class="sxs-lookup"><span data-stu-id="0e261-231">Automatic reconnection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-232">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-232">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-233">已啟用自動重新連接。</span><span class="sxs-lookup"><span data-stu-id="0e261-233">Automatic reconnection is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="0e261-234">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-234">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-235">**EnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="0e261-235">**EnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-236">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-237">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-238">指出是否已啟用或停用 (DFSS) 動態公平共用排程。</span><span class="sxs-lookup"><span data-stu-id="0e261-238">Indicates whether dynamic fair-share scheduling (DFSS) is enabled or disabled.</span></span> <span data-ttu-id="0e261-239">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0e261-239">This can be one of the following values.</span></span>

<span data-ttu-id="0e261-240">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="0e261-240">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="0e261-241">0</span><span class="sxs-lookup"><span data-stu-id="0e261-241">0</span></span>
</dt> <dd>

<span data-ttu-id="0e261-242">DFSS 已停用。</span><span class="sxs-lookup"><span data-stu-id="0e261-242">DFSS is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-243">1</span><span class="sxs-lookup"><span data-stu-id="0e261-243">1</span></span>
</dt> <dd>

<span data-ttu-id="0e261-244">DFSS 已啟用。</span><span class="sxs-lookup"><span data-stu-id="0e261-244">DFSS is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-245">**EnableDiskFSS**</span><span class="sxs-lookup"><span data-stu-id="0e261-245">**EnableDiskFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-246">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-247">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-248">指定是否啟用磁片公平共用排程。</span><span class="sxs-lookup"><span data-stu-id="0e261-248">Specifies if disk fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="0e261-249">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-249">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-250">已停用磁片公平共用排程。</span><span class="sxs-lookup"><span data-stu-id="0e261-250">Disk fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-251">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-251">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-252">已啟用磁片公平共用排程。</span><span class="sxs-lookup"><span data-stu-id="0e261-252">Disk fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="0e261-253">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-253">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-254">**EnableNetworkFSS**</span><span class="sxs-lookup"><span data-stu-id="0e261-254">**EnableNetworkFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-255">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-256">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-257">指定是否啟用網路公平共用排程。</span><span class="sxs-lookup"><span data-stu-id="0e261-257">Specifies if network fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="0e261-258">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-258">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-259">網路公平共用排程已停用。</span><span class="sxs-lookup"><span data-stu-id="0e261-259">Network fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-260">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-260">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-261">已啟用網路公平共用排程。</span><span class="sxs-lookup"><span data-stu-id="0e261-261">Network fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="0e261-262">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-262">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-263">**EnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="0e261-263">**EnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-264">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-266">指出是否啟用或停用遠端桌面 MSI。</span><span class="sxs-lookup"><span data-stu-id="0e261-266">Indicates whether the Remote Desktop MSI is enabled or disabled.</span></span>

<dt>

<span data-ttu-id="0e261-267">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-267">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-268">Disabled</span><span class="sxs-lookup"><span data-stu-id="0e261-268">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="0e261-269">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-269">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-270">已啟用</span><span class="sxs-lookup"><span data-stu-id="0e261-270">Enabled</span></span>

</dd> </dl>

<span data-ttu-id="0e261-271">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="0e261-271">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-272">**FallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="0e261-272">**FallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-273">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-275">指定要退回的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0e261-275">Specifies which printer driver to fallback to.</span></span>

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span data-ttu-id="0e261-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**沒有 fallback dirvers = 0** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No fallback dirvers=0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-277">無備用驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0e261-277">No fallback drivers.</span></span>

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span data-ttu-id="0e261-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**最佳猜測 = 1** (1) </span><span class="sxs-lookup"><span data-stu-id="0e261-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Best guess=1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-279">最佳猜測。</span><span class="sxs-lookup"><span data-stu-id="0e261-279">Best guess.</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span data-ttu-id="0e261-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**最佳猜測，如果找不到符合的結果，則會回復至 PCL = 2** (2) </span><span class="sxs-lookup"><span data-stu-id="0e261-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Best guess, if no match is found fallback to PCL=2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-281">最佳猜測。</span><span class="sxs-lookup"><span data-stu-id="0e261-281">Best guess.</span></span> <span data-ttu-id="0e261-282">如果找不到相符項，則會切換回 Hewlett-Packard 印表機控制語言 (PCL) 。</span><span class="sxs-lookup"><span data-stu-id="0e261-282">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span data-ttu-id="0e261-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**最佳猜測，如果找不到相符的結果，請回到 PS = 3** (3) </span><span class="sxs-lookup"><span data-stu-id="0e261-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Best guess, if no match is found fallback to PS=3** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-284">最佳猜測。</span><span class="sxs-lookup"><span data-stu-id="0e261-284">Best guess.</span></span> <span data-ttu-id="0e261-285">如果找不到相符的結果，則會改回 Postscript (PS) 。</span><span class="sxs-lookup"><span data-stu-id="0e261-285">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span data-ttu-id="0e261-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**最佳猜測，如果找不到相符項，則會顯示 PCL 和 PS 驅動程式 = 4** (4) </span><span class="sxs-lookup"><span data-stu-id="0e261-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Best guess, if no match is found show both PCL and PS drivers=4** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-287">最佳猜測。</span><span class="sxs-lookup"><span data-stu-id="0e261-287">Best guess.</span></span> <span data-ttu-id="0e261-288">如果找不到相符的，則會顯示 PS 和 PCL 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0e261-288">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-289">**GetCapabilitiesID**</span><span class="sxs-lookup"><span data-stu-id="0e261-289">**GetCapabilitiesID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-290">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-292">提供者的功能識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e261-292">Capabilities ID for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-293">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="0e261-293">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-296">電腦的根目錄。</span><span class="sxs-lookup"><span data-stu-id="0e261-296">The root directory for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e261-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-298">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0e261-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e261-300">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="0e261-300">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0e261-301">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="0e261-301">The date the object was installed.</span></span> <span data-ttu-id="0e261-302">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="0e261-302">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0e261-303">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0e261-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e261-304">**LicensingDescription**</span><span class="sxs-lookup"><span data-stu-id="0e261-304">**LicensingDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-307">授權模式的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="0e261-307">A brief description of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-308">**LicensingName**</span><span class="sxs-lookup"><span data-stu-id="0e261-308">**LicensingName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-311">授權模式的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e261-311">The name of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-312">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="0e261-312">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-313">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-315">指定伺服器模式的授權類型。</span><span class="sxs-lookup"><span data-stu-id="0e261-315">The licensing type for the specified server mode.</span></span>

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span data-ttu-id="0e261-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**個人終端機伺服器** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-317">個人 RD 工作階段主機 server。</span><span class="sxs-lookup"><span data-stu-id="0e261-317">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span data-ttu-id="0e261-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>管理 (1) **的遠端桌面**</span><span class="sxs-lookup"><span data-stu-id="0e261-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remote Desktop for Administration** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-319">用於系統管理的遠端桌面。</span><span class="sxs-lookup"><span data-stu-id="0e261-319">Remote Desktop for Administration.</span></span>

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="0e261-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**每一裝置** (2) </span><span class="sxs-lookup"><span data-stu-id="0e261-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per Device** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-321">每一裝置。</span><span class="sxs-lookup"><span data-stu-id="0e261-321">Per Device.</span></span> <span data-ttu-id="0e261-322">適用于應用程式伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-322">Valid for application servers.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="0e261-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (3) </span><span class="sxs-lookup"><span data-stu-id="0e261-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-324">每個使用者。</span><span class="sxs-lookup"><span data-stu-id="0e261-324">Per User.</span></span> <span data-ttu-id="0e261-325">適用于應用程式伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-325">Valid for application servers.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0e261-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (4) </span><span class="sxs-lookup"><span data-stu-id="0e261-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-327">未設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-327">Not Configured.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-328">**LimitedUserSessions**</span><span class="sxs-lookup"><span data-stu-id="0e261-328">**LimitedUserSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-329">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-330">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-330">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-331">指出是否已啟用 RD 工作階段主機伺服器上允許的作用中和非作用中會話的數目限制的功能。</span><span class="sxs-lookup"><span data-stu-id="0e261-331">Indicates whether the feature to limit the number of both active and inactive sessions that are allowed on an RD Session Host server is enabled.</span></span> <span data-ttu-id="0e261-332">例如，您可能想要設定 **LimitedUserSessions** ，以保證 RD 工作階段主機伺服器上所安裝特定應用程式的授權合規性。</span><span class="sxs-lookup"><span data-stu-id="0e261-332">For example, you may want to set **LimitedUserSessions** to guarantee license compliance for a particular application that is installed on the RD Session Host server.</span></span> <span data-ttu-id="0e261-333">或者，您可能會想要在負載平衡的伺服器陣列中限制 RD 工作階段主機伺服器上的最大會話數目，如此一來，如果伺服器陣列中的另一部伺服器失敗，伺服器將不會超載。</span><span class="sxs-lookup"><span data-stu-id="0e261-333">Or, you may want to limit the maximum number of sessions on an RD Session Host server in a load-balanced farm so that the server will not be overloaded if another server in the farm fails.</span></span>

> [!Note]
>
> <span data-ttu-id="0e261-334">用來連線到伺服器以進行系統管理的會話不會受到 **LimitedUserSessions** 的影響。</span><span class="sxs-lookup"><span data-stu-id="0e261-334">The session that is used to connect to the server for administrative purposes is not affected by **LimitedUserSessions**.</span></span>
>
> <span data-ttu-id="0e261-335">在 RD 工作階段主機伺服器陣列中，如果使用者超過會話限制，則會 RD 連線代理人負載平衡，將會話導向至另一部伺服器。</span><span class="sxs-lookup"><span data-stu-id="0e261-335">In an RD Session Host server farm, if a user exceeds the session limit, the session will be directed to another server by RD Connection Broker load balancing.</span></span> <span data-ttu-id="0e261-336">如果伺服器是獨立伺服器，使用者將無法連接。</span><span class="sxs-lookup"><span data-stu-id="0e261-336">If the server is a stand-alone server, the user will not be able to connect.</span></span>
>
> <span data-ttu-id="0e261-337">由於基於系統管理目的而用來連線到伺服器的會話，以及在登入週期強制執行會話數目的時間，建議您將 **LimitedUserSessions** 設定為小於伺服器上會話數目的實體限制的值，以稍微低一點。</span><span class="sxs-lookup"><span data-stu-id="0e261-337">Because of the session that is used to connect to the server for administrative purposes, and the timing of the enforcement of the number of sessions during the logon cycle, it is recommended that you set **LimitedUserSessions** to a value that is slightly lower that the physical limit for the number of sessions on a server.</span></span>
>
> <span data-ttu-id="0e261-338">只有在安裝 RD 工作階段主機角色服務時， **LimitedUserSessions** 屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="0e261-338">The **LimitedUserSessions** property is only valid if the RD Session Host role service is installed.</span></span>

 

<dt>

<span data-ttu-id="0e261-339">0</span><span class="sxs-lookup"><span data-stu-id="0e261-339">0</span></span>
</dt> <dd>

<span data-ttu-id="0e261-340">這項功能已停用。</span><span class="sxs-lookup"><span data-stu-id="0e261-340">The feature is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-341">1或更大</span><span class="sxs-lookup"><span data-stu-id="0e261-341">1 or greater</span></span>
</dt> <dd>

<span data-ttu-id="0e261-342">一個或多個值代表 RD 工作階段主機伺服器上允許的作用中和非作用中)  (會話的最大數目。</span><span class="sxs-lookup"><span data-stu-id="0e261-342">A value of one or greater represents the maximum number of sessions (both active and inactive) that are allowed on the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-343">**登錄**</span><span class="sxs-lookup"><span data-stu-id="0e261-343">**Logons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-344">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-345">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-345">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-346">指定是否允許新的會話。</span><span class="sxs-lookup"><span data-stu-id="0e261-346">Specifies whether new sessions are allowed.</span></span> <span data-ttu-id="0e261-347">此設定不會影響現有的設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-347">This setting does not affect existing settings.</span></span>

<dt>

<span data-ttu-id="0e261-348">0</span><span class="sxs-lookup"><span data-stu-id="0e261-348">0</span></span>
</dt> <dd>

<span data-ttu-id="0e261-349">允許新的會話。</span><span class="sxs-lookup"><span data-stu-id="0e261-349">New sessions are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-350">1</span><span class="sxs-lookup"><span data-stu-id="0e261-350">1</span></span>
</dt> <dd>

<span data-ttu-id="0e261-351">不允許新的會話。</span><span class="sxs-lookup"><span data-stu-id="0e261-351">New sessions are not allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-352">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0e261-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-355">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e261-355">The name of the object.</span></span>

<span data-ttu-id="0e261-356">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0e261-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e261-357">**NetworkFSSCatchAllWeight**</span><span class="sxs-lookup"><span data-stu-id="0e261-357">**NetworkFSSCatchAllWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-358">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-359">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-359">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-360">指定全部攔截網路流量的預設網路公平共用權數。</span><span class="sxs-lookup"><span data-stu-id="0e261-360">Specifies the default network fair share weight for catch-all network traffic.</span></span> <span data-ttu-id="0e261-361">有效的值為1到9。</span><span class="sxs-lookup"><span data-stu-id="0e261-361">Valid values are 1 to 9.</span></span>

<span data-ttu-id="0e261-362">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-362">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-363">**NetworkFSSLocalSystemWeight**</span><span class="sxs-lookup"><span data-stu-id="0e261-363">**NetworkFSSLocalSystemWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-364">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-365">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-365">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-366">指定本機系統進程的預設網路公平共用權數。</span><span class="sxs-lookup"><span data-stu-id="0e261-366">Specifies the default network fair share weight for a local system processes.</span></span> <span data-ttu-id="0e261-367">有效的值為1到9。</span><span class="sxs-lookup"><span data-stu-id="0e261-367">Valid values are 1 to 9.</span></span>

<span data-ttu-id="0e261-368">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-368">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-369">**NetworkFSSUserSessionWeight**</span><span class="sxs-lookup"><span data-stu-id="0e261-369">**NetworkFSSUserSessionWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-370">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-371">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-371">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-372">指定使用者會話的預設網路公平共用權數。</span><span class="sxs-lookup"><span data-stu-id="0e261-372">Specifies the default network fair share weight for a user session.</span></span> <span data-ttu-id="0e261-373">有效的值為1到9。</span><span class="sxs-lookup"><span data-stu-id="0e261-373">Valid values are 1 to 9.</span></span>

<span data-ttu-id="0e261-374">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-374">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-375">**PolicySourceAllowTSConnections**</span><span class="sxs-lookup"><span data-stu-id="0e261-375">**PolicySourceAllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-376">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-378">指出 **AllowTSConnections** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-378">Indicates whether the **AllowTSConnections** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-379">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-379">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-380">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-380">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-381">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-381">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-382">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-382">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-383">**PolicySourceConfiguredLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="0e261-383">**PolicySourceConfiguredLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-384">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-384">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-386">指出 [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) 方法所傳回的授權伺服器是否由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-386">Indicates whether the license servers returned by the [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) method are configured by the server or by group policy.</span></span>

<span data-ttu-id="0e261-387">**Windows Server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-387">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="0e261-388">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-388">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-389">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-389">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-390">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-390">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-391">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-391">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-392">**PolicySourceDeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="0e261-392">**PolicySourceDeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-393">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-395">指出 **DeleteTempFolders** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-395">Indicates whether the **DeleteTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-396">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-396">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-397">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-397">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-398">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-398">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-399">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-399">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-400">**PolicySourceDirectConnectLicenseServers**</span><span class="sxs-lookup"><span data-stu-id="0e261-400">**PolicySourceDirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-401">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-401">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e261-403">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0e261-403">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0e261-404">無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-404">This property is not available.</span></span>

<span data-ttu-id="0e261-405">**Windows Server 2008：** 指出 **DirectConnectLicenseServers** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-405">**Windows Server 2008:** Indicates whether the **DirectConnectLicenseServers** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-406">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-406">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-407">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-407">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-408">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-408">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-409">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-409">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-410">**PolicySourceDisableForcibleLogoff**</span><span class="sxs-lookup"><span data-stu-id="0e261-410">**PolicySourceDisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-411">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-413">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-413">This property is not supported.</span></span>

<span data-ttu-id="0e261-414">**Windows Server 2008：** 判斷 **DisableForcibleLogoff** 屬性是否由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-414">**Windows Server 2008:** Determines whether the **DisableForcibleLogoff** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-415">0</span><span class="sxs-lookup"><span data-stu-id="0e261-415">0</span></span>
</dt> <dd>

<span data-ttu-id="0e261-416">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-416">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-417">1</span><span class="sxs-lookup"><span data-stu-id="0e261-417">1</span></span>
</dt> <dd>

<span data-ttu-id="0e261-418">群組原則。</span><span class="sxs-lookup"><span data-stu-id="0e261-418">Group Policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-419">**PolicySourceEnableAutomaticReconnection**</span><span class="sxs-lookup"><span data-stu-id="0e261-419">**PolicySourceEnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-420">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-422">指出是否由伺服器或群組原則設定 **EnableAutomaticReconnection** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-422">Indicates whether the **EnableAutomaticReconnection** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="0e261-423">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-424">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-425">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-426">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-426">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="0e261-427">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-427">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-428">**PolicySourceEnableDFSS**</span><span class="sxs-lookup"><span data-stu-id="0e261-428">**PolicySourceEnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-429">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-431">指出 **EnableDFSS** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-431">Indicates whether the **EnableDFSS** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-432">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-432">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-433">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-433">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-434">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-434">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-435">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-435">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="0e261-436">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="0e261-436">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-437">**PolicySourceEnableRemoteDesktopMSI**</span><span class="sxs-lookup"><span data-stu-id="0e261-437">**PolicySourceEnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-438">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-440">指出是否由伺服器或群組原則設定 **EnableRemoteDesktopMSI** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-440">Indicates whether the **EnableRemoteDesktopMSI** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="0e261-441">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-441">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-442">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-442">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-443">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-443">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-444">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-444">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="0e261-445">**Windows Server 2008：** 此屬性在 Windows Server 2008 R2 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="0e261-445">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-446">**PolicySourceFallbackPrintDriverType**</span><span class="sxs-lookup"><span data-stu-id="0e261-446">**PolicySourceFallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-447">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-447">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-448">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-449">指出 **FallbackPrintDriverType** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-449">Indicates whether the **FallbackPrintDriverType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-450">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-450">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-451">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-451">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-452">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-452">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-453">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-453">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-454">**PolicySourceHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="0e261-454">**PolicySourceHomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-455">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-455">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-456">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-457">指出 **HomeDirectory** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-457">Indicates whether the **HomeDirectory** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-458">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-458">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-459">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-459">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-460">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-460">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-461">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-461">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-462">**PolicySourceLicensingType**</span><span class="sxs-lookup"><span data-stu-id="0e261-462">**PolicySourceLicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-463">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-464">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-465">指出 **LicensingType** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-465">Indicates whether the **LicensingType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-466">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-466">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-467">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-467">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-468">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-468">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-469">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-469">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-470">**PolicySourceProfilePath**</span><span class="sxs-lookup"><span data-stu-id="0e261-470">**PolicySourceProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-471">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-473">指出 **ProfilePath** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-473">Indicates whether the **ProfilePath** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-474">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-474">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-475">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-475">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-476">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-476">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-477">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-477">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-478">**PolicySourceRedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="0e261-478">**PolicySourceRedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-479">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-479">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-480">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-481">指出是否由伺服器或群組原則設定 **RedirectSmartCards** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-481">Indicates whether the **RedirectSmartCards** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="0e261-482">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-482">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-483">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-483">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-484">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-484">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-485">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-485">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="0e261-486">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-486">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-487">**PolicySourceSingleSession**</span><span class="sxs-lookup"><span data-stu-id="0e261-487">**PolicySourceSingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-488">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-489">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-490">指出屬性 **SingleSession** 是否由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-490">Indicates whether the property **SingleSession** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-491">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-491">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-492">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-492">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-493">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-493">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-494">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-494">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-495">**PolicySourceTimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="0e261-495">**PolicySourceTimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-496">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-497">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-498">指出屬性 **TimeZoneRedirection** 是否由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-498">Indicates whether the property **TimeZoneRedirection** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-499">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-499">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-500">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-500">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-501">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-501">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-502">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-502">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-503">**PolicySourceUseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="0e261-503">**PolicySourceUseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-504">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-505">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-506">指出是否由伺服器或群組原則設定 **UseRDEasyPrintDriver** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-506">Indicates whether the **UseRDEasyPrintDriver** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="0e261-507">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-507">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-508">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-508">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-509">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-509">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-510">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-510">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="0e261-511">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-511">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-512">**PolicySourceUseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="0e261-512">**PolicySourceUseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-513">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-514">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-515">指出 **UseTempFolders** 屬性是由伺服器或群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="0e261-515">Indicates whether the **UseTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0e261-516">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-516">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-517">伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-517">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e261-518">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-518">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-519">群組原則</span><span class="sxs-lookup"><span data-stu-id="0e261-519">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-520">**PossibleLicensingTypes**</span><span class="sxs-lookup"><span data-stu-id="0e261-520">**PossibleLicensingTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-521">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-522">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e261-523">限定詞： [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ( "0"、"1"、"2"、"4"、"5" ) 、 [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「個人終端機伺服器」、「系統管理遠端桌面」、「個別裝置」、「每位使用者」、「未設定」 ) </span><span class="sxs-lookup"><span data-stu-id="0e261-523">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Remote Desktop for Administration", "Per Device", "Per User", "Not Configured")</span></span>
</dt> </dl>

<span data-ttu-id="0e261-524">指定可用授權類型的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="0e261-524">A bitmask that specifies the licensing types that are available.</span></span> <span data-ttu-id="0e261-525">這可以是下列一或多個值的組合。</span><span class="sxs-lookup"><span data-stu-id="0e261-525">This can be a combination of one or more of the following values.</span></span>

<dt>

<span data-ttu-id="0e261-526">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-526">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-527">支援個人 RD 工作階段主機 server 授權。</span><span class="sxs-lookup"><span data-stu-id="0e261-527">Personal RD Session Host server licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-528">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="0e261-528">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-529">支援遠端桌面授權。</span><span class="sxs-lookup"><span data-stu-id="0e261-529">Remote Desktop licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-530">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="0e261-530">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-531">支援每一裝置的授權。</span><span class="sxs-lookup"><span data-stu-id="0e261-531">Per device licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-532">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="0e261-532">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-533">支援每個使用者授權。</span><span class="sxs-lookup"><span data-stu-id="0e261-533">Per user licenses are supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-534">**ProfilePath**</span><span class="sxs-lookup"><span data-stu-id="0e261-534">**ProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-536">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-537">電腦的設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="0e261-537">Profile path for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-538">**RedirectSmartCards**</span><span class="sxs-lookup"><span data-stu-id="0e261-538">**RedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-539">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-540">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-540">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-541">指定是否允許在遠端會話中使用智慧卡裝置的重新導向。</span><span class="sxs-lookup"><span data-stu-id="0e261-541">Specifies if redirection of smart card devices is allowed in a remote session.</span></span>

<dt>

<span data-ttu-id="0e261-542">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="0e261-542">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-543">不允許智慧卡裝置重新導向。</span><span class="sxs-lookup"><span data-stu-id="0e261-543">Smart card device redirection is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-544">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0e261-544">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0e261-545">允許智慧卡裝置重新導向。</span><span class="sxs-lookup"><span data-stu-id="0e261-545">Smart card device redirection is allowed.</span></span>

</dd> </dl>

<span data-ttu-id="0e261-546">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-546">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-547">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="0e261-547">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-548">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-549">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e261-550">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0e261-550">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0e261-551">有興趣其屬性的 RD 工作階段主機伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0e261-551">Name of the RD Session Host server whose properties are of interest.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-552">**SessionBrokerDrainMode**</span><span class="sxs-lookup"><span data-stu-id="0e261-552">**SessionBrokerDrainMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-553">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-553">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-554">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-555">RD 連線代理人的使用者登入模式。</span><span class="sxs-lookup"><span data-stu-id="0e261-555">The RD Connection Broker user logon mode.</span></span>

<dt>

<span data-ttu-id="0e261-556">0</span><span class="sxs-lookup"><span data-stu-id="0e261-556">0</span></span>
</dt> <dd>

<span data-ttu-id="0e261-557">允許所有連接。</span><span class="sxs-lookup"><span data-stu-id="0e261-557">Allow all connections.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-558">1</span><span class="sxs-lookup"><span data-stu-id="0e261-558">1</span></span>
</dt> <dd>

<span data-ttu-id="0e261-559">允許重新開機，但在重新開機伺服器之前防止新的登入。</span><span class="sxs-lookup"><span data-stu-id="0e261-559">Allow reconnections, but prevent new logons until the server is restarted.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-560">2</span><span class="sxs-lookup"><span data-stu-id="0e261-560">2</span></span>
</dt> <dd>

<span data-ttu-id="0e261-561">允許重新登錄，但防止新的登入。</span><span class="sxs-lookup"><span data-stu-id="0e261-561">Allow reconnections, but prevent new logons.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-562">**SingleSession**</span><span class="sxs-lookup"><span data-stu-id="0e261-562">**SingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-563">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-564">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-565">指定是否允許每位使用者使用一或多個遠端桌面服務會話。</span><span class="sxs-lookup"><span data-stu-id="0e261-565">Specifies whether one or more Remote Desktop Services sessions are allowed per user.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="0e261-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-567">每位使用者可以有一個以上的會話。</span><span class="sxs-lookup"><span data-stu-id="0e261-567">More than one session is allowed per user.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="0e261-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1) </span><span class="sxs-lookup"><span data-stu-id="0e261-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-569">每位使用者只允許一個會話。</span><span class="sxs-lookup"><span data-stu-id="0e261-569">Only one session is allowed per user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-570">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0e261-570">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-571">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e261-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-572">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e261-573">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="0e261-573">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0e261-574">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0e261-574">Current status of the object.</span></span> <span data-ttu-id="0e261-575">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="0e261-575">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0e261-576">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="0e261-576">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0e261-577">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0e261-577">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0e261-578">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="0e261-578">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0e261-579">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0e261-579">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0e261-580">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0e261-580">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0e261-581"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0e261-581">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e261-582"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0e261-582">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e261-583"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0e261-583">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e261-584"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0e261-584">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e261-585"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0e261-585">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e261-586"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0e261-586">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e261-587"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0e261-587">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e261-588"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="0e261-588">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-589">**TerminalServerMode**</span><span class="sxs-lookup"><span data-stu-id="0e261-589">**TerminalServerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-590">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-591">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-592">遠端桌面服務服務的 RD 工作階段主機 server 操作模式。</span><span class="sxs-lookup"><span data-stu-id="0e261-592">The RD Session Host server operating mode of the Remote Desktop Services service.</span></span> <span data-ttu-id="0e261-593">此模式會控制適用的授權原則，以及是否啟用應用程式相容性功能。</span><span class="sxs-lookup"><span data-stu-id="0e261-593">This mode controls the licensing policies that are applicable as well as whether application-compatibility features are enabled.</span></span>

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span data-ttu-id="0e261-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**>appserver** (1) </span><span class="sxs-lookup"><span data-stu-id="0e261-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-595">伺服器會以應用程式伺服器的形式運作。</span><span class="sxs-lookup"><span data-stu-id="0e261-595">The server operates as an application server.</span></span>

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span data-ttu-id="0e261-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-597">會話是從遠端系統管理。</span><span class="sxs-lookup"><span data-stu-id="0e261-597">The session is administered remotely.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-598">**TimeZoneRedirection**</span><span class="sxs-lookup"><span data-stu-id="0e261-598">**TimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-599">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-599">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-600">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-600">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-601">指定用戶端電腦是否可以將其時區設定重新導向至遠端桌面服務會話。</span><span class="sxs-lookup"><span data-stu-id="0e261-601">Specifies whether the client computer can redirect its time zone settings to the Remote Desktop Services session.</span></span>

<dt>

<span data-ttu-id="0e261-602">0</span><span class="sxs-lookup"><span data-stu-id="0e261-602">0</span></span>
</dt> <dd>

<span data-ttu-id="0e261-603">重新導向已停用。</span><span class="sxs-lookup"><span data-stu-id="0e261-603">Redirection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-604">1</span><span class="sxs-lookup"><span data-stu-id="0e261-604">1</span></span>
</dt> <dd>

<span data-ttu-id="0e261-605">重新導向已啟用。</span><span class="sxs-lookup"><span data-stu-id="0e261-605">Redirection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-606">**UseRDEasyPrintDriver**</span><span class="sxs-lookup"><span data-stu-id="0e261-606">**UseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-607">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-607">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-608">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-608">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-609">指定是否先使用遠端桌面輕鬆列印印表機驅動程式來安裝所有用戶端印表機。</span><span class="sxs-lookup"><span data-stu-id="0e261-609">Specifies whether the Remote Desktop Easy Print printer driver is used first to install all client printers.</span></span>

<dt>

<span data-ttu-id="0e261-610">0</span><span class="sxs-lookup"><span data-stu-id="0e261-610">0</span></span>
</dt> <dd>

<span data-ttu-id="0e261-611">RD 工作階段主機伺服器會嘗試找出合適的印表機驅動程式來安裝用戶端印表機。</span><span class="sxs-lookup"><span data-stu-id="0e261-611">The RD Session Host server tries to find a suitable printer driver to install the client printer.</span></span> <span data-ttu-id="0e261-612">如果 RD 工作階段主機伺服器沒有符合用戶端印表機的印表機驅動程式，伺服器會嘗試使用遠端桌面輕鬆列印驅動程式來安裝用戶端印表機。</span><span class="sxs-lookup"><span data-stu-id="0e261-612">If the RD Session Host server does not have a printer driver that matches the client printer, the server tries to use the Remote Desktop Easy Print driver to install the client printer.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-613">1</span><span class="sxs-lookup"><span data-stu-id="0e261-613">1</span></span>
</dt> <dd>

<span data-ttu-id="0e261-614">RD 工作階段主機伺服器會先嘗試使用遠端桌面輕鬆列印印表機驅動程式來安裝所有用戶端印表機。</span><span class="sxs-lookup"><span data-stu-id="0e261-614">The RD Session Host server first tries to use the Remote Desktop Easy Print printer driver to install all client printers.</span></span> <span data-ttu-id="0e261-615">如果基於任何原因而無法使用遠端桌面輕鬆列印印表機驅動程式，則會使用 RD 工作階段主機伺服器上符合用戶端印表機的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0e261-615">If for any reason the Remote Desktop Easy Print printer driver cannot be used, a printer driver on the RD Session Host server that matches the client printer is used.</span></span>

</dd> </dl>

<span data-ttu-id="0e261-616">**Windows server 2008 R2 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-616">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0e261-617">**UserPermission**</span><span class="sxs-lookup"><span data-stu-id="0e261-617">**UserPermission**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-618">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-618">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-619">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0e261-619">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e261-620">指定每個使用者會話是否具有嚴格或寬鬆的安全性。</span><span class="sxs-lookup"><span data-stu-id="0e261-620">Specifies if each user session has tight or relaxed security.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0e261-621"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-621"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-622">安全性是嚴格的。</span><span class="sxs-lookup"><span data-stu-id="0e261-622">Security is tight.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0e261-623"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="0e261-623"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-624">安全性被放寬。</span><span class="sxs-lookup"><span data-stu-id="0e261-624">Security is relaxed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e261-625">**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="0e261-625">**UseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e261-626">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0e261-626">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e261-627">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e261-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e261-628">指定是否在每個會話中建立和刪除臨時目錄。</span><span class="sxs-lookup"><span data-stu-id="0e261-628">Specifies whether temporary directories are created and deleted on a per-session basis.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0e261-629"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="0e261-629"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-630">系統不會針對每個會話建立和刪除臨時目錄。</span><span class="sxs-lookup"><span data-stu-id="0e261-630">Temporary directories are not created and deleted for each session.</span></span> <span data-ttu-id="0e261-631">第一個會話會建立一個，而且永遠不會刪除。</span><span class="sxs-lookup"><span data-stu-id="0e261-631">One is created for the first session and never deleted.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0e261-632"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="0e261-632"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e261-633">系統會為每個會話建立和刪除臨時目錄。</span><span class="sxs-lookup"><span data-stu-id="0e261-633">Temporary directories are created and deleted for each session.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e261-634">備註</span><span class="sxs-lookup"><span data-stu-id="0e261-634">Remarks</span></span>

<span data-ttu-id="0e261-635">**Win32 \_TerminalServiceSetting** 會與 [**win32 \_ TerminalService**](win32-terminalservice.md)相關聯，作為 [**win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)關聯的 **設定** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-635">**Win32\_TerminalServiceSetting** is associated to [**Win32\_TerminalService**](win32-terminalservice.md) as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="0e261-636">[**Win32 \_TerminalSetting**](win32-terminalsetting.md)會與 [**win32 \_ 終端**](win32-terminal.md)機相關聯，作為 [**win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)關聯的 **設定** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0e261-636">[**Win32\_TerminalSetting**](win32-terminalsetting.md) is associated to [**Win32\_Terminal**](win32-terminal.md) as the **Setting** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="0e261-637">若要連接到根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="0e261-637">To connect to the Root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="0e261-638">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="0e261-638">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="0e261-639">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為六。</span><span class="sxs-lookup"><span data-stu-id="0e261-639">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="0e261-640">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="0e261-640">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="0e261-641">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0e261-641">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0e261-642">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0e261-642">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0e261-643">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0e261-643">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0e261-644">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="0e261-644">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e261-645">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e261-645">Requirements</span></span>



| <span data-ttu-id="0e261-646">需求</span><span class="sxs-lookup"><span data-stu-id="0e261-646">Requirement</span></span> | <span data-ttu-id="0e261-647">值</span><span class="sxs-lookup"><span data-stu-id="0e261-647">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e261-648">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e261-648">Minimum supported client</span></span><br/> | <span data-ttu-id="0e261-649">都不支援</span><span class="sxs-lookup"><span data-stu-id="0e261-649">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0e261-650">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e261-650">Minimum supported server</span></span><br/> | <span data-ttu-id="0e261-651">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e261-651">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e261-652">命名空間</span><span class="sxs-lookup"><span data-stu-id="0e261-652">Namespace</span></span><br/>                | <span data-ttu-id="0e261-653">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0e261-653">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0e261-654">MOF</span><span class="sxs-lookup"><span data-stu-id="0e261-654">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e261-655"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e261-655"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e261-656">DLL</span><span class="sxs-lookup"><span data-stu-id="0e261-656">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e261-657"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e261-657"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e261-658">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e261-658">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e261-659">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="0e261-659">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="0e261-660">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="0e261-660">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="0e261-661">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="0e261-661">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="0e261-662">**Win32 \_ TerminalServiceToSetting**</span><span class="sxs-lookup"><span data-stu-id="0e261-662">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="0e261-663">**Win32 \_ TerminalTerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="0e261-663">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dt>

[<span data-ttu-id="0e261-664">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="0e261-664">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

