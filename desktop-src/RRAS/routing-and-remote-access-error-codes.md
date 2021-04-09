---
title: 路由和遠端存取錯誤代碼
description: 下列路由和遠端存取 (RRAS) API 錯誤碼定義于 raserror 中。
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15966d009f0690a1db24c21460da5b9e08a38347
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024777"
---
# <a name="routing-and-remote-access-error-codes"></a><span data-ttu-id="881db-103">路由和遠端存取錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="881db-103">Routing and Remote Access Error Codes</span></span>

<span data-ttu-id="881db-104">下列路由和遠端存取 (RRAS) API 錯誤碼定義于 raserror 中。</span><span class="sxs-lookup"><span data-stu-id="881db-104">The following Routing and Remote Access (RRAS) API error codes are defined in raserror.h.</span></span> <span data-ttu-id="881db-105">除非另有指定，否則 Windows 2000 或更新版本的 Windows 中都支援所有錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="881db-105">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="881db-106">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="881db-106">Return code/value</span></span></th>
<th><span data-ttu-id="881db-107">Description</span><span class="sxs-lookup"><span data-stu-id="881db-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <span data-ttu-id="881db-108"><dt><strong>擱置</strong></dt> <dt>600</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-108"><dt><strong>PENDING</strong></dt> <dt>600</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-109">作業暫止。</span><span class="sxs-lookup"><span data-stu-id="881db-109">An operation is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <span data-ttu-id="881db-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-111">提供的埠控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="881db-111">The port handle supplied is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <span data-ttu-id="881db-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-113">指定的埠已開啟。</span><span class="sxs-lookup"><span data-stu-id="881db-113">The specified port is already open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <span data-ttu-id="881db-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-115">提供的緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="881db-115">The buffer supplied is too small.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <span data-ttu-id="881db-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-117">指定的埠資訊不正確。</span><span class="sxs-lookup"><span data-stu-id="881db-117">The port information specified is incorrect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <span data-ttu-id="881db-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-119">無法設定指定的埠資訊。</span><span class="sxs-lookup"><span data-stu-id="881db-119">The port information specified cannot be set.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-120">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-120">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <span data-ttu-id="881db-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-122">指定的埠未連接。</span><span class="sxs-lookup"><span data-stu-id="881db-122">The port specified is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <span data-ttu-id="881db-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-124">偵測到不正確事件。</span><span class="sxs-lookup"><span data-stu-id="881db-124">An event that is not valid was detected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-125">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-125">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <span data-ttu-id="881db-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-127">指定的裝置不存在。</span><span class="sxs-lookup"><span data-stu-id="881db-127">The specified device does not exist.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <span data-ttu-id="881db-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-129">指定的裝置類型不存在。</span><span class="sxs-lookup"><span data-stu-id="881db-129">The specified device type does not exist.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <span data-ttu-id="881db-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-131">提供的緩衝區無效。</span><span class="sxs-lookup"><span data-stu-id="881db-131">The buffer supplied is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <span data-ttu-id="881db-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-133">指定了無法使用的路由。</span><span class="sxs-lookup"><span data-stu-id="881db-133">A route was specified that is not available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-134">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-134">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <span data-ttu-id="881db-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-136">未配置指定的路由。</span><span class="sxs-lookup"><span data-stu-id="881db-136">The specified route is not allocated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <span data-ttu-id="881db-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-138">指定的壓縮無效。</span><span class="sxs-lookup"><span data-stu-id="881db-138">The specified compression is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-139">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-139">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <span data-ttu-id="881db-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-141">可用的緩衝區不足。</span><span class="sxs-lookup"><span data-stu-id="881db-141">There were insufficient buffers available.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <span data-ttu-id="881db-142"><dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-142"><dt><strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-143">找不到指定的埠。</span><span class="sxs-lookup"><span data-stu-id="881db-143">The specified port was not found.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <span data-ttu-id="881db-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-145">非同步要求暫止。</span><span class="sxs-lookup"><span data-stu-id="881db-145">An asynchronous request is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <span data-ttu-id="881db-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-147">指定的埠或裝置已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="881db-147">The specified port or device is already disconnecting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <span data-ttu-id="881db-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-149">指定的連接埠未開啟。</span><span class="sxs-lookup"><span data-stu-id="881db-149">The specified port is not open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <span data-ttu-id="881db-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-151">指定的埠已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="881db-151">The specified port is disconnected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <span data-ttu-id="881db-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-153">無法判斷任何端點。</span><span class="sxs-lookup"><span data-stu-id="881db-153">No endpoints could be determined.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-154">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-154">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <span data-ttu-id="881db-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-156">無法開啟指定的電話簿檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-156">Cannot open the specified phone book file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <span data-ttu-id="881db-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-158">無法載入指定的電話簿檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-158">Cannot load the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <span data-ttu-id="881db-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-160">找不到指定的電話簿專案。</span><span class="sxs-lookup"><span data-stu-id="881db-160">Cannot find the specified phone book entry.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <span data-ttu-id="881db-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-162">無法寫入指定的電話簿檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-162">Cannot write to the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <span data-ttu-id="881db-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-164">指定電話簿中找到的資訊無效。</span><span class="sxs-lookup"><span data-stu-id="881db-164">Information found in the specified phone book is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <span data-ttu-id="881db-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-166">無法載入字串。</span><span class="sxs-lookup"><span data-stu-id="881db-166">A string could not be loaded.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-167">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-167">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <span data-ttu-id="881db-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-169">找不到指定的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="881db-169">Cannot find the specified key.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <span data-ttu-id="881db-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-171">指定的埠已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="881db-171">The specified port was disconnected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <span data-ttu-id="881db-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-173">指定的埠已由遠端電腦中斷連線。</span><span class="sxs-lookup"><span data-stu-id="881db-173">The specified port was disconnected by the remote computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <span data-ttu-id="881db-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-175">指定的埠因硬體失敗而中斷連線。</span><span class="sxs-lookup"><span data-stu-id="881db-175">The specified port was disconnected due to hardware failure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <span data-ttu-id="881db-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-177">指定的埠已被使用者中斷連線。</span><span class="sxs-lookup"><span data-stu-id="881db-177">The specified port was disconnected by the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <span data-ttu-id="881db-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-179">結構大小不正確。</span><span class="sxs-lookup"><span data-stu-id="881db-179">Incorrect structure size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <span data-ttu-id="881db-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-181">指定的埠已在使用中，或未設定遠端存取撥出。</span><span class="sxs-lookup"><span data-stu-id="881db-181">The specified port is already in use or is not configured for remote access dial-out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <span data-ttu-id="881db-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-183">無法在遠端網路上註冊您的電腦。</span><span class="sxs-lookup"><span data-stu-id="881db-183">Your computer could not be registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-184">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-184">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <span data-ttu-id="881db-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-186">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-186">An unknown error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <span data-ttu-id="881db-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-188">錯誤的裝置已附加至指定的埠。</span><span class="sxs-lookup"><span data-stu-id="881db-188">The wrong device is attached to the specified port.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <span data-ttu-id="881db-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-190">偵測到無法轉換的字串。</span><span class="sxs-lookup"><span data-stu-id="881db-190">A string was detected that could not be converted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-191">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-191">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <span data-ttu-id="881db-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-193">要求已逾時。</span><span class="sxs-lookup"><span data-stu-id="881db-193">The request has timed out.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <span data-ttu-id="881db-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-195">沒有任何可用的非同步網路。</span><span class="sxs-lookup"><span data-stu-id="881db-195">No asynchronous net is available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-196">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-196">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <span data-ttu-id="881db-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-198">涉及 NetBIOS 時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-198">An error has occurred involving NetBIOS.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-199">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-199">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <span data-ttu-id="881db-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-201">他的伺服器無法配置支援用戶端所需的 NetBIOS 資源。</span><span class="sxs-lookup"><span data-stu-id="881db-201">he server cannot allocate NetBIOS resources needed to support the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-202">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-202">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <span data-ttu-id="881db-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-204">其中一部電腦的 NetBIOS 名稱已在遠端網路上註冊。</span><span class="sxs-lookup"><span data-stu-id="881db-204">One of your computer's NetBIOS names is already registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-205">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-205">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <span data-ttu-id="881db-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-207">伺服器上的網路介面卡失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-207">A network adapter at the server failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-208">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-208">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <span data-ttu-id="881db-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-210">您將不會收到網路訊息快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="881db-210">You will not receive network message popups.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-211">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-211">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <span data-ttu-id="881db-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-213">發生內部驗證錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-213">An internal authentication error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <span data-ttu-id="881db-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-215">指定的帳號不允許在當日登入。</span><span class="sxs-lookup"><span data-stu-id="881db-215">The specified account is not permitted to log in at this time of day.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <span data-ttu-id="881db-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-217">已停用指定的帳戶。</span><span class="sxs-lookup"><span data-stu-id="881db-217">The specified account is disabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <span data-ttu-id="881db-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-219">指定的密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="881db-219">The specified password has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <span data-ttu-id="881db-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-221">指定的帳號沒有遠端存取許可權。</span><span class="sxs-lookup"><span data-stu-id="881db-221">The specified account does not have remote access permissions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <span data-ttu-id="881db-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-223">遠端存取服務器沒有回應。</span><span class="sxs-lookup"><span data-stu-id="881db-223">The remote access server is not responding.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-224">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-224">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <span data-ttu-id="881db-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-226">您的數據機或其他連接裝置回報了錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-226">Your modem or other connection device has reported an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <span data-ttu-id="881db-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-228">裝置傳回無法辨識的回應。</span><span class="sxs-lookup"><span data-stu-id="881db-228">An unrecognized response was returned by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <span data-ttu-id="881db-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-230">裝置中找不到裝置所需的宏。INF 檔案區段。</span><span class="sxs-lookup"><span data-stu-id="881db-230">A macro required by the device was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <span data-ttu-id="881db-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-232">裝置中的命令或回應。INF 檔案區段指的是未定義的宏。</span><span class="sxs-lookup"><span data-stu-id="881db-232">A command or response in the device .INF file section refers to an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <span data-ttu-id="881db-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-234">在 <message> 裝置中找不到宏。INF 檔案區段。</span><span class="sxs-lookup"><span data-stu-id="881db-234">The <message> macro was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <span data-ttu-id="881db-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-236"><defaultoff>裝置中的宏。INF 檔案區段包含未定義的宏。</span><span class="sxs-lookup"><span data-stu-id="881db-236">The <defaultoff> macro in the device .INF file section contains an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <span data-ttu-id="881db-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-238">裝置。無法開啟 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-238">The device .INF file could not be opened.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <span data-ttu-id="881db-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-240">裝置中的裝置名稱。INF 或媒體。INI 檔案太長。</span><span class="sxs-lookup"><span data-stu-id="881db-240">The device name in the device .INF or media .INI file is too long.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <span data-ttu-id="881db-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-242">媒體。INI 檔案參考未知的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="881db-242">The media .INI file refers to an unknown device name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <span data-ttu-id="881db-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-244">裝置。INF 檔案未包含命令的回應。</span><span class="sxs-lookup"><span data-stu-id="881db-244">The device .INF file contains no responses for the command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <span data-ttu-id="881db-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-246">裝置。INF 檔案遺漏了命令。</span><span class="sxs-lookup"><span data-stu-id="881db-246">The device .INF file is missing a command.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <span data-ttu-id="881db-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-248">嘗試設定未列在裝置中的宏。INF 檔案區段。</span><span class="sxs-lookup"><span data-stu-id="881db-248">Attempted to set a macro not listed in device .INF file section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <span data-ttu-id="881db-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-250">媒體。INI 檔案參考未知的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="881db-250">The media .INI file refers to an unknown device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <span data-ttu-id="881db-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-252">無法配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="881db-252">Cannot allocate memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <span data-ttu-id="881db-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-254">埠未設定遠端存取。</span><span class="sxs-lookup"><span data-stu-id="881db-254">The port is not configured for remote access.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <span data-ttu-id="881db-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-256">您的數據機或其他連接裝置無法運作。</span><span class="sxs-lookup"><span data-stu-id="881db-256">Your modem or other connection device is not functioning.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <span data-ttu-id="881db-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-258">無法讀取媒體。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-258">Cannot read the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <span data-ttu-id="881db-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-260">連線已中斷。</span><span class="sxs-lookup"><span data-stu-id="881db-260">The connection was dropped.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <span data-ttu-id="881db-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-262">Media .ini 檔案中的 usage 參數無效。</span><span class="sxs-lookup"><span data-stu-id="881db-262">The usage parameter in the media .ini file is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <span data-ttu-id="881db-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-264">無法讀取媒體中的區段名稱。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-264">Cannot read the section name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <span data-ttu-id="881db-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-266">無法從媒體讀取裝置類型。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-266">Cannot read the device type from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <span data-ttu-id="881db-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-268">無法從媒體讀取裝置名稱。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-268">Cannot read the device name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <span data-ttu-id="881db-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-270">無法讀取媒體的使用量。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-270">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <span data-ttu-id="881db-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-272">系統無法讀取媒體的最大電訊廠商連線速度。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-272">The system was unable to read the maximum carrier connection speed from the media .INI file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-273">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-273">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <span data-ttu-id="881db-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-275">無法讀取媒體的使用量。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="881db-275">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <span data-ttu-id="881db-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-277">線路忙碌中。</span><span class="sxs-lookup"><span data-stu-id="881db-277">The line is busy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <span data-ttu-id="881db-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-279">有人已回答而非數據機。</span><span class="sxs-lookup"><span data-stu-id="881db-279">A person answered instead of a modem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <span data-ttu-id="881db-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-281">沒有解答。</span><span class="sxs-lookup"><span data-stu-id="881db-281">There is no answer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <span data-ttu-id="881db-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-283">無法偵測到貨運公司信號。</span><span class="sxs-lookup"><span data-stu-id="881db-283">Cannot detect a carrier signal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <span data-ttu-id="881db-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-285">沒有撥號音。</span><span class="sxs-lookup"><span data-stu-id="881db-285">There is no dial tone.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <span data-ttu-id="881db-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-287">數據機 (或其他連接的裝置) 回報了一般錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-287">The modem (or other connecting device) reported a general error.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-288">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-288">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <span data-ttu-id="881db-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-290">寫入區段名稱時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-290">There was an error in writing the section name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <span data-ttu-id="881db-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-292">寫入裝置類型時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-292">There was an error in writing the device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <span data-ttu-id="881db-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-294">寫入裝置名稱時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-294">There was an error in writing the device name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <span data-ttu-id="881db-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-296">寫入連線速度上限時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-296">There was an error in writing the maximum connection speed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <span data-ttu-id="881db-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-298">寫入最大的電訊廠商速度時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-298">There was an error in writing the maximum carrier speed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <span data-ttu-id="881db-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-300">寫入使用方式時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-300">There was an error in writing the usage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <span data-ttu-id="881db-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-302">寫入預設值時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-302">There was an error in writing the default-off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <span data-ttu-id="881db-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span></span></dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <span data-ttu-id="881db-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-305">媒體。INI 檔案是空的。</span><span class="sxs-lookup"><span data-stu-id="881db-305">The media .INI file is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <span data-ttu-id="881db-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-307">拒絕存取，因為網域上的使用者名稱、密碼或兩者皆無效。</span><span class="sxs-lookup"><span data-stu-id="881db-307">Access denied because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <span data-ttu-id="881db-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-309">埠或連接的裝置發生硬體故障</span><span class="sxs-lookup"><span data-stu-id="881db-309">A hardware failure has occurred in the port or attached device</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <span data-ttu-id="881db-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-311">宏不是二進位宏。</span><span class="sxs-lookup"><span data-stu-id="881db-311">The macro is not a binary macro.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <span data-ttu-id="881db-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-313">找不到 DCB。</span><span class="sxs-lookup"><span data-stu-id="881db-313">DCB not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <span data-ttu-id="881db-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-315">狀態機器尚未啟動。</span><span class="sxs-lookup"><span data-stu-id="881db-315">State machines are not started.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <span data-ttu-id="881db-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-317">狀態機器已啟動。</span><span class="sxs-lookup"><span data-stu-id="881db-317">State machines are already started.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <span data-ttu-id="881db-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-319">部分回應迴圈。</span><span class="sxs-lookup"><span data-stu-id="881db-319">Partial response looping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <span data-ttu-id="881db-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-321">裝置中的回應金鑰名稱。INF 檔案的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="881db-321">A response key name in the device .INF file is not in the expected format.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <span data-ttu-id="881db-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-323">裝置回應造成緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="881db-323">The device response caused a buffer overflow.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <span data-ttu-id="881db-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-325">裝置中的展開命令。INF 檔案太長。</span><span class="sxs-lookup"><span data-stu-id="881db-325">The expanded command in the device .INF file is too long.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <span data-ttu-id="881db-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-327">裝置已移至 COM 驅動程式不支援的連線速度。</span><span class="sxs-lookup"><span data-stu-id="881db-327">The device moved to a connection speed that is not supported by the COM driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <span data-ttu-id="881db-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-329">未預期時收到的裝置回應。</span><span class="sxs-lookup"><span data-stu-id="881db-329">Device response received when none expected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <span data-ttu-id="881db-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-331">發生錯誤，因為互動模式已啟用。</span><span class="sxs-lookup"><span data-stu-id="881db-331">An error occurred because the interactive mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <span data-ttu-id="881db-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-333">指定了不正確的回呼號碼。</span><span class="sxs-lookup"><span data-stu-id="881db-333">A bad callback number was specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <span data-ttu-id="881db-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-335">指定的驗證狀態無效。</span><span class="sxs-lookup"><span data-stu-id="881db-335">The specified authentication state is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <span data-ttu-id="881db-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-337">寫入初始連線速度時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-337">An error occurred when writing the initial connection speed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-338">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-338">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <span data-ttu-id="881db-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-340">收到的是25個診斷指示。</span><span class="sxs-lookup"><span data-stu-id="881db-340">An X.25 diagnostic indication was received.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <span data-ttu-id="881db-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-342">指定的帳號已過期。</span><span class="sxs-lookup"><span data-stu-id="881db-342">The specified account has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <span data-ttu-id="881db-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-344">嘗試變更網域上的密碼時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-344">An error occurred while attempting to change the password on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <span data-ttu-id="881db-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-346">與您的數據機通訊時偵測到序列溢出錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-346">Serial overrun errors were detected while communicating with your modem.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <span data-ttu-id="881db-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-348">RasMan 初始化失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-348">RasMan initialization failure.</span></span> <span data-ttu-id="881db-349">檢查事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="881db-349">Check the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <span data-ttu-id="881db-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-351">雙向埠正在初始化。</span><span class="sxs-lookup"><span data-stu-id="881db-351">The two-way port is initializing.</span></span> <span data-ttu-id="881db-352">等候幾秒鐘後重撥。</span><span class="sxs-lookup"><span data-stu-id="881db-352">Wait a few seconds and redial.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-353">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-353">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <span data-ttu-id="881db-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-355">未提供任何可用的 ISDN 線路。</span><span class="sxs-lookup"><span data-stu-id="881db-355">No active ISDN lines are available.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <span data-ttu-id="881db-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-357">沒有任何 ISDN 通道可以進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="881db-357">No ISDN channels are available to make the call.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-358">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-358">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <span data-ttu-id="881db-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-360">因為電話線路品質不佳而發生太多錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-360">Too many errors occurred because of poor phone line quality.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-361">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-361">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <span data-ttu-id="881db-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-363">遠端存取 IP 設定無法使用。</span><span class="sxs-lookup"><span data-stu-id="881db-363">The remote access IP configuration is unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <span data-ttu-id="881db-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-365">遠端存取 IP 位址的靜態集區中沒有任何可用的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="881db-365">No IP addresses are available in the static pool of remote access IP addresses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <span data-ttu-id="881db-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-367">發生 PPP 超時。</span><span class="sxs-lookup"><span data-stu-id="881db-367">A PPP timeout occurred.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <span data-ttu-id="881db-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-369">遠端電腦已終止連接。</span><span class="sxs-lookup"><span data-stu-id="881db-369">The connection was terminated by the remote computer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-370">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-370">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <span data-ttu-id="881db-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-372">未設定任何 PPP 控制通訊協定。</span><span class="sxs-lookup"><span data-stu-id="881db-372">No PPP control protocols are configured.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <span data-ttu-id="881db-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-374">遠端 PPP 對等沒有回應。</span><span class="sxs-lookup"><span data-stu-id="881db-374">The remote PPP peer is not responding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <span data-ttu-id="881db-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-376">PPP 封包無效。</span><span class="sxs-lookup"><span data-stu-id="881db-376">The PPP packet is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <span data-ttu-id="881db-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-378">電話號碼（包括前置詞和尾碼）太長。</span><span class="sxs-lookup"><span data-stu-id="881db-378">The phone number, including the prefix and suffix, is too long.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <span data-ttu-id="881db-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-380">IPX 通訊協定無法在數據機 (或其他連線的裝置) 上撥出，因為這部電腦未設定為撥出 (它是 IPX 路由器) 。</span><span class="sxs-lookup"><span data-stu-id="881db-380">The IPX protocol cannot dial out on the modem (or other connecting device) because this computer is not configured for dialing out (it is an IPX router).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-381">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-381">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <span data-ttu-id="881db-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-383">IPX 通訊協定無法在數據機 (或其他連線的裝置) 上撥入，因為此電腦未設定為在 (未安裝 IPX 路由器) 中進行撥號。</span><span class="sxs-lookup"><span data-stu-id="881db-383">The IPX protocol cannot dial in on the modem (or other connecting device) because this computer is not configured for dialing in (the IPX router is not installed).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-384">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-384">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <span data-ttu-id="881db-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-386">IPX 通訊協定一次不能用於一個以上的埠上的撥號。</span><span class="sxs-lookup"><span data-stu-id="881db-386">The IPX protocol cannot be used for dial-out on more than one port at a time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <span data-ttu-id="881db-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-388">無法存取 TCPCFG.DLL。</span><span class="sxs-lookup"><span data-stu-id="881db-388">Cannot access TCPCFG.DLL.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-389">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-389">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <span data-ttu-id="881db-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-391">找不到系結至遠端存取的 IP 介面卡。</span><span class="sxs-lookup"><span data-stu-id="881db-391">Cannot find an IP adapter bound to remote access.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <span data-ttu-id="881db-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-393">除非已安裝 IP 通訊協定，否則無法使用 SLIP。</span><span class="sxs-lookup"><span data-stu-id="881db-393">SLIP cannot be used unless the IP protocol is installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <span data-ttu-id="881db-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-395">電腦註冊未完成。</span><span class="sxs-lookup"><span data-stu-id="881db-395">Computer registration is not complete.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-396">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-396">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <span data-ttu-id="881db-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-398">未設定指定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="881db-398">The specified protocol is not configured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <span data-ttu-id="881db-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-400">PPP 協商未聚合。</span><span class="sxs-lookup"><span data-stu-id="881db-400">The PPP negotiation is not converging.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <span data-ttu-id="881db-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-402">無法在伺服器上使用指定之網路通訊協定的 PPP 控制通訊協定。</span><span class="sxs-lookup"><span data-stu-id="881db-402">the PPP control protocol for the specified network protocol is not available on the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <span data-ttu-id="881db-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-404">PPP 連結控制通訊協定已終止。</span><span class="sxs-lookup"><span data-stu-id="881db-404">The PPP link control protocol was terminated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <span data-ttu-id="881db-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-406">伺服器拒絕了要求的位址。</span><span class="sxs-lookup"><span data-stu-id="881db-406">The requested address was rejected by the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <span data-ttu-id="881db-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-408">遠端電腦已終止控制通訊協定。</span><span class="sxs-lookup"><span data-stu-id="881db-408">The remote computer terminated the control protocol.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <span data-ttu-id="881db-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-410">偵測到回送。</span><span class="sxs-lookup"><span data-stu-id="881db-410">Loopback detected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <span data-ttu-id="881db-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-412">伺服器未指派位址。</span><span class="sxs-lookup"><span data-stu-id="881db-412">The server did not assign an address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <span data-ttu-id="881db-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-414">遠端伺服器無法使用 Windows NT 加密密碼。</span><span class="sxs-lookup"><span data-stu-id="881db-414">The remote server cannot use the Windows NT encrypted password.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <span data-ttu-id="881db-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-416">為遠端存取設定的 TAPI 裝置無法初始化或未正確安裝。</span><span class="sxs-lookup"><span data-stu-id="881db-416">The TAPI devices configured for remote access failed to initialize or were not installed correctly.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <span data-ttu-id="881db-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-418">本機電腦不支援加密。</span><span class="sxs-lookup"><span data-stu-id="881db-418">The local computer does not support encryption.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <span data-ttu-id="881db-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-420">遠端伺服器不支援加密。</span><span class="sxs-lookup"><span data-stu-id="881db-420">The remote server does not support encryption.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <span data-ttu-id="881db-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-422">遠端電腦需要資料加密。</span><span class="sxs-lookup"><span data-stu-id="881db-422">The remote computer requires data encryption.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-423">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-423">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <span data-ttu-id="881db-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-425">系統無法使用遠端電腦指派的 IPX 網路編號。</span><span class="sxs-lookup"><span data-stu-id="881db-425">The system cannot use the IPX network number assigned by the remote computer.</span></span> <span data-ttu-id="881db-426">事件記錄檔中會提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="881db-426">Additional information is provided in the event log.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-427">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-427">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <span data-ttu-id="881db-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-429">會話管理模組 (SMM) 無效。</span><span class="sxs-lookup"><span data-stu-id="881db-429">The Session Management Module (SMM) is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-430">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-430">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <span data-ttu-id="881db-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-432">SMM 未初始化。</span><span class="sxs-lookup"><span data-stu-id="881db-432">The SMM is uninitialized.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-433">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-433">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <span data-ttu-id="881db-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-435">沒有適用于埠的 MAC。</span><span class="sxs-lookup"><span data-stu-id="881db-435">No MAC for port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-436">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-436">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <span data-ttu-id="881db-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-438">SMM 超時。</span><span class="sxs-lookup"><span data-stu-id="881db-438">The SMM timed out.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-439">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-439">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <span data-ttu-id="881db-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-441">指定的電話號碼不正確。</span><span class="sxs-lookup"><span data-stu-id="881db-441">A bad phone number was specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <span data-ttu-id="881db-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-443">指定了錯誤的 SMM。</span><span class="sxs-lookup"><span data-stu-id="881db-443">The wrong SMM was specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-444">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-444">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <span data-ttu-id="881db-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-446">回呼號碼包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="881db-446">The callback number contains a character that is not valid.</span></span> <span data-ttu-id="881db-447">只允許下列18個字元：0到9、T、P、W、 (、) 、-、@ 和 space。</span><span class="sxs-lookup"><span data-stu-id="881db-447">Only the following 18 characters are allowed: 0 to 9, T, P, W, (, ), -, @, and space.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-448">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-448">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <span data-ttu-id="881db-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-450">處理腳本時遇到語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-450">A syntax error was encountered while processing a script.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <span data-ttu-id="881db-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-452">連接無法中斷連線，因為它是由多通訊協定路由器所建立。</span><span class="sxs-lookup"><span data-stu-id="881db-452">The connection could not be disconnected because it was created by the multi-protocol router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <span data-ttu-id="881db-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-454">系統找不到多重連結套件組合。</span><span class="sxs-lookup"><span data-stu-id="881db-454">The system could not find the multi-link bundle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <span data-ttu-id="881db-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-456">系統無法執行自動撥號，因為此連接已指定自訂撥號程式。</span><span class="sxs-lookup"><span data-stu-id="881db-456">The system cannot perform automated dial because this connection has a custom dialer specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <span data-ttu-id="881db-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-458">此連接已被撥號。</span><span class="sxs-lookup"><span data-stu-id="881db-458">This connection is already being dialed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <span data-ttu-id="881db-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-460">RAS 無法自動啟動。</span><span class="sxs-lookup"><span data-stu-id="881db-460">RAS could not be started automatically.</span></span> <span data-ttu-id="881db-461">事件記錄檔中會提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="881db-461">Additional information is provided in the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <span data-ttu-id="881db-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-463">連接上已啟用 (ICS) 的網際網路連線共用。</span><span class="sxs-lookup"><span data-stu-id="881db-463">Internet Connection Sharing (ICS) is already enabled on the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-464">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-464">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <span data-ttu-id="881db-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-466">變更現有的網際網路連線共用設定時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-466">An error occurred while the existing Internet Connection Sharing settings were being changed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-467">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-467">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <span data-ttu-id="881db-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-469">啟用路由功能時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-469">An error occurred while routing capabilities were being enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-470">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-470">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <span data-ttu-id="881db-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-472">啟用連接的網際網路連線共用時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-472">An error occurred while Internet Connection Sharing was being enabled for the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-473">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-473">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <span data-ttu-id="881db-474"><dt><strong>7ERROR_SHARING_PRI加值稅E_INSTALL64</strong></dt> <dt>762</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-475">設定局域網路進行共用時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-475">An error occurred while the local network was being configured for sharing.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-476">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-476">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <span data-ttu-id="881db-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-478">無法啟用網際網路連線共用。</span><span class="sxs-lookup"><span data-stu-id="881db-478">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="881db-479">除了要共用的連線之外，還有一個以上的 LAN 連接。</span><span class="sxs-lookup"><span data-stu-id="881db-479">There is more than one LAN connection other than the connection to be shared.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-480">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-480">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <span data-ttu-id="881db-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-482">沒有安裝智慧卡讀取裝置。</span><span class="sxs-lookup"><span data-stu-id="881db-482">No smart card reader is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <span data-ttu-id="881db-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-484">無法啟用網際網路連線共用。</span><span class="sxs-lookup"><span data-stu-id="881db-484">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="881db-485">已使用自動 IP 位址所需的 IP 位址設定局域網路連線。</span><span class="sxs-lookup"><span data-stu-id="881db-485">A LAN connection is already configured with the IP address that is required for automatic IP addressing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <span data-ttu-id="881db-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-487">找不到憑證。</span><span class="sxs-lookup"><span data-stu-id="881db-487">A certificate could not be found.</span></span> <span data-ttu-id="881db-488">透過 IPSec 使用 L2TP 通訊協定的連線需要安裝電腦憑證（也稱為電腦憑證）。</span><span class="sxs-lookup"><span data-stu-id="881db-488">Connections that use the L2TP protocol over IPSec require the installation of a machine certificate, also known as a computer certificate.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <span data-ttu-id="881db-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-490">無法啟用網際網路連線共用。</span><span class="sxs-lookup"><span data-stu-id="881db-490">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="881db-491">選取作為私人網路的 LAN 連線已設定一個以上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="881db-491">The LAN connection selected as the private network has more than one IP address configured.</span></span> <span data-ttu-id="881db-492">請在啟用網際網路連線共用之前，以單一 IP 位址重新設定 LAN 連線。</span><span class="sxs-lookup"><span data-stu-id="881db-492">Please reconfigure the LAN connection with a single IP address before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <span data-ttu-id="881db-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-494">連接嘗試失敗，因為加密資料失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-494">The connection attempt failed because of failure to encrypt data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <span data-ttu-id="881db-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-496">無法連線到指定的目的地。</span><span class="sxs-lookup"><span data-stu-id="881db-496">The specified destination is not reachable.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <span data-ttu-id="881db-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-498">遠端電腦拒絕連接嘗試。</span><span class="sxs-lookup"><span data-stu-id="881db-498">The remote computer rejected the connection attempt.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <span data-ttu-id="881db-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-500">連接嘗試失敗，因為網路忙碌中。</span><span class="sxs-lookup"><span data-stu-id="881db-500">The connection attempt failed because the network is busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <span data-ttu-id="881db-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-502">遠端電腦的網路硬體與要求的呼叫類型不相容。</span><span class="sxs-lookup"><span data-stu-id="881db-502">The remote computer's network hardware is incompatible with the type of call requested.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <span data-ttu-id="881db-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-504">連接嘗試失敗，因為目的地號碼已變更。</span><span class="sxs-lookup"><span data-stu-id="881db-504">The connection attempt failed because the destination number has changed.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <span data-ttu-id="881db-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-506">連接嘗試失敗，因為暫時性失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-506">The connection attempt failed because of a temporary failure.</span></span> <span data-ttu-id="881db-507">請嘗試重新連線。</span><span class="sxs-lookup"><span data-stu-id="881db-507">Try connecting again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <span data-ttu-id="881db-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-509">遠端電腦封鎖了呼叫。</span><span class="sxs-lookup"><span data-stu-id="881db-509">The call was blocked by the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <span data-ttu-id="881db-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-511">因為遠端電腦已叫用「請勿打擾」功能，所以無法連接此呼叫。</span><span class="sxs-lookup"><span data-stu-id="881db-511">The call could not be connected because the remote computer has invoked the Do Not Disturb feature.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <span data-ttu-id="881db-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-513">連接嘗試失敗，因為遠端電腦上的數據機或其他連線裝置順序不相同。</span><span class="sxs-lookup"><span data-stu-id="881db-513">The connection attempt failed because the modem or other connection device on the remote computer is out of order.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <span data-ttu-id="881db-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-515">無法驗證服務器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="881db-515">It was not possible to verify the identity of the server.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <span data-ttu-id="881db-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-517">若要使用此連接撥出，您必須使用智慧卡。</span><span class="sxs-lookup"><span data-stu-id="881db-517">To dial out using this connection you must use a smart card.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-518">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-518">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <span data-ttu-id="881db-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-520">嘗試的函式對此連接無效。</span><span class="sxs-lookup"><span data-stu-id="881db-520">An attempted function is not valid for this connection.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <span data-ttu-id="881db-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-522">因為找不到有效的憑證，所以加密嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-522">The encryption attempt failed because no valid certificate was found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-523">在 Windows Vista 和更新版本的 Windows 中已淘汰。</span><span class="sxs-lookup"><span data-stu-id="881db-523">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <span data-ttu-id="881db-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-525">目前已將 (NAT) 的連線共用安裝為路由通訊協定，必須先將其移除，才能啟用網際網路連線共用。</span><span class="sxs-lookup"><span data-stu-id="881db-525">Connection Sharing (NAT) is currently installed as a routing protocol, and must be removed before enabling Internet Connection Sharing.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <span data-ttu-id="881db-526"><dt><strong>ERROR_SHARING_NO_PRI加值稅E_LAN</strong></dt> <dt>783</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-527">無法啟用網際網路連線共用。</span><span class="sxs-lookup"><span data-stu-id="881db-527">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="881db-528">選取為私人網路的 LAN 連線可能不存在，或已從網路中斷連線。</span><span class="sxs-lookup"><span data-stu-id="881db-528">The LAN connection selected as the private network is either not present, or is disconnected from the network.</span></span> <span data-ttu-id="881db-529">請先確認局域網路介面卡已連線，然後再啟用網際網路連線共用。</span><span class="sxs-lookup"><span data-stu-id="881db-529">Please ensure that the LAN adapter is connected before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <span data-ttu-id="881db-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-531">您無法在登入時使用此連接撥號，因為它設定為使用與智慧卡上不同的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="881db-531">You cannot dial using this connection at login time because it is configured to use a user name different than the one on the smart card.</span></span> <span data-ttu-id="881db-532">如果您想要在登入時使用此連接，您必須將它設定為使用智慧卡上的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="881db-532">If you want to use this connection at login time, you must configure it to use the user name on the smart card.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <span data-ttu-id="881db-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-534">您無法在登入時使用此連線撥號，因為它未設定為使用智慧卡。</span><span class="sxs-lookup"><span data-stu-id="881db-534">You cannot dial using this connection at login time because it is not configured to use a smart card.</span></span> <span data-ttu-id="881db-535">如果您想要在登入時使用它，您必須編輯此連接的內容，讓它使用智慧卡。</span><span class="sxs-lookup"><span data-stu-id="881db-535">If you want to use it at login time, you must edit the properties of this connection so that it uses a smart card.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <span data-ttu-id="881db-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-537">L2TP 連線嘗試失敗，因為您的電腦上沒有有效的電腦憑證可進行安全性驗證。</span><span class="sxs-lookup"><span data-stu-id="881db-537">The L2TP connection attempt failed because there is no valid machine certificate on your computer for security authentication.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <span data-ttu-id="881db-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-539">L2TP 連接嘗試失敗，因為安全性層無法驗證遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="881db-539">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <span data-ttu-id="881db-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-541">L2TP 連接嘗試失敗，因為安全性層無法與遠端電腦協調相容的參數。</span><span class="sxs-lookup"><span data-stu-id="881db-541">The L2TP connection attempt failed because the security layer could not negotiate compatible parameters with the remote computer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <span data-ttu-id="881db-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-543">L2TP 連線嘗試失敗，因為安全性層在與遠端電腦的初始協商期間發生處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-543">The L2TP connection attempt failed because the security layer encountered a processing error during initial negotiations with the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <span data-ttu-id="881db-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-545">L2TP 連接嘗試失敗，因為遠端電腦上的憑證驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-545">The L2TP connection attempt failed because certificate validation on the remote computer failed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <span data-ttu-id="881db-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-547">L2TP 連接嘗試失敗，因為找不到連接的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="881db-547">The L2TP connection attempt failed because security policy for the connection was not found.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <span data-ttu-id="881db-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-549">L2TP 連線嘗試失敗，因為安全性協商已超時。</span><span class="sxs-lookup"><span data-stu-id="881db-549">The L2TP connection attempt failed because security negotiation timed out.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <span data-ttu-id="881db-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-551">L2TP 連線嘗試失敗，因為協調安全性時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-551">The L2TP connection attempt failed because an error occurred while negotiating security.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <span data-ttu-id="881db-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-553">此使用者的框架通訊協定 RADIUS 屬性不是 PPP。</span><span class="sxs-lookup"><span data-stu-id="881db-553">The Framed Protocol RADIUS attribute for this user is not PPP.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <span data-ttu-id="881db-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-555">此使用者的通道類型 RADIUS 屬性不正確。</span><span class="sxs-lookup"><span data-stu-id="881db-555">The Tunnel Type RADIUS attribute for this user is not correct.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <span data-ttu-id="881db-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-557">此使用者的服務類型 RADIUS 屬性不是框架，也不是回呼的框架。</span><span class="sxs-lookup"><span data-stu-id="881db-557">The Service Type RADIUS attribute for this user is neither Framed nor Callback Framed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <span data-ttu-id="881db-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-559">無法建立與遠端電腦的連線，因為找不到數據機或其忙碌中。</span><span class="sxs-lookup"><span data-stu-id="881db-559">A connection to the remote computer could not be established because the modem was not found or was busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <span data-ttu-id="881db-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-561">找不到可搭配可延伸驗證通訊協定 (EAP) 使用的憑證。</span><span class="sxs-lookup"><span data-stu-id="881db-561">A certificate could not be found that can be used with the Extensible Authentication Protocol (EAP).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <span data-ttu-id="881db-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-563">因為網路上的 IP 位址衝突，所以無法啟用 (ICS) 的網際網路連線共用。</span><span class="sxs-lookup"><span data-stu-id="881db-563">Internet Connection Sharing (ICS) cannot be enabled due to an IP address conflict on the network.</span></span> <span data-ttu-id="881db-564">ICS 要求主機必須設定為使用 <strong>192.168.0.1</strong>。</span><span class="sxs-lookup"><span data-stu-id="881db-564">ICS requires the host be configured to use <strong>192.168.0.1</strong>.</span></span> <span data-ttu-id="881db-565">確定網路上沒有其他用戶端設定為使用 <strong>192.168.0.1</strong>。</span><span class="sxs-lookup"><span data-stu-id="881db-565">Ensure that no other client on the network is configured to use <strong>192.168.0.1</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-566">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-566">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-567">Windows 7 和更新版本：主機必須設定為使用 <strong>192.168.137.1</strong>
</span><span class="sxs-lookup"><span data-stu-id="881db-567">Windows 7 and later: The host must be configured to use <strong>192.168.137.1</strong>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <span data-ttu-id="881db-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-569">無法建立 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="881db-569">Unable to establish the VPN connection.</span></span> <span data-ttu-id="881db-570">可能無法連線到 VPN 伺服器，或可能未正確設定此連線的安全性參數。</span><span class="sxs-lookup"><span data-stu-id="881db-570">The VPN server may be unreachable, or security parameters may not be configured properly for this connection.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-571">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-571">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <span data-ttu-id="881db-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-573">此連接設定為驗證存取伺服器的身分識別，但 Windows 無法驗證服務器所傳送的數位憑證。</span><span class="sxs-lookup"><span data-stu-id="881db-573">This connection is configured to validate the identity of the access server, but Windows cannot verify the digital certificate sent by the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-574">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-574">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <span data-ttu-id="881db-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-576">提供的卡片無法辨識。</span><span class="sxs-lookup"><span data-stu-id="881db-576">The card supplied was not recognized.</span></span> <span data-ttu-id="881db-577">請檢查卡片是否已正確插入，並且安全地納入。</span><span class="sxs-lookup"><span data-stu-id="881db-577">Please check that the card is inserted correctly, and fits securely.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-578">在 Windows XP SP1 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-578">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <span data-ttu-id="881db-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-580">儲存在會話 cookie 中的 PEAP 設定不符合目前的會話設定。</span><span class="sxs-lookup"><span data-stu-id="881db-580">The PEAP configuration stored in the session cookie does not match the current session configuration.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-581">在 Windows XP SP1 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-581">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <span data-ttu-id="881db-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-583">儲存在會話 cookie 中的 PEAP 身分識別不符合目前的身分識別。</span><span class="sxs-lookup"><span data-stu-id="881db-583">The PEAP identity stored in the session cookie does not match the current identity.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-584">在 Windows XP SP1 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-584">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <span data-ttu-id="881db-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-586">您無法在登入時使用此連接撥號，因為它已設定為使用目前登入的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="881db-586">You cannot dial using this connection at login time because it is configured to use the currently-logged-in user's credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-587">在 Windows XP SP1 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-587">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <span data-ttu-id="881db-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-589">您的電腦與 VPN 伺服器之間的連接已啟動，但無法完成 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="881db-589">A connection between your computer and the VPN server has been started, but the VPN connection cannot be completed.</span></span> <span data-ttu-id="881db-590">最常見的原因是至少有一個網際網路裝置 (例如，您的電腦與 VPN 伺服器之間的防火牆或路由器) 未設定成允許 (GRE) 通訊協定封包的一般路由封裝。</span><span class="sxs-lookup"><span data-stu-id="881db-590">The most common cause for this is that at least one Internet device (for example, a firewall or a router) between your computer and the VPN server is not configured to allow Generic Routing Encapsulation (GRE) protocol packets.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-591">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-591">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <span data-ttu-id="881db-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-593">電腦與 VPN 伺服器之間的網路連線已中斷。</span><span class="sxs-lookup"><span data-stu-id="881db-593">The network connection between your computer and the VPN server was interrupted.</span></span> <span data-ttu-id="881db-594">這可能是因為 VPN 傳輸中的問題所造成，而且通常是因為網際網路等待時間，或是您的 VPN 伺服器已達到容量。</span><span class="sxs-lookup"><span data-stu-id="881db-594">This can be caused by a problem in the VPN transmission and is commonly the result of internet latency or simply that your VPN server has reached capacity.</span></span> <span data-ttu-id="881db-595">嘗試重新連線至 VPN 伺服器。</span><span class="sxs-lookup"><span data-stu-id="881db-595">Try to reconnect to the VPN server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-596">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-596">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <span data-ttu-id="881db-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-598">無法建立您的電腦與 VPN 伺服器之間的網路連線，因為遠端伺服器拒絕了連接。</span><span class="sxs-lookup"><span data-stu-id="881db-598">The network connection between your computer and the VPN server could not be established because the remote server refused the connection.</span></span> <span data-ttu-id="881db-599">這通常是因為伺服器的設定與連線設定不相符所造成。</span><span class="sxs-lookup"><span data-stu-id="881db-599">This is typically caused by a mismatch between the server's configuration and your connection settings.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-600">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-600">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <span data-ttu-id="881db-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-602">因為遠端伺服器沒有回應，所以無法建立您的電腦與 VPN 伺服器之間的網路連線。</span><span class="sxs-lookup"><span data-stu-id="881db-602">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="881db-603">這可能是因為其中一個網路裝置 (例如，您的電腦與遠端伺服器之間的防火牆、NAT、路由器) 未設定成允許 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="881db-603">This could be because one of the network devices (for example, firewalls, NAT, routers) between your computer and the remote server is not configured to allow VPN connections.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-604">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-604">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <span data-ttu-id="881db-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-606">您的電腦與 VPN 伺服器之間的網路連線已啟動，但未完成 VPN 連接。</span><span class="sxs-lookup"><span data-stu-id="881db-606">A network connection between your computer and the VPN server was started, but the VPN connection was not completed.</span></span> <span data-ttu-id="881db-607">這通常是因為在用戶端與伺服器之間使用不正確或已過期的憑證來進行驗證所致。</span><span class="sxs-lookup"><span data-stu-id="881db-607">This is typically caused by the use of an incorrect or expired certificate for authentication between the client and the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-608">Windows Vista 和更新版本的 Windows 支援</span><span class="sxs-lookup"><span data-stu-id="881db-608">Supported in Windows Vista and later versions of Windows</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <span data-ttu-id="881db-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-610">因為遠端伺服器沒有回應，所以無法建立您的電腦與 VPN 伺服器之間的網路連線。</span><span class="sxs-lookup"><span data-stu-id="881db-610">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="881db-611">這通常是因為用戶端與伺服器之間的預先共用金鑰問題所造成。</span><span class="sxs-lookup"><span data-stu-id="881db-611">This is typically caused by a pre-shared key problem between the client and server.</span></span> <span data-ttu-id="881db-612">預先共用金鑰是用來確保您是在 IP 安全性 (IPSec) 通訊週期的身分。</span><span class="sxs-lookup"><span data-stu-id="881db-612">A pre-shared key is used to guarantee you are who you say you are in an IP Security (IPSec) communication cycle.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-613">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-613">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <span data-ttu-id="881db-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-615">因為您 RAS/VPN 伺服器設定的原則，連線被禁止。</span><span class="sxs-lookup"><span data-stu-id="881db-615">The connection was prevented because of a policy configured on your RAS/VPN server.</span></span> <span data-ttu-id="881db-616">具體而言，伺服器用來驗證您的使用者名稱和密碼的驗證方法，可能不符合連線設定檔中設定的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="881db-616">Specifically, the authentication method used by the server to verify your username and password may not match the authentication method configured in your connection profile.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-617">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-617">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <span data-ttu-id="881db-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-619">當先前的寬頻連線已使用相同的裝置或埠建立時，您已嘗試建立第二個寬頻連線。</span><span class="sxs-lookup"><span data-stu-id="881db-619">You have attempted to establish a second broadband connection while a previous broadband connection is already established using the same device or port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-620">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-620">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <span data-ttu-id="881db-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-622">找不到寬頻連線所需的基礎乙太網路連接。</span><span class="sxs-lookup"><span data-stu-id="881db-622">The underlying Ethernet connectivity required for the broadband connection was not found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-623">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-623">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <span data-ttu-id="881db-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-625">因為遠端伺服器沒有回應，所以無法在您的電腦上建立寬頻網路連接。</span><span class="sxs-lookup"><span data-stu-id="881db-625">The broadband network connection could not be established on your computer because the remote server is not responding.</span></span> <span data-ttu-id="881db-626">這可能是因為值對此連接的 [服務名稱] 欄位無效。</span><span class="sxs-lookup"><span data-stu-id="881db-626">This could be caused by a value that is not valid for the 'Service Name' field for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-627">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-627">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <span data-ttu-id="881db-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-629">遠端存取服務已不再支援您嘗試啟用的功能或設定。</span><span class="sxs-lookup"><span data-stu-id="881db-629">A feature or setting you have tried to enable is no longer supported by the remote access service.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-630">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-630">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <span data-ttu-id="881db-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-632">連接時無法刪除連接。</span><span class="sxs-lookup"><span data-stu-id="881db-632">Cannot delete a connection while it is connected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-633">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-633">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <span data-ttu-id="881db-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-635">網路存取保護 (NAP) 強制用戶端無法建立遠端存取連線的系統資源。</span><span class="sxs-lookup"><span data-stu-id="881db-635">The Network Access Protection (NAP) enforcement client could not create system resources for remote access connections.</span></span> <span data-ttu-id="881db-636">某些網路服務或資源可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="881db-636">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-637">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-637">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <span data-ttu-id="881db-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-639">網路存取保護代理程式 (NAP 代理程式) 服務已停用或未安裝在這部電腦上。</span><span class="sxs-lookup"><span data-stu-id="881db-639">The Network Access Protection Agent (NAP Agent) service has been disabled or is not installed on this computer.</span></span> <span data-ttu-id="881db-640">某些網路服務或資源可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="881db-640">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-641">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-641">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <span data-ttu-id="881db-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-643">網路存取保護 (NAP) 強制用戶端無法向網路存取保護代理程式註冊 (NAP 代理程式) 服務。</span><span class="sxs-lookup"><span data-stu-id="881db-643">The Network Access Protection (NAP) enforcement client failed to register with the Network Access Protection Agent (NAP Agent) service.</span></span> <span data-ttu-id="881db-644">某些網路服務或資源可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="881db-644">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-645">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-645">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <span data-ttu-id="881db-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-647">網路存取保護 (NAP) 強制用戶端無法處理要求，因為遠端存取連接不存在。</span><span class="sxs-lookup"><span data-stu-id="881db-647">The Network Access Protection (NAP) enforcement client was unable to process the request because the remote access connection does not exist.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-648">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-648">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <span data-ttu-id="881db-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-650">網路存取保護 (NAP) 強制用戶端沒有回應。</span><span class="sxs-lookup"><span data-stu-id="881db-650">The Network Access Protection (NAP) enforcement client did not respond.</span></span> <span data-ttu-id="881db-651">某些網路服務或資源可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="881db-651">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-652">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-652">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <span data-ttu-id="881db-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-654">收到的 Crypto-Binding 類型長度-值 (的 TLV) 無效。</span><span class="sxs-lookup"><span data-stu-id="881db-654">The Crypto-Binding type-length-value (TLV) received is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-655">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-655">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <span data-ttu-id="881db-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-657">未收到 Crypto-Binding 的 TLV。</span><span class="sxs-lookup"><span data-stu-id="881db-657">Crypto-Binding TLV was not received.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-658">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-658">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <span data-ttu-id="881db-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-660">點對點通道通訊協定 (PPTP) 與 IPv6 不相容。</span><span class="sxs-lookup"><span data-stu-id="881db-660">Point-to-Point Tunneling Protocol (PPTP) is incompatible with IPv6.</span></span> <span data-ttu-id="881db-661">將虛擬私人網路的類型變更為 (L2TP) 的第二層通道通訊協定。</span><span class="sxs-lookup"><span data-stu-id="881db-661">Change the type of virtual private network to Layer Two Tunneling Protocol (L2TP).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-662">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-662">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <span data-ttu-id="881db-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-664">EAPTLS 快取認證的驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-664">EAPTLS validation of the cached credentials failed.</span></span> <span data-ttu-id="881db-665">捨棄快取的認證。</span><span class="sxs-lookup"><span data-stu-id="881db-665">Discard cached credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-666">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-666">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <span data-ttu-id="881db-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-668">無法完成 L2TP/IPsec 連線，因為 IKE 和 AuthIP IPSec 金鑰模組服務及/或基礎篩選引擎服務未執行。</span><span class="sxs-lookup"><span data-stu-id="881db-668">The L2TP/IPsec connection cannot be completed because the IKE and AuthIP IPSec Keying Modules service and/or the Base Filtering Engine service is not running.</span></span> <span data-ttu-id="881db-669">必須要有這些服務，才能建立 L2TP/IPSec 連線。</span><span class="sxs-lookup"><span data-stu-id="881db-669">These services are required to establish an L2TP/IPSec connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-670">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-670">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <span data-ttu-id="881db-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-672">因為閒置超時，所以已終止連接。</span><span class="sxs-lookup"><span data-stu-id="881db-672">The connection was terminated because of idle timeout.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-673">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-673">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <span data-ttu-id="881db-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-675">數據機 (或其他連接的裝置) 因連結失敗而中斷連線。</span><span class="sxs-lookup"><span data-stu-id="881db-675">The modem (or other connecting device) was disconnected due to link failure.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-676">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-676">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <span data-ttu-id="881db-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-678">因為使用者已登出，所以已終止連接。</span><span class="sxs-lookup"><span data-stu-id="881db-678">The connection was terminated because user logged off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-679">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-679">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <span data-ttu-id="881db-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-681">因為發生使用者切換，所以已終止連接。</span><span class="sxs-lookup"><span data-stu-id="881db-681">The connection was terminated because user switch happened.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-682">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-682">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <span data-ttu-id="881db-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-684">連接因休眠而終止。</span><span class="sxs-lookup"><span data-stu-id="881db-684">The connection was terminated because of hibernation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-685">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-685">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <span data-ttu-id="881db-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-687">因為系統已暫止，所以已終止連接。</span><span class="sxs-lookup"><span data-stu-id="881db-687">The connection was terminated because the system got suspended.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-688">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-688">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <span data-ttu-id="881db-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-690">連接已終止，因為遠端存取連線管理員已停止。</span><span class="sxs-lookup"><span data-stu-id="881db-690">The connection was terminated because Remote Access Connection manager stopped.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-691">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-691">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <span data-ttu-id="881db-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-693">L2TP 連接嘗試失敗，因為安全性層無法驗證遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="881db-693">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <span data-ttu-id="881db-694">這可能是因為遠端伺服器所提供之憑證的一或多個欄位無法驗證為屬於目標目的地。</span><span class="sxs-lookup"><span data-stu-id="881db-694">This could be because one or more fields of the certificate presented by the remote server could not be validated as belonging to the target destination.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-695">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-695">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <span data-ttu-id="881db-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-697">電腦不支援 NAP。</span><span class="sxs-lookup"><span data-stu-id="881db-697">The machine is not NAP capable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-698">在 Windows Vista 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-698">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <span data-ttu-id="881db-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-700">不正確通道識別碼。</span><span class="sxs-lookup"><span data-stu-id="881db-700">Invalid Tunnel ID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-701">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-701">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <span data-ttu-id="881db-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-703">另一個更新連接要求正在進行中。</span><span class="sxs-lookup"><span data-stu-id="881db-703">Another update connection request is in progress.</span></span> <span data-ttu-id="881db-704">RAS 一次只允許一個更新連接要求。</span><span class="sxs-lookup"><span data-stu-id="881db-704">RAS allows only one update connection request at a time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-705">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-705">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <span data-ttu-id="881db-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-707">使用設定的通訊協定進行協商是停用的。</span><span class="sxs-lookup"><span data-stu-id="881db-707">Negotiating using configured protocol is disable.</span></span> <span data-ttu-id="881db-708">編輯連線屬性，並選取不同的通訊協定進行協商，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="881db-708">Edit connection properties and select different protocol for negotiation and try again.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-709">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-709">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <span data-ttu-id="881db-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-711">內部位址協商失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-711">Internal address negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-712">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-712">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <span data-ttu-id="881db-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-714">用戶端必須要求內部 IPv4 或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="881db-714">Client has to request an Internal IPv4 or IPv6 address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-715">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-715">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <span data-ttu-id="881db-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-717">流量選取器協商失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-717">Traffic Selectors negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-718">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-718">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <span data-ttu-id="881db-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-720">此連接已停用行動性。</span><span class="sxs-lookup"><span data-stu-id="881db-720">Mobility is disabled for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-721">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-721">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <span data-ttu-id="881db-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-723">因為隔離狀態變更，所以 VPN 連線仍在連線或重新驗證。</span><span class="sxs-lookup"><span data-stu-id="881db-723">The VPN Connection is still connecting or re-authenticating because of Quarantine state change.</span></span> <span data-ttu-id="881db-724">只有當連接狀態為 [已連線] 時，才會起始行動更新。</span><span class="sxs-lookup"><span data-stu-id="881db-724">Initiate mobile update only when connection state is 'Connected'.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-725">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-725">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <span data-ttu-id="881db-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-727">伺服器拒絕用戶端驗證，因為 TLV 的非預期的 TLV 或值不符。</span><span class="sxs-lookup"><span data-stu-id="881db-727">Server rejected client authentication, due to unexpected TLV or value mismatch for a TLV.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-728">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-728">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <span data-ttu-id="881db-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-730">使用者未選取任何 VPN 目的地喜好設定，或它不再有效。</span><span class="sxs-lookup"><span data-stu-id="881db-730">Either VPN destination preference is not selected by the user or it is no longer valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-731">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-731">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <span data-ttu-id="881db-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-733">快取的智慧卡認證無效。</span><span class="sxs-lookup"><span data-stu-id="881db-733">Cached smart card credential is invalid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-734">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-734">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <span data-ttu-id="881db-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-736">因為將 cookie 新增至安全通訊端通道通訊協定 (SSTP) 時發生內部錯誤，所以 VPN 連線嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="881db-736">VPN connection attempt failed due to internal error occurred while adding cookies to the Secure Socket Tunneling Protocol (SSTP).</span></span> <span data-ttu-id="881db-737">如需詳細資訊，請參閱系統事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="881db-737">Please see the System Event Log for the detailed information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <span data-ttu-id="881db-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-739">) 儲存在 cookie 中的 PEAP 內部方法屬性 (s 為/無效。</span><span class="sxs-lookup"><span data-stu-id="881db-739">The PEAP inner method attribute(s) stored in the cookie is/are invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <span data-ttu-id="881db-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-741">電腦上未安裝驗證遠端存取連線所需的可延伸驗證通訊協定類型。</span><span class="sxs-lookup"><span data-stu-id="881db-741">The Extensible Authentication Protocol type required for authentication of the remote access connection is not installed on your computer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <span data-ttu-id="881db-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-743">遠端存取連線上設定的可延伸驗證通訊協定類型不支援單一登入。</span><span class="sxs-lookup"><span data-stu-id="881db-743">The Extensible Authentication Protocol type configured on the remote access connection does not support single sign-on.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <span data-ttu-id="881db-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-745">遠端存取連線上設定的可延伸驗證通訊協定類型不支援要求的操作。</span><span class="sxs-lookup"><span data-stu-id="881db-745">The Extensible Authentication Protocol type configured on the remote access connection does not support the requested operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <span data-ttu-id="881db-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-747">遠端存取連線已完成，但驗證失敗，因為向伺服器驗證用戶端的憑證無效。</span><span class="sxs-lookup"><span data-stu-id="881db-747">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is not valid.</span></span> <span data-ttu-id="881db-748">確定用於驗證的憑證有效。</span><span class="sxs-lookup"><span data-stu-id="881db-748">Ensure that the certificate used for authentication is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <span data-ttu-id="881db-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-750">遠端存取連線已完成，但驗證失敗，因為向伺服器驗證用戶端的憑證已過期。</span><span class="sxs-lookup"><span data-stu-id="881db-750">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is expired.</span></span> <span data-ttu-id="881db-751">更新憑證。</span><span class="sxs-lookup"><span data-stu-id="881db-751">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <span data-ttu-id="881db-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-753">遠端存取連線已完成，但驗證失敗，因為對伺服器驗證用戶端的憑證已撤銷。</span><span class="sxs-lookup"><span data-stu-id="881db-753">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is revoked.</span></span> <span data-ttu-id="881db-754">使用尚未撤銷的憑證。</span><span class="sxs-lookup"><span data-stu-id="881db-754">Use a certificate that has not been revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <span data-ttu-id="881db-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-756">遠端存取連線已完成，但驗證失敗，因為憑證中的錯誤會向伺服器驗證用戶端。</span><span class="sxs-lookup"><span data-stu-id="881db-756">The remote access connection completed, but authentication failed because of an error in the certificate that authenticates the client to the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <span data-ttu-id="881db-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-758">遠端存取連線已完成，但驗證失敗，因為用戶端用來驗證服務器的憑證無效。</span><span class="sxs-lookup"><span data-stu-id="881db-758">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <span data-ttu-id="881db-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-760">遠端存取連線已完成，但驗證失敗，因為用戶端用來驗證服務器的憑證已過期。</span><span class="sxs-lookup"><span data-stu-id="881db-760">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <span data-ttu-id="881db-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-762">遠端存取連線已完成，但驗證失敗，因為用戶端用來驗證服務器的憑證已撤銷。</span><span class="sxs-lookup"><span data-stu-id="881db-762">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <span data-ttu-id="881db-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-764">遠端存取連線已完成，但驗證失敗，因為用戶端用來驗證服務器的憑證發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="881db-764">The remote access connection completed, but authentication failed because of an error in the certificate that the client uses to authenticate the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <span data-ttu-id="881db-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-766">遠端存取連線已完成，但驗證失敗，因為在 [信任的根憑證授權單位] 憑證存放區中找不到驗證使用者憑證的受信任根憑證。</span><span class="sxs-lookup"><span data-stu-id="881db-766">The remote access connection completed, but authentication failed because a trusted root certificate that validates the user certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <span data-ttu-id="881db-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-768">遠端存取連線已完成，但驗證失敗，因為用來驗證使用者憑證的受信任根憑證無效。</span><span class="sxs-lookup"><span data-stu-id="881db-768">The remote access connection completed, but authentication failed because the trusted root certificate that is used to validate the user certificate is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <span data-ttu-id="881db-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-770">遠端存取連線已完成，但驗證失敗，因為驗證使用者憑證的「信任的根憑證授權單位」憑證存放區中的憑證已過期。</span><span class="sxs-lookup"><span data-stu-id="881db-770">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that authenticates the user certificate is expired.</span></span> <span data-ttu-id="881db-771">更新憑證。</span><span class="sxs-lookup"><span data-stu-id="881db-771">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <span data-ttu-id="881db-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-773">遠端存取連線已完成，但驗證失敗，因為在 [信任的根憑證授權單位] 憑證存放區中找不到驗證伺服器憑證的憑證。</span><span class="sxs-lookup"><span data-stu-id="881db-773">The remote access connection completed, but authentication failed because a certificate that validates the server certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <span data-ttu-id="881db-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-775">遠端存取連線已完成，但驗證失敗，因為驗證伺服器憑證的信任根憑證授權單位憑證存放區中的憑證無效。</span><span class="sxs-lookup"><span data-stu-id="881db-775">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that validates the server certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <span data-ttu-id="881db-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-777">遠端存取連線已完成，但驗證失敗，因為伺服器電腦上的憑證未指定伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="881db-777">The remote access connection completed, but authentication failed because the certificate on the server computer does not have a server name specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <span data-ttu-id="881db-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-779">當身分識別隱私權關閉時，PEAP 外部識別與內部身分識別不相同。</span><span class="sxs-lookup"><span data-stu-id="881db-779">The PEAP outer identity is not same as the inner identity when identity privacy is turned OFF.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <span data-ttu-id="881db-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-781">因為遠端存取服務器的名稱無法解析，所以未建立遠端連線。</span><span class="sxs-lookup"><span data-stu-id="881db-781">The remote connection was not made because the name of the remote access server did not resolve.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <span data-ttu-id="881db-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-783">為憑證提供的密碼無效。</span><span class="sxs-lookup"><span data-stu-id="881db-783">The password provided for the certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <span data-ttu-id="881db-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-785">無法啟用介面，因為使用預先共用金鑰驗證方法建立了一個以上具有相同目的地的介面。</span><span class="sxs-lookup"><span data-stu-id="881db-785">The interface could not be enabled because more than one interface with the same destination has been created with the pre-shared key authentication method.</span></span> <span data-ttu-id="881db-786">變更目的地/auth 方法並啟用介面。</span><span class="sxs-lookup"><span data-stu-id="881db-786">Change the destination/auth method and enable the interface.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="881db-787">下列路由和遠端存取 (RRAS) API 錯誤碼定義于 mprerror 中。</span><span class="sxs-lookup"><span data-stu-id="881db-787">The following Routing and Remote Access (RRAS) API error codes are defined in mprerror.h.</span></span> <span data-ttu-id="881db-788">除非另有指定，否則 Windows 2000 或更新版本的 Windows 中都支援所有錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="881db-788">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="881db-789">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="881db-789">Return code/value</span></span></th>
<th><span data-ttu-id="881db-790">Description</span><span class="sxs-lookup"><span data-stu-id="881db-790">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <span data-ttu-id="881db-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-792">路由器未執行。</span><span class="sxs-lookup"><span data-stu-id="881db-792">The router is not running.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <span data-ttu-id="881db-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-794">介面已連接。</span><span class="sxs-lookup"><span data-stu-id="881db-794">The interface is already connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <span data-ttu-id="881db-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-796">路由器不知道指定的通訊協定識別碼。</span><span class="sxs-lookup"><span data-stu-id="881db-796">The specified protocol identifier is not known to the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <span data-ttu-id="881db-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-798">指定撥號介面管理員 (DDM) 未執行。</span><span class="sxs-lookup"><span data-stu-id="881db-798">The Demand-dial Interface Manager (DDM) is not running.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <span data-ttu-id="881db-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-800">已向路由器註冊此名稱的介面。</span><span class="sxs-lookup"><span data-stu-id="881db-800">An interface with this name is already registered with the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <span data-ttu-id="881db-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-802">具有此名稱的介面未向路由器註冊。</span><span class="sxs-lookup"><span data-stu-id="881db-802">An interface with this name is not registered with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <span data-ttu-id="881db-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-804">介面未連接。</span><span class="sxs-lookup"><span data-stu-id="881db-804">The interface is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <span data-ttu-id="881db-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-806">指定的通訊協定正在停止。</span><span class="sxs-lookup"><span data-stu-id="881db-806">The specified protocol is stopping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <span data-ttu-id="881db-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-808">介面已連線，因此無法刪除。</span><span class="sxs-lookup"><span data-stu-id="881db-808">The interface is connected and hence cannot be deleted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <span data-ttu-id="881db-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-810">尚未設定介面認證。</span><span class="sxs-lookup"><span data-stu-id="881db-810">The interface credentials have not been set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <span data-ttu-id="881db-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-812">此介面已在連接的進程中。</span><span class="sxs-lookup"><span data-stu-id="881db-812">This interface is already in the process of connecting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <span data-ttu-id="881db-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-814">此介面上的路由資訊更新已在進行中。</span><span class="sxs-lookup"><span data-stu-id="881db-814">An update of routing information on this interface is already in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <span data-ttu-id="881db-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-816">介面的無法進行程式。</span><span class="sxs-lookup"><span data-stu-id="881db-816">The interface configration is not valid.</span></span> <span data-ttu-id="881db-817">已經有另一個介面連線到遠端路由器上的相同介面。</span><span class="sxs-lookup"><span data-stu-id="881db-817">There is already another interface that is connected to the same interface on the remote router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <span data-ttu-id="881db-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-819">遠端存取用戶端嘗試透過只保留給路由器的埠進行連接。</span><span class="sxs-lookup"><span data-stu-id="881db-819">A Remote Access Client attempted to connect over a port that was reserved for routers only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <span data-ttu-id="881db-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-821">要求撥號路由器嘗試透過只保留給遠端存取用戶端的埠進行連線。</span><span class="sxs-lookup"><span data-stu-id="881db-821">A Demand Dial Router attempted to connect over a port that was reserved for Remote Access Clients only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <span data-ttu-id="881db-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-823">具有此名稱的用戶端介面已經存在，且目前已連接。</span><span class="sxs-lookup"><span data-stu-id="881db-823">The client interface with this name already exists and is currently connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <span data-ttu-id="881db-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-825">介面處於停用狀態。</span><span class="sxs-lookup"><span data-stu-id="881db-825">The interface is in a disabled state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <span data-ttu-id="881db-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-827">遠端對等已拒絕驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="881db-827">The authentication protocol was rejected by the remote peer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <span data-ttu-id="881db-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-829">沒有可供使用的驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="881db-829">There are no authentication protocols available for use.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <span data-ttu-id="881db-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-831">無法建立連線，因為 RAS/VPN 伺服器用來驗證您的使用者名稱和密碼的驗證通訊協定，無法與連線設定檔中的設定相符。</span><span class="sxs-lookup"><span data-stu-id="881db-831">The connection could not be established because the authentication protocol used by the RAS/VPN server to verify your username and password could not be matched with the settings in your connection profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <span data-ttu-id="881db-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-833">遠端帳戶沒有遠端存取許可權。</span><span class="sxs-lookup"><span data-stu-id="881db-833">The remote account does not have Remote Access permission.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <span data-ttu-id="881db-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-835">遠端帳戶已過期。</span><span class="sxs-lookup"><span data-stu-id="881db-835">The remote account has expired.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <span data-ttu-id="881db-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-837">遠端帳戶已停用。</span><span class="sxs-lookup"><span data-stu-id="881db-837">The remote account is disabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <span data-ttu-id="881db-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-839">遠端帳戶在一天內不允許登入。</span><span class="sxs-lookup"><span data-stu-id="881db-839">The remote account is not permitted to logon at this time of day.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <span data-ttu-id="881db-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-841">拒絕存取遠端對等，因為網域上的使用者名稱、密碼或兩者皆無效。</span><span class="sxs-lookup"><span data-stu-id="881db-841">Access was denied to the remote peer because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <span data-ttu-id="881db-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-843">沒有可供此要求撥號介面使用的路由啟用埠。</span><span class="sxs-lookup"><span data-stu-id="881db-843">There are no routing enabled ports available for use by this demand dial interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <span data-ttu-id="881db-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-845">埠已中斷連線，因為沒有活動。</span><span class="sxs-lookup"><span data-stu-id="881db-845">The port has been disconnected due to inactivity.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <span data-ttu-id="881db-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-847">目前無法連接介面。</span><span class="sxs-lookup"><span data-stu-id="881db-847">The interface is not reachable at this time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <span data-ttu-id="881db-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-849">要求撥號服務處於暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="881db-849">The Demand Dial service is in a paused state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <span data-ttu-id="881db-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-851">系統管理員已將介面中斷連接。</span><span class="sxs-lookup"><span data-stu-id="881db-851">The interface has been disconnected by the administrator.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <span data-ttu-id="881db-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-853">驗證服務器未及時回應驗證要求。</span><span class="sxs-lookup"><span data-stu-id="881db-853">The authentication server did not respond to authentication requests in a timely fashion.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <span data-ttu-id="881db-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-855">已達到允許在多連結連接中使用的埠數目上限。</span><span class="sxs-lookup"><span data-stu-id="881db-855">The maximum number of ports allowed for use in the multi-linked connection has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <span data-ttu-id="881db-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-857">已達到使用者的連線時間限制。</span><span class="sxs-lookup"><span data-stu-id="881db-857">The connection time limit for the user has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <span data-ttu-id="881db-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-859">已達到支援的 LAN 介面數目上限。</span><span class="sxs-lookup"><span data-stu-id="881db-859">The maximum limit on the number of LAN interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <span data-ttu-id="881db-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-861">已達到所支援的最大要求撥號介面數目上限。</span><span class="sxs-lookup"><span data-stu-id="881db-861">The maximum limit on the number of Demand Dial interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <span data-ttu-id="881db-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-863">已達到支援的遠端存取用戶端數目上限。</span><span class="sxs-lookup"><span data-stu-id="881db-863">The maximum limit on the number of Remote Access Clients supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <span data-ttu-id="881db-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-865">埠已中斷連線，因為頻寬配置通訊協定 (BAP) 原則。</span><span class="sxs-lookup"><span data-stu-id="881db-865">The port has been disconnected due to the Bandwidth Allocation Protocol (BAP) policy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <span data-ttu-id="881db-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-867">因為您類型的另一個連接正在使用中，所以連入連線無法接受您的連線要求。</span><span class="sxs-lookup"><span data-stu-id="881db-867">Because another connection of your type is in use, the incoming connection cannot accept your connection request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <span data-ttu-id="881db-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-869">網路上找不到任何 RADIUS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="881db-869">No RADIUS servers were located on the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <span data-ttu-id="881db-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-871">從 RADIUS 驗證服務器收到的回應無效。</span><span class="sxs-lookup"><span data-stu-id="881db-871">The response received from the RADIUS authentication server was not valid.</span></span> <span data-ttu-id="881db-872">請確定已正確設定 RADIUS 伺服器的區分大小寫秘密密碼。</span><span class="sxs-lookup"><span data-stu-id="881db-872">Make sure that the case sensitive secret password for the RADIUS server is set correctly.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <span data-ttu-id="881db-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-874">您目前沒有連接的許可權。</span><span class="sxs-lookup"><span data-stu-id="881db-874">You do not have permission to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <span data-ttu-id="881db-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-876">您沒有使用目前裝置類型連接的許可權。</span><span class="sxs-lookup"><span data-stu-id="881db-876">You do not have permission to connect using the current device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <span data-ttu-id="881db-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-878">無法建立連線，因為在 RAS/VPN 伺服器上設定的存取原則，不允許連線設定檔使用的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="881db-878">The connection could not be established because the authentication method used by your connection profile is not permitted for use by an access policy configured on the RAS/VPN server.</span></span> <span data-ttu-id="881db-879">具體而言，這可能是因為 RAS/VPN 伺服器上所選取的驗證方法與設定的存取原則之間的設定差異所致。</span><span class="sxs-lookup"><span data-stu-id="881db-879">Specifically, this could be due to configuration differences between the authentication method selected on the RAS/VPN server and the access policy configured for it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <span data-ttu-id="881db-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-881">此使用者需要 BAP。</span><span class="sxs-lookup"><span data-stu-id="881db-881">BAP is required for this user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <span data-ttu-id="881db-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-883">目前不允許介面進行連接。</span><span class="sxs-lookup"><span data-stu-id="881db-883">The interface is not allowed to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <span data-ttu-id="881db-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-885">儲存的路由器設定與目前的路由器不相容。</span><span class="sxs-lookup"><span data-stu-id="881db-885">The saved router configuration is incompatible with the current router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <span data-ttu-id="881db-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-887">遠端存取偵測到較舊的格式使用者帳戶，將不會自動遷移。</span><span class="sxs-lookup"><span data-stu-id="881db-887">Remote Access has detected older format user accounts that will not be migrated automatically.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <span data-ttu-id="881db-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-889">此傳輸已與路由器一起安裝。</span><span class="sxs-lookup"><span data-stu-id="881db-889">The transport is already installed with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <span data-ttu-id="881db-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-891">在 RADIUS 伺服器的封包中收到的簽章長度無效。</span><span class="sxs-lookup"><span data-stu-id="881db-891">The signature length received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-892">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-892">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <span data-ttu-id="881db-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-894">在 RADIUS 伺服器的封包中收到的簽章無效。</span><span class="sxs-lookup"><span data-stu-id="881db-894">The signature received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-895">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-895">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <span data-ttu-id="881db-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-897">未收到來自 RADIUS 伺服器的簽章和 EAPMessage。</span><span class="sxs-lookup"><span data-stu-id="881db-897">Did not receive signature along with EAPMessage from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-898">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-898">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <span data-ttu-id="881db-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-900">在 RADIUS 伺服器的封包中收到的長度或識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="881db-900">The length or Id received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-901">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-901">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <span data-ttu-id="881db-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-903">在具有 RADIUS 伺服器之屬性的封包中收到的長度無效。</span><span class="sxs-lookup"><span data-stu-id="881db-903">The length received in a packet with attribute from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-904">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-904">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <span data-ttu-id="881db-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-906">從 RADIUS 伺服器收到的封包無效。</span><span class="sxs-lookup"><span data-stu-id="881db-906">The packet received from RADIUS server in not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-907">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-907">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <span data-ttu-id="881db-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-909">驗證器不符合 RADIUS 伺服器的封包。</span><span class="sxs-lookup"><span data-stu-id="881db-909">Authenticator does not match in packet from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-910">在 Windows XP 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-910">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <span data-ttu-id="881db-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span><span class="sxs-lookup"><span data-stu-id="881db-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span></span></dl></td>
<td><span data-ttu-id="881db-912">路由及遠端存取服務器未設定或未執行。</span><span class="sxs-lookup"><span data-stu-id="881db-912">Routing and Remote access server is either not configured or not running.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="881db-913">在 Windows 7 和更新版本的 Windows 中支援。</span><span class="sxs-lookup"><span data-stu-id="881db-913">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="881db-914">規格需求</span><span class="sxs-lookup"><span data-stu-id="881db-914">Requirements</span></span>



| <span data-ttu-id="881db-915">需求</span><span class="sxs-lookup"><span data-stu-id="881db-915">Requirement</span></span> | <span data-ttu-id="881db-916">值</span><span class="sxs-lookup"><span data-stu-id="881db-916">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="881db-917">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="881db-917">Minimum supported client</span></span><br/> | <span data-ttu-id="881db-918">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="881db-918">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="881db-919">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="881db-919">Minimum supported server</span></span><br/> | <span data-ttu-id="881db-920">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="881db-920">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 





