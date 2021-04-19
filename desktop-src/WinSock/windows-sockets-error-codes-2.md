---
description: Windows 通訊端 (Winsock) WSAGetLastError 函數所傳回的錯誤碼。
ms.assetid: 50b924f3-2c88-443b-8a90-4293fe5c3048
title: 'Windows 通訊端錯誤碼 (Winsock2. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c251d63872c05623a6d1c9e3820edd2d8f670e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981658"
---
# <a name="windows-sockets-error-codes"></a>Windows 通訊端錯誤碼

大部分的 Windows 通訊端2函式在函式傳回時，不會傳回錯誤的特定原因。 如需詳細資訊，請參閱 [處理 Winsock 錯誤](handling-winsock-errors.md) 主題。

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)函式會傳回呼叫執行緒所發生的最後一個錯誤。 當特定的 Windows 通訊端函式指出發生錯誤時，應該立即呼叫這個函式，以取得失敗函式呼叫的擴充錯誤碼。 這些錯誤碼和與錯誤碼相關聯的簡短文字描述會定義在 *winerror.h .h* 標頭檔中。 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)函數可用來取得傳回錯誤的訊息字串。

如需如何在將通訊端應用程式移植到 Winsock 時處理錯誤碼的詳細資訊，請參閱 [錯誤碼-errno、h \_ Errno 和 WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)。

