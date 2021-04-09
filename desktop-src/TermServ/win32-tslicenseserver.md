---
title: Win32_TSLicenseServer 類別
description: 提供方法和屬性，以在遠端桌面授權伺服器上查看並設定遠端桌面授權 (RD 授權) 。
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer 類別遠端桌面服務
- Win32_TSLicenseServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934654"
---
# <a name="win32_tslicenseserver-class"></a><span data-ttu-id="e5b6c-105">Win32 \_ TSLicenseServer 類別</span><span class="sxs-lookup"><span data-stu-id="e5b6c-105">Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="e5b6c-106">提供方法和屬性，以在遠端桌面授權伺服器上查看並設定遠端桌面授權 (RD 授權) 。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-106">Provides methods and properties to view and configure Remote Desktop Licensing (RD Licensing) on a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b6c-107">語法</span><span class="sxs-lookup"><span data-stu-id="e5b6c-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a><span data-ttu-id="e5b6c-108">成員</span><span class="sxs-lookup"><span data-stu-id="e5b6c-108">Members</span></span>

<span data-ttu-id="e5b6c-109">**Win32 \_ TSLicenseServer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e5b6c-109">The **Win32\_TSLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="e5b6c-110">方法</span><span class="sxs-lookup"><span data-stu-id="e5b6c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5b6c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e5b6c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5b6c-112">方法</span><span class="sxs-lookup"><span data-stu-id="e5b6c-112">Methods</span></span>

<span data-ttu-id="e5b6c-113">**Win32 \_ TSLicenseServer** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-113">The **Win32\_TSLicenseServer** class has these methods.</span></span>



