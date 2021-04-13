---
title: 'RAS_PORT_0 結構 (Rassapi .h) '
description: RAS \_ 埠 \_ 0 結構包含描述 RAS 埠的資訊。
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 結構 RAS
- PRAS_PORT_0 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508644"
---
# <a name="ras_port_0-structure"></a><span data-ttu-id="00194-105">RAS \_ 埠 \_ 0 結構</span><span class="sxs-lookup"><span data-stu-id="00194-105">RAS\_PORT\_0 structure</span></span>

<span data-ttu-id="00194-106">\[Windows Vista 不支援這個版本的 **RAS \_ 埠 \_ 0** 結構。</span><span class="sxs-lookup"><span data-stu-id="00194-106">\[This version of the **RAS\_PORT\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="00194-107">請改用 mprapi 中定義的較新 [**RAS \_ 埠 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) 。\]</span><span class="sxs-lookup"><span data-stu-id="00194-107">Use the newer [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="00194-108">**Ras \_ 埠 \_ 0** 結構包含描述 RAS 埠的資訊。</span><span class="sxs-lookup"><span data-stu-id="00194-108">The **RAS\_PORT\_0** structure contains information that describes a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="00194-109">語法</span><span class="sxs-lookup"><span data-stu-id="00194-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a><span data-ttu-id="00194-110">成員</span><span class="sxs-lookup"><span data-stu-id="00194-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="00194-111">**wszPortName**</span><span class="sxs-lookup"><span data-stu-id="00194-111">**wszPortName**</span></span>
</dt> <dd>

<span data-ttu-id="00194-112">以 null 結束的 Unicode 字串，指定埠的名稱，例如 "COM1"。</span><span class="sxs-lookup"><span data-stu-id="00194-112">A null-terminated Unicode string that specifies the name of the port, such as "COM1".</span></span>

</dd> <dt>

<span data-ttu-id="00194-113">**wszDeviceType**</span><span class="sxs-lookup"><span data-stu-id="00194-113">**wszDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="00194-114">以 null 終止的 Unicode 字串，這個字串會指定建立連線的裝置類型，例如數據機或 ISDN。</span><span class="sxs-lookup"><span data-stu-id="00194-114">A null-terminated Unicode string that specifies the type of the device on which the connection was made, such as Modem or ISDN.</span></span> <span data-ttu-id="00194-115">可能在此成員中指定的裝置類型清單，包括安裝在伺服器上的所有裝置類型，包括協力廠商裝置。</span><span class="sxs-lookup"><span data-stu-id="00194-115">The list of device types that might be specified in this member includes all the device types installed on the server, including third-party devices.</span></span>

</dd> <dt>

<span data-ttu-id="00194-116">**wszDeviceName**</span><span class="sxs-lookup"><span data-stu-id="00194-116">**wszDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="00194-117">以 null 終止的 Unicode 字串，這個字串會指定建立連接的裝置名稱，例如 "Hayes 9600" 或 "PCIMACISDN1"。</span><span class="sxs-lookup"><span data-stu-id="00194-117">A null-terminated Unicode string that specifies the name of the device on which the connection was made, such as "Hayes 9600" or "PCIMACISDN1".</span></span>

</dd> <dt>

<span data-ttu-id="00194-118">**wszMediaName**</span><span class="sxs-lookup"><span data-stu-id="00194-118">**wszMediaName**</span></span>
</dt> <dd>

<span data-ttu-id="00194-119">指定以 null 終止的 Unicode 字串，這個字串會指定用於連接的媒體名稱，例如 *rasser* 或 *rastapi*。</span><span class="sxs-lookup"><span data-stu-id="00194-119">Specifies a null-terminated Unicode string that specifies the name of the media used for the connection, such as *rasser* or *rastapi*.</span></span>

</dd> <dt>

<span data-ttu-id="00194-120">**保留**</span><span class="sxs-lookup"><span data-stu-id="00194-120">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="00194-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="00194-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="00194-122">**旗標**</span><span class="sxs-lookup"><span data-stu-id="00194-122">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="00194-123">指定一組位旗標，指定在此埠上進行之連接的本質。</span><span class="sxs-lookup"><span data-stu-id="00194-123">Specifies a set of bit flags that specify the nature of the connection made on this port.</span></span> <span data-ttu-id="00194-124">這個成員可以是下列旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="00194-124">This member can be a combination of the following flags.</span></span>



| <span data-ttu-id="00194-125">值</span><span class="sxs-lookup"><span data-stu-id="00194-125">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="00194-126">意義</span><span class="sxs-lookup"><span data-stu-id="00194-126">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <span data-ttu-id="00194-127"><dt>**閘道作用中 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="00194-127"><dt>**GATEWAY\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="00194-128">如果設定此旗標，則 NetBIOS 閘道會在伺服器上啟用。</span><span class="sxs-lookup"><span data-stu-id="00194-128">If this flag is set, the NetBIOS gateway is active on the server.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <span data-ttu-id="00194-129"><dt>**\_存在 MESSENGER**</dt></span><span class="sxs-lookup"><span data-stu-id="00194-129"><dt>**MESSENGER\_PRESENT**</dt></span></span> </dl>    | <span data-ttu-id="00194-130">如果設定此旗標，則會在遠端用戶端上執行 messenger 服務。</span><span class="sxs-lookup"><span data-stu-id="00194-130">If this flag is set, the messenger service is running on the remote client.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <span data-ttu-id="00194-131"><dt>**埠 \_ 多重連結**</dt></span><span class="sxs-lookup"><span data-stu-id="00194-131"><dt>**PORT\_MULTILINKED**</dt></span></span> </dl>       | <span data-ttu-id="00194-132">如果設定此旗標，埠會與其他埠相互連結。</span><span class="sxs-lookup"><span data-stu-id="00194-132">If this flag is set, the port is multilinked with other ports.</span></span> <span data-ttu-id="00194-133">您可以使用此資訊，將線上狀態顯示為多重連結埠。</span><span class="sxs-lookup"><span data-stu-id="00194-133">Use this information to display the connection status as a multilinked port.</span></span> <br/> <span data-ttu-id="00194-134">若是多重連結埠， [**RAS \_ 埠 \_ 統計**](ras-port-statistics-str.md) 結構會包含兩組統計資料：一個用於埠，另一個用於多重連結連接中的合併埠。</span><span class="sxs-lookup"><span data-stu-id="00194-134">For a multilinked port, the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure contains two sets of statistics: one for the port alone, and another for the combined ports in the multilink connection.</span></span><br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <span data-ttu-id="00194-135"><dt>**PPP \_ 用戶端**</dt></span><span class="sxs-lookup"><span data-stu-id="00194-135"><dt>**PPP\_CLIENT**</dt></span></span> </dl>                         | <span data-ttu-id="00194-136">如果設定此旗標，則會使用 PPP 連接遠端用戶端。</span><span class="sxs-lookup"><span data-stu-id="00194-136">If this flag is set, the remote client connected using PPP.</span></span> <span data-ttu-id="00194-137">如果未設定此旗標，則會使用 AMB 通訊協定來連接遠端用戶端。</span><span class="sxs-lookup"><span data-stu-id="00194-137">If this flag is not set, the remote client connected using the AMB protocol.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <span data-ttu-id="00194-138"><dt>**遠端 \_ 接聽**</dt></span><span class="sxs-lookup"><span data-stu-id="00194-138"><dt>**REMOTE\_LISTEN**</dt></span></span> </dl>                | <span data-ttu-id="00194-139">如果設定此旗標，則會在伺服器上將 NetBIOS 閘道的 RemoteListen 參數設定為1。</span><span class="sxs-lookup"><span data-stu-id="00194-139">If this flag is set, the RemoteListen parameter of the NetBIOS gateway is set to 1 on the server.</span></span><br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <span data-ttu-id="00194-140"><dt>**使用者 \_ 驗證**</dt></span><span class="sxs-lookup"><span data-stu-id="00194-140"><dt>**USER\_AUTHENTICATED**</dt></span></span> </dl> | <span data-ttu-id="00194-141">如果設定此旗標，遠端用戶端就會連接到伺服器，且使用者已經過驗證。</span><span class="sxs-lookup"><span data-stu-id="00194-141">If this flag is set, a remote client is connected to the server and the user has been authenticated.</span></span> <span data-ttu-id="00194-142">檢查此旗標以確定用戶端實際上已連線到埠。</span><span class="sxs-lookup"><span data-stu-id="00194-142">Check this flag to ensure that a client is actually connected to a port.</span></span><br/>                                                                                                                                                                                                   |



 

<span data-ttu-id="00194-143">如果 MESSENGER \_ 存在、閘道作用 \_ 中和遠端 \_ 接聽旗標已設定，請使用 messenger 服務將系統管理訊息傳送至遠端用戶端。</span><span class="sxs-lookup"><span data-stu-id="00194-143">If the MESSENGER\_PRESENT, GATEWAY\_ACTIVE, and REMOTE\_LISTEN flags are set, use the messenger service to send an administrative message to the remote client.</span></span> <span data-ttu-id="00194-144">如果 \_ 已設定 MESSENGER 且已 \_ 設定遠端接聽，但閘道為使用中，則 \_ 只會從用戶端連線到的 RAS 伺服器傳送訊息到用戶端。</span><span class="sxs-lookup"><span data-stu-id="00194-144">If MESSENGER\_PRESENT and REMOTE\_LISTEN are set, but GATEWAY\_ACTIVE is not, send messages to the client only from the RAS server to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="00194-145">**wszUserName**</span><span class="sxs-lookup"><span data-stu-id="00194-145">**wszUserName**</span></span>
</dt> <dd>

<span data-ttu-id="00194-146">以 null 結束的 Unicode 字串，指定連接至此埠的遠端使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="00194-146">A null-terminated Unicode string that specifies the name of the remote user connected to this port.</span></span>

</dd> <dt>

<span data-ttu-id="00194-147">**wszComputer**</span><span class="sxs-lookup"><span data-stu-id="00194-147">**wszComputer**</span></span>
</dt> <dd>

<span data-ttu-id="00194-148">以 null 結束的 Unicode 字串，指定遠端用戶端電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="00194-148">A null-terminated Unicode string that specifies the name of the remote client computer.</span></span>

</dd> <dt>

<span data-ttu-id="00194-149">**dwStartSessionTime**</span><span class="sxs-lookup"><span data-stu-id="00194-149">**dwStartSessionTime**</span></span>
</dt> <dd>

<span data-ttu-id="00194-150">指定用戶端在此埠上連線到 RAS 伺服器的時間，以秒為單位，從1970年1月1日開始。</span><span class="sxs-lookup"><span data-stu-id="00194-150">Specifies the time, in seconds from January 1, 1970, that the client connected to the RAS server on this port.</span></span> <span data-ttu-id="00194-151">使用標準時間函數來格式化此值以供顯示。</span><span class="sxs-lookup"><span data-stu-id="00194-151">Use the standard time functions to format this value for display.</span></span>

</dd> <dt>

<span data-ttu-id="00194-152">**wszLogonDomain**</span><span class="sxs-lookup"><span data-stu-id="00194-152">**wszLogonDomain**</span></span>
</dt> <dd>

<span data-ttu-id="00194-153">指定以 null 終止的 Unicode 字串，這個字串會指定遠端使用者已驗證之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="00194-153">Specifies a null-terminated Unicode string that specifies the name of the domain on which the remote user was authenticated.</span></span> <span data-ttu-id="00194-154">這個字串是唯一的功能變數名稱，沒有 " \\ \\ " 前置詞。</span><span class="sxs-lookup"><span data-stu-id="00194-154">This string is the domain name only, with no "\\\\" prefix.</span></span>

</dd> <dt>

<span data-ttu-id="00194-155">**fAdvancedServer**</span><span class="sxs-lookup"><span data-stu-id="00194-155">**fAdvancedServer**</span></span>
</dt> <dd>

<span data-ttu-id="00194-156">如果與此埠相關聯的 RAS 伺服器是 advanced server （例如 Windows 2000 Advanced Server），則指定非零的旗標。</span><span class="sxs-lookup"><span data-stu-id="00194-156">Specifies a flag that is nonzero if the RAS server associated with this port is an advanced server such as Windows 2000 Advanced Server.</span></span> <span data-ttu-id="00194-157">您可以使用這項資訊來判斷具有使用者帳戶資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="00194-157">Use this information to determine the name of the server that has the user account database.</span></span> <span data-ttu-id="00194-158">如果 RAS 伺服器是 advanced server，請將前置詞 " \\ \\ " 串連到 **wszLogonDomain** 成員所傳回的名稱，以取得使用者帳戶伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="00194-158">If the RAS server is an advanced server, get the name of the user account server by concatenating the prefix "\\\\" to the name returned in the **wszLogonDomain** member.</span></span> <span data-ttu-id="00194-159">這是因為 advanced server 的本機登入功能變數名稱與伺服器名稱相同。</span><span class="sxs-lookup"><span data-stu-id="00194-159">This is because for an advanced server the local logon domain name is the same as the server name.</span></span> <span data-ttu-id="00194-160">如果 RAS 伺服器是工作站，請使用 [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) 函數來取得使用者帳戶伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="00194-160">If the RAS server is a workstation, use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get the name of the user account server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00194-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="00194-161">Requirements</span></span>



| <span data-ttu-id="00194-162">需求</span><span class="sxs-lookup"><span data-stu-id="00194-162">Requirement</span></span> | <span data-ttu-id="00194-163">值</span><span class="sxs-lookup"><span data-stu-id="00194-163">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00194-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00194-164">Minimum supported client</span></span><br/> | <span data-ttu-id="00194-165">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00194-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="00194-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00194-166">Minimum supported server</span></span><br/> | <span data-ttu-id="00194-167">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00194-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="00194-168">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="00194-168">End of client support</span></span><br/>    | <span data-ttu-id="00194-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00194-169">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="00194-170">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="00194-170">End of server support</span></span><br/>    | <span data-ttu-id="00194-171">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00194-171">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="00194-172">標頭</span><span class="sxs-lookup"><span data-stu-id="00194-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="00194-173"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="00194-173"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00194-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00194-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00194-175">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="00194-175">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="00194-176">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="00194-176">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="00194-177">**RAS \_ 埠 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="00194-177">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="00194-178">**RAS \_ 埠 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="00194-178">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="00194-179">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="00194-179">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="00194-180">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="00194-180">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> </dl>

 

 





