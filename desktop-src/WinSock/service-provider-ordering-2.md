---
description: 最初安裝傳輸服務提供者的順序，會控制在服務提供者介面上透過 WSCEnumProtocols 和 WSCEnumProtocols32 列舉的順序，或透過應用程式介面上的 WSAEnumProtocols 來進行列舉的順序。 更重要的是，當用戶端要求根據地址系列、類型和通訊協定識別碼建立通訊端時，此順序也會控制通訊協定和服務提供者的順序。
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: 服務提供者排序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848637"
---
# <a name="service-provider-ordering"></a><span data-ttu-id="78bf0-104">服務提供者排序</span><span class="sxs-lookup"><span data-stu-id="78bf0-104">Service Provider Ordering</span></span>

<span data-ttu-id="78bf0-105">最初安裝傳輸服務提供者的順序，會控制在服務提供者介面上透過 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) 和 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 列舉的順序，或透過應用程式介面上的 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 來進行列舉的順序。</span><span class="sxs-lookup"><span data-stu-id="78bf0-105">The order in which transport service providers are initially installed governs the order in which they are enumerated through [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) and [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) at the service provider interface, or through [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) at the application interface.</span></span> <span data-ttu-id="78bf0-106">更重要的是，當用戶端要求根據地址系列、類型和通訊協定識別碼建立通訊端時，此順序也會控制通訊協定和服務提供者的順序。</span><span class="sxs-lookup"><span data-stu-id="78bf0-106">More importantly, this order also governs the order in which protocols and service providers are considered when a client requests creation of a socket based on its address family, type, and protocol identifier.</span></span>

<span data-ttu-id="78bf0-107">Windows 通訊端2包含稱為 Sporder.exe 的小程式，可讓已安裝的通訊協定目錄在安裝通訊協定之後以互動方式重新排序。</span><span class="sxs-lookup"><span data-stu-id="78bf0-107">Windows Sockets 2 includes an applet called Sporder.exe that allows the catalog of installed protocols to be reordered interactively after protocols have already been installed.</span></span> <span data-ttu-id="78bf0-108">Winsock 也包含 Sporder.dll 的輔助 DLL，可匯出重新排列通訊協定的程式性介面。</span><span class="sxs-lookup"><span data-stu-id="78bf0-108">Winsock also includes an auxiliary DLL, Sporder.dll, that exports a procedural interface for reordering protocols.</span></span> <span data-ttu-id="78bf0-109">這個程式介面是由稱為 [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder)的單一程式所組成。</span><span class="sxs-lookup"><span data-stu-id="78bf0-109">This procedural interface consists of a single procedure called [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span></span>

<span data-ttu-id="78bf0-110">介面定義可以透過 include 檔 Sporder 匯入 C 或 c + + 程式。</span><span class="sxs-lookup"><span data-stu-id="78bf0-110">The interface definition may be imported into a C or C++ program by means of the include file Sporder.h.</span></span> <span data-ttu-id="78bf0-111">您可以使用 lib 檔案 Sporder 連結進入點。</span><span class="sxs-lookup"><span data-stu-id="78bf0-111">The entry point may be linked by means of the lib file Sporder.lib.</span></span>

 

 



