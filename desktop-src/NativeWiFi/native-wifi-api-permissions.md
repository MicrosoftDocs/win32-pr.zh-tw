---
description: 原生 Wifi API 許可權
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: 原生 Wifi API 許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afafec7619e0920a17e3769a430c8c79aeff3828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192644"
---
# <a name="native-wifi-api-permissions"></a><span data-ttu-id="f3c99-103">原生 Wifi API 許可權</span><span class="sxs-lookup"><span data-stu-id="f3c99-103">Native Wifi API Permissions</span></span>

<span data-ttu-id="f3c99-104">當呼叫端沒有足夠的許可權可執行要求的作業時，原生 Wifi API 呼叫可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="f3c99-104">A Native Wifi API call may fail with when a caller does not have adequate permissions to perform the requested operation.</span></span>

<span data-ttu-id="f3c99-105">許可權會儲存在 [任意的存取控制清單中， (DACL)](../secauthz/access-control-lists.md) 與 [**WLAN \_ 安全 \_ 物件**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)相關聯。</span><span class="sxs-lookup"><span data-stu-id="f3c99-105">Permissions are stored in a [discretionary access control lists (DACL)](../secauthz/access-control-lists.md) associated with a [**WLAN\_SECURABLE\_OBJECT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span></span> <span data-ttu-id="f3c99-106">如需 Dacl 和安全物件的詳細資訊，請參閱 [Dacl 如何控制物件的存取權](../secauthz/how-dacls-control-access-to-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="f3c99-106">For more information about DACLs and securable objects, see [How DACLs Control Access to an Object](../secauthz/how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="f3c99-107">下表顯示使用安全物件的原生 Wifi 函式，以判斷呼叫端是否有足夠的許可權來執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="f3c99-107">The following table shows the Native Wifi functions that use securable objects to determine if the caller has sufficient permissions to perform the requested operation.</span></span> <span data-ttu-id="f3c99-108">它也會顯示每個函式所使用的安全物件。</span><span class="sxs-lookup"><span data-stu-id="f3c99-108">It also shows the securable objects used by each function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3c99-109">函式</span><span class="sxs-lookup"><span data-stu-id="f3c99-109">Function</span></span></th>
<th><span data-ttu-id="f3c99-110">安全物件</span><span class="sxs-lookup"><span data-stu-id="f3c99-110">Securable object</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3c99-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>、 <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3c99-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"><strong>WlanSetFilterList</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="f3c99-112">wlan_secure_deny_list</span><span class="sxs-lookup"><span data-stu-id="f3c99-112">wlan_secure_deny_list</span></span></li>
<li><span data-ttu-id="f3c99-113">wlan_secure_permit_list</span><span class="sxs-lookup"><span data-stu-id="f3c99-113">wlan_secure_permit_list</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c99-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3c99-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="f3c99-115">wlan_secure_ihv_control</span><span class="sxs-lookup"><span data-stu-id="f3c99-115">wlan_secure_ihv_control</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c99-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>、 <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3c99-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"><strong>WlanSetAutoConfigParameter</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="f3c99-117">wlan_secure_show_denied</span><span class="sxs-lookup"><span data-stu-id="f3c99-117">wlan_secure_show_denied</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c99-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>、 <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3c99-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"><strong>WlanSetInterface</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="f3c99-119">wlan_secure_ac_enabled</span><span class="sxs-lookup"><span data-stu-id="f3c99-119">wlan_secure_ac_enabled</span></span></li>
<li><span data-ttu-id="f3c99-120">wlan_secure_bc_scan_enabled</span><span class="sxs-lookup"><span data-stu-id="f3c99-120">wlan_secure_bc_scan_enabled</span></span></li>
<li><span data-ttu-id="f3c99-121">wlan_secure_bss_type</span><span class="sxs-lookup"><span data-stu-id="f3c99-121">wlan_secure_bss_type</span></span></li>
<li><span data-ttu-id="f3c99-122">wlan_secure_current_operation_mode</span><span class="sxs-lookup"><span data-stu-id="f3c99-122">wlan_secure_current_operation_mode</span></span></li>
<li><span data-ttu-id="f3c99-123">wlan_secure_interface_properties</span><span class="sxs-lookup"><span data-stu-id="f3c99-123">wlan_secure_interface_properties</span></span></li>
<li><span data-ttu-id="f3c99-124">wlan_secure_media_streaming_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="f3c99-124">wlan_secure_media_streaming_mode_enabled</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3c99-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3c99-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="f3c99-126">wlan_secure_add_new_all_user_profiles</span><span class="sxs-lookup"><span data-stu-id="f3c99-126">wlan_secure_add_new_all_user_profiles</span></span></li>
<li><span data-ttu-id="f3c99-127">wlan_secure_add_new_per_user_profiles</span><span class="sxs-lookup"><span data-stu-id="f3c99-127">wlan_secure_add_new_per_user_profiles</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3c99-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>、 <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3c99-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"><strong>WlanSetProfilePosition</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="f3c99-129">wlan_secure_all_user_profiles_order</span><span class="sxs-lookup"><span data-stu-id="f3c99-129">wlan_secure_all_user_profiles_order</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f3c99-130">在上述其中一個命名函式完成其作業之前，函式會抓取儲存在適當安全物件中的 DACL。</span><span class="sxs-lookup"><span data-stu-id="f3c99-130">Before one of the above-named functions completes its operation, the function retrieves the DACL stored in the appropriate securable object.</span></span> <span data-ttu-id="f3c99-131">然後，此函式會檢查 DACL 以查看呼叫端是否有足夠的許可權。</span><span class="sxs-lookup"><span data-stu-id="f3c99-131">The function then checks the DACL to see if the caller has sufficient permissions.</span></span> <span data-ttu-id="f3c99-132">WlanGet \* 和 WlanQuery 函 \* 式需要 DACL 包含 [ (ACE) 的存取控制專案 ](../secauthz/access-control-entries.md) ，以授與呼叫執行緒的 WLAN 讀取權限 [存取權杖](../secauthz/access-tokens.md) \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f3c99-132">The WlanGet\* and WlanQuery\* functions require that the DACL contains an [access control entry (ACE)](../secauthz/access-control-entries.md) that grants the [access token](../secauthz/access-tokens.md) of the calling thread WLAN\_READ\_ACCESS to the function.</span></span> <span data-ttu-id="f3c99-133">WlanSet 函 \* 式需要一個 ACE，以授與呼叫執行緒 WLAN 寫入存取權的存取權杖 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="f3c99-133">The WlanSet\* functions require an ACE that grants the access token of the calling thread WLAN\_WRITE\_ACCESS.</span></span> <span data-ttu-id="f3c99-134">如果呼叫端沒有足夠的許可權，函式呼叫會失敗，並出現錯誤 \_ 拒絕存取 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f3c99-134">If the caller does not have sufficient permissions, the function call fails with the error ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="f3c99-135">根據預設，每個安全物件都有與其相關聯的 DACL。</span><span class="sxs-lookup"><span data-stu-id="f3c99-135">Each securable object has a DACL associated with it by default.</span></span> <span data-ttu-id="f3c99-136">您可以使用 [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) 函數來變更 DACL 中儲存的預設許可權。</span><span class="sxs-lookup"><span data-stu-id="f3c99-136">The default permissions stored in the DACL can be changed using the [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) function.</span></span> <span data-ttu-id="f3c99-137">若要判斷在特定系統上執行操作所需的有效使用者權限，請呼叫 [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings)。</span><span class="sxs-lookup"><span data-stu-id="f3c99-137">To determine the effective user rights required to perform an operation on a particular system, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="f3c99-138">所有使用者設定檔都具有與設定檔本身相關聯的其他許可權。</span><span class="sxs-lookup"><span data-stu-id="f3c99-138">All-user profiles have additional permissions associated with the profile itself.</span></span> <span data-ttu-id="f3c99-139">當使用 [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) 或 [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile)建立或修改設定檔時，會建立所有使用者設定檔的許可權。</span><span class="sxs-lookup"><span data-stu-id="f3c99-139">The permissions on an all-user profile are established when the profile is created or modified using [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) or [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span></span> <span data-ttu-id="f3c99-140">*StrAllUserProfileSecurity* 參數會指定修改設定檔、刪除設定檔，或使用設定檔連接到網路所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="f3c99-140">The *strAllUserProfileSecurity* parameter specifies the required permissions for modifying a profile, deleting a profile, or connecting to a network using a profile.</span></span> <span data-ttu-id="f3c99-141">刪除或修改設定檔需要 WLAN \_ 寫入 \_ 存取權限。</span><span class="sxs-lookup"><span data-stu-id="f3c99-141">Deleting or modifying a profile requires WLAN\_WRITE\_ACCESS permission.</span></span> <span data-ttu-id="f3c99-142">使用設定檔連接到網路時，需要 WLAN \_ 執行 \_ 存取權限。</span><span class="sxs-lookup"><span data-stu-id="f3c99-142">Connecting to a network using a profile requires WLAN\_EXECUTE\_ACCESS permission.</span></span>

<span data-ttu-id="f3c99-143">\* \* Windows XP 含 SP3 和適用于 Windows XP SP2 的無線區域網路 API： \* \* 不支援 [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) 和 [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) 功能。</span><span class="sxs-lookup"><span data-stu-id="f3c99-143">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* The [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) and [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) functions are not supported.</span></span> <span data-ttu-id="f3c99-144">未使用 *strAllUserProfileSecurity* 參數。</span><span class="sxs-lookup"><span data-stu-id="f3c99-144">The *strAllUserProfileSecurity* parameter is not used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3c99-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3c99-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c99-146">Dacl 如何控制物件的存取</span><span class="sxs-lookup"><span data-stu-id="f3c99-146">How DACLs Control Access to an Object</span></span>](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="f3c99-147">**WLAN \_ 安全 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="f3c99-147">**WLAN\_SECURABLE\_OBJECT**</span></span>](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