| <span data-ttu-id="e5b6c-114">方法</span><span class="sxs-lookup"><span data-stu-id="e5b6c-114">Method</span></span>                                                                                   | <span data-ttu-id="e5b6c-115">描述</span><span class="sxs-lookup"><span data-stu-id="e5b6c-115">Description</span></span>                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5b6c-116">**ActivateServer**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-116">**ActivateServer**</span></span>](activateserver-win32-tslicenseserver.md)                           | <span data-ttu-id="e5b6c-117">使用透過電話或網際網路取得的遠端桌面授權伺服器識別碼，來啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-117">Activates the Remote Desktop license server by using a Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e5b6c-118">**ActivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-118">**ActivateServerAutomatic**</span></span>](activateserverautomatic-win32-tslicenseserver.md)         | <span data-ttu-id="e5b6c-119">透過網際網路自動啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-119">Activates the Remote Desktop license server automatically over the Internet.</span></span> <span data-ttu-id="e5b6c-120">當呼叫這個方法時， **FirstName**、 **LastName**、 **Company** 和 **國家/地區** 屬性不得為空白，否則方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-120">The **FirstName**, **LastName**, **Company**, and **CountryRegion** properties must not be empty when this method is called, or the method will fail.</span></span><br/> |
| [<span data-ttu-id="e5b6c-121">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-121">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)                       | <span data-ttu-id="e5b6c-122">將遠端桌面授權伺服器新增至與授權伺服器相同網域中網域控制站上的遠端桌面授權伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-122">Adds the Remote Desktop license server to the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                                |
| [<span data-ttu-id="e5b6c-123">**ChangeRole**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-123">**ChangeRole**</span></span>](changerole-win32-tslicenseserver.md)                                   | <span data-ttu-id="e5b6c-124">變更遠端桌面授權伺服器的探索領域。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-124">Changes the discovery scope of the Remote Desktop license server.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="e5b6c-125">**CreateTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-125">**CreateTSCGroup**</span></span>](createtscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="e5b6c-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-126">This method is not supported.</span></span><br/> <span data-ttu-id="e5b6c-127">**Windows server 2008 R2 和 Windows server 2008：** 在遠端桌面授權伺服器上建立終端機伺服器電腦本機群組。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-127">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                               |
| [<span data-ttu-id="e5b6c-128">**DeactivateServer**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-128">**DeactivateServer**</span></span>](deactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="e5b6c-129">使用透過電話收到的確認碼來停用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-129">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="e5b6c-130">**DeactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-130">**DeactivateServerAutomatic**</span></span>](deactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="e5b6c-131">透過網際網路停用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-131">Deactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="e5b6c-132">當呼叫這個方法時， **FirstName** 和 **LastName** 屬性不得為空白，否則方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-132">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="e5b6c-133">**GetActivationStatus**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-133">**GetActivationStatus**</span></span>](getactivationstatus-win32-tslicenseserver.md)                 | <span data-ttu-id="e5b6c-134">抓取目前的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-134">Retrieves the current activation status.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="e5b6c-135">**GetLicenseServerId**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-135">**GetLicenseServerId**</span></span>](getlicenseserverid-win32-tslicenseserver.md)                   | <span data-ttu-id="e5b6c-136">如果伺服器目前已啟用，則抓取遠端桌面授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-136">Retrieves a Remote Desktop license server ID if the server is currently activated.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="e5b6c-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)                         | <span data-ttu-id="e5b6c-138">抓取遠端桌面授權伺服器是否為指定網域中網域控制站上的遠端桌面授權伺服器群組的成員。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-138">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop License Servers group on a domain controller in a given domain.</span></span><br/>                                                                              |
| [<span data-ttu-id="e5b6c-139">**IsLSonDC**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-139">**IsLSonDC**</span></span>](islsondc-win32-tslicenseserver.md)                                       | <span data-ttu-id="e5b6c-140">抓取 RD 授權是否安裝在網域控制站上。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-140">Retrieves whether RD Licensing is installed on a domain controller.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="e5b6c-141">**IsLSPreventUpgradeGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-141">**IsLSPreventUpgradeGPEnabled**</span></span>](islspreventupgradegpenabled-win32-tslicenseserver.md) | <span data-ttu-id="e5b6c-142">抓取是否已在遠端桌面授權伺服器上啟用「防止授權升級」群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-142">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e5b6c-143">**IsLSPublished**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-143">**IsLSPublished**</span></span>](islspublished-win32-tslicenseserver.md)                             | <span data-ttu-id="e5b6c-144">抓取 Active Directory Domain Services (AD DS) 中是否發佈遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-144">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="e5b6c-145">**IsLSRegisteredToSCP**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-145">**IsLSRegisteredToSCP**</span></span>](win32-tslicenseserver-islsregisteredtoscp.md)                 | <span data-ttu-id="e5b6c-146">抓取是否在 Active Directory Domain Services 中將遠端桌面授權伺服器註冊為服務連接點。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-146">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                               |
| [<span data-ttu-id="e5b6c-147">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-147">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)                 | <span data-ttu-id="e5b6c-148">抓取是否已在遠端桌面授權伺服器上啟用 [授權伺服器安全性群組] 群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-148">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="e5b6c-149">**IsSecureAccessAllowed**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-149">**IsSecureAccessAllowed**</span></span>](issecureaccessallowed-win32-tslicenseserver.md)             | <span data-ttu-id="e5b6c-150">抓取 RD 工作階段主機伺服器是否允許從遠端桌面授權伺服器 (RDS Cal) 要求遠端桌面服務用戶端存取授權。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-150">Retrieves whether an RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span><br/>                                                                |
| [<span data-ttu-id="e5b6c-151">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-151">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)                     | <span data-ttu-id="e5b6c-152">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-152">This method is not supported.</span></span><br/> <span data-ttu-id="e5b6c-153">**Windows server 2008 R2 和 Windows server 2008：** 抓取終端機伺服器電腦本機群組是否存在於遠端桌面授權伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-153">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span><br/>                              |
| [<span data-ttu-id="e5b6c-154">**IsTSinTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-154">**IsTSinTSCGroup**</span></span>](istsintscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="e5b6c-155">抓取 RD 工作階段主機伺服器是否為遠端桌面授權伺服器上終端機伺服器電腦本機群組的成員。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-155">Retrieves whether an RD Session Host server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="e5b6c-156">**PublishLS**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-156">**PublishLS**</span></span>](publishls-win32-tslicenseserver.md)                                     | <span data-ttu-id="e5b6c-157">在 AD DS 發佈遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-157">Publishes the Remote Desktop license server in AD DS.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="e5b6c-158">**ReactivateServer**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-158">**ReactivateServer**</span></span>](reactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="e5b6c-159">使用透過電話或網際網路取得的新遠端桌面授權伺服器識別碼，重新開機遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-159">Reactivates the Remote Desktop license server by using a new Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                     |
| [<span data-ttu-id="e5b6c-160">**ReactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-160">**ReactivateServerAutomatic**</span></span>](reactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="e5b6c-161">透過網際網路重新開機遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-161">Reactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="e5b6c-162">當呼叫這個方法時， **FirstName** 和 **LastName** 屬性不得為空白，否則方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-162">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="e5b6c-163">**RegisterLSToSCP**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-163">**RegisterLSToSCP**</span></span>](win32-tslicenseserver-registerlstoscp.md)                         | <span data-ttu-id="e5b6c-164">在 Active Directory Domain Services 中，將遠端桌面授權伺服器註冊為服務連接點。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-164">Registers the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="e5b6c-165">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-165">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)             | <span data-ttu-id="e5b6c-166">從與授權伺服器相同網域的網域控制站上的遠端桌面授權伺服器群組中，移除遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-166">Removes the Remote Desktop license server from the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                           |
| [<span data-ttu-id="e5b6c-167">**RemoveTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-167">**RemoveTSCGroup**</span></span>](removetscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="e5b6c-168">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-168">This method is not supported.</span></span><br/> <span data-ttu-id="e5b6c-169">**Windows server 2008 R2 和 Windows server 2008：** 從遠端桌面授權伺服器移除終端機伺服器電腦本機群組。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-169">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span><br/>                                             |
| [<span data-ttu-id="e5b6c-170">**UnpublishLS**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-170">**UnpublishLS**</span></span>](unpublishls-win32-tslicenseserver.md)                                 | <span data-ttu-id="e5b6c-171">從 AD DS Unpublishes 遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-171">Unpublishes a Remote Desktop license server from AD DS.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="e5b6c-172">**UnRegisterLSFromSCP**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-172">**UnRegisterLSFromSCP**</span></span>](win32-tslicenseserver-unregisterlsfromscp.md)                 | <span data-ttu-id="e5b6c-173">將遠端桌面授權伺服器移除為 Active Directory Domain Services 中的服務連接點。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-173">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="e5b6c-174">屬性</span><span class="sxs-lookup"><span data-stu-id="e5b6c-174">Properties</span></span>

<span data-ttu-id="e5b6c-175">**Win32 \_ TSLicenseServer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-175">The **Win32\_TSLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5b6c-176">**位址**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-176">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-179">RD 授權連絡人的街道位址。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-179">Street address of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-180">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-180">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="e5b6c-181">使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) </span><span class="sxs-lookup"><span data-stu-id="e5b6c-181">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-182">**城市**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-182">**City**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-185">RD 授權連絡人的城市。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-185">City of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-186">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-186">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="e5b6c-187">使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) </span><span class="sxs-lookup"><span data-stu-id="e5b6c-187">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-188">**公司**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-188">**Company**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-191">RD 授權連絡人的公司。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-191">Company of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-192">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性 (和必要的) 。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-192">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-193">**/**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-193">**CountryRegion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-195">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-195">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-196">RD 授權連絡人的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-196">Country/region of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-197">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性 (和必要的) 。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-197">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-198">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-198">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5b6c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-201">RDS 授權資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-201">Path of the RDS Licensing database.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-202">**電子郵件**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-202">**eMail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-204">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-204">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-205">RD 授權連絡人的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-205">Email address of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-206">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)、 [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)或 [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-206">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span> <span data-ttu-id="e5b6c-207"> (針對這些方法呼叫，這個屬性是選擇性的。 ) </span><span class="sxs-lookup"><span data-stu-id="e5b6c-207">(This property is optional for these method calls.)</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-208">**名字**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-208">**FirstName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-210">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-211">RD 授權連絡人的名字。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-211">First name of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-212">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)、 [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)或 [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性 (和必要的) 。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-212">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-213">**姓氏**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-213">**LastName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-215">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-215">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-216">RD 授權連絡人的姓氏。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-216">Last name of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-217">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)、 [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)或 [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性 (和必要的) 。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-217">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-218">**OrgUnit**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-218">**OrgUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-221">RD 授權連絡人的組織單位。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-221">Organizational unit of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-222">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 時，會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-222">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) is called.</span></span> <span data-ttu-id="e5b6c-223">使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) </span><span class="sxs-lookup"><span data-stu-id="e5b6c-223">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-224">**PostalCode**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-224">**PostalCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-227">RD 授權連絡人的郵遞區號。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-227">Postal code of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-228">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-228">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="e5b6c-229">使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) </span><span class="sxs-lookup"><span data-stu-id="e5b6c-229">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-230">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-230">**ProductId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5b6c-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-233">遠端桌面授權伺服器的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-233">Product ID of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-234">**ServerRole**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-234">**ServerRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-235">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5b6c-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-237">描述組織內遠端桌面授權伺服器的授權範圍。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-237">Describes the licensing scope for the Remote Desktop license server within the organization.</span></span>

<dt>

<span data-ttu-id="e5b6c-238">0</span><span class="sxs-lookup"><span data-stu-id="e5b6c-238">0</span></span>
</dt> <dd>

<span data-ttu-id="e5b6c-239">相同工作組中的 RD 工作階段主機伺服器可以探索授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-239">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-240">1</span><span class="sxs-lookup"><span data-stu-id="e5b6c-240">1</span></span>
</dt> <dd>

<span data-ttu-id="e5b6c-241">相同網域中 RD 工作階段主機伺服器可以探索授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-241">RD Session Host servers in the same domain can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-242">2</span><span class="sxs-lookup"><span data-stu-id="e5b6c-242">2</span></span>
</dt> <dd>

<span data-ttu-id="e5b6c-243">相同樹系中的多個網域 RD 工作階段主機伺服器可以探索授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-243">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5b6c-244">**State**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-244">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-246">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e5b6c-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-247">RD 授權連絡人的狀態。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-247">State of the contact for RD Licensing.</span></span> <span data-ttu-id="e5b6c-248">呼叫 [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) 方法時，會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-248">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="e5b6c-249">使用 **ActivateServerAutomatic** 方法時， (這個屬性是選擇性的。 ) </span><span class="sxs-lookup"><span data-stu-id="e5b6c-249">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-250">**版本**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-250">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5b6c-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-253">遠端桌面授權伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-253">Version of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="e5b6c-254">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-254">**VersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b6c-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5b6c-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5b6c-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5b6c-257">遠端桌面授權伺服器的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-257">Version number of the Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5b6c-258">備註</span><span class="sxs-lookup"><span data-stu-id="e5b6c-258">Remarks</span></span>

<span data-ttu-id="e5b6c-259">這個類別是 [單一](/windows/desktop/WmiSdk/standard-wmi-qualifiers) 類別，而且只能有一個實例。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-259">This class is a [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) class and can have only one instance.</span></span> <span data-ttu-id="e5b6c-260">此類別中包含的所有方法都是靜態的。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-260">All of the methods contained within this class are static.</span></span>

<span data-ttu-id="e5b6c-261">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-261">You must be a member of the Administrators group to use this class.</span></span> <span data-ttu-id="e5b6c-262">如果呼叫端不是系統管理員群組的成員，則傳回的屬性會是空的。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-262">If the caller is not a member of the Administrators group, the properties returned will be empty.</span></span>

<span data-ttu-id="e5b6c-263">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-263">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e5b6c-264">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-264">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e5b6c-265">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-265">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e5b6c-266">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e5b6c-266">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b6c-267">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5b6c-267">Requirements</span></span>



| <span data-ttu-id="e5b6c-268">需求</span><span class="sxs-lookup"><span data-stu-id="e5b6c-268">Requirement</span></span> | <span data-ttu-id="e5b6c-269">值</span><span class="sxs-lookup"><span data-stu-id="e5b6c-269">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b6c-270">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5b6c-270">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b6c-271">都不支援</span><span class="sxs-lookup"><span data-stu-id="e5b6c-271">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e5b6c-272">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5b6c-272">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b6c-273">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5b6c-273">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e5b6c-274">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5b6c-274">Namespace</span></span><br/>                | <span data-ttu-id="e5b6c-275">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e5b6c-275">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e5b6c-276">MOF</span><span class="sxs-lookup"><span data-stu-id="e5b6c-276">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5b6c-277"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5b6c-277"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5b6c-278">DLL</span><span class="sxs-lookup"><span data-stu-id="e5b6c-278">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5b6c-279"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5b6c-279"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b6c-280">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5b6c-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b6c-281">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-281">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="e5b6c-282">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-282">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="e5b6c-283">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-283">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="e5b6c-284">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="e5b6c-284">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

