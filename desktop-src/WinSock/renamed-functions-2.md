---
description: 在兩種情況下，您必須重新命名 Berkeley 通訊端中使用的函式，以避免與其他 Microsoft Windows API 函數發生衝突。
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: 重新命名的函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848639"
---
# <a name="renamed-functions"></a>重新命名的函式

在兩種情況下，您必須重新命名 Berkeley 通訊端中使用的函式，以避免與其他 Microsoft Windows API 函數發生衝突。

## <a name="close-and-closesocket"></a>Close 和導致 closesocket

通訊端會以 Berkeley 通訊端中的標準檔案描述項表示，因此 **close** 函式可以用來關閉通訊端以及一般檔案。 雖然 Windows 通訊端中的任何專案都無法使用一般檔案控制代碼來識別通訊端，但任何專案都不需要。 在 Windows 上，必須使用 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 常式關閉通訊端。 在 Windows 上，使用 **close** 函式關閉通訊端不正確，且此規格未定義執行此動作的效果。

## <a name="ioctl-and-ioctlsocketwsaioctl"></a>Ioctl 和 Ioctlsocket/WSAIoctl

不同的 C 語言執行時間系統會使用 IOCTLs，用於與 Windows 通訊端無關的用途。 因此， [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) 函式和 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式已定義為處理由 Berkeley Software 散發中的 **IOCTL** 和 **fcntl.h>** 所執行的通訊端函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> <dt>

[**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



