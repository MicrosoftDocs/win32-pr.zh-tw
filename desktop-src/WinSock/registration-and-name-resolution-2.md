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
# <a name="registration-and-name-resolution"></a><span data-ttu-id="fa0d4-103">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="fa0d4-103">Registration and Name Resolution</span></span>

<span data-ttu-id="fa0d4-104">Windows 通訊端2是一組功能，可將應用程式存取和使用各種網路命名服務的方式標準化。</span><span class="sxs-lookup"><span data-stu-id="fa0d4-104">Windows Sockets 2 is a set of functions that standardizes the way applications access and use the various network naming services.</span></span> <span data-ttu-id="fa0d4-105">使用這些功能時，應用程式不需要區分與名稱服務相關的廣泛不同通訊協定，例如 DNS、NIS、X. 500、SAP 等等。為了維持與 Windows 通訊端1.1 的完整回溯相容性，現有的 **getXbyY** 和非同步 **WSAAsyncGetXbyY** 資料庫查閱函數會繼續受到支援，但會根據新的名稱解析功能，在 Windows 通訊端服務提供者介面中執行。</span><span class="sxs-lookup"><span data-stu-id="fa0d4-105">When using these functions, applications need not distinguish the widely differing protocols associated with name services such as DNS, NIS, X.500, SAP, etc. To maintain full backward compatibility with Windows Sockets 1.1, the existing **getXbyY** and asynchronous **WSAAsyncGetXbyY** database-lookup functions continue to be supported, but are implemented in the Windows Sockets service provider interface in terms of the new name resolution capabilities.</span></span> <span data-ttu-id="fa0d4-106">如需詳細資訊，請參閱 [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) 和 [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) 函數。</span><span class="sxs-lookup"><span data-stu-id="fa0d4-106">For more information, see the [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions.</span></span> <span data-ttu-id="fa0d4-107">此外，請參閱 [Windows 通訊端 1.1 SPI 中 tcp/ip 的相容名稱解析](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md)。</span><span class="sxs-lookup"><span data-stu-id="fa0d4-107">Also, see [Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span></span>

<span data-ttu-id="fa0d4-108">本節說明 Winsock 開發人員可用的註冊和名稱解析功能。</span><span class="sxs-lookup"><span data-stu-id="fa0d4-108">This section describes registration and name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="fa0d4-109">下列清單說明本節中的主題：</span><span class="sxs-lookup"><span data-stu-id="fa0d4-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="fa0d4-110">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="fa0d4-110">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
-   [<span data-ttu-id="fa0d4-111">Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析</span><span class="sxs-lookup"><span data-stu-id="fa0d4-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="fa0d4-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa0d4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa0d4-113">關於 Winsock</span><span class="sxs-lookup"><span data-stu-id="fa0d4-113">About Winsock</span></span>](about-winsock.md)
</dt> <dt>

[<span data-ttu-id="fa0d4-114">使用 Winsock</span><span class="sxs-lookup"><span data-stu-id="fa0d4-114">Using Winsock</span></span>](using-winsock.md)
</dt> </dl>

 

 