下列清單描述 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 函數所傳回的可能錯誤碼。 錯誤會以數位順序列出，並顯示錯誤宏名稱。 在 *Winsock2* 標頭檔中定義的某些錯誤碼不會從任何函數傳回。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>傳回碼/值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="WSA_INVALID_HANDLE"></span><span id="wsa_invalid_handle"></span><dl> <dt><strong>WSA_INVALID_HANDLE</strong></dt> <dt>6</dt> </dl></td>
<td><dl> <dt><span id="Specified_event_object_handle_is_invalid."></span><span id="specified_event_object_handle_is_invalid."></span><span id="SPECIFIED_EVENT_OBJECT_HANDLE_IS_INVALID."></span>指定的事件物件控制碼無效。</dt> <dd> 應用程式嘗試使用事件物件，但指定的控制碼無效。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span><dl> <dt><strong>WSA_NOT_ENOUGH_MEMORY</strong></dt> <dt>8</dt> </dl></td>
<td><dl> <dt><span id="Insufficient_memory_available."></span><span id="insufficient_memory_available."></span><span id="INSUFFICIENT_MEMORY_AVAILABLE."></span>可用的記憶體不足。</dt> <dd> 應用程式使用的 Windows 通訊端函式會直接對應至 Windows 函式。 Windows 函數指出缺少必要的記憶體資源。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_INVALID_PARAMETER"></span><span id="wsa_invalid_parameter"></span><dl> <dt><strong>WSA_INVALID_PARAMETER</strong></dt> <dt>87</dt> </dl></td>
<td><dl> <dt><span id="One_or_more_parameters_are_invalid."></span><span id="one_or_more_parameters_are_invalid."></span><span id="ONE_OR_MORE_PARAMETERS_ARE_INVALID."></span>一或多個參數無效。</dt> <dd> 應用程式使用的 Windows 通訊端函式會直接對應至 Windows 函式。 Windows 函數指出有一或多個參數發生問題。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span><dl> <dt><strong>WSA_OPERATION_ABORTED</strong></dt> <dt>995</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_operation_aborted."></span><span id="overlapped_operation_aborted."></span><span id="OVERLAPPED_OPERATION_ABORTED."></span>重迭的作業已中止。</dt> <dd> 因為通訊端關閉或在 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a>中執行 SIO_FLUSH 命令，所以重迭的作業已取消。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_IO_INCOMPLETE"></span><span id="wsa_io_incomplete"></span><dl> <dt><strong>WSA_IO_INCOMPLETE</strong></dt> <dt>996</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_I_O_event_object_not_in_signaled_state."></span><span id="overlapped_i_o_event_object_not_in_signaled_state."></span><span id="OVERLAPPED_I_O_EVENT_OBJECT_NOT_IN_SIGNALED_STATE."></span>重迭的 i/o 事件物件未處於已發出信號的狀態。</dt> <dd> 應用程式已嘗試判斷尚未完成之重迭作業的狀態。 使用 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult"><strong>WSAGetOverlappedResult</strong></a> (將 <em>fWait</em> 旗標設為 FALSE 的應用程式會在輪詢模式中設定為 <strong>FALSE</strong>) 以判斷重迭作業是否已完成，請在作業完成之前取得此錯誤碼。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_IO_PENDING"></span><span id="wsa_io_pending"></span><dl> <dt><strong>WSA_IO_PENDING</strong></dt> <dt>997</dt> </dl></td>
<td>重迭的作業會在稍後完成。 <br/> <dl> <dt><span></span></dt> <dd> 應用程式初始化了無法立即完成的重疊作業。 稍後當作業完成時，將會提供完成指示。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINTR"></span><span id="wsaeintr"></span><dl> <dt><strong>WSAEINTR</strong></dt> <dt>10004</dt> </dl></td>
<td><dl> <dt><span id="Interrupted_function_call."></span><span id="interrupted_function_call."></span><span id="INTERRUPTED_FUNCTION_CALL."></span>中斷函式呼叫。</dt> <dd> 呼叫 <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>時，封鎖作業中斷。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEBADF"></span><span id="wsaebadf"></span><dl> <dt><strong>WSAEBADF</strong></dt> <dt>10009</dt> </dl></td>
<td><dl> <dt><span id="File_handle_is_not_valid."></span><span id="file_handle_is_not_valid."></span><span id="FILE_HANDLE_IS_NOT_VALID."></span>檔案控制代碼無效。</dt> <dd> 提供的檔案控制代碼無效。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEACCES"></span><span id="wsaeacces"></span><dl> <dt><strong>WSAEACCES</strong></dt> <dt>10013</dt> </dl></td>
<td><dl> <dt><span id="Permission_denied."></span><span id="permission_denied."></span><span id="PERMISSION_DENIED."></span>許可權被拒。</dt> <dd> 嘗試以存取權限禁止的方式存取通訊端。 例如，在未使用<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> (SO_BROADCAST) 設定廣播許可權的<a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>中使用廣播位址。 <br/> WSAEACCES <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>錯誤的另</strong></a> 一個可能原因是呼叫系結函式時， (在 Windows NT 4.0 加裝 SP4 和更新) 版本時，其他應用程式、服務或核心模式驅動程式都會系結至具有獨佔存取權的相同位址。 這種獨佔存取是 Windows NT 4.0 加裝 SP4 和更新版本的新功能，並使用 <a href="/windows/desktop/winsock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a> 選項來執行。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEFAULT"></span><span id="wsaefault"></span><dl> <dt><strong>WSAEFAULT</strong></dt> <dt>10014</dt> </dl></td>
<td><dl> <dt><span id="Bad_address."></span><span id="bad_address."></span><span id="BAD_ADDRESS."></span>位址錯誤。</dt> <dd> 系統在嘗試使用呼叫的指標引數時偵測到不正確指標位址。 如果應用程式傳遞不正確指標值，或緩衝區的長度太小，就會發生這個錯誤。 比方說，如果引數的長度是 <a href="/windows/desktop/winsock/sockaddr-2"><strong>sockaddr</strong></a> 結構，則小於 sizeof (sockaddr) 。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVAL"></span><span id="wsaeinval"></span><dl> <dt><strong>WSAEINVAL</strong></dt> <dt>10022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_argument."></span><span id="invalid_argument."></span><span id="INVALID_ARGUMENT."></span>不正確引數。</dt> <dd> 提供了一些不正確引數 (例如，指定了不正確層級給 <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> 函數) 。 在某些情況下，它也是指通訊端目前的狀態，例如，在未接聽的通訊端上呼叫 <a href="/windows/desktop/api/Winsock2/nf-winsock2-accept"><strong>accept</strong></a> 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMFILE"></span><span id="wsaemfile"></span><dl> <dt><strong>WSAEMFILE</strong></dt> <dt>10024</dt> </dl></td>
<td><dl> <dt><span id="Too_many_open_files."></span><span id="too_many_open_files."></span><span id="TOO_MANY_OPEN_FILES."></span>開啟太多檔案。</dt> <dd> 開啟的通訊端太多。 每個實作為可供使用的通訊端控制碼數目上限有可能是全域、每個進程或每個執行緒。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span><dl> <dt><strong>WSAEWOULDBLOCK</strong></dt> <dt>10035</dt> </dl></td>
<td><dl> <dt><span id="Resource_temporarily_unavailable."></span><span id="resource_temporarily_unavailable."></span><span id="RESOURCE_TEMPORARILY_UNAVAILABLE."></span>資源暫時無法使用。</dt> <dd> 無法立即完成的非封鎖通訊端上的作業會傳回此錯誤，例如，在沒有資料排入佇列以從通訊端讀取時，就會 <a href="/windows/desktop/api/winsock/nf-winsock-recv"><strong>接收</strong></a> 此錯誤。 這是非嚴重錯誤，而且應該稍後重試作業。 WSAEWOULDBLOCK 在非封鎖 SOCK_STREAM 通訊端上呼叫 <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>connect</strong></a> 的結果是正常的，因為必須經過一些時間才能建立連接。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span><dl> <dt><strong>WSAEINPROGRESS</strong></dt> <dt>10036</dt> </dl></td>
<td><dl> <dt><span id="Operation_now_in_progress."></span><span id="operation_now_in_progress."></span><span id="OPERATION_NOW_IN_PROGRESS."></span>作業正在進行中。</dt> <dd> 正在執行封鎖作業。 Windows 通訊端只允許一項封鎖作業（每個工作或執行緒）處於未處理狀態，而且如果 (任何其他函式呼叫，則不論是否參考該函式或任何其他通訊端) 函數都會失敗並出現 WSAEINPROGRESS 錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEALREADY"></span><span id="wsaealready"></span><dl> <dt><strong>WSAEALREADY</strong></dt> <dt>10037</dt> </dl></td>
<td><dl> <dt><span id="Operation_already_in_progress."></span><span id="operation_already_in_progress."></span><span id="OPERATION_ALREADY_IN_PROGRESS."></span>作業已在進行中。</dt> <dd> 在非封鎖通訊端上嘗試操作，但作業已在進行中，也就是在已連線的非封鎖通訊端上第二次呼叫 <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>連接</strong></a> ，或取消非同步要求 (<strong>WSAAsyncGetXbyY</strong> 已取消或已完成的) 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span><dl> <dt><strong>WSAENOTSOCK</strong></dt> <dt>10038</dt> </dl></td>
<td><dl> <dt><span id="Socket_operation_on_nonsocket."></span><span id="socket_operation_on_nonsocket."></span><span id="SOCKET_OPERATION_ON_NONSOCKET."></span>Nonsocket 上的通訊端作業。</dt> <dd> 嘗試對不是通訊端的某個作業進行作業。 可能是通訊端控制碼參數未參考有效的通訊端，或針對 <a href="/windows/desktop/api/Winsock2/nf-winsock2-select"><strong>select</strong></a>， <strong>fd_set</strong> 的成員無效。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span><dl> <dt><strong>WSAEDESTADDRREQ</strong></dt> <dt>10039</dt> </dl></td>
<td><dl> <dt><span id="Destination_address_required."></span><span id="destination_address_required."></span><span id="DESTINATION_ADDRESS_REQUIRED."></span>需要目的地位址。</dt> <dd> 已從通訊端上的作業省略必要的位址。 例如，如果使用 ADDR_ANY 的遠端位址來呼叫 <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> ，則會傳回此錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span><dl> <dt><strong>WSAEMSGSIZE</strong></dt> <dt>10040</dt> </dl></td>
<td><dl> <dt><span id="Message_too_long."></span><span id="message_too_long."></span><span id="MESSAGE_TOO_LONG."></span>訊息太長。</dt> <dd> 在資料包通訊端上傳送的訊息大於內部訊息緩衝區或其他網路限制，或是用來接收資料包的緩衝區小於資料包本身。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span><dl> <dt><strong>WSAEPROTOTYPE</strong></dt> <dt>10041</dt> </dl></td>
<td><dl> <dt><span id="Protocol_wrong_type_for_socket."></span><span id="protocol_wrong_type_for_socket."></span><span id="PROTOCOL_WRONG_TYPE_FOR_SOCKET."></span>通訊端的通訊協定類型錯誤。</dt> <dd> 在 <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>通訊端</strong></a> 函數呼叫中指定的通訊協定不支援所要求之通訊端類型的語法。 例如，ARPA 網際網路 UDP 通訊協定無法指定 SOCK_STREAM 的通訊端類型。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span><dl> <dt><strong>WSAENOPROTOOPT</strong></dt> <dt>10042</dt> </dl></td>
<td><dl> <dt><span id="Bad_protocol_option."></span><span id="bad_protocol_option."></span><span id="BAD_PROTOCOL_OPTION."></span>錯誤的通訊協定選項。</dt> <dd> 在 <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt"><strong>getsockopt</strong></a> 或 <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> 呼叫中指定了未知、無效或不支援的選項或層級。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span><dl> <dt><strong>WSAEPROTONOSUPPORT</strong></dt> <dt>10043</dt> </dl></td>
<td><dl> <dt><span id="Protocol_not_supported."></span><span id="protocol_not_supported."></span><span id="PROTOCOL_NOT_SUPPORTED."></span>不支援的通訊協定。</dt> <dd> 要求的通訊協定尚未設定到系統中，或其不存在。 例如， <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>通訊端</strong></a> 呼叫會要求 SOCK_DGRAM 通訊端，但會指定串流通訊協定。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span><dl> <dt><strong>WSAESOCKTNOSUPPORT</strong></dt> <dt>10044</dt> </dl></td>
<td><dl> <dt><span id="Socket_type_not_supported."></span><span id="socket_type_not_supported."></span><span id="SOCKET_TYPE_NOT_SUPPORTED."></span>不支援通訊端類型。</dt> <dd> 這個地址家族中不存在對指定通訊端類型的支援。 例如，可能會在 <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>通訊端</strong></a> 呼叫中選取選擇性的 SOCK_RAW 型別，而執行完全不支援 SOCK_RAW 通訊端。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span><dl> <dt><strong>WSAEOPNOTSUPP</strong></dt> <dt>10045</dt> </dl></td>
<td><dl> <dt><span id="Operation_not_supported."></span><span id="operation_not_supported."></span><span id="OPERATION_NOT_SUPPORTED."></span>不支援操作。</dt> <dd> 所參考的物件類型不支援所嘗試的操作。 當通訊端的通訊端描述項無法支援此作業時，通常會發生這種情況，因為它會嘗試接受資料包通訊端上的連接。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span><dl> <dt><strong>WSAEPFNOSUPPORT</strong></dt> <dt>10046</dt> </dl></td>
<td><dl> <dt><span id="Protocol_family_not_supported."></span><span id="protocol_family_not_supported."></span><span id="PROTOCOL_FAMILY_NOT_SUPPORTED."></span>不支援通訊協定系列。</dt> <dd> 通訊協定系列尚未設定為系統，或其不存在。 這則訊息與 WSAEAFNOSUPPORT 有稍微不同的意義。 不過，在大部分情況下，它是可互換的，而傳回其中一個訊息的所有 Windows 通訊端函數也會指定 WSAEAFNOSUPPORT。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span><dl> <dt><strong>WSAEAFNOSUPPORT</strong></dt> <dt>10047</dt> </dl></td>
<td><dl> <dt><span id="Address_family_not_supported_by_protocol_family."></span><span id="address_family_not_supported_by_protocol_family."></span><span id="ADDRESS_FAMILY_NOT_SUPPORTED_BY_PROTOCOL_FAMILY."></span>通訊協定系列不支援位址系列。</dt> <dd> 使用的位址與要求的通訊協定不相容。 所有通訊端都會使用相關聯的位址系列來建立 (也就是網際網路通訊協定的 AF_INET) 和一般通訊協定類型 (也就是 SOCK_STREAM) 。 如果在 <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>通訊端</strong></a> 呼叫中明確要求不正確的通訊協定，或針對通訊端使用錯誤家族的位址（例如，在 <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>中），則會傳回此錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span><dl> <dt><strong>WSAEADDRINUSE</strong></dt> <dt>10048</dt> </dl></td>
<td><dl> <dt><span id="Address_already_in_use."></span><span id="address_already_in_use."></span><span id="ADDRESS_ALREADY_IN_USE."></span>位址已在使用中。</dt> <dd> 一般來說，只允許每個通訊端位址 (通訊協定/IP 位址/埠) 的一個使用。 如果應用程式嘗試將通訊端系 <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>結至已</strong></a> 用於現有通訊端的 IP 位址/埠，或是未正確關閉或仍在關閉進程中的通訊端，就會發生此錯誤。 針對需要將多個通訊端系 <strong>結至相同</strong> 埠號碼的伺服器應用程式，請考慮使用 <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> (SO_REUSEADDR) 。 用戶端應用程式通常不 <strong>需要呼叫系結，而</strong> 是<a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>connect</strong></a> 會自動選擇未使用的埠。 當使用包含 ADDR_ANY) 的萬用字元位址來呼叫 <strong>bind</strong> (時，WSAEADDRINUSE 錯誤可能會延遲，直到特定的位址認可為止。 在稍後呼叫另一個函式（包括 <strong>connect</strong>、 <a href="/windows/desktop/api/Winsock2/nf-winsock2-listen"><strong>接聽</strong></a>、 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>或 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>）時，可能會發生這種情況。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span><dl> <dt><strong>WSAEADDRNOTAVAIL</strong></dt> <dt>10049</dt> </dl></td>
<td><dl> <dt><span id="Cannot_assign_requested_address."></span><span id="cannot_assign_requested_address."></span><span id="CANNOT_ASSIGN_REQUESTED_ADDRESS."></span>無法指派要求的位址。</dt> <dd> 要求的位址在它的內容中無效。 這通常是因為嘗試系結 <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>至對</strong></a> 本機電腦不正確位址所產生。 當遠端位址或埠對遠端電腦而言是不正確 (例如，位址或埠 0) 時，這也可能是因為 <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>連接</strong></a>、 <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>、 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>、 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>或 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsasendto"><strong>WSASendTo</strong></a> 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span><dl> <dt><strong>WSAENETDOWN</strong></dt> <dt>10050</dt> </dl></td>
<td><dl> <dt><span id="Network_is_down."></span><span id="network_is_down."></span><span id="NETWORK_IS_DOWN."></span>網路已關閉。</dt> <dd> 通訊端作業遇到停止的網路。 這可能表示一個嚴重的網路系統 (也就是，執行 Windows Sockets DLL 的通訊協定堆疊)、網路介面或區域網路本身故障。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span><dl> <dt><strong>WSAENETUNREACH</strong></dt> <dt>10051</dt> </dl></td>
<td><dl> <dt><span id="Network_is_unreachable."></span><span id="network_is_unreachable."></span><span id="NETWORK_IS_UNREACHABLE."></span>無法連線到網路。</dt> <dd> 已嘗試對無法連線的網路進行通訊端作業。 這通常表示本機軟體不知道要連線到遠端主機的路由。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETRESET"></span><span id="wsaenetreset"></span><dl> <dt><strong>WSAENETRESET</strong></dt> <dt>10052</dt> </dl></td>
<td><dl> <dt><span id="Network_dropped_connection_on_reset."></span><span id="network_dropped_connection_on_reset."></span><span id="NETWORK_DROPPED_CONNECTION_ON_RESET."></span>重設時網路中斷連接。</dt> <dd> 連接已中斷，因為在作業進行時偵測到失敗。 如果嘗試在已失敗的連接上設定<a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> ，也可以透過<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a>傳回。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span><dl> <dt><strong>WSAECONNABORTED</strong></dt> <dt>10053</dt> </dl></td>
<td><dl> <dt><span id="Software_caused_connection_abort."></span><span id="software_caused_connection_abort."></span><span id="SOFTWARE_CAUSED_CONNECTION_ABORT."></span>軟體導致連接中止。</dt> <dd> 您主機電腦中的軟體已中止建立的連線，可能是因為資料傳輸超時或通訊協定錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span><dl> <dt><strong>WSAECONNRESET</strong></dt> <dt>10054</dt> </dl></td>
<td><dl> <dt><span id="Connection_reset_by_peer."></span><span id="connection_reset_by_peer."></span><span id="CONNECTION_RESET_BY_PEER."></span>對等互連的連接重設。</dt> <dd> 遠端主機已強制關閉一個現有連線。 如果遠端主機上的對等應用程式突然停止、主機重新開機、主機或遠端網路介面已停用，或遠端主機使用硬關閉 (請參閱 <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> ，以取得遠端通訊端) 上 SO_LINGER 選項的詳細資訊，通常會產生此情況。 如果連接因為持續運作活動在一或多個作業進行中偵測到失敗，也可能會導致此錯誤。 進行中的作業失敗，WSAENETRESET。 後續作業會失敗並出現 WSAECONNRESET。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span><dl> <dt><strong>WSAENOBUFS</strong></dt> <dt>10055</dt> </dl></td>
<td><dl> <dt><span id="No_buffer_space_available."></span><span id="no_buffer_space_available."></span><span id="NO_BUFFER_SPACE_AVAILABLE."></span>沒有可用的緩衝區空間。</dt> <dd> 無法執行通訊端上的作業，因為系統缺乏足夠的緩衝區空間，或佇列已滿。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEISCONN"></span><span id="wsaeisconn"></span><dl> <dt><strong>WSAEISCONN</strong></dt> <dt>10056</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_already_connected."></span><span id="socket_is_already_connected."></span><span id="SOCKET_IS_ALREADY_CONNECTED."></span>通訊端已連線。</dt> <dd> 已連線的通訊端上提出了 connect 要求。 如果在 SOCK_STREAM 通訊端的連接 SOCK_DGRAM 通訊端 (上呼叫<a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> ，某些執行也) 會傳回此錯誤，不過，其他<em>的</em><strong>執行會將</strong>其視為合法發生。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span><dl> <dt><strong>WSAENOTCONN</strong></dt> <dt>10057</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_not_connected."></span><span id="socket_is_not_connected."></span><span id="SOCKET_IS_NOT_CONNECTED."></span>通訊端未連線。</dt> <dd> 不允許傳送或接收資料的要求，因為通訊端未連線，而且在使用 <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> 傳送資料包通訊端時 (，) 未提供任何位址。 任何其他類型的作業也會傳回此錯誤，例如，如果已重設連接， <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> 設定 <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span><dl> <dt><strong>WSAESHUTDOWN</strong></dt> <dt>10058</dt> </dl></td>
<td><dl> <dt><span id="Cannot_send_after_socket_shutdown."></span><span id="cannot_send_after_socket_shutdown."></span><span id="CANNOT_SEND_AFTER_SOCKET_SHUTDOWN."></span>無法在通訊端關閉之後傳送。</dt> <dd> 不允許傳送或接收資料的要求，因為先前的 <a href="/windows/desktop/api/winsock/nf-winsock-shutdown"><strong>關機</strong></a> 呼叫已在該方向關閉通訊端。 藉由呼叫 <strong>shutdown</strong> ，會要求通訊端的部分封閉，也就是傳送或接收的信號，或兩者皆已停止。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span><dl> <dt><strong>WSAETOOMANYREFS</strong></dt> <dt>10059</dt> </dl></td>
<td><dl> <dt><span id="Too_many_references."></span><span id="too_many_references."></span><span id="TOO_MANY_REFERENCES."></span>參考太多。</dt> <dd> 某些核心物件的參考太多。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span><dl> <dt><strong>WSAETIMEDOUT</strong></dt> <dt>10060</dt> </dl></td>
<td><dl> <dt><span id="Connection_timed_out."></span><span id="connection_timed_out."></span><span id="CONNECTION_TIMED_OUT."></span>連接逾時。</dt> <dd> 連接嘗試失敗，因為連線的合作物件在一段時間後未正確回應，或建立的連接失敗，因為連線的主機無法回應。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span><dl> <dt><strong>WSAECONNREFUSED</strong></dt> <dt>10061</dt> </dl></td>
<td><dl> <dt><span id="Connection_refused."></span><span id="connection_refused."></span><span id="CONNECTION_REFUSED."></span>連接遭到拒絕。</dt> <dd> 因為目的電腦主動拒絕連線，所以無法進行連接。 這通常是因為嘗試連接至外部主機上非使用中的服務（也就是沒有執行伺服器應用程式的服務）的結果。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAELOOP"></span><span id="wsaeloop"></span><dl> <dt><strong>WSAELOOP</strong></dt> <dt>10062</dt> </dl></td>
<td><dl> <dt><span id="Cannot_translate_name."></span><span id="cannot_translate_name."></span><span id="CANNOT_TRANSLATE_NAME."></span>無法轉譯名稱。</dt> <dd> 無法轉譯名稱。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span><dl> <dt><strong>WSAENAMETOOLONG</strong></dt> <dt>10063</dt> </dl></td>
<td><dl> <dt><span id="Name_too_long."></span><span id="name_too_long."></span><span id="NAME_TOO_LONG."></span>名稱太長。</dt> <dd> 名稱元件或名稱太長。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span><dl> <dt><strong>WSAEHOSTDOWN</strong></dt> <dt>10064</dt> </dl></td>
<td><dl> <dt><span id="Host_is_down."></span><span id="host_is_down."></span><span id="HOST_IS_DOWN."></span>主機已關閉。</dt> <dd> 通訊端作業失敗，因為目的地主機已關閉。 通訊端作業遇到無法正常運作的主機。 尚未起始本機主機上的網路活動。 這些條件更可能由錯誤 WSAETIMEDOUT 來表示。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span><dl> <dt><strong>WSAEHOSTUNREACH</strong></dt> <dt>10065</dt> </dl></td>
<td><dl> <dt><span id="No_route_to_host."></span><span id="no_route_to_host."></span><span id="NO_ROUTE_TO_HOST."></span>沒有路由到主機。</dt> <dd> 已嘗試對無法連接的主機進行通訊端作業。 請參閱 WSAENETUNREACH。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span><dl> <dt><strong>WSAENOTEMPTY</strong></dt> <dt>10066</dt> </dl></td>
<td><dl> <dt><span id="Directory_not_empty."></span><span id="directory_not_empty."></span><span id="DIRECTORY_NOT_EMPTY."></span>目錄不是空的。</dt> <dd> 無法移除非空白的目錄。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span><dl> <dt><strong>WSAEPROCLIM</strong></dt> <dt>10067</dt> </dl></td>
<td><dl> <dt><span id="Too_many_processes."></span><span id="too_many_processes."></span><span id="TOO_MANY_PROCESSES."></span>太多進程。</dt> <dd> Windows 通訊端執行可能會限制可同時使用它的應用程式數目。 如果已達到此限制， <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a>可能會失敗併發生此錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEUSERS"></span><span id="wsaeusers"></span><dl> <dt><strong>WSAEUSERS</strong></dt> <dt>10068</dt> </dl></td>
<td><dl> <dt><span id="User_quota_exceeded."></span><span id="user_quota_exceeded."></span><span id="USER_QUOTA_EXCEEDED."></span>超過使用者配額。</dt> <dd> 使用者配額已用盡。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDQUOT"></span><span id="wsaedquot"></span><dl> <dt><strong>WSAEDQUOT</strong></dt> <dt>10069</dt> </dl></td>
<td><dl> <dt><span id="Disk_quota_exceeded."></span><span id="disk_quota_exceeded."></span><span id="DISK_QUOTA_EXCEEDED."></span>超過磁片配額。</dt> <dd> 磁片配額已用盡。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESTALE"></span><span id="wsaestale"></span><dl> <dt><strong>WSAESTALE</strong></dt> <dt>10070</dt> </dl></td>
<td><dl> <dt><span id="Stale_file_handle_reference."></span><span id="stale_file_handle_reference."></span><span id="STALE_FILE_HANDLE_REFERENCE."></span>過時的檔案控制代碼參考。</dt> <dd> 無法再使用檔案控制代碼參考。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEREMOTE"></span><span id="wsaeremote"></span><dl> <dt><strong>WSAEREMOTE</strong></dt> <dt>10071</dt> </dl></td>
<td><dl> <dt><span id="Item_is_remote."></span><span id="item_is_remote."></span><span id="ITEM_IS_REMOTE."></span>專案為遠端。</dt> <dd> 專案無法在本機使用。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span><dl> <dt><strong>WSASYSNOTREADY</strong></dt> <dt>10091</dt> </dl></td>
<td><dl> <dt><span id="Network_subsystem_is_unavailable."></span><span id="network_subsystem_is_unavailable."></span><span id="NETWORK_SUBSYSTEM_IS_UNAVAILABLE."></span>網路子系統無法使用。</dt> <dd> 此錯誤是由 <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> 傳回，如果 Windows 通訊端執行目前無法運作，因為它用來提供網路服務的基礎系統目前無法使用。 使用者應該檢查：<br/> </dd> </dl>
<ul>
<li>適當的 Windows 通訊端 DLL 檔案位於目前的路徑中。</li>
<li>他們不會嘗試同時使用一個以上的 Windows 通訊端執行。 如果您的系統上有一個以上的 Winsock DLL，請確定路徑中的第一個 DLL 適用于目前載入的網路子系統。</li>
<li>Windows 通訊端執行檔，以確定目前已正確安裝及設定所有必要元件。</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span><dl> <dt><strong>WSAVERNOTSUPPORTED</strong></dt> <dt>10092</dt> </dl></td>
<td><dl> <dt><span id="Winsock.dll_version_out_of_range."></span><span id="winsock.dll_version_out_of_range."></span><span id="WINSOCK.DLL_VERSION_OUT_OF_RANGE."></span>Winsock.dll 版本超出範圍。</dt> <dd> 目前的 Windows 通訊端執行不支援應用程式所要求的 Windows 通訊端規格版本。 檢查是否未存取舊的 Windows Sockets DLL 檔案。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span><dl> <dt><strong>WSANOTINITIALISED</strong></dt> <dt>10093</dt> </dl></td>
<td><dl> <dt><span id="Successful_WSAStartup_not_yet_performed."></span><span id="successful_wsastartup_not_yet_performed."></span><span id="SUCCESSFUL_WSASTARTUP_NOT_YET_PERFORMED."></span>尚未執行成功的 WSAStartup。</dt> <dd> 可能是應用程式未呼叫 <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> 或 <strong>WSAStartup</strong> 失敗。 應用程式可能正在存取目前作用中工作沒有的通訊端 (也就是嘗試在工作) 之間共用通訊端，或呼叫 <a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup"><strong>WSACleanup</strong></a> 太多次。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDISCON"></span><span id="wsaediscon"></span><dl> <dt><strong>WSAEDISCON</strong></dt> <dt>10101</dt> </dl></td>
<td><dl> <dt><span id="Graceful_shutdown_in_progress."></span><span id="graceful_shutdown_in_progress."></span><span id="GRACEFUL_SHUTDOWN_IN_PROGRESS."></span>正常關機進行中。</dt> <dd> 由 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecv"><strong>WSARecv</strong></a> 和 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom"><strong>WSARecvFrom</strong></a> 傳回，表示遠端方已起始正常關機順序。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOMORE"></span><span id="wsaenomore"></span><dl> <dt><strong>WSAENOMORE</strong></dt> <dt>10102</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>沒有其他結果。</dt> <dd> <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>函數不會傳回任何結果。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span><dl> <dt><strong>WSAECANCELLED</strong></dt> <dt>10103</dt> </dl></td>
<td><dl> <dt><span id="Call_has_been_canceled."></span><span id="call_has_been_canceled."></span><span id="CALL_HAS_BEEN_CANCELED."></span>呼叫已取消。</dt> <dd> 呼叫 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd</strong></a> 函式是因為這個呼叫仍在處理中。 呼叫已取消。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span><dl> <dt><strong>WSAEINVALIDPROCTABLE</strong></dt> <dt>10104</dt> </dl></td>
<td><dl> <dt><span id="Procedure_call_table_is_invalid."></span><span id="procedure_call_table_is_invalid."></span><span id="PROCEDURE_CALL_TABLE_IS_INVALID."></span>程序呼叫資料表無效。</dt> <dd> 服務提供者程序呼叫資料表無效。 服務提供者將假程式資料表傳回 Ws2_32.dll。 這通常是由一或多個函式指標 <strong>為 Null</strong>所造成。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span><dl> <dt><strong>WSAEINVALIDPROVIDER</strong></dt> <dt>10105</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_is_invalid."></span><span id="service_provider_is_invalid."></span><span id="SERVICE_PROVIDER_IS_INVALID."></span>服務提供者無效。</dt> <dd> 要求的服務提供者無效。 如果找不到指定的通訊協定專案， <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo"><strong>WSCGetProviderInfo</strong></a> 和 <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32"><strong>WSCGetProviderInfo32</strong></a> 函數會傳回此錯誤。 如果服務提供者傳回的版本號碼不是2.0，也會傳回此錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span><dl> <dt><strong>WSAEPROVIDERFAILEDINIT</strong></dt> <dt>10106</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_failed_to_initialize."></span><span id="service_provider_failed_to_initialize."></span><span id="SERVICE_PROVIDER_FAILED_TO_INITIALIZE."></span>服務提供者無法初始化。</dt> <dd> 無法載入或初始化要求的服務提供者。 如果無法載入服務提供者的 DLL (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> 失敗) 或提供者的 <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup"><strong>WSPStartup</strong></a> 或 <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup"><strong>NSPStartup</strong></a> 函數失敗，則會傳回此錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span><dl> <dt><strong>WSASYSCALLFAILURE</strong></dt> <dt>10107</dt> </dl></td>
<td><dl> <dt><span id="System_call_failure."></span><span id="system_call_failure."></span><span id="SYSTEM_CALL_FAILURE."></span>系統呼叫失敗。</dt> <dd> 永遠不會失敗的系統呼叫失敗。 這是在各種情況下傳回的一般錯誤碼。 <br/> 在永遠不會失敗的系統呼叫失敗時傳回。 例如，如果呼叫 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents"><strong>WaitForMultipleEvents</strong></a> 失敗，或其中一個登錄函式嘗試操作通訊協定/命名空間目錄時失敗。<br/> 當提供者未傳回成功，但未提供延伸的錯誤碼時傳回。 可以指出服務提供者的執行錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span><dl> <dt><strong>WSASERVICE_NOT_FOUND</strong></dt> <dt>10108</dt> </dl></td>
<td><dl> <dt><span id="Service_not_found."></span><span id="service_not_found."></span><span id="SERVICE_NOT_FOUND."></span>找不到服務。</dt> <dd> 沒有已知的服務。 在指定的命名空間中找不到服務。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span><dl> <dt><strong>WSATYPE_NOT_FOUND</strong></dt> <dt>10109</dt> </dl></td>
<td><dl> <dt><span id="Class_type_not_found."></span><span id="class_type_not_found."></span><span id="CLASS_TYPE_NOT_FOUND."></span>找不到類別類型。</dt> <dd> 找不到指定的類別。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span><dl> <dt><strong>WSA_E_NO_MORE</strong></dt> <dt>10110</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>沒有其他結果。</dt> <dd> <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>函數不會傳回任何結果。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span><dl> <dt><strong>WSA_E_CANCELLED</strong></dt> <dt>10111</dt> </dl></td>
<td><dl> <dt><span id="Call_was_canceled."></span><span id="call_was_canceled."></span><span id="CALL_WAS_CANCELED."></span>呼叫已取消。</dt> <dd> 呼叫 <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd</strong></a> 函式是因為這個呼叫仍在處理中。 呼叫已取消。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEREFUSED"></span><span id="wsaerefused"></span><dl> <dt><strong>WSAEREFUSED</strong></dt> <dt>10112</dt> </dl></td>
<td><dl> <dt><span id="Database_query_was_refused."></span><span id="database_query_was_refused."></span><span id="DATABASE_QUERY_WAS_REFUSED."></span>資料庫查詢遭到拒絕。</dt> <dd> 資料庫查詢失敗，因為它已被主動拒絕。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span><dl> <dt><strong>WSAHOST_NOT_FOUND</strong></dt> <dt>11001</dt> </dl></td>
<td><dl> <dt><span id="Host_not_found."></span><span id="host_not_found."></span><span id="HOST_NOT_FOUND."></span>找不到主機。</dt> <dd> 沒有已知的此類主機。 名稱不是官方的主機名稱或別名，或在查詢 () 中找不到該名稱或別名。 通訊協定和服務查詢可能也會傳回此錯誤，表示在相關資料庫中找不到指定的名稱。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span><dl> <dt><strong>WSATRY_AGAIN</strong></dt> <dt>11002</dt> </dl></td>
<td><dl> <dt><span id="Nonauthoritative_host_not_found."></span><span id="nonauthoritative_host_not_found."></span><span id="NONAUTHORITATIVE_HOST_NOT_FOUND."></span>找不到非權威主機。</dt> <dd> 這通常是主機名稱解析期間的暫時錯誤，表示本機伺服器未收到來自授權伺服器的回應。 稍後重試也許可以成功。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span><dl> <dt><strong>WSANO_RECOVERY</strong></dt> <dt>11003</dt> </dl></td>
<td><dl> <dt><span id="This_is_a_nonrecoverable_error."></span><span id="this_is_a_nonrecoverable_error."></span><span id="THIS_IS_A_NONRECOVERABLE_ERROR."></span>這是無法恢復的錯誤。</dt> <dd> 這表示在資料庫查閱期間發生某種無法恢復的錯誤。 這可能是因為找不到資料庫檔案 (例如，) 找不到與 BSD 相容的主機、服務或通訊協定檔案，或伺服器傳回的 DNS 要求發生嚴重錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANO_DATA"></span><span id="wsano_data"></span><dl> <dt><strong>WSANO_DATA</strong></dt> <dt>11004</dt> </dl></td>
<td><dl> <dt><span id="Valid_name__no_data_record_of_requested_type."></span><span id="valid_name__no_data_record_of_requested_type."></span><span id="VALID_NAME__NO_DATA_RECORD_OF_REQUESTED_TYPE."></span>有效的名稱，沒有所要求類型的資料記錄。</dt> <dd> 要求的名稱是有效的，而且在資料庫中找到，但沒有解析正確的相關資料。 這種情況的常見範例是使用 <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname"><strong>gethostbyname</strong></a> 或 <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname"><strong>WSAAsyncGetHostByName</strong></a>) （使用 DNS (功能變數名稱伺服器) ） (的主機名稱對位址轉譯嘗試。 傳回 MX 記錄，但不含記錄，表示主機本身存在，但無法直接連線。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span><dl> <dt><strong>WSA_QOS_RECEIVERS</strong></dt> <dt>11005</dt> </dl></td>
<td><dl> <dt><span id="QoS_receivers."></span><span id="qos_receivers."></span><span id="QOS_RECEIVERS."></span>QoS 接收者。</dt> <dd> 至少有一個 QoS 保留已抵達。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span><dl> <dt><strong>WSA_QOS_SENDERS</strong></dt> <dt>11006</dt> </dl></td>
<td><dl> <dt><span id="QoS_senders."></span><span id="qos_senders."></span><span id="QOS_SENDERS."></span>QoS 寄件者。</dt> <dd> 至少有一個 QoS 傳送路徑已抵達。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span><dl> <dt><strong>WSA_QOS_NO_SENDERS</strong></dt> <dt>11007</dt> </dl></td>
<td><dl> <dt><span id="No_QoS_senders."></span><span id="no_qos_senders."></span><span id="NO_QOS_SENDERS."></span>無 QoS 寄件者。</dt> <dd> 沒有任何 QoS 寄件者。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span><dl> <dt><strong>WSA_QOS_NO_RECEIVERS</strong></dt> <dt>11008</dt> </dl></td>
<td><dl> <dt><span id="QoS_no_receivers."></span><span id="qos_no_receivers."></span><span id="QOS_NO_RECEIVERS."></span>QoS 無接收者。</dt> <dd> 沒有任何 QoS 接收者。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span><dl> <dt><strong>WSA_QOS_REQUEST_CONFIRMED</strong></dt> <dt>11009</dt> </dl></td>
<td><dl> <dt><span id="QoS_request_confirmed."></span><span id="qos_request_confirmed."></span><span id="QOS_REQUEST_CONFIRMED."></span>已確認 QoS 要求。</dt> <dd> 已確認 QoS 保留要求。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span><dl> <dt><strong>WSA_QOS_ADMISSION_FAILURE</strong></dt> <dt>11010</dt> </dl></td>
<td><dl> <dt><span id="QoS_admission_error."></span><span id="qos_admission_error."></span><span id="QOS_ADMISSION_ERROR."></span>QoS 許可錯誤。</dt> <dd> 因為缺少資源，所以發生 QoS 錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span><dl> <dt><strong>WSA_QOS_POLICY_FAILURE</strong></dt> <dt>11011</dt> </dl></td>
<td><dl> <dt><span id="QoS_policy_failure."></span><span id="qos_policy_failure."></span><span id="QOS_POLICY_FAILURE."></span>QoS 原則失敗。</dt> <dd> QoS 要求遭到拒絕，因為原則系統無法在現有的原則內配置要求的資源。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span><dl> <dt><strong>WSA_QOS_BAD_STYLE</strong></dt> <dt>11012</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_style."></span><span id="qos_bad_style."></span><span id="QOS_BAD_STYLE."></span>QoS 不正確的樣式。</dt> <dd> 遇到不明或衝突的 QoS 樣式。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span><dl> <dt><strong>WSA_QOS_BAD_OBJECT</strong></dt> <dt>11013</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_object."></span><span id="qos_bad_object."></span><span id="QOS_BAD_OBJECT."></span>QoS 錯誤物件。</dt> <dd> 部分 filterspec 或提供者特定的緩衝區通常會發生問題。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span><dl> <dt><strong>WSA_QOS_TRAFFIC_CTRL_ERROR</strong></dt> <dt>11014</dt> </dl></td>
<td><dl> <dt><span id="QoS_traffic_control_error."></span><span id="qos_traffic_control_error."></span><span id="QOS_TRAFFIC_CONTROL_ERROR."></span>QoS 流量控制錯誤。</dt> <dd> 基礎流量控制 (TC) API 的錯誤，因為一般 QoS 要求已針對 TC API 的本機強制進行轉換。 這可能是因為記憶體不足的錯誤或內部的 QoS 提供者錯誤。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span><dl> <dt><strong>WSA_QOS_GENERIC_ERROR</strong></dt> <dt>11015</dt> </dl></td>
<td><dl> <dt><span id="QoS_generic_error."></span><span id="qos_generic_error."></span><span id="QOS_GENERIC_ERROR."></span>QoS 一般錯誤。</dt> <dd> 一般的 QoS 錯誤。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span><dl> <dt><strong>WSA_QOS_ESERVICETYPE</strong></dt> <dt>11016</dt> </dl></td>
<td><dl> <dt><span id="QoS_service_type_error."></span><span id="qos_service_type_error."></span><span id="QOS_SERVICE_TYPE_ERROR."></span>QoS 服務類型錯誤。</dt> <dd> 在 QoS flowspec 中找到無效或無法辨識的服務類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span><dl> <dt><strong>WSA_QOS_EFLOWSPEC</strong></dt> <dt>11017</dt> </dl></td>
<td><dl> <dt><span id="QoS_flowspec_error."></span><span id="qos_flowspec_error."></span><span id="QOS_FLOWSPEC_ERROR."></span>QoS flowspec 錯誤。</dt> <dd> 在 <a href="/windows/win32/api/winsock2/ns-winsock2-qos"><strong>QOS</strong></a> 結構中發現無效或不一致的 flowspec。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span><dl> <dt><strong>WSA_QOS_EPROVSPECBUF</strong></dt> <dt>11018</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider_buffer."></span><span id="invalid_qos_provider_buffer."></span><span id="INVALID_QOS_PROVIDER_BUFFER."></span>不正確 QoS 提供者緩衝區。</dt> <dd> 不正確 QoS 提供者特定緩衝區。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span><dl> <dt><strong>WSA_QOS_EFILTERSTYLE</strong></dt> <dt>11019</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_style."></span><span id="invalid_qos_filter_style."></span><span id="INVALID_QOS_FILTER_STYLE."></span>不正確 QoS 篩選樣式。</dt> <dd> 使用了不正確 QoS 篩選樣式。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span><dl> <dt><strong>WSA_QOS_EFILTERTYPE</strong></dt> <dt>11020</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_type."></span><span id="invalid_qos_filter_type."></span><span id="INVALID_QOS_FILTER_TYPE."></span>QoS 篩選器類型無效。</dt> <dd> 使用了不正確 QoS 篩選類型。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span><dl> <dt><strong>WSA_QOS_EFILTERCOUNT</strong></dt> <dt>11021</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_filter_count."></span><span id="incorrect_qos_filter_count."></span><span id="INCORRECT_QOS_FILTER_COUNT."></span>QoS 篩選計數不正確。</dt> <dd> 在 FLOWDESCRIPTOR 中指定了不正確的 QoS FILTERSPECs 數目。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span><dl> <dt><strong>WSA_QOS_EOBJLENGTH</strong></dt> <dt>11022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_object_length."></span><span id="invalid_qos_object_length."></span><span id="INVALID_QOS_OBJECT_LENGTH."></span>QoS 物件長度無效。</dt> <dd> 在 QoS 提供者特定的緩衝區中指定了 ObjectLength 欄位不正確物件。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span><dl> <dt><strong>WSA_QOS_EFLOWCOUNT</strong></dt> <dt>11023</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_flow_count."></span><span id="incorrect_qos_flow_count."></span><span id="INCORRECT_QOS_FLOW_COUNT."></span>QoS 流程計數不正確。</dt> <dd> QoS 結構中指定了不正確數目的流程描述項。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span><dl> <dt><strong>WSA_QOS_EUNKOWNPSOBJ</strong></dt> <dt>11024</dt> </dl></td>
<td><dl> <dt><span id="Unrecognized_QoS_object."></span><span id="unrecognized_qos_object."></span><span id="UNRECOGNIZED_QOS_OBJECT."></span>無法辨識的 QoS 物件。</dt> <dd> 在 QoS 提供者特定的緩衝區中找到無法辨識的物件。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span><dl> <dt><strong>WSA_QOS_EPOLICYOBJ</strong></dt> <dt>11025</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_policy_object."></span><span id="invalid_qos_policy_object."></span><span id="INVALID_QOS_POLICY_OBJECT."></span>不正確 QoS 原則物件。</dt> <dd> 在 QoS 提供者特定的緩衝區中找到不正確原則物件。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span><dl> <dt><strong>WSA_QOS_EFLOWDESC</strong></dt> <dt>11026</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_flow_descriptor."></span><span id="invalid_qos_flow_descriptor."></span><span id="INVALID_QOS_FLOW_DESCRIPTOR."></span>QoS 流程描述項無效。</dt> <dd> 在流程描述項清單中找到不正確 QoS 流程描述項。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span><dl> <dt><strong>WSA_QOS_EPSFLOWSPEC</strong></dt> <dt>11027</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_flowspec."></span><span id="invalid_qos_provider-specific_flowspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FLOWSPEC."></span>QoS 提供者特定的 flowspec 無效。</dt> <dd> 在 QoS 提供者特定的緩衝區中找到無效或不一致的 flowspec。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span><dl> <dt><strong>WSA_QOS_EPSFILTERSPEC</strong></dt> <dt>11028</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_filterspec."></span><span id="invalid_qos_provider-specific_filterspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FILTERSPEC."></span>QoS 提供者特定的 filterspec 無效。</dt> <dd> 在 QoS 提供者特定的緩衝區中找到不正確 FILTERSPEC。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span><dl> <dt><strong>WSA_QOS_ESDMODEOBJ</strong></dt> <dt>11029</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shape_discard_mode_object."></span><span id="invalid_qos_shape_discard_mode_object."></span><span id="INVALID_QOS_SHAPE_DISCARD_MODE_OBJECT."></span>不正確 QoS 圖形捨棄模式物件。</dt> <dd> 在 QoS 提供者特定的緩衝區中找到不正確圖形捨棄模式物件。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span><dl> <dt><strong>WSA_QOS_ESHAPERATEOBJ</strong></dt> <dt>11030</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shaping_rate_object."></span><span id="invalid_qos_shaping_rate_object."></span><span id="INVALID_QOS_SHAPING_RATE_OBJECT."></span>不正確 QoS 成形率物件。</dt> <dd> 在 QoS 提供者特定的緩衝區中找到不正確成形率物件。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span><dl> <dt><strong>WSA_QOS_RESERVED_PETYPE</strong></dt> <dt>11031</dt> </dl></td>
<td><dl> <dt><span id="Reserved_policy_QoS_element_type."></span><span id="reserved_policy_qos_element_type."></span><span id="RESERVED_POLICY_QOS_ELEMENT_TYPE."></span>保留原則 QoS 元素類型。</dt> <dd> 在 QoS 提供者特定的緩衝區中找到保留的原則元素。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winsock2. h;</dt><dt>Winerror.h .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤碼-errno、h \_ errno 和 WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[處理 Winsock 錯誤](handling-winsock-errors.md)
</dt> <dt>

[**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
