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
ms.openlocfilehash: 67891ccd65aaa56fc41dd077ae46bd4bf61f816cdc02afeb65964886cbaf9562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673128"
---
# <a name="ras_port_0-structure"></a>RAS \_ 埠 \_ 0 結構

\[Windows Vista 不支援這個版本的 **RAS \_ 埠 \_ 0** 結構。 請改用 mprapi 中定義的較新 [**RAS \_ 埠 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) 。\]

**Ras \_ 埠 \_ 0** 結構包含描述 RAS 埠的資訊。

## <a name="syntax"></a>語法


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



## <a name="members"></a>成員

<dl> <dt>

**wszPortName**
</dt> <dd>

以 null 結束的 Unicode 字串，指定埠的名稱，例如 "COM1"。

</dd> <dt>

**wszDeviceType**
</dt> <dd>

以 null 終止的 Unicode 字串，這個字串會指定建立連線的裝置類型，例如數據機或 ISDN。 可能在此成員中指定的裝置類型清單，包括安裝在伺服器上的所有裝置類型，包括協力廠商裝置。

</dd> <dt>

**wszDeviceName**
</dt> <dd>

以 null 終止的 Unicode 字串，這個字串會指定建立連接的裝置名稱，例如 "Hayes 9600" 或 "PCIMACISDN1"。

</dd> <dt>

**wszMediaName**
</dt> <dd>

指定以 null 終止的 Unicode 字串，這個字串會指定用於連接的媒體名稱，例如 *rasser* 或 *rastapi*。

</dd> <dt>

**保留**
</dt> <dd>

保留的。

</dd> <dt>

**旗標**
</dt> <dd>

指定一組位旗標，指定在此埠上進行之連接的本質。 這個成員可以是下列旗標的組合。



| 值                                                                                                                                                                        | 意義                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**閘道作用中 \_**</dt> </dl>             | 如果設定此旗標，則 NetBIOS 閘道會在伺服器上啟用。<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**\_存在 MESSENGER**</dt> </dl>    | 如果設定此旗標，則會在遠端用戶端上執行 messenger 服務。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**埠 \_ 多重連結**</dt> </dl>       | 如果設定此旗標，埠會與其他埠相互連結。 您可以使用此資訊，將線上狀態顯示為多重連結埠。 <br/> 若是多重連結埠， [**RAS \_ 埠 \_ 統計**](ras-port-statistics-str.md) 結構會包含兩組統計資料：一個用於埠，另一個用於多重連結連接中的合併埠。<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**PPP \_ 用戶端**</dt> </dl>                         | 如果設定此旗標，則會使用 PPP 連接遠端用戶端。 如果未設定此旗標，則會使用 AMB 通訊協定來連接遠端用戶端。<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**遠端 \_ 接聽**</dt> </dl>                | 如果設定此旗標，則會在伺服器上將 NetBIOS 閘道的 RemoteListen 參數設定為1。<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**使用者 \_ 驗證**</dt> </dl> | 如果設定此旗標，遠端用戶端就會連接到伺服器，且使用者已經過驗證。 檢查此旗標以確定用戶端實際上已連線到埠。<br/>                                                                                                                                                                                                   |



 

如果 MESSENGER \_ 存在、閘道作用 \_ 中和遠端 \_ 接聽旗標已設定，請使用 messenger 服務將系統管理訊息傳送至遠端用戶端。 如果 \_ 已設定 MESSENGER 且已 \_ 設定遠端接聽，但閘道為使用中，則 \_ 只會從用戶端連線到的 RAS 伺服器傳送訊息到用戶端。

</dd> <dt>

**wszUserName**
</dt> <dd>

以 null 結束的 Unicode 字串，指定連接至此埠的遠端使用者名稱。

</dd> <dt>

**wszComputer**
</dt> <dd>

以 null 結束的 Unicode 字串，指定遠端用戶端電腦的名稱。

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

指定用戶端在此埠上連線到 RAS 伺服器的時間，以秒為單位，從1970年1月1日開始。 使用標準時間函數來格式化此值以供顯示。

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

指定以 null 終止的 Unicode 字串，這個字串會指定遠端使用者已驗證之網域的名稱。 這個字串是唯一的功能變數名稱，沒有 " \\ \\ " 前置詞。

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

如果與此埠相關聯的 RAS 伺服器是 advanced server （例如 Windows 2000 advanced server），則指定非零的旗標。 您可以使用這項資訊來判斷具有使用者帳戶資料庫的伺服器名稱。 如果 RAS 伺服器是 advanced server，請將前置詞 " \\ \\ " 串連到 **wszLogonDomain** 成員所傳回的名稱，以取得使用者帳戶伺服器的名稱。 這是因為 advanced server 的本機登入功能變數名稱與伺服器名稱相同。 如果 RAS 伺服器是工作站，請使用 [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) 函數來取得使用者帳戶伺服器的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Rassapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端存取服務 (RAS) 總覽](about-remote-access-service.md)
</dt> <dt>

[RAS 伺服器管理結構](ras-server-administration-structures.md)
</dt> <dt>

[**RAS \_ 埠 \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**RAS \_ 埠 \_ 統計資料**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





