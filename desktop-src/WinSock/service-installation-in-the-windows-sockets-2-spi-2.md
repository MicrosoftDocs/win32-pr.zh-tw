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
# <a name="service-installation-in-the-windows-sockets-2-spi"></a><span data-ttu-id="06bcf-103">Windows 通訊端 2 SPI 中的服務安裝</span><span class="sxs-lookup"><span data-stu-id="06bcf-103">Service Installation in the Windows Sockets 2 SPI</span></span>

-   [<span data-ttu-id="06bcf-104">**NSPInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="06bcf-104">**NSPInstallServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [<span data-ttu-id="06bcf-105">**NSPRemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="06bcf-105">**NSPRemoveServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [<span data-ttu-id="06bcf-106">**NSPSetService**</span><span class="sxs-lookup"><span data-stu-id="06bcf-106">**NSPSetService**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

<span data-ttu-id="06bcf-107">當必要的服務類別不存在時，命名空間 SPI 用戶端會使用 [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) 來安裝新的服務類別，方法是提供服務類別名稱、服務類別識別碼的 GUID，以及一系列的 [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) 結構。</span><span class="sxs-lookup"><span data-stu-id="06bcf-107">When the required service class does not already exist, a namespace SPI client uses [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="06bcf-108">這些結構各自適用于特定的命名空間，並提供一般值，例如建議的 TCP 埠號碼或 NetWare SAP 識別碼。</span><span class="sxs-lookup"><span data-stu-id="06bcf-108">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="06bcf-109">您可以藉由呼叫 [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) 並提供對應至類別識別碼的 GUID，來移除服務類別。</span><span class="sxs-lookup"><span data-stu-id="06bcf-109">A service class can be removed by calling [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="06bcf-110">服務類別存在之後，就可以透過 [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)安裝或移除服務的特定實例。</span><span class="sxs-lookup"><span data-stu-id="06bcf-110">Once a service class exists, specific instances of a service can be installed or removed via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span></span> <span data-ttu-id="06bcf-111">此函式會採用 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構做為輸入參數，以及作業程式碼和作業旗標。</span><span class="sxs-lookup"><span data-stu-id="06bcf-111">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="06bcf-112">作業程式碼會指出服務是否正在安裝或移除。</span><span class="sxs-lookup"><span data-stu-id="06bcf-112">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="06bcf-113">**WSAQUERYSET** 結構提供服務的所有相關資訊，包括服務類別識別碼、此實例的服務名稱 () 、適用的命名空間識別碼和通訊協定資訊，以及服務所接聽的一組傳輸位址。</span><span class="sxs-lookup"><span data-stu-id="06bcf-113">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses to which the service listens.</span></span>

 

 



