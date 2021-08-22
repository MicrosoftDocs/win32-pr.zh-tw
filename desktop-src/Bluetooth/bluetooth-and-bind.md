---
title: 藍牙和系結
description: 藍牙使用系結函數系結至通訊端。
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- 藍牙
- 藍牙
- 藍牙和系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7e7571e8d8a2c1a6dee29dc5f4839af5f1064bc5351cd3a13937f5750dd04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588488"
---
# <a name="bluetooth-and-bind"></a>藍牙和系結

藍牙使用系 [**結函數系**](/windows/desktop/api/winsock/nf-winsock-bind)結至通訊端。 若要系結藍牙通訊端，請使用 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構來呼叫系 **結函數。** 使用 **SOCKADDR \_ BTH** 結構搭配下列設定：

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

在用戶端應用程式上，埠成員必須為零，才能讓指派適當的本機端點。 在伺服器應用程式上，埠成員必須是有效的埠號碼或 BT \_ 埠 \_ any; 使用 BT 埠自動指派的埠， \_ \_ 之後可能會透過呼叫 [**getsockname**](bluetooth-and-getsockname.md) 函式來進行查詢。 要求特定 RFCOMM 埠的有效範圍是1到30。 伺服器通道是全域資源，而且只有30個伺服器通道可供 RFCOMM 在任何藍牙裝置上，其必須由屬於藍牙位址家族的所有 Windows 通訊端共用。 如果沒有可用的伺服器通道，或指定的伺服器通道已經保留，系 [**結呼叫就**](/windows/desktop/api/winsock/nf-winsock-bind) 會失敗。

從 bind 成功傳回時，會保留伺服器通道，直到通訊端關閉為止。 使用 [**getsockname**](bluetooth-and-getsockname.md) 函式來取得 SDP 註冊的通道號碼。

應用程式應該使用伺服器通道的自動設定。

系 [](/windows/desktop/api/winsock/nf-winsock-bind)結函式不會使用藍牙 SDP 自動通告伺服器應用程式;應用程式必須呼叫 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)函數，以供遠端藍牙應用程式找到。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**綁定**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 