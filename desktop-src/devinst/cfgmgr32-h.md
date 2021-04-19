---
title: Cfgmgr32.h
description: 本節包含 Cfgmgr32 標頭的參考主題。
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ccc2baf458fea5e20842c9bfa60028c2cb8e23
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106966273"
---
# <a name="cfgmgr32h"></a><span data-ttu-id="95288-103">Cfgmgr32.h</span><span class="sxs-lookup"><span data-stu-id="95288-103">Cfgmgr32.h</span></span>

<span data-ttu-id="95288-104">本節包含 Cfgmgr32 標頭的參考主題。</span><span class="sxs-lookup"><span data-stu-id="95288-104">This section contains reference topics for the Cfgmgr32.h header.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="95288-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="95288-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95288-106">主題</span><span class="sxs-lookup"><span data-stu-id="95288-106">Topic</span></span></th>
<th><span data-ttu-id="95288-107">描述</span><span class="sxs-lookup"><span data-stu-id="95288-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95288-108"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-108"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-109">BUSNUMBER_DES 結構是用來指定資源清單或資源需求清單，以描述裝置實例的匯流排編號使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-109">The BUSNUMBER_DES structure is used for specifying either a resource list or a resource requirements list that describes bus number usage for a device instance.</span></span> <span data-ttu-id="95288-110">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-110">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-111"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-111"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-112">BUSNUMBER_RANGE 結構會指定資源需求清單，以描述裝置實例的匯流排數量使用情形。</span><span class="sxs-lookup"><span data-stu-id="95288-112">The BUSNUMBER_RANGE structure specifies a resource requirements list that describes bus number usage for a device instance.</span></span> <span data-ttu-id="95288-113">如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-113">For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-114"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-114"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-115">BUSNUMBER_RESOURCE 結構會指定資源清單或資源需求清單，以說明裝置實例的匯流排編號使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-115">The BUSNUMBER_RESOURCE structure specifies either a resource list or a resource requirements list that describes bus number usage for a device instance.</span></span> <span data-ttu-id="95288-116">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-116">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-117"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-117"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-118"><strong>CM_Add_Empty_Log_Conf</strong>函式會在本機電腦上，針對指定的設定類型和指定的裝置實例建立空白<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。</span><span class="sxs-lookup"><span data-stu-id="95288-118">The <strong>CM_Add_Empty_Log_Conf</strong> function creates an empty <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a>, for a specified configuration type and a specified device instance, on the local machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-119"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-119"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-120">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-120">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-121">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-121">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-122"><strong>CM_Add_Empty_Log_Conf_Ex</strong>函式會在本機或遠端電腦上，為指定的設定類型和指定的裝置實例建立空白<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。</span><span class="sxs-lookup"><span data-stu-id="95288-122">The <strong>CM_Add_Empty_Log_Conf_Ex</strong> function creates an empty <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a>, for a specified configuration type and a specified device instance, on either the local or a remote machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-123"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-123"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-124"><strong>CM_Add_ID</strong>函式會將指定的<a href="/windows-hardware/drivers/install/device-ids">裝置識別碼</a>附加 (（如果尚未在<a href="/windows-hardware/drivers/">裝置實例的</a><a href="/windows-hardware/drivers/install/hardware-ids">硬體識別碼</a>清單或<a href="/windows-hardware/drivers/install/compatible-ids">相容識別碼</a>清單中提供) ）。</span><span class="sxs-lookup"><span data-stu-id="95288-124">The <strong>CM_Add_ID</strong> function appends a specified <a href="/windows-hardware/drivers/install/device-ids">device ID</a> (if not already present) to a <a href="/windows-hardware/drivers/">device instance's</a> <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> list or <a href="/windows-hardware/drivers/install/compatible-ids">compatible ID</a> list.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-125"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-125"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-126">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-126">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-127">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-127">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-128"><strong>CM_Add_ID_Ex</strong>函式會在本機或遠端電腦上，將<a href="/windows-hardware/drivers/install/device-ids">裝置識別碼</a> (附加至裝置實例的<a href="/windows-hardware/drivers/install/hardware-ids">硬體識別碼</a>清單或<a href="/windows-hardware/drivers/install/compatible-ids">相容識別碼</a>清單（若尚未) 存在）。</span><span class="sxs-lookup"><span data-stu-id="95288-128">The <strong>CM_Add_ID_Ex</strong> function appends a <a href="/windows-hardware/drivers/install/device-ids">device ID</a> (if not already present) to a device instance's <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a> list or <a href="/windows-hardware/drivers/install/compatible-ids">compatible ID</a> list, on either the local or a remote machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-129"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-129"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-130"><strong>CM_Add_Res_Des</strong>函數會將<a href="/windows-hardware/drivers/">資源描述</a>項新增至<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。</span><span class="sxs-lookup"><span data-stu-id="95288-130">The <strong>CM_Add_Res_Des</strong> function adds a <a href="/windows-hardware/drivers/">resource descriptor</a> to a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-131"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-131"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-132">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-132">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-133">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-133">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-134"><strong>CM_Add_Res_Des_Ex</strong>函數會將<a href="/windows-hardware/drivers/">資源描述</a>項新增至<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。</span><span class="sxs-lookup"><span data-stu-id="95288-134">The <strong>CM_Add_Res_Des_Ex</strong> function adds a <a href="/windows-hardware/drivers/">resource descriptor</a> to a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a>.</span></span> <span data-ttu-id="95288-135">邏輯設定可以位於本機或遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="95288-135">The logical configuration can be on either the local or a remote machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-136"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-136"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-137">從 Windows 8 開始，已移除存取遠端電腦的 Windows Server 2012 功能。</span><span class="sxs-lookup"><span data-stu-id="95288-137">Beginning in Windows 8 and Windows Server 2012 functionality to access remote machines has been removed.</span></span> <span data-ttu-id="95288-138">在這些版本的 Windows 上執行時，您無法存取遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="95288-138">You cannot access remote machines when running on these versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-139"><strong>CM_Connect_Machine</strong>函式會建立與遠端電腦的連接。</span><span class="sxs-lookup"><span data-stu-id="95288-139">The <strong>CM_Connect_Machine</strong> function creates a connection to a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-140"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-140"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-141"><strong>CM_Delete_Class_Key</strong>函數會從系統中移除指定的已安裝<a href="/windows-hardware/drivers/">裝置類別</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-141">The <strong>CM_Delete_Class_Key</strong> function removes the specified installed <a href="/windows-hardware/drivers/">device class</a> from the system.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-142"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-142"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-143"><strong>CM_Delete_Device_Interface_Key</strong>函式會刪除應用程式和驅動程式用來儲存介面特定資訊的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="95288-143">The <strong>CM_Delete_Device_Interface_Key</strong> function deletes the registry subkey that is used by applications and drivers to store interface-specific information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-144"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-144"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-145">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-145">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-146">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-146">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-147"><strong>CM_Delete_Device_Interface_Key_ExA</strong>函式會刪除應用程式和驅動程式用來儲存介面特定資訊的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="95288-147">The <strong>CM_Delete_Device_Interface_Key_ExA</strong> function deletes the registry subkey that is used by applications and drivers to store interface-specific information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-148"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-148"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-149">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-149">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-150">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-150">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-151"><strong>CM_Delete_Device_Interface_Key_ExW</strong>函式會刪除應用程式和驅動程式用來儲存介面特定資訊的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="95288-151">The <strong>CM_Delete_Device_Interface_Key_ExW</strong> function deletes the registry subkey that is used by applications and drivers to store interface-specific information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-152"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-152"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-153"><strong>CM_Delete_DevNode_Key</strong>函式會刪除與裝置相關聯之指定的使用者可存取登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="95288-153">The <strong>CM_Delete_DevNode_Key</strong> function deletes the specified user-accessible registry keys that are associated with a device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-154"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-154"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-155"><strong>CM_Disable_DevNode</strong>函式會停用裝置。</span><span class="sxs-lookup"><span data-stu-id="95288-155">The <strong>CM_Disable_DevNode</strong> function disables a device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-156"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-156"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-157">從 Windows 8 開始，已移除存取遠端電腦的 Windows Server 2012 功能。</span><span class="sxs-lookup"><span data-stu-id="95288-157">Beginning in Windows 8 and Windows Server 2012 functionality to access remote machines has been removed.</span></span> <span data-ttu-id="95288-158">在這些版本的 Windows 上執行時，您無法存取遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="95288-158">You cannot access remote machines when running on these versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-159"><strong>CM_Disconnect_Machine</strong>函式會移除遠端電腦的連接。</span><span class="sxs-lookup"><span data-stu-id="95288-159">The <strong>CM_Disconnect_Machine</strong> function removes a connection to a remote machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-160"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-160"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-161"><strong>CM_Enable_DevNode</strong>函式會啟用裝置。</span><span class="sxs-lookup"><span data-stu-id="95288-161">The <strong>CM_Enable_DevNode</strong> function enables a device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-162"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-162"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-163">重複呼叫 <strong>CM_Enumerate_Classes</strong> 函式時，會藉由提供每個類別的 GUID 來列舉本機電腦已安裝的 <a href="/windows-hardware/drivers/">裝置類別</a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-163">The <strong>CM_Enumerate_Classes</strong> function, when called repeatedly, enumerates the local machine's installed <a href="/windows-hardware/drivers/">device classes</a> by supplying each class's GUID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-164"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-164"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-165">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-165">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-166">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-166">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-167">重複呼叫 <strong>CM_Enumerate_Classes_Ex</strong> 函式時，會藉由提供每個類別的 GUID 來列舉本機或遠端電腦的已安裝 <a href="/windows-hardware/drivers/">裝置類別</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-167">The <strong>CM_Enumerate_Classes_Ex</strong> function, when called repeatedly, enumerates a local or a remote machine's installed <a href="/windows-hardware/drivers/">device classes</a>, by supplying each class's GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-168"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-168"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-169"><strong>CM_Enumerate_Enumerators</strong>函式會藉由提供每個列舉值的名稱來列舉本機電腦的裝置枚舉器。</span><span class="sxs-lookup"><span data-stu-id="95288-169">The <strong>CM_Enumerate_Enumerators</strong> function enumerates the local machine's device enumerators by supplying each enumerator's name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-170"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-170"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-171">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-171">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-172">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-172">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-173"><strong>CM_Enumerate_Enumerators_Ex</strong>函式會藉由提供每個列舉值的名稱，來列舉本機或遠端電腦的裝置枚舉器。</span><span class="sxs-lookup"><span data-stu-id="95288-173">The <strong>CM_Enumerate_Enumerators_Ex</strong> function enumerates a local or a remote machine's device enumerators, by supplying each enumerator's name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-174"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-174"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-175"><strong>CM_Free_Log_Conf</strong>函式會從本機電腦移除<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定和所有相關聯的<a href="/windows-hardware/drivers/">資源描述</a>項。</span><span class="sxs-lookup"><span data-stu-id="95288-175">The <strong>CM_Free_Log_Conf</strong> function removes a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> and all associated <a href="/windows-hardware/drivers/">resource descriptors</a> from the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-176"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-176"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-177">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-177">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-178">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-178">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-179"><strong>CM_Free_Log_Conf_Ex</strong>函式會從本機或遠端電腦移除<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定和所有相關聯的<a href="/windows-hardware/drivers/">資源描述</a>項。</span><span class="sxs-lookup"><span data-stu-id="95288-179">The <strong>CM_Free_Log_Conf_Ex</strong> function removes a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> and all associated <a href="/windows-hardware/drivers/">resource descriptors</a> from either a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-180"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-180"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-181"><strong>CM_Free_Log_Conf_Handle</strong>函式會使邏輯設定控制碼失效，並釋放其相關聯的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="95288-181">The <strong>CM_Free_Log_Conf_Handle</strong> function invalidates a logical configuration handle and frees its associated memory allocation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-182"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-182"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-183"><strong>CM_Free_Res_Des</strong>函式會從本機電腦上的<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定移除<a href="/windows-hardware/drivers/">資源描述</a>項。</span><span class="sxs-lookup"><span data-stu-id="95288-183">The <strong>CM_Free_Res_Des</strong> function removes a <a href="/windows-hardware/drivers/">resource descriptor</a> from a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-184"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-184"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-185">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-185">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-186">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-186">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-187"><strong>CM_Free_Res_Des_Ex</strong>函式會從本機或遠端電腦上的<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定移除<a href="/windows-hardware/drivers/">資源描述</a>項。</span><span class="sxs-lookup"><span data-stu-id="95288-187">The <strong>CM_Free_Res_Des_Ex</strong> function removes a <a href="/windows-hardware/drivers/">resource descriptor</a> from a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on either a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-188"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-188"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-189"><strong>CM_Free_Res_Des_Handle</strong>函式會使資源描述控制碼失效，並釋放其相關聯的記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="95288-189">The <strong>CM_Free_Res_Des_Handle</strong> function invalidates a resource description handle and frees its associated memory allocation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-190"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-190"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-191"><strong>CM_Free_Resource_Conflict_Handle</strong>函式會使資源衝突清單的控制碼失效，並釋放控制碼的相關記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="95288-191">The <strong>CM_Free_Resource_Conflict_Handle</strong> function invalidates a handle to a resource conflict list, and frees the handle's associated memory allocation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-192"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-192"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-193"><strong>CM_Get_Child</strong>函式可用來將裝置實例控制碼取出至指定裝置節點的第一個子節點， (<a href="/windows-hardware/drivers/">devnode</a>) 在本機電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中。</span><span class="sxs-lookup"><span data-stu-id="95288-193">The <strong>CM_Get_Child</strong> function is used to retrieve a device instance handle to the first child node of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) in the local machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-194"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-194"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-195">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-195">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-196">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-196">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-197"><strong>CM_Get_Child_Ex</strong>函式可用來將裝置實例控制碼取出至指定裝置節點的第一個子節點， (在本機或遠端電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中<a href="/windows-hardware/drivers/">devnode</a>) 。</span><span class="sxs-lookup"><span data-stu-id="95288-197">The <strong>CM_Get_Child_Ex</strong> function is used to retrieve a device instance handle to the first child node of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) in a local or a remote machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-198"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-198"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-199"><strong>CM_Get_Class_Property</strong>函式會抓取針對<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>或<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-199">The <strong>CM_Get_Class_Property</strong> function retrieves a device property that is set for a <a href="/windows-hardware/drivers/install/device-interface-classes">device interface class</a> or <a href="/windows-hardware/drivers/install/device-setup-classes">device setup class</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-200"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-200"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-201">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-201">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-202">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-202">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-203"><strong>CM_Get_Class_Property_ExW</strong>函式會抓取針對<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>或<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-203">The <strong>CM_Get_Class_Property_ExW</strong> function retrieves a device property that is set for a <a href="/windows-hardware/drivers/install/device-interface-classes">device interface class</a> or <a href="/windows-hardware/drivers/install/device-setup-classes">device setup class</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-204"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-204"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-205"><strong>CM_Get_Class_Property_Keys</strong>函式會抓取裝置屬性索引鍵的陣列，該陣列代表針對<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>或<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>所設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-205">The <strong>CM_Get_Class_Property_Keys</strong> function retrieves an array of the device property keys that represent the device properties that are set for a <a href="/windows-hardware/drivers/install/device-interface-classes">device interface class</a> or <a href="/windows-hardware/drivers/install/device-setup-classes">device setup class</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-206"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-206"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-207">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-207">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-208">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-208">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-209"><strong>CM_Get_Class_Property_Keys_Ex</strong>函式會抓取裝置屬性索引鍵的陣列，該陣列代表針對<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>或<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>所設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-209">The <strong>CM_Get_Class_Property_Keys_Ex</strong> function retrieves an array of the device property keys that represent the device properties that are set for a <a href="/windows-hardware/drivers/install/device-interface-classes">device interface class</a> or <a href="/windows-hardware/drivers/install/device-setup-classes">device setup class</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-210"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-210"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-211"><strong>CM_Get_Class_Registry_Property</strong>函式會捕獲<a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">裝置安裝類別屬性</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-211">The <strong>CM_Get_Class_Registry_Property</strong> function retrieves a <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">device setup class property</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-212"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-212"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-213"><strong>CM_Get_Depth</strong>函式可用來取得指定裝置節點的深度 (在本機電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中的<a href="/windows-hardware/drivers/">devnode</a>) 。</span><span class="sxs-lookup"><span data-stu-id="95288-213">The <strong>CM_Get_Depth</strong> function is used to obtain the depth of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) within the local machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-214"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-214"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-215">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-215">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-216">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-216">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-217"><strong>CM_Get_Depth_Ex</strong>函式可用來取得指定裝置節點的深度 (在本機或遠端電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中的<a href="/windows-hardware/drivers/">devnode</a>) 。</span><span class="sxs-lookup"><span data-stu-id="95288-217">The <strong>CM_Get_Depth_Ex</strong> function is used to obtain the depth of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) within a local or a remote machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-218"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-218"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-219"><strong>CM_Get_Device_ID</strong>函式會取得本機電腦上指定之<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-219">The <strong>CM_Get_Device_ID</strong> function retrieves the <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> for a specified <a href="/windows-hardware/drivers/">device instance</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-220"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-220"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-221">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-221">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-222">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-222">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-223"><strong>CM_Get_Device_ID_Ex</strong>函式會抓取本機或遠端電腦上指定之<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-223">The <strong>CM_Get_Device_ID_Ex</strong> function retrieves the <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> for a specified <a href="/windows-hardware/drivers/">device instance</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-224"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-224"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-225"><strong>CM_Get_Device_ID_List</strong>函式會針對本機電腦的<a href="/windows-hardware/drivers/">裝置實例</a>，抓取<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>的清單。</span><span class="sxs-lookup"><span data-stu-id="95288-225">The <strong>CM_Get_Device_ID_List</strong> function retrieves a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for the local computer's <a href="/windows-hardware/drivers/">device instances</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-226"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-226"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-227">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-227">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-228">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-228">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-229"><strong>CM_Get_Device_ID_List_Ex</strong>函式會針對本機或遠端電腦上的<a href="/windows-hardware/drivers/">裝置實例</a>，抓取<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>的清單。</span><span class="sxs-lookup"><span data-stu-id="95288-229">The <strong>CM_Get_Device_ID_List_Ex</strong> function retrieves a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for the <a href="/windows-hardware/drivers/">device instances</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-230"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-230"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-231"><strong>CM_Get_Device_ID_List_Size</strong>函式會抓取保存本機電腦<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>清單所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="95288-231">The <strong>CM_Get_Device_ID_List_Size</strong> function retrieves the buffer size required to hold a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for the local machine's <a href="/windows-hardware/drivers/">device instances</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-232"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-232"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-233">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-233">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-234">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-234">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-235"><strong>CM_Get_Device_ID_List_Size_Ex</strong>函式會抓取保存本機或遠端電腦<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>清單所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="95288-235">The <strong>CM_Get_Device_ID_List_Size_Ex</strong> function retrieves the buffer size required to hold a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for a local or a remote machine's <a href="/windows-hardware/drivers/">device instances</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-236"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-236"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-237"><strong>CM_Get_Device_ID_Size</strong>函式會抓取在本機電腦上保存<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="95288-237">The <strong>CM_Get_Device_ID_Size</strong> function retrieves the buffer size required to hold a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> for a <a href="/windows-hardware/drivers/">device instance</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-238"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-238"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-239">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-239">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-240">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-240">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-241"><strong>CM_Get_Device_ID_Size_Ex</strong>函式會抓取在本機或遠端電腦上保存<a href="/windows-hardware/drivers/">裝置實例</a>的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="95288-241">The <strong>CM_Get_Device_ID_Size_Ex</strong> function retrieves the buffer size required to hold a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> for a <a href="/windows-hardware/drivers/">device instance</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-242"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-242"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-243">如果別名存在， <strong>CM_Get_Device_Interface_Alias</strong> 函數會傳回指定之裝置介面實例的別名。</span><span class="sxs-lookup"><span data-stu-id="95288-243">The <strong>CM_Get_Device_Interface_Alias</strong> function returns the alias of the specified device interface instance, if the alias exists.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-244"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-244"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-245"><strong>CM_Get_Device_Interface_List</strong>函式會抓取屬於指定<a href="/windows-hardware/drivers/install/device-interface-classes">裝置介面類別別</a>的裝置介面實例清單。</span><span class="sxs-lookup"><span data-stu-id="95288-245">The <strong>CM_Get_Device_Interface_List</strong> function retrieves a list of device interface instances that belong to a specified <a href="/windows-hardware/drivers/install/device-interface-classes">device interface class</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-246"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-246"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-247"><strong>CM_Get_Device_Interface_List_Size</strong>函式會抓取必須傳遞至<a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a>函數的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="95288-247">The <strong>CM_Get_Device_Interface_List_Size</strong> function retrieves the buffer size that must be passed to the <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-248"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-248"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-249"><strong>CM_Get_Device_Interface_Property</strong>函式會抓取針對裝置介面設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-249">The <strong>CM_Get_Device_Interface_Property</strong> function retrieves a device property that is set for a device interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-250"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-250"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-251">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-251">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-252">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-252">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-253"><strong>CM_Get_Device_Interface_Property_ExW</strong>函式會抓取針對裝置介面設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-253">The <strong>CM_Get_Device_Interface_Property_ExW</strong> function retrieves a device property that is set for a device interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-254"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-254"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-255"><strong>CM_Get_Device_Interface_Property_Keys</strong>函式會抓取裝置屬性索引鍵的陣列，代表針對裝置介面設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-255">The <strong>CM_Get_Device_Interface_Property_Keys</strong> function retrieves an array of device property keys that represent the device properties that are set for a device interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-256"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-256"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-257">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-257">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-258">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-258">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-259"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong>函式會抓取裝置屬性索引鍵的陣列，代表針對裝置介面設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-259">The <strong>CM_Get_Device_Interface_Property_Keys_ExW</strong> function retrieves an array of device property keys that represent the device properties that are set for a device interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-260"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-260"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-261"><strong>CM_Get_DevNode_Property</strong>函式會捕獲裝置實例屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-261">The <strong>CM_Get_DevNode_Property</strong> function retrieves a device instance property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-262"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-262"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-263">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-263">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-264">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-264">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-265"><strong>CM_Get_DevNode_Property_ExW</strong>函式會捕獲裝置實例屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-265">The <strong>CM_Get_DevNode_Property_ExW</strong> function retrieves a device instance property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-266"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-266"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-267"><strong>CM_Get_DevNode_Property_Keys</strong>函式會抓取裝置屬性索引鍵的陣列，以代表針對裝置實例所設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-267">The <strong>CM_Get_DevNode_Property_Keys</strong> function retrieves an array of the device property keys that represent the device properties that are set for a device instance.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-268"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-268"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-269">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-269">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-270">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-270">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-271"><strong>CM_Get_DevNode_Property_Keys_Ex</strong>函式會抓取裝置屬性索引鍵的陣列，以代表針對裝置實例所設定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-271">The <strong>CM_Get_DevNode_Property_Keys_Ex</strong> function retrieves an array of the device property keys that represent the device properties that are set for a device instance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-272"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-272"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-273"><strong>CM_Get_DevNode_Registry_Property</strong>函式會從登錄中取出指定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-273">The <strong>CM_Get_DevNode_Registry_Property</strong> function retrieves a specified device property from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-274"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-274"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-275"><strong>CM_Get_DevNode_Status</strong>函式會在本機電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中，從其裝置節點 (<a href="/windows-hardware/drivers/">DevNode</a>) 取得裝置實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="95288-275">The <strong>CM_Get_DevNode_Status</strong> function obtains the status of a device instance from its device node (<a href="/windows-hardware/drivers/">devnode</a>) in the local machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-276"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-276"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-277">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-277">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-278">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-278">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-279"><strong>CM_Get_DevNode_Status_Ex</strong>函式會從本機或遠端電腦<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>上的裝置節點 (<a href="/windows-hardware/drivers/">DevNode</a>) 取得裝置實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="95288-279">The <strong>CM_Get_DevNode_Status_Ex</strong> function obtains the status of a device instance from its device node (<a href="/windows-hardware/drivers/">devnode</a>) on a local or a remote machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-280"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-280"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-281"><strong>CM_Get_First_Log_Conf</strong>函式會取得指定之設定類型的第一個<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定，此設定類型與本機電腦上指定的<a href="/windows-hardware/drivers/">裝置實例</a>相關聯。</span><span class="sxs-lookup"><span data-stu-id="95288-281">The <strong>CM_Get_First_Log_Conf</strong> function obtains the first <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a>, of a specified configuration type, associated with a specified <a href="/windows-hardware/drivers/">device instance</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-282"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-282"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-283">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-283">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-284">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-284">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-285"><strong>CM_Get_First_Log_Conf_Ex</strong>函式會取得與本機或遠端電腦上指定之<a href="/windows-hardware/drivers/">裝置實例</a>相關聯的第一個<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。</span><span class="sxs-lookup"><span data-stu-id="95288-285">The <strong>CM_Get_First_Log_Conf_Ex</strong> function obtains the first <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> associated with a specified <a href="/windows-hardware/drivers/">device instance</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-286"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-286"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-287">從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="95288-287">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-288"><strong>CM_Get_HW_Prof_Flags</strong>函式會針對本機電腦上的<a href="/windows-hardware/drivers/">裝置實例</a>，抓取<a href="/windows-hardware/drivers/">硬體設定檔</a>特定的設定旗標。</span><span class="sxs-lookup"><span data-stu-id="95288-288">The <strong>CM_Get_HW_Prof_Flags</strong> function retrieves the <a href="/windows-hardware/drivers/">hardware profile</a>-specific configuration flags for a <a href="/windows-hardware/drivers/">device instance</a> on a local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-289"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-289"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-290">此函式已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="95288-290">This function has been deprecated and should not be used.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-291"><strong>CM_Get_HW_Prof_Flags_Ex</strong>函式會針對遠端電腦或本機電腦上的<a href="/windows-hardware/drivers/">裝置實例</a>，抓取<a href="/windows-hardware/drivers/">硬體設定檔</a>特定的設定旗標。</span><span class="sxs-lookup"><span data-stu-id="95288-291">The <strong>CM_Get_HW_Prof_Flags_Ex</strong> function retrieves the <a href="/windows-hardware/drivers/">hardware profile</a>-specific configuration flags for a <a href="/windows-hardware/drivers/">device instance</a> on a remote machine or a local machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-292"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-292"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-293"><strong>CM_Get_Log_Conf_Priority</strong>函式會取得本機電腦上指定之<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定的設定優先權。</span><span class="sxs-lookup"><span data-stu-id="95288-293">The <strong>CM_Get_Log_Conf_Priority</strong> function obtains the configuration priority of a specified <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-294"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-294"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-295">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-295">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-296">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-296">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-297"><strong>CM_Get_Log_Conf_Priority_Ex</strong>函數會取得本機或遠端電腦上指定之<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定的設定優先權。</span><span class="sxs-lookup"><span data-stu-id="95288-297">The <strong>CM_Get_Log_Conf_Priority_Ex</strong> function obtains the configuration priority of a specified <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-298"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-298"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-299"><strong>CM_Get_Next_Log_Conf</strong>函數會取得與本機電腦上特定<a href="/windows-hardware/drivers/">裝置實例</a>相關聯的下一個<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。</span><span class="sxs-lookup"><span data-stu-id="95288-299">The <strong>CM_Get_Next_Log_Conf</strong> function obtains the next <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> associated with a specific <a href="/windows-hardware/drivers/">device instance</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-300"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-300"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-301">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-301">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-302">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-302">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-303"><strong>CM_Get_Next_Log_Conf_Ex</strong>函數會取得與本機或遠端電腦上特定<a href="/windows-hardware/drivers/">裝置實例</a>相關聯的下一個<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定。</span><span class="sxs-lookup"><span data-stu-id="95288-303">The <strong>CM_Get_Next_Log_Conf_Ex</strong> function obtains the next <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> associated with a specific <a href="/windows-hardware/drivers/">device instance</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-304"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-304"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-305"><strong>CM_Get_Next_Res_Des</strong>函式會針對本機電腦上的<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定，取得指定資源類型之下一個<a href="/windows-hardware/drivers/">資源描述</a>項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="95288-305">The <strong>CM_Get_Next_Res_Des</strong> function obtains a handle to the next <a href="/windows-hardware/drivers/">resource descriptor</a>, of a specified resource type, for a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-306"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-306"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-307">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-307">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-308">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-308">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-309"><strong>CM_Get_Next_Res_Des_Ex</strong>函式會針對本機或遠端電腦上的<a href="/windows-hardware/drivers/kernel/hardware-resources">邏輯</a>設定，取得所指定資源類型之下一個<a href="/windows-hardware/drivers/">資源描述</a>元的控制碼。</span><span class="sxs-lookup"><span data-stu-id="95288-309">The <strong>CM_Get_Next_Res_Des_Ex</strong> function obtains a handle to the next <a href="/windows-hardware/drivers/">resource descriptor</a>, of a specified resource type, for a <a href="/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-310"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-310"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-311"><strong>CM_Get_Parent</strong>函式會取得裝置實例控制碼，以在本機電腦的裝置樹狀結構中 (<a href="/windows-hardware/drivers/">devnode</a>) 的指定裝置節點的父節點。</span><span class="sxs-lookup"><span data-stu-id="95288-311">The <strong>CM_Get_Parent</strong> function obtains a device instance handle to the parent node of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) in the local machine's device tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-312"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-312"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-313">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-313">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-314">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-314">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-315"><strong>CM_Get_Parent_Ex</strong>函式會取得指定裝置節點的父節點的裝置實例控制碼， (在本機或遠端電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中<a href="/windows-hardware/drivers/">devnode</a>) 。</span><span class="sxs-lookup"><span data-stu-id="95288-315">The <strong>CM_Get_Parent_Ex</strong> function obtains a device instance handle to the parent node of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) in a local or a remote machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-316"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-316"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-317"><strong>CM_Get_Res_Des_Data</strong>函式會抓取儲存在本機電腦上的<a href="/windows-hardware/drivers/">資源描述</a>項中的資訊。</span><span class="sxs-lookup"><span data-stu-id="95288-317">The <strong>CM_Get_Res_Des_Data</strong> function retrieves the information stored in a <a href="/windows-hardware/drivers/">resource descriptor</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-318"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-318"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-319">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-319">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-320">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-320">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-321"><strong>CM_Get_Res_Des_Data_Ex</strong>函式會抓取儲存在本機或遠端電腦上<a href="/windows-hardware/drivers/">資源描述</a>項中的資訊。</span><span class="sxs-lookup"><span data-stu-id="95288-321">The <strong>CM_Get_Res_Des_Data_Ex</strong> function retrieves the information stored in a <a href="/windows-hardware/drivers/">resource descriptor</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-322"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-322"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-323"><strong>CM_Get_Res_Des_Data_Size</strong>函式會取得保存本機電腦上指定之<a href="/windows-hardware/drivers/">資源描述</a>項所需資訊的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="95288-323">The <strong>CM_Get_Res_Des_Data_Size</strong> function obtains the buffer size required to hold the information contained in a specified <a href="/windows-hardware/drivers/">resource descriptor</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-324"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-324"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-325">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-325">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-326">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-326">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-327"><strong>CM_Get_Res_Des_Data_Size_Ex</strong>函式會取得保存本機或遠端電腦上指定之<a href="/windows-hardware/drivers/">資源描述</a>項所需資訊的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="95288-327">The <strong>CM_Get_Res_Des_Data_Size_Ex</strong> function obtains the buffer size required to hold the information contained in a specified <a href="/windows-hardware/drivers/">resource descriptor</a> on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-328"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-328"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-329"><strong>CM_Get_Resource_Conflict_Count</strong>函數會取得指定之資源衝突清單中包含的衝突數目。</span><span class="sxs-lookup"><span data-stu-id="95288-329">The <strong>CM_Get_Resource_Conflict_Count</strong> function obtains the number of conflicts contained in a specified resource conflict list.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-330"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-330"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-331"><strong>CM_Get_Resource_Conflict_Details</strong>函數會取得衝突清單中其中一個資源衝突的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="95288-331">The <strong>CM_Get_Resource_Conflict_Details</strong> function obtains the details about one of the resource conflicts in a conflict list.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-332"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-332"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-333"><strong>CM_Get_Sibling</strong>函式會取得裝置實例控制碼至指定裝置節點的下一個同級節點， (<a href="/windows-hardware/drivers/">devnode</a>) 在本機電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中。</span><span class="sxs-lookup"><span data-stu-id="95288-333">The <strong>CM_Get_Sibling</strong> function obtains a device instance handle to the next sibling node of a specified device node (<a href="/windows-hardware/drivers/">devnode</a>) in the local machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-334"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-334"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-335">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-335">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-336">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-336">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-337"><strong>CM_Get_Sibling_Ex</strong>函式會在本機或遠端電腦的<a href="/windows-hardware/drivers/kernel/device-tree">裝置樹狀結構</a>中，取得指定裝置節點下一個同級節點的裝置實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="95288-337">The <strong>CM_Get_Sibling_Ex</strong> function obtains a device instance handle to the next sibling node of a specified device node, in a local or a remote machine's <a href="/windows-hardware/drivers/kernel/device-tree">device tree</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-338"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-338"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-339">從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="95288-339">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-340"><strong>CM_Get_Version</strong>函式會針對本機電腦，傳回隨插即用 (PnP) <a href="/windows-hardware/drivers/"></a>設定管理員 DLL <em> (Cfgmgr32.dll) 的</em>4.0 版。</span><span class="sxs-lookup"><span data-stu-id="95288-340">The <strong>CM_Get_Version</strong> function returns version 4.0 of the Plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) for a local machine.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-341"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-341"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-342">從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="95288-342">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-343"><strong>CM_Get_Version_Ex</strong>函式會針對本機或遠端電腦，傳回隨插即用 (PnP) 設定管理員<a href="/windows-hardware/drivers/">DLL</a> <em> (Cfgmgr32.dll) 的</em>4.0 版。</span><span class="sxs-lookup"><span data-stu-id="95288-343">The <strong>CM_Get_Version_Ex</strong> function returns version 4.0 of the Plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) for a local or a remote machine.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-344"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-344"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-345"><strong>CM_Is_Dock_Station_Present</strong>函式會識別<a href="/windows-hardware/drivers/">銜接站</a>是否存在於本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="95288-345">The <strong>CM_Is_Dock_Station_Present</strong> function identifies whether a <a href="/windows-hardware/drivers/">docking station</a> is present in a local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-346"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-346"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-347">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-347">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-348">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-348">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-349"><strong>CM_Is_Dock_Station_Present_Ex</strong>函式會識別<a href="/windows-hardware/drivers/">銜接站</a>是否存在於本機或遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="95288-349">The <strong>CM_Is_Dock_Station_Present_Ex</strong> function identifies whether a <a href="/windows-hardware/drivers/">docking station</a> is present in a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-350"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-350"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-351">從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="95288-351">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-352"><strong>CM_Is_Version_Available</strong>函式會指出本機電腦是否支援指定版本的隨插即用 (PnP) 設定管理員<a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) 。</span><span class="sxs-lookup"><span data-stu-id="95288-352">The <strong>CM_Is_Version_Available</strong> function indicates whether a specified version of the Plug and Play (PnP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) is supported by a local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-353"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-353"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-354">從 Windows 8 和 Windows Server 2012 開始，此函式已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="95288-354">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-355"><strong>CM_Is_Version_Available_Ex</strong>函式會指出本機或遠端電腦是否支援指定版本的隨插即用 (PNP) 設定管理員<a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) 。</span><span class="sxs-lookup"><span data-stu-id="95288-355">The <strong>CM_Is_Version_Available_Ex</strong> function indicates whether a specified version of the Plug and Play (PNP) Configuration Manager <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) is supported by a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-356"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-356"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-357"><strong>CM_Locate_DevNode</strong>函式會取得與本機電腦上指定的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>相關聯之裝置節點的裝置實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="95288-357">The <strong>CM_Locate_DevNode</strong> function obtains a device instance handle to the device node that is associated with a specified <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> on the local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-358"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-358"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-359">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-359">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-360">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-360">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-361"><strong>CM_Locate_DevNode_Ex</strong>函式會在本機電腦或遠端電腦上，取得與指定的<a href="/windows-hardware/drivers/install/device-instance-ids">裝置實例識別碼</a>相關聯之裝置節點的裝置實例控制碼。</span><span class="sxs-lookup"><span data-stu-id="95288-361">The <strong>CM_Locate_DevNode_Ex</strong> function obtains a device instance handle to the device node that is associated with a specified <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>, on a local machine or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-362"><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-362"><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-363">將指定的 <strong>CONFIGRET</strong> 程式碼轉換成其對等的系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="95288-363">Converts a specified <strong>CONFIGRET</strong> code to its equivalent system error code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-364"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-364"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-365"><strong>CM_Modify_Res_Des</strong>函數會修改本機電腦上指定的資源描述項。</span><span class="sxs-lookup"><span data-stu-id="95288-365">The <strong>CM_Modify_Res_Des</strong> function modifies a specified resource descriptor on the local machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-366"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-366"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-367">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-367">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-368">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-368">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-369"><strong>CM_Modify_Res_Des_Ex</strong>函數會修改本機或遠端電腦上指定的資源描述項。</span><span class="sxs-lookup"><span data-stu-id="95288-369">The <strong>CM_Modify_Res_Des_Ex</strong> function modifies a specified resource descriptor on a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-370"><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-370"><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-371">此列舉會識別隨插即用裝置事件種類。</span><span class="sxs-lookup"><span data-stu-id="95288-371">This enumeration identifies Plug and Play device event types.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-372"><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-372"><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-373">這是裝置通知事件資料結構。</span><span class="sxs-lookup"><span data-stu-id="95288-373">This is a device notification event data structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-374"><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-374"><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-375">裝置通知篩選結構</span><span class="sxs-lookup"><span data-stu-id="95288-375">Device notification filter structure</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-376"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-376"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-377"><strong>CM_Open_Class_Key</strong>函式會開啟裝置安裝類別登錄機碼、裝置介面類別別登錄機碼或類別的特定子機碼。</span><span class="sxs-lookup"><span data-stu-id="95288-377">The <strong>CM_Open_Class_Key</strong> function opens the device setup class registry key, the device interface class registry key, or a specific subkey of a class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-378"><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-378"><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-379"><strong>CM_Open_Device_Interface_Key</strong>函式會開啟登錄子機碼，讓應用程式和驅動程式用來儲存特定于裝置介面的資訊。</span><span class="sxs-lookup"><span data-stu-id="95288-379">The <strong>CM_Open_Device_Interface_Key</strong> function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-380"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-380"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-381">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-381">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-382">請改用 <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-382">Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-383"><strong>CM_Open_Device_Interface_Key_ExA</strong>函式會開啟登錄子機碼，讓應用程式和驅動程式用來儲存特定于裝置介面的資訊。</span><span class="sxs-lookup"><span data-stu-id="95288-383">The <strong>CM_Open_Device_Interface_Key_ExA</strong> function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-384"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-384"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-385">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-385">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-386">請改用 <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-386">Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-387"><strong>CM_Open_Device_Interface_Key_ExW</strong>函式會開啟登錄子機碼，讓應用程式和驅動程式用來儲存特定于裝置介面的資訊。</span><span class="sxs-lookup"><span data-stu-id="95288-387">The <strong>CM_Open_Device_Interface_Key_ExW</strong> function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-388"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-388"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-389"><strong>CM_Open_DevNode_Key</strong>函式會開啟登錄機碼，以取得裝置特定的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="95288-389">The <strong>CM_Open_DevNode_Key</strong> function opens a registry key for device-specific configuration information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-390"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-390"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-391"><strong>CM_Query_And_Remove_SubTree</strong>函式會檢查是否可以移除裝置實例和其子系，如果是，則會移除它們。</span><span class="sxs-lookup"><span data-stu-id="95288-391">The <strong>CM_Query_And_Remove_SubTree</strong> function checks whether a device instance and its children can be removed and, if so, it removes them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-392"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-392"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-393">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-393">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-394">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-394">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-395"><strong>CM_Query_And_Remove_SubTree_Ex</strong>函式會檢查是否可以移除裝置實例和其子系，如果是，則會移除它們。</span><span class="sxs-lookup"><span data-stu-id="95288-395">The <strong>CM_Query_And_Remove_SubTree_Ex</strong> function checks whether a device instance and its children can be removed and, if so, it removes them.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-396"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-396"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-397"><strong>CM_Query_Resource_Conflict_List</strong>函式會識別有資源需求與指定裝置實例的資源描述衝突的裝置實例。</span><span class="sxs-lookup"><span data-stu-id="95288-397">The <strong>CM_Query_Resource_Conflict_List</strong> function identifies device instances having resource requirements that conflict with a specified device instance's resource description.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-398"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-398"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-399"><strong>CM_Reenumerate_DevNode</strong>函式會列舉指定裝置節點及其所有子系所識別的裝置。</span><span class="sxs-lookup"><span data-stu-id="95288-399">The <strong>CM_Reenumerate_DevNode</strong> function enumerates the devices identified by a specified device node and all of its children.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-400"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-400"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-401">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-401">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-402">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-402">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-403"><strong>CM_Reenumerate_DevNode_Ex</strong>函式會列舉指定裝置節點及其所有子系所識別的裝置。</span><span class="sxs-lookup"><span data-stu-id="95288-403">The <strong>CM_Reenumerate_DevNode_Ex</strong> function enumerates the devices identified by a specified device node and all of its children.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-404"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-404"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-405">如果您的程式碼是以 Windows 7 或較早的 Windows 版本為目標，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>RegisterDeviceNotification</strong></a> 而不是 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-405">Use <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>RegisterDeviceNotification</strong></a> instead of <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> if your code targets Windows 7 or earlier versions of Windows.</span></span> <span data-ttu-id="95288-406">核心模式呼叫端應該改用 <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-406">Kernel mode callers should use <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification</strong></a> instead.</span></span><br/> <span data-ttu-id="95288-407">當所指定類型的 PnP 事件發生時， <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> 函數會註冊要呼叫的應用程式回呼常式。</span><span class="sxs-lookup"><span data-stu-id="95288-407">The <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> function registers an application callback routine to be called when a PnP event of the specified type occurs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-408"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-408"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-409">如果裝置是卸載式的， <strong>CM_Request_Device_Eject</strong> 函數會準備本機裝置實例以進行安全移除。</span><span class="sxs-lookup"><span data-stu-id="95288-409">The <strong>CM_Request_Device_Eject</strong> function prepares a local device instance for safe removal, if the device is removable.</span></span> <span data-ttu-id="95288-410">如果裝置可以實際退出，則會是。</span><span class="sxs-lookup"><span data-stu-id="95288-410">If the device can be physically ejected, it will be.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-411"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-411"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-412">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-412">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-413">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-413">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-414">如果裝置是卸載式的， <strong>CM_Request_Device_Eject_Ex</strong> 函數會準備本機或遠端裝置實例，以安全地移除。</span><span class="sxs-lookup"><span data-stu-id="95288-414">The <strong>CM_Request_Device_Eject_Ex</strong> function prepares a local or a remote device instance for safe removal, if the device is removable.</span></span> <span data-ttu-id="95288-415">如果裝置可以實際退出，則會是。</span><span class="sxs-lookup"><span data-stu-id="95288-415">If the device can be physically ejected, it will be.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-416"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-416"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-417"><strong>CM_Request_Eject_PC</strong>函式會要求將插入本機<a href="/windows-hardware/drivers/">銜接站</a>的可攜式電腦退出。</span><span class="sxs-lookup"><span data-stu-id="95288-417">The <strong>CM_Request_Eject_PC</strong> function requests that a portable PC, which is inserted in a local <a href="/windows-hardware/drivers/">docking station</a>, be ejected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-418"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-418"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-419">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-419">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-420">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-420">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-421"><strong>CM_Request_Eject_PC_Ex</strong>函式會要求您將插入本機或遠端<a href="/windows-hardware/drivers/">銜接站</a>的可攜式電腦退出。</span><span class="sxs-lookup"><span data-stu-id="95288-421">The <strong>CM_Request_Eject_PC_Ex</strong> function requests that a portable PC, which is inserted in a local or a remote <a href="/windows-hardware/drivers/">docking station</a>, be ejected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-422"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-422"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-423"><strong>CM_Set_Class_Property</strong>函式會設定裝置安裝類別或裝置介面類別別的類別屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-423">The <strong>CM_Set_Class_Property</strong> function sets a class property for a device setup class or a device interface class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-424"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-424"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-425">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-425">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-426">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-426">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-427"><strong>CM_Set_Class_Property_ExW</strong>函式會設定裝置安裝類別或裝置介面類別別的類別屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-427">The <strong>CM_Set_Class_Property_ExW</strong> function sets a class property for a device setup class or a device interface class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-428"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-428"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-429"><strong>CM_Set_Class_Registry_Property</strong>函數會設定或刪除<a href="/windows-hardware/drivers/install/device-setup-classes">裝置安裝類別</a>的屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-429">The <strong>CM_Set_Class_Registry_Property</strong> function sets or deletes a property of a <a href="/windows-hardware/drivers/install/device-setup-classes">device setup class</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-430"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-430"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-431"><strong>CM_Set_Device_Interface_Property</strong>函式會設定裝置介面的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-431">The <strong>CM_Set_Device_Interface_Property</strong> function sets a device property of a device interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-432"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-432"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-433">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-433">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-434">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-434">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-435"><strong>CM_Set_Device_Interface_Property_ExW</strong>函式會設定裝置介面的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-435">The <strong>CM_Set_Device_Interface_Property_ExW</strong> function sets a device property of a device interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-436"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-436"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-437"><strong>CM_Set_DevNode_Problem</strong>函式會針對安裝在本機電腦上的裝置設定問題代碼。</span><span class="sxs-lookup"><span data-stu-id="95288-437">The <strong>CM_Set_DevNode_Problem</strong> function sets a problem code for a device that is installed in a local machine.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-438"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-438"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-439">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-439">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-440">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-440">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-441"><strong>CM_Set_DevNode_Problem_Ex</strong>函式會針對安裝在本機或遠端電腦上的裝置，設定問題代碼。</span><span class="sxs-lookup"><span data-stu-id="95288-441">The <strong>CM_Set_DevNode_Problem_Ex</strong> function sets a problem code for a device that is installed in a local or a remote machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-442"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-442"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-443"><strong>CM_Set_DevNode_Property</strong>函數會設定裝置實例屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-443">The <strong>CM_Set_DevNode_Property</strong> function sets a device instance property.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-444"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-444"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="95288-445">從 Windows 8 和 Windows Server 2012 開始，此函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="95288-445">Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.</span></span> <span data-ttu-id="95288-446">請改用 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="95288-446">Please use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="95288-447"><strong>CM_Set_DevNode_Property_ExW</strong>函數會設定裝置實例屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-447">The <strong>CM_Set_DevNode_Property_ExW</strong> function sets a device instance property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-448"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-448"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-449"><strong>CM_Set_DevNode_Registry_Property</strong>函數會在登錄中設定指定的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="95288-449">The <strong>CM_Set_DevNode_Registry_Property</strong> function sets a specified device property in the registry.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-450"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-450"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-451"><strong>CM_Setup_DevNode</strong>函式會重新開機未執行的裝置實例，因為裝置設定有問題。</span><span class="sxs-lookup"><span data-stu-id="95288-451">The <strong>CM_Setup_DevNode</strong> function restarts a device instance that is not running because there is a problem with the device configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-452"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-452"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-453"><strong>CM_Uninstall_DevNode</strong>函式會移除與裝置實例相關聯的所有持續性狀態。</span><span class="sxs-lookup"><span data-stu-id="95288-453">The <strong>CM_Uninstall_DevNode</strong> function removes all persistent state associated with a device instance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-454"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-454"><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-455">如果您的程式碼是以 Windows 7 或較早的 Windows 版本為目標，請使用 <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>UnregisterDeviceNotification</strong></a> 而不是 <strong>CM_Unregister_Notification</strong> 。</span><span class="sxs-lookup"><span data-stu-id="95288-455">Use <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>UnregisterDeviceNotification</strong></a> instead of <strong>CM_Unregister_Notification</strong> if your code targets Windows 7 or earlier versions of Windows.</span></span><br/> <span data-ttu-id="95288-456"><strong>CM_Unregister_Notification</strong>函式會關閉指定的 HCMNOTIFICATION 控制碼。</span><span class="sxs-lookup"><span data-stu-id="95288-456">The <strong>CM_Unregister_Notification</strong> function closes the specified HCMNOTIFICATION handle.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-457"><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-457"><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-458"><strong>CMP_WaitNoPendingInstallEvents</strong>函式會等到沒有任何擱置中的裝置安裝活動，PnP 管理員才能執行。</span><span class="sxs-lookup"><span data-stu-id="95288-458">The <strong>CMP_WaitNoPendingInstallEvents</strong> function waits until there are no pending device installation activities for the PnP manager to perform.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-459"><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-459"><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-460">CONFLICT_DETAILS 結構會當做 <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> 函數的參數使用。</span><span class="sxs-lookup"><span data-stu-id="95288-460">The CONFLICT_DETAILS structure is used as a parameter to the <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-461"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-461"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-462">CS_DES 結構是用來指定資源清單，以描述裝置實例的裝置類別特定資源使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-462">The CS_DES structure is used for specifying a resource list that describes device class-specific resource usage for a device instance.</span></span> <span data-ttu-id="95288-463">如需資源清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-463">For more information about resource lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-464"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-464"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-465">CS_RESOURCE 結構是用來指定資源清單，以描述裝置實例的裝置類別特定資源使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-465">The CS_RESOURCE structure is used for specifying a resource list that describes device class-specific resource usage for a device instance.</span></span> <span data-ttu-id="95288-466">如需資源清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-466">For more information about resource lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-467"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-467"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-468">DMA_DES 結構會用來指定資源清單或資源需求清單，以描述裝置實例的直接記憶體存取 (DMA) 通道使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-468">The DMA_DES structure is used for specifying either a resource list or a resource requirements list that describes direct memory access (DMA) channel usage for a device instance.</span></span> <span data-ttu-id="95288-469">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-469">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-470"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-470"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-471">DMA_RANGE 結構會指定描述裝置實例 DMA 通道使用方式的資源需求清單。</span><span class="sxs-lookup"><span data-stu-id="95288-471">The DMA_RANGE structure specifies a resource requirements list that describes DMA channel usage for a device instance.</span></span> <span data-ttu-id="95288-472">如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-472">For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-473"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-473"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-474">DMA_RESOURCE 結構是用來指定資源清單或資源需求清單，以描述裝置實例的 DMA 通道使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-474">The DMA_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes DMA channel usage for a device instance.</span></span> <span data-ttu-id="95288-475">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-475">For more information about resource list and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-476"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-476"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-477">IO_DES 結構會用來指定資源清單或資源需求清單，以說明裝置實例的 i/o 埠使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-477">The IO_DES structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance.</span></span> <span data-ttu-id="95288-478">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-478">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-479"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-479"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-480">IO_RANGE 結構會指定資源需求清單，以說明裝置實例的 i/o 埠使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-480">The IO_RANGE structure specifies a resource requirements list that describes I/O port usage for a device instance.</span></span> <span data-ttu-id="95288-481">如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-481">For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-482"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-482"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-483">IO_RESOURCE 結構會用來指定資源清單或資源需求清單，以說明裝置實例的 i/o 埠使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-483">The IO_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes I/O port usage for a device instance.</span></span> <span data-ttu-id="95288-484">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-484">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-485"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-485"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-486">IRQ_DES 結構會用來指定資源清單或資源需求清單，以描述裝置實例的 IRQ 線路使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-486">The IRQ_DES structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance.</span></span> <span data-ttu-id="95288-487">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-487">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-488"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-488"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-489">IRQ_RANGE 結構會指定資源需求清單，以描述裝置實例的 IRQ 線路使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-489">The IRQ_RANGE structure specifies a resource requirements list that describes IRQ line usage for a device instance.</span></span> <span data-ttu-id="95288-490">如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-490">For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-491"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-491"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-492">IRQ_RESOURCE 結構會用來指定資源清單或資源需求清單，以描述裝置實例的 IRQ 線路使用方式。</span><span class="sxs-lookup"><span data-stu-id="95288-492">The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance.</span></span> <span data-ttu-id="95288-493">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-493">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-494"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-494"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-495">MEM_DES 結構會用來指定資源清單或資源需求清單，以描述裝置實例的記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-495">The MEM_DES structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance.</span></span> <span data-ttu-id="95288-496">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-496">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-497"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-497"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-498">MEM_RANGE 結構會指定描述裝置實例記憶體使用量的資源需求清單。</span><span class="sxs-lookup"><span data-stu-id="95288-498">The MEM_RANGE structure specifies a resource requirements list that describes memory usage for a device instance.</span></span> <span data-ttu-id="95288-499">如需資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-499">For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-500"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-500"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-501">MEM_RESOURCE 結構會用來指定資源清單或資源需求清單，以描述裝置實例的記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-501">The MEM_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes memory usage for a device instance.</span></span> <span data-ttu-id="95288-502">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-502">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-503"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-503"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-504">MFCARD_DES 結構是用來指定資源清單或資源需求清單，此清單會說明多功能裝置實例所提供之 <em>其中一個</em> 硬體功能的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-504">The MFCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by <em>one</em> of the hardware functions provided by an instance of a multifunction device.</span></span> <span data-ttu-id="95288-505">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-505">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-506"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-506"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-507">MFCARD_RESOURCE 結構是用來指定資源清單或資源需求清單，此清單會說明多功能裝置實例所提供之 <em>其中一個</em> 硬體功能的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-507">The MFCARD_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes resource usage by <em>one</em> of the hardware functions provided by an instance of a multifunction device.</span></span> <span data-ttu-id="95288-508">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-508">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95288-509"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-509"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-510">PCCARD_DES 結構是用來指定資源清單或資源需求清單，以描述電腦卡實例的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-510">The PCCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by a PC Card instance.</span></span> <span data-ttu-id="95288-511">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-511">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95288-512"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="95288-512"><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="95288-513">PCCARD_RESOURCE 結構是用來指定資源清單或資源需求清單，以描述電腦卡實例的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="95288-513">The PCCARD_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes resource usage by a PC Card instance.</span></span> <span data-ttu-id="95288-514">如需資源清單和資源需求清單的詳細資訊，請參閱 <a href="/windows-hardware/drivers/kernel/hardware-resources">硬體資源</a>。</span><span class="sxs-lookup"><span data-stu-id="95288-514">For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 

[<span data-ttu-id="95288-515">將關於本主題的意見傳送給 Microsoft</span><span class="sxs-lookup"><span data-stu-id="95288-515">Send comments about this topic to Microsoft</span></span>](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "將關於本主題的意見傳送給 Microsoft")