---
description: 下表說明適用于 \_ 針對 appletalk 位址系列 (AF appletalk) 所建立之通訊端的 SOL APPLETALK 通訊端選項 \_ 。
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: 'SOL_APPLETALK 通訊端選項 (Atalkwsh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SOL_APPLETALK
- Windows
api_type:
- HeaderDef
api_location:
- Atalkwsh.h
ms.openlocfilehash: 5ea45b4007a3bd36d2cfbceda5b7ec4f2cff20d9bb2387fb2d184710a8a4492c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740005"
---
# <a name="sol_appletalk-socket-options"></a>SOL \_ APPLETALK 通訊端選項

下表說明適用于針對 AppleTalk 位址系列 (AF appletalk) 所建立之通訊端的 **SOL \_ APPLETALK** 通訊端選項 \_ 。 如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數參考頁面。

若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**SOL \_ APPLETALK 通訊端選項**</dt> <dd> <dl> <dt> 

| 選項                          | Get | 集合 | Optval 類型                          | 描述                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_確認 \_ 名稱               | 是 |     | **WSH \_ NBP \_ 元組**                  | 確認指定的 AppleTalk 名稱已系結至指定的位址。                                                                                                                                  |
| 所以取消 \_ 註冊 \_ 名稱            |     | 是 | **WSH \_ 註冊 \_ 名稱**              | 從網路取消註冊名稱。                                                                                                                                                               |
| \_GETLOCALZONES               | 是 |     | **WSH \_ 查閱 \_ 區域**               | 傳回指定介面卡名稱已知的區功能變數名稱稱清單。                                                                                                                                        |
| \_GETMYZONE                   | 是 |     | 字元 \[\]                            | 傳回網路上的預設區域。                                                                                                                                                             |
| \_GETNETINFO                  | 是 |     | **\_ \_ \_ 在 \_ 介面卡上 NETDEF WSH 查閱** | 傳回網路的植入值以及預設區域。 *Optlen* 參數必須至少有一個位元組大於在 **\_ \_ \_ \_ 介面卡結構上的 WSH LOOKUP NETDEF** 大小。  |
| \_GETZONELIST                 | 是 |     | **WSH \_ 查閱 \_ 區域**               | 從網際網路區域清單傳回區功能變數名稱稱。 *Optlen* 參數必須至少有一個位元組大於 **WSH \_ 查閱 \_ 區域** 結構的大小。                                       |
| \_LOOKUP \_ MYZONE              | 是 |     |                                      | 與 GETMYZONE 相同 \_                                                                                                                                                                                |
| \_查詢 \_ 名稱                | 是 |     | **WSH \_ 查閱 \_ 名稱**                | 查閱指定的 NBP 名稱，並傳回相符的名稱和 NBP 資訊元組。 *Optlen* 參數必須至少有一個位元組大於 WSH \_ 查閱 \_ 名稱結構的大小。 |
| \_ \_ \_ 在 \_ 介面卡上查閱 NETDEF | 是 |     | **\_ \_ \_ 在 \_ 介面卡上 NETDEF WSH 查閱** | 與 GETNETINFO 相同 \_ 。                                                                                                                                                                              |
| \_查找 \_ 區域               | 是 |     | **WSH \_ 查閱 \_ 區域**               | 與 GETZONELIST 相同 \_ 。                                                                                                                                                                             |
| \_ \_ \_ 在 \_ 介面卡上查找區域  | 是 |     | **WSH \_ 查閱 \_ 區域**               | 與 GETLOCALZONES 相同 \_ 。                                                                                                                                                                           |
| 所以 \_ PAP \_ 取得 \_ 伺服器 \_ 狀態    | 是 |     | **WSH \_ PAP \_ 取得 \_ 伺服器 \_ 狀態**    | 傳回指定伺服器的 PAP 狀態                                                                                                                                                           |
| 所以 \_ PAP \_ 質數 \_ READ            |     | 是 | 字元 \[\]                            | 此呼叫會質數 PAP 連接上的讀取，讓傳送者可以開始傳送資料                                                                                                                 |
| 所以 \_ PAP \_ 設定 \_ 伺服器 \_ 狀態    |     | 是 | 字元 \[\]                            | 設定當其他用戶端要求狀態時要傳送的狀態                                                                                                                                     |
| \_註冊 \_ 名稱              |     | 是 | **WSH \_ 註冊 \_ 名稱**              | 在 AppleTalk 網路上註冊指定的名稱                                                                                                                                                    |
| \_移除 \_ 名稱                |     | 是 | **WSH \_ 註冊 \_ 名稱**              | 與取消 \_ 註冊 \_ 名稱相同                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Windows支援 SOL \_ APPLETALK 選項**</dt> <dd> <dl> <dt> 

| 選項                          | WindowsVista 和更新版本 | Windows Server 2003 | Windows XP | Windows 2000 | WindowsNT4 | Windows 9x/我 |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| \_確認 \_ 名稱               |                         | x                   | x          | x            | x           |               |
| 所以取消 \_ 註冊 \_ 名稱            |                         | x                   | x          | x            | x           |               |
| \_GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| \_GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| \_GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| \_GETZONELIST                 |                         | x                   | x          | x            | x           |               |
| \_LOOKUP \_ MYZONE              |                         | x                   | x          | x            | x           |               |
| \_查詢 \_ 名稱                |                         | x                   | x          | x            | x           |               |
| \_ \_ \_ 在 \_ 介面卡上查閱 NETDEF |                         | x                   | x          | x            | x           |               |
| \_查找 \_ 區域               |                         | x                   | x          | x            | x           |               |
| \_ \_ \_ 在 \_ 介面卡上查找區域  |                         | x                   | x          | x            | x           |               |
| 所以 \_ PAP \_ 取得 \_ 伺服器 \_ 狀態    |                         | x                   | x          | x            | x           |               |
| 所以 \_ PAP \_ 質數 \_ READ            |                         | x                   | x          | x            | x           |               |
| 所以 \_ PAP \_ 設定 \_ 伺服器 \_ 狀態    |                         | x                   | x          | x            | x           |               |
| \_註冊 \_ 名稱              |                         | x                   | x          | x            | x           |               |
| \_移除 \_ 名稱                |                         | x                   | x          | x            | x           |               |



 

只有 Windows 2000 和 Windows NT 4.0 的伺服器版本才支援 **SOL \_ APPLETALK** 選項。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

**SOL \_ APPLETALK** 通訊端選項以及這些通訊端選項所使用的結構會定義在 *Atalkwsh .h* 標頭檔中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Atalkwsh。h</dt> </dl> |



 

 




