---
title: 藍牙和接受
description: 藍牙使用 accept 函式來啟用通訊端上的連入連線嘗試。
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accept
- Bluetooth
- Bluetooth
- 藍牙和接受
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966053"
---
# <a name="bluetooth-and-accept"></a>藍牙和接受

藍牙使用 [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) 函式來啟用通訊端上的連入連線嘗試。 \_用戶端應用程式的 BTH 位址是藉由讀取所傳回 [**sockaddr**](/windows/desktop/WinSock/sockaddr-2)結構的藍牙傳輸特定區段來取得。 使用 **accept** 函數搭配藍牙的格式如下：

-   [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)函式的 *addr* 參數是緩衝區的選擇性指標，可接收通訊層已知的連接實體位址。 傳回具有遠端藍牙裝置位址之 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) 結構的指標。
-   [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)函數的 *addrlen* 參數是包含長度（以位元組為單位）之整數的選擇性指標。整數必須大於或等於 **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)) 的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**接受**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 