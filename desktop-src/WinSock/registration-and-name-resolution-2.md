---
description: Windows 通訊端2是一組功能，可將應用程式存取和使用各種網路命名服務的方式標準化。
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: 註冊和名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001692"
---
# <a name="registration-and-name-resolution"></a>註冊和名稱解析

Windows 通訊端2是一組功能，可將應用程式存取和使用各種網路命名服務的方式標準化。 使用這些功能時，應用程式不需要區分與名稱服務相關的廣泛不同通訊協定，例如 DNS、NIS、X. 500、SAP 等等。為了維持與 Windows 通訊端1.1 的完整回溯相容性，現有的 **getXbyY** 和非同步 **WSAAsyncGetXbyY** 資料庫查閱函數會繼續受到支援，但會根據新的名稱解析功能，在 Windows 通訊端服務提供者介面中執行。 如需詳細資訊，請參閱 [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) 和 [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) 函數。 此外，請參閱 [Windows 通訊端 1.1 SPI 中 tcp/ip 的相容名稱解析](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md)。

本節說明 Winsock 開發人員可用的註冊和名稱解析功能。 下列清單說明本節中的主題：

-   [通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)
-   [Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Winsock](about-winsock.md)
</dt> <dt>

[使用 Winsock](using-winsock.md)
</dt> </dl>

 

 



