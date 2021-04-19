---
description: Windows 通訊端 2 (Winsock) SPI 中的服務安裝。
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Windows 通訊端 2 SPI 中的服務安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996677"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Windows 通訊端 2 SPI 中的服務安裝

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

當必要的服務類別不存在時，命名空間 SPI 用戶端會使用 [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) 來安裝新的服務類別，方法是提供服務類別名稱、服務類別識別碼的 GUID，以及一系列的 [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) 結構。 這些結構各自適用于特定的命名空間，並提供一般值，例如建議的 TCP 埠號碼或 NetWare SAP 識別碼。 您可以藉由呼叫 [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) 並提供對應至類別識別碼的 GUID，來移除服務類別。

服務類別存在之後，就可以透過 [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)安裝或移除服務的特定實例。 此函式會採用 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構做為輸入參數，以及作業程式碼和作業旗標。 作業程式碼會指出服務是否正在安裝或移除。 **WSAQUERYSET** 結構提供服務的所有相關資訊，包括服務類別識別碼、此實例的服務名稱 () 、適用的命名空間識別碼和通訊協定資訊，以及服務所接聽的一組傳輸位址。

 

 



