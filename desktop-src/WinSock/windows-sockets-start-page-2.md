---
description: Windows 通訊端 2 (Winsock) 可讓程式設計人員建立先進的網際網路、內部網路和其他具備網路功能的應用程式，以在網路上傳輸應用程式資料，而不受使用的網路通訊協定影響。
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows 通訊端2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114293"
---
# <a name="windows-sockets-2"></a>Windows 通訊端2

## <a name="purpose"></a>目的

Windows 通訊端 2 (Winsock) 可讓程式設計人員建立先進的網際網路、內部網路和其他具備網路功能的應用程式，以在網路上傳輸應用程式資料，而不受使用的網路通訊協定影響。 有了 Winsock，程式設計人員就可以存取 advanced Microsoft® Windows®的網路功能，例如多播和服務品質 (QoS) 。

Winsock 遵循 Windows Open System 架構 (WOSA) 模型;它會定義應用程式開發介面 (API) 之間的標準服務提供者介面 (SPI) ，以及其匯出的函式和通訊協定堆疊。 它會使用第一次由 Berkeley Software 散發 (BSD) UNIX 所普及化的通訊端範例。 它稍後是針對 windows 通訊端1.1 中的 Windows 進行調整，Windows 通訊端2應用程式可回溯相容。 Winsock 程式設計之前是以 TCP/IP 為中心。 某些搭配 TCP/IP 使用的程式設計實務無法用於每個通訊協定。 因此，Windows 通訊端 2 API 會在需要處理數個通訊協定的情況下新增函式。

## <a name="developer-audience"></a>開發人員對象

Windows 通訊端2是設計來供 C/c + + 程式設計人員使用。 需要熟悉 Windows 網路功能。

## <a name="run-time-requirements"></a>執行階段需求求

Windows 通訊端2可以在所有 Windows 平臺上使用。 當 Windows 通訊端2平臺限制的特定執行或功能存在時，就會在檔中清楚注明它們。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                             | 描述                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows 通訊端的新功能](what-s-new-for-windows-sockets-2.md)<br/>                 | Windows 通訊端新功能的相關資訊。<br/>                                                                                                                                                                                                                                 |
| [Windows 中的 Winsock 網路通訊協定支援](network-protocol-support-in-windows.md)<br/> | 不同 Windows 通訊端在不同版本的 Windows 上的網路通訊協定支援的相關資訊。<br/>                                                                                                                                                                                    |
| [關於 Winsock](about-winsock.md)<br/>                                                     | 適用于開發人員的 Windows 通訊端程式設計考慮、架構和功能的一般資訊。<br/>                                                                                                                                                       |
| [使用 Winsock](using-winsock.md)<br/>                                                     | 搭配 Windows 通訊端使用的程式和程式設計技術。 本節包含基本的 Winsock 程式設計技術，例如 [使用 winsock 開始使用](getting-started-with-winsock.md)，以及適用于有經驗的 winsock 開發人員的先進技術。<br/> |
| [Winsock 參考](winsock-reference.md)<br/>                                             | Windows 通訊端 API 的檔。<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IP 協助程式](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[服務品質](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
