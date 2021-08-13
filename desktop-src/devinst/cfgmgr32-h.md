---
title: Cfgmgr32.h
description: 本節包含 Cfgmgr32 標頭的參考主題。
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd09a0e905b85d2eae52bb267929d2e1e89e5c6c179a8d6ab4de00320e9f8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541422"
---
# <a name="cfgmgr32h"></a>Cfgmgr32.h

本節包含 Cfgmgr32 標頭的參考主題。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a><br/></td>
<td>BUSNUMBER_DES 結構是用來指定資源清單或資源需求清單，以描述裝置實例的匯流排編號使用量。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a><br/></td>
<td>BUSNUMBER_RANGE 結構會指定資源需求清單，以描述裝置實例的匯流排數量使用情形。 如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a><br/></td>
<td>BUSNUMBER_RESOURCE 結構會指定資源清單或資源需求清單，以說明裝置實例的匯流排編號使用量。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a><br/></td>
<td><strong>CM_Add_Empty_Log_Conf</strong>函式會在本機電腦上，針對指定的設定類型和指定的裝置實例建立空白<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> 。
</blockquote>
<br/> <strong>CM_Add_Empty_Log_Conf_Ex</strong>函式會在本機或遠端電腦上，為指定的設定類型和指定的裝置實例建立空白<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a><br/></td>
<td><strong>CM_Add_ID</strong>函式會將指定的<a href="/windows-hardware/drivers/install/device-ids">裝置識別碼</a>附加 (（如果尚未在<a href="/windows-hardware/drivers/">裝置實例的</a><a href="/windows-hardware/drivers/install/hardware-ids">硬體識別碼</a>清單或<a href="/windows-hardware/drivers/install/compatible-ids">相容識別碼</a>清單中提供) ）。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> 。
</blockquote>
<br/> <strong>CM_Add_ID_Ex</strong>函式會在本機或遠端電腦上，將<a href="/windows-hardware/drivers/install/device-ids">裝置識別碼</a> (附加至裝置實例的<a href="/windows-hardware/drivers/install/hardware-ids">硬體識別碼</a>清單或<a href="/windows-hardware/drivers/install/compatible-ids">相容識別碼</a>清單（若尚未) 存在）。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a><br/></td>
<td><strong>CM_Add_Res_Des</strong>函數會將<a href="/windows-hardware/drivers/">資源描述</a>項新增至<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> 。
</blockquote>
<br/> <strong>CM_Add_Res_Des_Ex</strong>函數會將<a href="/windows-hardware/drivers/">資源描述</a>項新增至<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。 邏輯設定可以位於本機或遠端電腦上。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 開始，已移除存取遠端電腦的 Windows Server 2012 功能。 在這些版本的 Windows 上執行時，您無法存取遠端電腦。
</blockquote>
<br/> <strong>CM_Connect_Machine</strong>函式會建立與遠端電腦的連接。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a><br/></td>
<td><strong>CM_Delete_Class_Key</strong>函數會從系統中移除指定的已安裝<a href="/windows-hardware/drivers/">裝置類別</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a><br/></td>
<td><strong>CM_Delete_Device_Interface_Key</strong>函式會刪除應用程式和驅動程式用來儲存介面特定資訊的登錄子機碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> 。
</blockquote>
<br/> <strong>CM_Delete_Device_Interface_Key_ExA</strong>函式會刪除應用程式和驅動程式用來儲存介面特定資訊的登錄子機碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> 。
</blockquote>
<br/> <strong>CM_Delete_Device_Interface_Key_ExW</strong>函式會刪除應用程式和驅動程式用來儲存介面特定資訊的登錄子機碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a><br/></td>
<td><strong>CM_Delete_DevNode_Key</strong>函式會刪除與裝置相關聯之指定的使用者可存取登錄機碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a><br/></td>
<td><strong>CM_Disable_DevNode</strong>函式會停用裝置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 開始，已移除存取遠端電腦的 Windows Server 2012 功能。 在這些版本的 Windows 上執行時，您無法存取遠端電腦。
</blockquote>
<br/> <strong>CM_Disconnect_Machine</strong>函式會移除遠端電腦的連接。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a><br/></td>
<td><strong>CM_Enable_DevNode</strong>函式會啟用裝置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a><br/></td>
<td>重複呼叫 <strong>CM_Enumerate_Classes</strong> 函式時，會藉由提供每個類別的 GUID 來列舉本機電腦已安裝的 <a href="/windows-hardware/drivers/">裝置類別</a> 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> 。
</blockquote>
<br/> 重複呼叫 <strong>CM_Enumerate_Classes_Ex</strong> 函式時，會藉由提供每個類別的 GUID 來列舉本機或遠端電腦的已安裝 <a href="/windows-hardware/drivers/">裝置類別</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a><br/></td>
<td><strong>CM_Enumerate_Enumerators</strong>函式會藉由提供每個列舉值的名稱來列舉本機電腦的裝置枚舉器。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> 。
</blockquote>
<br/> <strong>CM_Enumerate_Enumerators_Ex</strong>函式會藉由提供每個列舉值的名稱，來列舉本機或遠端電腦的裝置枚舉器。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a><br/></td>
<td><strong>CM_Free_Log_Conf</strong>函式會從本機電腦移除<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定和所有相關聯的<a href="/windows-hardware/drivers/">資源描述</a>項。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> 。
</blockquote>
<br/> <strong>CM_Free_Log_Conf_Ex</strong>函式會從本機或遠端電腦移除<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定和所有相關聯的<a href="/windows-hardware/drivers/">資源描述</a>項。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a><br/></td>
<td><strong>CM_Free_Log_Conf_Handle</strong>函式會使邏輯設定控制碼失效，並釋放其相關聯的記憶體配置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a><br/></td>
<td><strong>CM_Free_Res_Des</strong>函式會從本機電腦上的<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定移除<a href="/windows-hardware/drivers/">資源描述</a>項。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> 。
</blockquote>
<br/> <strong>CM_Free_Res_Des_Ex</strong>函式會從本機或遠端電腦上的<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定移除<a href="/windows-hardware/drivers/">資源描述</a>項。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a><br/></td>
<td><strong>CM_Free_Res_Des_Handle</strong>函式會使資源描述控制碼失效，並釋放其相關聯的記憶體配置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a><br/></td>
<td><strong>CM_Free_Resource_Conflict_Handle</strong>函式會使資源衝突清單的控制碼失效，並釋放控制碼的相關記憶體配置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a><br/></td>
<td><strong>CM_Get_Child</strong>函式可用來將裝置實例控制碼取出至指定裝置節點的第一個子節點， (<a href="/windows-hardware/drivers/">devnode</a>) 在本機電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Child_Ex</strong>函式可用來將裝置實例控制碼取出至指定裝置節點的第一個子節點， (在本機或遠端電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中<a href="/windows-hardware/drivers/">devnode</a>) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a><br/></td>
<td><strong>CM_Get_Class_Property</strong>函式會抓取針對<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>或<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>設定的裝置屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Class_Property_ExW</strong>函式會抓取針對<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>或<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>設定的裝置屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a><br/></td>
<td><strong>CM_Get_Class_Property_Keys</strong>函式會抓取裝置屬性索引鍵的陣列，該陣列代表針對<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>或<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>所設定的裝置屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Class_Property_Keys_Ex</strong>函式會抓取裝置屬性索引鍵的陣列，該陣列代表針對<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>或<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>所設定的裝置屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a><br/></td>
<td><strong>CM_Get_Class_Registry_Property</strong>函式會捕獲<a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">裝置安裝類別屬性</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a><br/></td>
<td><strong>CM_Get_Depth</strong>函式可用來取得指定裝置節點的深度 (在本機電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中的<a href="/windows-hardware/drivers/">devnode</a>) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Depth_Ex</strong>函式可用來取得指定裝置節點的深度 (在本機或遠端電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中的<a href="/windows-hardware/drivers/">devnode</a>) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a><br/></td>
<td><strong>CM_Get_Device_ID</strong>函式會取得本機電腦上指定之<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Device_ID_Ex</strong>函式會抓取本機或遠端電腦上指定之<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a><br/></td>
<td><strong>CM_Get_Device_ID_List</strong>函式會針對本機電腦的<a href="/windows-hardware/drivers/">裝置實例</a>，抓取<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>的清單。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Device_ID_List_Ex</strong>函式會針對本機或遠端電腦上的<a href="/windows-hardware/drivers/">裝置實例</a>，抓取<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>的清單。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a><br/></td>
<td><strong>CM_Get_Device_ID_List_Size</strong>函式會抓取保存本機電腦<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>清單所需的緩衝區大小。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Device_ID_List_Size_Ex</strong>函式會抓取保存本機或遠端電腦<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>清單所需的緩衝區大小。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a><br/></td>
<td><strong>CM_Get_Device_ID_Size</strong>函式會抓取在本機電腦上保存<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>所需的緩衝區大小。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Device_ID_Size_Ex</strong>函式會抓取在本機或遠端電腦上保存<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>所需的緩衝區大小。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a><br/></td>
<td>如果別名存在， <strong>CM_Get_Device_Interface_Alias</strong> 函數會傳回指定之裝置介面實例的別名。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a><br/></td>
<td><strong>CM_Get_Device_Interface_List</strong>函式會抓取屬於指定<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>的裝置介面實例清單。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a><br/></td>
<td><strong>CM_Get_Device_Interface_List_Size</strong>函式會抓取必須傳遞至<a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a>函數的緩衝區大小。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a><br/></td>
<td><strong>CM_Get_Device_Interface_Property</strong>函式會抓取針對裝置介面設定的裝置屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Device_Interface_Property_ExW</strong>函式會抓取針對裝置介面設定的裝置屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a><br/></td>
<td><strong>CM_Get_Device_Interface_Property_Keys</strong>函式會抓取裝置屬性索引鍵的陣列，代表針對裝置介面設定的裝置屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Device_Interface_Property_Keys_ExW</strong>函式會抓取裝置屬性索引鍵的陣列，代表針對裝置介面設定的裝置屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a><br/></td>
<td><strong>CM_Get_DevNode_Property</strong>函式會捕獲裝置實例屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_DevNode_Property_ExW</strong>函式會捕獲裝置實例屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a><br/></td>
<td><strong>CM_Get_DevNode_Property_Keys</strong>函式會抓取裝置屬性索引鍵的陣列，以代表針對裝置實例所設定的裝置屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_DevNode_Property_Keys_Ex</strong>函式會抓取裝置屬性索引鍵的陣列，以代表針對裝置實例所設定的裝置屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a><br/></td>
<td><strong>CM_Get_DevNode_Registry_Property</strong>函式會從登錄中取出指定的裝置屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a><br/></td>
<td><strong>CM_Get_DevNode_Status</strong>函式會在本機電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中，從其裝置節點 (<a href="/windows-hardware/drivers/">DevNode</a>) 取得裝置實例的狀態。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_DevNode_Status_Ex</strong>函式會從本機或遠端電腦<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>上的裝置節點 (<a href="/windows-hardware/drivers/">DevNode</a>) 取得裝置實例的狀態。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a><br/></td>
<td><strong>CM_Get_First_Log_Conf</strong>函式會取得指定之設定類型的第一個<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定，此設定類型與本機電腦上指定的<a href="/windows-hardware/drivers/">裝置實例</a>相關聯。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_First_Log_Conf_Ex</strong>函式會取得與本機或遠端電腦上指定之<a href="/windows-hardware/drivers/">裝置實例</a>相關聯的第一個<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。
</blockquote>
<br/> <strong>CM_Get_HW_Prof_Flags</strong>函式會針對本機電腦上的<a href="/windows-hardware/drivers/">裝置實例</a>，抓取<a href="/windows-hardware/drivers/">硬體設定檔</a>特定的設定旗標。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
此函式已被取代，不應該使用。
</blockquote>
<br/> <strong>CM_Get_HW_Prof_Flags_Ex</strong>函式會針對遠端電腦或本機電腦上的<a href="/windows-hardware/drivers/">裝置實例</a>，抓取<a href="/windows-hardware/drivers/">硬體設定檔</a>特定的設定旗標。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a><br/></td>
<td><strong>CM_Get_Log_Conf_Priority</strong>函式會取得本機電腦上指定之<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定的設定優先權。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Log_Conf_Priority_Ex</strong>函數會取得本機或遠端電腦上指定之<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定的設定優先權。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a><br/></td>
<td><strong>CM_Get_Next_Log_Conf</strong>函數會取得與本機電腦上特定<a href="/windows-hardware/drivers/">裝置實例</a>相關聯的下一個<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Next_Log_Conf_Ex</strong>函數會取得與本機或遠端電腦上特定<a href="/windows-hardware/drivers/">裝置實例</a>相關聯的下一個<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a><br/></td>
<td><strong>CM_Get_Next_Res_Des</strong>函式會針對本機電腦上的<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定，取得指定資源類型之下一個<a href="/windows-hardware/drivers/">資源描述</a>項的控制碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Next_Res_Des_Ex</strong>函式會針對本機或遠端電腦上的<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定，取得所指定資源類型之下一個<a href="/windows-hardware/drivers/">資源描述</a>元的控制碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a><br/></td>
<td><strong>CM_Get_Parent</strong>函式會取得裝置實例控制碼，以在本機電腦的裝置樹狀結構中 (<a href="/windows-hardware/drivers/">devnode</a>) 的指定裝置節點的父節點。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Parent_Ex</strong>函式會取得指定裝置節點的父節點的裝置實例控制碼， (在本機或遠端電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中<a href="/windows-hardware/drivers/">devnode</a>) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a><br/></td>
<td><strong>CM_Get_Res_Des_Data</strong>函式會抓取儲存在本機電腦上的<a href="/windows-hardware/drivers/">資源描述</a>項中的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Res_Des_Data_Ex</strong>函式會抓取儲存在本機或遠端電腦上<a href="/windows-hardware/drivers/">資源描述</a>項中的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a><br/></td>
<td><strong>CM_Get_Res_Des_Data_Size</strong>函式會取得保存本機電腦上指定之<a href="/windows-hardware/drivers/">資源描述</a>項所需資訊的緩衝區大小。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Res_Des_Data_Size_Ex</strong>函式會取得保存本機或遠端電腦上指定之<a href="/windows-hardware/drivers/">資源描述</a>項所需資訊的緩衝區大小。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a><br/></td>
<td><strong>CM_Get_Resource_Conflict_Count</strong>函數會取得指定之資源衝突清單中包含的衝突數目。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a><br/></td>
<td><strong>CM_Get_Resource_Conflict_Details</strong>函數會取得衝突清單中其中一個資源衝突的詳細資料。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a><br/></td>
<td><strong>CM_Get_Sibling</strong>函式會取得裝置實例控制碼至指定裝置節點的下一個同級節點， (<a href="/windows-hardware/drivers/">devnode</a>) 在本機電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> 。
</blockquote>
<br/> <strong>CM_Get_Sibling_Ex</strong>函式會在本機或遠端電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中，取得指定裝置節點下一個同級節點的裝置實例控制碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。
</blockquote>
<br/> <strong>CM_Get_Version</strong>函式會針對本機電腦，傳回隨插即用 (PnP) <a href="/windows-hardware/drivers/"></a>設定管理員 DLL <em> (Cfgmgr32.dll) 的</em>4.0 版。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。
</blockquote>
<br/> <strong>CM_Get_Version_Ex</strong>函式會針對本機或遠端電腦，傳回隨插即用 (PnP) 設定管理員<a href="/windows-hardware/drivers/">DLL</a> <em> (Cfgmgr32.dll) 的</em>4.0 版。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a><br/></td>
<td><strong>CM_Is_Dock_Station_Present</strong>函式會識別<a href="/windows-hardware/drivers/">銜接站</a>是否存在於本機電腦上。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> 。
</blockquote>
<br/> <strong>CM_Is_Dock_Station_Present_Ex</strong>函式會識別<a href="/windows-hardware/drivers/">銜接站</a>是否存在於本機或遠端電腦上。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。
</blockquote>
<br/> <strong>CM_Is_Version_Available</strong>函式會指出本機電腦是否支援指定版本的隨插即用 (PnP) 設定管理員<a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。
</blockquote>
<br/> <strong>CM_Is_Version_Available_Ex</strong>函式會指出本機或遠端電腦是否支援指定版本的隨插即用 (PNP) 設定管理員<a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) 。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a><br/></td>
<td><strong>CM_Locate_DevNode</strong>函式會取得與本機電腦上指定的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>相關聯之裝置節點的裝置實例控制碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> 。
</blockquote>
<br/> <strong>CM_Locate_DevNode_Ex</strong>函式會在本機電腦或遠端電腦上，取得與指定的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>相關聯之裝置節點的裝置實例控制碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a><br/></td>
<td>將指定的 <strong>CONFIGRET</strong> 程式碼轉換成其對等的系統錯誤碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a><br/></td>
<td><strong>CM_Modify_Res_Des</strong>函數會修改本機電腦上指定的資源描述項。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> 。
</blockquote>
<br/> <strong>CM_Modify_Res_Des_Ex</strong>函數會修改本機或遠端電腦上指定的資源描述項。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a><br/></td>
<td>此列舉會識別隨插即用裝置事件種類。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a><br/></td>
<td>這是裝置通知事件資料結構。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a><br/></td>
<td>裝置通知篩選結構<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a><br/></td>
<td><strong>CM_Open_Class_Key</strong>函式會開啟裝置安裝類別登錄機碼、裝置介面類別別登錄機碼或類別的特定子機碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a><br/></td>
<td><strong>CM_Open_Device_Interface_Key</strong>函式會開啟登錄子機碼，讓應用程式和驅動程式用來儲存特定于裝置介面的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> 。
</blockquote>
<br/> <strong>CM_Open_Device_Interface_Key_ExA</strong>函式會開啟登錄子機碼，讓應用程式和驅動程式用來儲存特定于裝置介面的資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> 。
</blockquote>
<br/> <strong>CM_Open_Device_Interface_Key_ExW</strong>函式會開啟登錄子機碼，讓應用程式和驅動程式用來儲存特定于裝置介面的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a><br/></td>
<td><strong>CM_Open_DevNode_Key</strong>函式會開啟登錄機碼，以取得裝置特定的設定資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a><br/></td>
<td><strong>CM_Query_And_Remove_SubTree</strong>函式會檢查是否可以移除裝置實例和其子系，如果是，則會移除它們。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> 。
</blockquote>
<br/> <strong>CM_Query_And_Remove_SubTree_Ex</strong>函式會檢查是否可以移除裝置實例和其子系，如果是，則會移除它們。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a><br/></td>
<td><strong>CM_Query_Resource_Conflict_List</strong>函式會識別有資源需求與指定裝置實例的資源描述衝突的裝置實例。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a><br/></td>
<td><strong>CM_Reenumerate_DevNode</strong>函式會列舉指定裝置節點及其所有子系所識別的裝置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> 。
</blockquote>
<br/> <strong>CM_Reenumerate_DevNode_Ex</strong>函式會列舉指定裝置節點及其所有子系所識別的裝置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a><br/></td>
<td>如果您的程式碼是以 Windows 7 或舊版 Windows 為目標，請使用<a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>RegisterDeviceNotification</strong></a>而不是<a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> 。 核心模式呼叫端應該改用 <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification</strong></a> 。<br/> 當所指定類型的 PnP 事件發生時， <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> 函數會註冊要呼叫的應用程式回呼常式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a><br/></td>
<td>如果裝置是卸載式的， <strong>CM_Request_Device_Eject</strong> 函數會準備本機裝置實例以進行安全移除。 如果裝置可以實際退出，則會是。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> 。
</blockquote>
<br/> 如果裝置是卸載式的， <strong>CM_Request_Device_Eject_Ex</strong> 函數會準備本機或遠端裝置實例，以安全地移除。 如果裝置可以實際退出，則會是。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a><br/></td>
<td><strong>CM_Request_Eject_PC</strong>函式會要求將插入本機<a href="/windows-hardware/drivers/">銜接站</a>的可攜式電腦退出。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> 。
</blockquote>
<br/> <strong>CM_Request_Eject_PC_Ex</strong>函式會要求您將插入本機或遠端<a href="/windows-hardware/drivers/">銜接站</a>的可攜式電腦退出。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a><br/></td>
<td><strong>CM_Set_Class_Property</strong>函式會設定裝置安裝類別或裝置介面類別別的類別屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> 。
</blockquote>
<br/> <strong>CM_Set_Class_Property_ExW</strong>函式會設定裝置安裝類別或裝置介面類別別的類別屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a><br/></td>
<td><strong>CM_Set_Class_Registry_Property</strong>函數會設定或刪除<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>的屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a><br/></td>
<td><strong>CM_Set_Device_Interface_Property</strong>函式會設定裝置介面的裝置屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> 。
</blockquote>
<br/> <strong>CM_Set_Device_Interface_Property_ExW</strong>函式會設定裝置介面的裝置屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a><br/></td>
<td><strong>CM_Set_DevNode_Problem</strong>函式會針對安裝在本機電腦上的裝置設定問題代碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> 。
</blockquote>
<br/> <strong>CM_Set_DevNode_Problem_Ex</strong>函式會針對安裝在本機或遠端電腦上的裝置，設定問題代碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a><br/></td>
<td><strong>CM_Set_DevNode_Property</strong>函數會設定裝置實例屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。 請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> 。
</blockquote>
<br/> <strong>CM_Set_DevNode_Property_ExW</strong>函數會設定裝置實例屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a><br/></td>
<td><strong>CM_Set_DevNode_Registry_Property</strong>函數會在登錄中設定指定的裝置屬性。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a><br/></td>
<td><strong>CM_Setup_DevNode</strong>函式會重新開機未執行的裝置實例，因為裝置設定有問題。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a><br/></td>
<td><strong>CM_Uninstall_DevNode</strong>函式會移除與裝置實例相關聯的所有持續性狀態。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a><br/></td>
<td>如果您的程式碼是以 Windows 7 或舊版 Windows 為目標，請使用<a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>UnregisterDeviceNotification</strong></a>而不是<strong>CM_Unregister_Notification</strong> 。<br/> <strong>CM_Unregister_Notification</strong>函式會關閉指定的 HCMNOTIFICATION 控制碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a><br/></td>
<td><strong>CMP_WaitNoPendingInstallEvents</strong>函式會等到沒有任何擱置中的裝置安裝活動，PnP 管理員才能執行。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a><br/></td>
<td>CONFLICT_DETAILS 結構會當做 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> 函數的參數使用。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a><br/></td>
<td>CS_DES 結構是用來指定資源清單，以描述裝置實例的裝置類別特定資源使用方式。 如需資源清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a><br/></td>
<td>CS_RESOURCE 結構是用來指定資源清單，以描述裝置實例的裝置類別特定資源使用方式。 如需資源清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a><br/></td>
<td>DMA_DES 結構會用來指定資源清單或資源需求清單，以描述裝置實例的直接記憶體存取 (DMA) 通道使用方式。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a><br/></td>
<td>DMA_RANGE 結構會指定描述裝置實例 DMA 通道使用方式的資源需求清單。 如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a><br/></td>
<td>DMA_RESOURCE 結構是用來指定資源清單或資源需求清單，以描述裝置實例的 DMA 通道使用方式。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a><br/></td>
<td>IO_DES 結構會用來指定資源清單或資源需求清單，以說明裝置實例的 i/o 埠使用方式。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a><br/></td>
<td>IO_RANGE 結構會指定資源需求清單，以說明裝置實例的 i/o 埠使用量。 如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a><br/></td>
<td>IO_RESOURCE 結構會用來指定資源清單或資源需求清單，以說明裝置實例的 i/o 埠使用方式。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a><br/></td>
<td>IRQ_DES 結構會用來指定資源清單或資源需求清單，以描述裝置實例的 IRQ 線路使用方式。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a><br/></td>
<td>IRQ_RANGE 結構會指定資源需求清單，以描述裝置實例的 IRQ 線路使用方式。 如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a><br/></td>
<td>IRQ_RESOURCE 結構會用來指定資源清單或資源需求清單，以描述裝置實例的 IRQ 線路使用方式。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a><br/></td>
<td>MEM_DES 結構會用來指定資源清單或資源需求清單，以描述裝置實例的記憶體使用量。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a><br/></td>
<td>MEM_RANGE 結構會指定描述裝置實例記憶體使用量的資源需求清單。 如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a><br/></td>
<td>MEM_RESOURCE 結構會用來指定資源清單或資源需求清單，以描述裝置實例的記憶體使用量。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a><br/></td>
<td>MFCARD_DES 結構是用來指定資源清單或資源需求清單，此清單會說明多功能裝置實例所提供之 <em>其中一個</em> 硬體功能的資源使用量。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a><br/></td>
<td>MFCARD_RESOURCE 結構是用來指定資源清單或資源需求清單，此清單會說明多功能裝置實例所提供之 <em>其中一個</em> 硬體功能的資源使用量。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a><br/></td>
<td>PCCARD_DES 結構是用來指定資源清單或資源需求清單，以描述電腦卡實例的資源使用量。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a><br/></td>
<td>PCCARD_RESOURCE 結構是用來指定資源清單或資源需求清單，以描述電腦卡實例的資源使用量。 如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。<br/></td>
</tr>
</tbody>
</table>



 

 

 

[將關於本主題的意見傳送給 Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "將關於本主題的意見傳送給 Microsoft")