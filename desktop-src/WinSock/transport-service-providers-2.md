---
description: 傳輸服務提供者和 Windows 通訊端 (Winsock) 。
ms.assetid: 4ded519d-d9c2-4ef3-80f5-e6ec40adf938
title: 傳輸服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114eefa67bbb2d7afdf46b74f1a9524e7a77b7c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985605"
---
# <a name="transport-service-providers"></a>傳輸服務提供者

指定的傳輸服務提供者支援一或多個通訊協定。 例如，TCP/IP 提供者會提供最少的 TCP 和 UDP 通訊協定，而 IPX/SPX 提供者可能會提供 IPX、SPX 和 SPX II。 特定提供者所支援的每個通訊協定都是由 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構所描述，而這類結構的總集合可視為已安裝之通訊協定的目錄。 應用程式可以取出此目錄的內容 (如需詳細資訊，請參閱 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)和 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)) ，以及藉由檢查可用的 **WSAPROTOCOL \_ 資訊** 結構，探索與每個通訊協定相關聯的通訊屬性。

## <a name="layered-protocols-and-protocol-chains-in-the-spi"></a>SPI 中的多層通訊協定和通訊協定鏈

Windows 通訊端2容納分層式通訊協定的概念。 分層式通訊協定是一種只會執行較高層級通訊函式的通訊協定，同時依賴于與遠端端點實際交換資料的基礎傳輸堆疊。 這類分層式通訊協定的其中一個範例就是安全性層級，將通訊協定新增至連線建立程式，以執行驗證並建立相互同意的加密配置。 這種安全性通訊協定通常需要基礎可靠傳輸通訊協定（例如 TCP 或 SPX）的服務。 「基本」（base protocol）一詞是指 TCP 或 SPX 這類通訊協定，其完全能夠執行與遠端端點的資料通訊，而「分層式通訊協定」一詞是用來描述無法獨立的通訊協定。 然後，通訊協定鏈會定義為一或多個階層式通訊協定總共串連在一起，並由基本通訊協定錨定。

您可以安排多層式通訊協定，以在其上和下邊緣支援 Winsock SPI，來完成此分層式通訊協定和基礎通訊協定的串連。 系統會建立一種特殊的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構，其會將整個通訊協定鏈視為整個通訊協定鏈，並說明多層式通訊協定聯結的明確順序。 下圖將說明這一點。

![通訊協定鏈](images/ovrvw2-3.png)

 

 
