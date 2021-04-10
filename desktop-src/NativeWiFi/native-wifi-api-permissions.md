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
# <a name="native-wifi-api-permissions"></a>原生 Wifi API 許可權

當呼叫端沒有足夠的許可權可執行要求的作業時，原生 Wifi API 呼叫可能會失敗。

許可權會儲存在 [任意的存取控制清單中， (DACL)](../secauthz/access-control-lists.md) 與 [**WLAN \_ 安全 \_ 物件**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)相關聯。 如需 Dacl 和安全物件的詳細資訊，請參閱 [Dacl 如何控制物件的存取權](../secauthz/how-dacls-control-access-to-an-object.md)。

下表顯示使用安全物件的原生 Wifi 函式，以判斷呼叫端是否有足夠的許可權來執行要求的作業。 它也會顯示每個函式所使用的安全物件。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>安全物件</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>、 <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a><br/></td>
<td><ul>
<li>wlan_secure_deny_list</li>
<li>wlan_secure_permit_list</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ihv_control</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>、 <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a><br/></td>
<td><ul>
<li>wlan_secure_show_denied</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>、 <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ac_enabled</li>
<li>wlan_secure_bc_scan_enabled</li>
<li>wlan_secure_bss_type</li>
<li>wlan_secure_current_operation_mode</li>
<li>wlan_secure_interface_properties</li>
<li>wlan_secure_media_streaming_mode_enabled</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a><br/></td>
<td><ul>
<li>wlan_secure_add_new_all_user_profiles</li>
<li>wlan_secure_add_new_per_user_profiles</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>、 <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a><br/></td>
<td><ul>
<li>wlan_secure_all_user_profiles_order</li>
</ul></td>
</tr>
</tbody>
</table>



 

在上述其中一個命名函式完成其作業之前，函式會抓取儲存在適當安全物件中的 DACL。 然後，此函式會檢查 DACL 以查看呼叫端是否有足夠的許可權。 WlanGet \* 和 WlanQuery 函 \* 式需要 DACL 包含 [ (ACE) 的存取控制專案 ](../secauthz/access-control-entries.md) ，以授與呼叫執行緒的 WLAN 讀取權限 [存取權杖](../secauthz/access-tokens.md) \_ \_ 。 WlanSet 函 \* 式需要一個 ACE，以授與呼叫執行緒 WLAN 寫入存取權的存取權杖 \_ \_ 。 如果呼叫端沒有足夠的許可權，函式呼叫會失敗，並出現錯誤 \_ 拒絕存取 \_ 。

根據預設，每個安全物件都有與其相關聯的 DACL。 您可以使用 [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) 函數來變更 DACL 中儲存的預設許可權。 若要判斷在特定系統上執行操作所需的有效使用者權限，請呼叫 [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings)。

所有使用者設定檔都具有與設定檔本身相關聯的其他許可權。 當使用 [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) 或 [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile)建立或修改設定檔時，會建立所有使用者設定檔的許可權。 *StrAllUserProfileSecurity* 參數會指定修改設定檔、刪除設定檔，或使用設定檔連接到網路所需的許可權。 刪除或修改設定檔需要 WLAN \_ 寫入 \_ 存取權限。 使用設定檔連接到網路時，需要 WLAN \_ 執行 \_ 存取權限。

* * Windows XP 含 SP3 和適用于 Windows XP SP2 的無線區域網路 API： * * 不支援 [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) 和 [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) 功能。 未使用 *strAllUserProfileSecurity* 參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Dacl 如何控制物件的存取](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**WLAN \_ 安全 \_ 物件**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
