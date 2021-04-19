---
description: 錯誤報表的配置與 SPI 和 API 介面不同。
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: 錯誤報表和參數驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970604"
---
# <a name="error-reporting-and-parameter-validation"></a><span data-ttu-id="69b5e-103">錯誤報表和參數驗證</span><span class="sxs-lookup"><span data-stu-id="69b5e-103">Error Reporting and Parameter Validation</span></span>

<span data-ttu-id="69b5e-104">錯誤報表的配置與 SPI 和 API 介面不同。</span><span class="sxs-lookup"><span data-stu-id="69b5e-104">The scheme for error reporting differs between the SPI and API interfaces.</span></span> <span data-ttu-id="69b5e-105">Windows 通訊端服務提供者會報告錯誤以及傳回的函式，而不是在 API 中使用的每個執行緒方法。</span><span class="sxs-lookup"><span data-stu-id="69b5e-105">Windows Sockets service providers report errors along with the function returning, as opposed to the per-thread based approach utilized in the API.</span></span> <span data-ttu-id="69b5e-106">Ws2 \_32.dll 會使用服務提供者的個別函式錯誤碼，來更新透過 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API 函式取得的每個執行緒錯誤值。</span><span class="sxs-lookup"><span data-stu-id="69b5e-106">The Ws2\_32.dll uses the service provider's per-function error code to update the per-thread error value that is obtained through the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API function.</span></span> <span data-ttu-id="69b5e-107">不過，仍需要服務提供者，才能維持以每一通訊端為基礎的錯誤，此錯誤可透過「 \_ 錯誤通訊端」選項來抓取。</span><span class="sxs-lookup"><span data-stu-id="69b5e-107">Service providers are still required, however, to maintain the per-socket based error which can be retrieved through the SO\_ERROR socket option.</span></span>

<span data-ttu-id="69b5e-108">Ws2 \_32.dll 只會在完全實作為其本身的函式呼叫上執行參數驗證。</span><span class="sxs-lookup"><span data-stu-id="69b5e-108">The Ws2\_32.dll performs parameter validation only on function calls that are implemented entirely within itself.</span></span> <span data-ttu-id="69b5e-109">服務提供者負責執行所有自己的參數驗證。</span><span class="sxs-lookup"><span data-stu-id="69b5e-109">Service providers are responsible for performing all of their own parameter validation.</span></span>

 

 



