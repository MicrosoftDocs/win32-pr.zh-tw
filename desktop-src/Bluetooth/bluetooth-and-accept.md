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
# <a name="bluetooth-and-accept"></a><span data-ttu-id="12eb6-107">藍牙和接受</span><span class="sxs-lookup"><span data-stu-id="12eb6-107">Bluetooth and accept</span></span>

<span data-ttu-id="12eb6-108">藍牙使用 [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) 函式來啟用通訊端上的連入連線嘗試。</span><span class="sxs-lookup"><span data-stu-id="12eb6-108">Bluetooth uses the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function to enable incoming connection attempts on a socket.</span></span> <span data-ttu-id="12eb6-109">\_用戶端應用程式的 BTH 位址是藉由讀取所傳回 [**sockaddr**](/windows/desktop/WinSock/sockaddr-2)結構的藍牙傳輸特定區段來取得。</span><span class="sxs-lookup"><span data-stu-id="12eb6-109">The BTH\_ADDR of the client application is obtained by reading the Bluetooth transport-specific section of the returned [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) structure.</span></span> <span data-ttu-id="12eb6-110">使用 **accept** 函數搭配藍牙的格式如下：</span><span class="sxs-lookup"><span data-stu-id="12eb6-110">Use of the **accept** function with Bluetooth has the following format:</span></span>

-   <span data-ttu-id="12eb6-111">[**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)函式的 *addr* 參數是緩衝區的選擇性指標，可接收通訊層已知的連接實體位址。</span><span class="sxs-lookup"><span data-stu-id="12eb6-111">The *addr* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to a buffer that receives the address of the connecting entity, as known to the communications layer.</span></span> <span data-ttu-id="12eb6-112">傳回具有遠端藍牙裝置位址之 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="12eb6-112">A pointer to a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure with the remote Bluetooth device address is returned.</span></span>
-   <span data-ttu-id="12eb6-113">[**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)函數的 *addrlen* 參數是包含長度（以位元組為單位）之整數的選擇性指標。整數必須大於或等於 **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)) 的值。</span><span class="sxs-lookup"><span data-stu-id="12eb6-113">The *addrlen* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to an integer that contains the length, in bytes, of addr. The integer must be greater or equal to the value of **sizeof** ([**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12eb6-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="12eb6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12eb6-115">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="12eb6-115">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="12eb6-116">**接受**</span><span class="sxs-lookup"><span data-stu-id="12eb6-116">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 