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
# <a name="renamed-functions"></a><span data-ttu-id="fe5ac-103">重新命名的函式</span><span class="sxs-lookup"><span data-stu-id="fe5ac-103">Renamed Functions</span></span>

<span data-ttu-id="fe5ac-104">在兩種情況下，您必須重新命名 Berkeley 通訊端中使用的函式，以避免與其他 Microsoft Windows API 函數發生衝突。</span><span class="sxs-lookup"><span data-stu-id="fe5ac-104">In two cases it was necessary to rename functions that are used in Berkeley Sockets in order to avoid clashes with other Microsoft Windows API functions.</span></span>

## <a name="close-and-closesocket"></a><span data-ttu-id="fe5ac-105">Close 和導致 closesocket</span><span class="sxs-lookup"><span data-stu-id="fe5ac-105">Close and Closesocket</span></span>

<span data-ttu-id="fe5ac-106">通訊端會以 Berkeley 通訊端中的標準檔案描述項表示，因此 **close** 函式可以用來關閉通訊端以及一般檔案。</span><span class="sxs-lookup"><span data-stu-id="fe5ac-106">Sockets are represented by standard file descriptors in Berkeley Sockets, so the **close** function can be used to close sockets as well as regular files.</span></span> <span data-ttu-id="fe5ac-107">雖然 Windows 通訊端中的任何專案都無法使用一般檔案控制代碼來識別通訊端，但任何專案都不需要。</span><span class="sxs-lookup"><span data-stu-id="fe5ac-107">While nothing in Windows Sockets prevents an implementation from using regular file handles to identify sockets, nothing requires it either.</span></span> <span data-ttu-id="fe5ac-108">在 Windows 上，必須使用 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 常式關閉通訊端。</span><span class="sxs-lookup"><span data-stu-id="fe5ac-108">On Windows, sockets must be closed by using the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) routine.</span></span> <span data-ttu-id="fe5ac-109">在 Windows 上，使用 **close** 函式關閉通訊端不正確，且此規格未定義執行此動作的效果。</span><span class="sxs-lookup"><span data-stu-id="fe5ac-109">ON Windows, using the **close** function to close a socket is incorrect and the effects of doing so are undefined by this specification.</span></span>

## <a name="ioctl-and-ioctlsocketwsaioctl"></a><span data-ttu-id="fe5ac-110">Ioctl 和 Ioctlsocket/WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="fe5ac-110">Ioctl and Ioctlsocket/WSAIoctl</span></span>

<span data-ttu-id="fe5ac-111">不同的 C 語言執行時間系統會使用 IOCTLs，用於與 Windows 通訊端無關的用途。</span><span class="sxs-lookup"><span data-stu-id="fe5ac-111">Various C language run-time systems use the IOCTLs for purposes unrelated to Windows Sockets.</span></span> <span data-ttu-id="fe5ac-112">因此， [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) 函式和 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式已定義為處理由 Berkeley Software 散發中的 **IOCTL** 和 **fcntl.h>** 所執行的通訊端函式。</span><span class="sxs-lookup"><span data-stu-id="fe5ac-112">As a consequence, the [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) function and the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function were defined to handle socket functions that were performed by **IOCTL** and **fcntl** in the Berkeley Software Distribution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe5ac-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe5ac-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe5ac-114">**導致 closesocket**</span><span class="sxs-lookup"><span data-stu-id="fe5ac-114">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="fe5ac-115">**ioctlsocket**</span><span class="sxs-lookup"><span data-stu-id="fe5ac-115">**ioctlsocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[<span data-ttu-id="fe5ac-116">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="fe5ac-116">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="fe5ac-117">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="fe5ac-117">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="fe5ac-118">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="fe5ac-118">**WSAIoctl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



