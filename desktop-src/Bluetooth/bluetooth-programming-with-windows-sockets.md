---
title: 藍牙使用 Windows 通訊端進行程式設計
description: 本節說明如何使用 Windows 通訊端函式和結構來撰寫藍牙應用程式的程式。
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- 藍牙，工作
- Windows Sockets
- 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20cebe459f17601c1c0cbb916be8844b1edbf3b36f974b47ce0d9b28d301d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004088"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>藍牙使用 Windows 通訊端進行程式設計

本節說明如何使用 Windows 通訊端函式和結構來撰寫藍牙應用程式的程式。 Windows 通訊端 API 元素的完整參考資訊可在[Windows 通訊端](/windows/desktop/WinSock/windows-sockets-start-page-2)中找到;本節只提供每個 Windows 通訊端程式設計項目的藍牙特定資訊。

您也可以下載[藍牙的連接範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)，以取得完整的範例。

如同所有 Windows 通訊端應用程式程式設計一樣，必須呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)函式來起始 Windows 通訊端功能，並啟用藍牙。

下列主題提供搭配 Microsoft 藍牙 API 使用 Windows 通訊端函式和結構的指引：



| 主題                                                                                            | 描述                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [藍牙並接受](bluetooth-and-accept.md)                                                 | 藍牙使用 [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)函式來啟用通訊端上的連入連線嘗試。<br/>                                                                                                                                                                                                  |
| [藍牙和系結](bluetooth-and-bind.md)                                                     | 藍牙使用系 [**結函數系**](/windows/desktop/api/winsock/nf-winsock-bind)結至通訊端。<br/>                                                                                                                                                                                                                                     |
| [藍牙和 BLOB](bluetooth-and-blob.md)                                                     | 藍牙在呼叫 [**WSASetService**](bluetooth-and-wsasetservice.md)或 **WSALookupService** 函式期間，使用 [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)結構來傳遞或接收傳輸特定資料到 [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)結構 \* 。 <br/>             |
| [藍牙並連接](bluetooth-and-connect.md)                                               | 藍牙使用 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)函式連接到目標藍牙裝置，並使用先前建立的藍牙通訊端。<br/>                                                                                                                                                              |
| [藍牙和 getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | [**Getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)函式會提供從主機名稱到位址的轉換，以供以 IP 為基礎的傳輸。<br/>                                                                                                                                                                                   |
| [藍牙和 getpeername](bluetooth-and-getpeername.md)                                       | 用來取得對等藍牙裝置的藍牙位址。<br/>                                                                                                                                                                                                                                            |
| [藍牙和 getsockname](bluetooth-and-getsockname.md)                                       | 藍牙使用 [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)函式，透過先前對系結函 [**式的呼叫**](/windows/desktop/api/winsock/nf-winsock-bind)，來取得配置給通訊端的伺服器裝置位址和埠號碼。<br/>                                                                                            |
| [藍牙和 getsockopt](bluetooth-and-getsockopt.md)                                         | 藍牙使用 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)函數來查詢與伺服器通道或連接相關聯的各種參數。 <br/>                                                                                                                                                           |
| [藍牙並接聽、選取和導致 closesocket](bluetooth-and-listen-select-and-closesocket.md) | 藍牙使用 [[**接聽**](/windows/desktop/api/winsock2/nf-winsock2-listen)]、[[**選取**](/windows/desktop/api/winsock2/nf-winsock2-select)] 和 [[**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) ] 函式，而不需修改標準 Windows 通訊端程式設計。<br/>                                                                                                   |
| [藍牙和讀取或寫入作業](bluetooth-and-read-or-write-operations.md)             | 詳述支援的 Winsock 讀取和寫入作業。<br/>                                                                                                                                                                                                                                                        |
| [藍牙和 setsockopt](bluetooth-and-setsockopt.md)                                         | 藍牙使用 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)函數來設定與伺服器通道或連接相關聯的各種參數。<br/>                                                                                                                                                              |
| [藍牙和關機](bluetooth-and-shutdown.md)                                             | 藍牙使用 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)功能中斷與遠端無線電的連線。<br/>                                                                                                                                                                                                             |
| [藍牙和通訊端](bluetooth-and-socket.md)                                                 | 藍牙使用 [**通訊端**](/windows/desktop/api/winsock2/nf-winsock2-socket)函式來建立傳入或傳出連接的通訊端。<br/>                                                                                                                                                                                               |
| [藍牙和通訊端選項](bluetooth-and-socket-options.md)                                 | 詳細說明 Microsoft 藍牙所支援的通訊端選項。<br/>                                                                                                                                                                                                                                                    |
| [藍牙和 WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | 用來將藍牙的裝置位址轉換成字串，然後在抓取裝置服務資訊時，透過 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構提供給 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式。<br/>                                           |
| [藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | 藍牙使用 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函式來查詢裝置及探索服務。<br/>                                                                                                                                                                         |
| [藍牙和 WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | 藍牙使用 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)函式來比對 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)先前呼叫中所指定的查詢。<br/>                                                                                                           |
| [藍牙和 WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | 藍牙使用 [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)函式來終止先前呼叫 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)時起始的查詢，而且可能會在後續的 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)呼叫中延伸。<br/> |
| [藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構用於作業中，包括裝置查詢、服務查詢和設定服務。<br/>                                                                                                                                                                |
| [藍牙和 WSASetService](bluetooth-and-wsasetservice.md)                                   | 藍牙使用 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)函式，在藍牙命名空間內登錄或移除服務實例 (從登錄 NS \_ BTH) 。<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

