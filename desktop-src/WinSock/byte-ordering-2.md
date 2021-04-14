---
description: 請務必務必將用來儲存整數的位元組順序和個別傳輸通訊協定在網路上使用的位元組順序之間的任何差異列入考慮。
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: 位元組順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469064"
---
# <a name="byte-ordering"></a><span data-ttu-id="8227b-103">位元組順序</span><span class="sxs-lookup"><span data-stu-id="8227b-103">Byte Ordering</span></span>

<span data-ttu-id="8227b-104">請務必務必將用來儲存整數的位元組順序和個別傳輸通訊協定在網路上使用的位元組順序之間的任何差異列入考慮。</span><span class="sxs-lookup"><span data-stu-id="8227b-104">Care must always be taken to account for any differences between the byte ordering used for storing integers by the host architecture and the byte ordering used on the wire by individual transport protocols.</span></span> <span data-ttu-id="8227b-105">任何對 Windows 通訊端常式傳遞或傳送的位址或埠號碼的參考，都必須以網路順序 (可供使用之通訊協定的位元組由大到小的) 。</span><span class="sxs-lookup"><span data-stu-id="8227b-105">Any reference to an address or port number passed to or from a Windows Sockets routine must be in the network order (big-endian) for the protocol being utilized.</span></span> <span data-ttu-id="8227b-106">在 IP 的案例中，這包括 [**sockaddr**](sockaddr-2.md) 結構的 ip 位址和埠參數 (但不是) 的 *sin \_ 系列* 參數。</span><span class="sxs-lookup"><span data-stu-id="8227b-106">In the case of IP, this includes the IP address and port parameters of a [**sockaddr**](sockaddr-2.md) structure (but not the *sin\_family* parameter).</span></span>

<span data-ttu-id="8227b-107">許多 UNIX 系統都是在 Cpu 上運作，以網路位元組順序表示整數 (位元組由大到小的) 。</span><span class="sxs-lookup"><span data-stu-id="8227b-107">A number of the UNIX systems operate on CPUs that represent integers in network byte order (big-endian).</span></span> <span data-ttu-id="8227b-108">因此，將整數從主機位元組順序轉換成網路位元組順序的需要略過，而不會造成問題，即使不建議對可攜性也是如此。</span><span class="sxs-lookup"><span data-stu-id="8227b-108">So the need to convert integers from host byte order to network byte order can be ignored without causing problems even if this is not recommended for portability.</span></span>

<span data-ttu-id="8227b-109">相反地，大部分 Intel® Cpu 用來表示整數的位元組順序是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="8227b-109">In contrast, the byte ordering used to represent integers by most Intel® CPUs is little-endian.</span></span> <span data-ttu-id="8227b-110">因此，從主機位元組順序轉換成網路位元組順序之前，必須先將整數轉換成網路位元組順序，然後才能在 Winsock 通訊端函數和結構中使用。</span><span class="sxs-lookup"><span data-stu-id="8227b-110">So it is becomes mandatory that integers be converted from host byte-order to network byte order before being used in Winsock Sockets functions and structures.</span></span>

<span data-ttu-id="8227b-111">假設應用程式通常會在與時間服務對應的 TCP 通訊埠上連線到伺服器，但提供了一種機制讓使用者指定替代埠。</span><span class="sxs-lookup"><span data-stu-id="8227b-111">Consider an application that normally contacts a server on the TCP port corresponding to the time service, but provides a mechanism for the user to specify an alternative port.</span></span> <span data-ttu-id="8227b-112">[**Getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)所傳回的埠號碼已是網路順序，這是用來建立位址以進行不需要轉譯的格式。</span><span class="sxs-lookup"><span data-stu-id="8227b-112">The port number returned by [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) is already in network order, which is the format required for constructing an address so that no translation is required.</span></span> <span data-ttu-id="8227b-113">不過，如果使用者想要使用不同的埠（輸入為整數），則應用程式必須在使用 [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) 或) [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) 函式之前，將它從主機轉換成 tcp/ip 網路順序 (，才能用來建立位址。</span><span class="sxs-lookup"><span data-stu-id="8227b-113">However, if the user elects to use a different port, entered as an integer, the application must convert this from host to TCP/IP network order (using the [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) or [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) function) before using it to construct an address.</span></span> <span data-ttu-id="8227b-114">相反地，如果應用程式要在 [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) 所傳回的位址 (（例如) ）中顯示埠號碼，則必須先使用 [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) 或 [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) 函式) 將埠號碼從網路轉換成主機順序 (，才能顯示該埠號碼。</span><span class="sxs-lookup"><span data-stu-id="8227b-114">Conversely, if the application were to display the number of the port within an address (returned by [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) for example), the port number must be converted from network to host order (using the [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) or [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) function) before it can be displayed.</span></span>

<span data-ttu-id="8227b-115">由於 Intel 和網際網路位元組的順序不同，因此上述的轉換是不可避免的。</span><span class="sxs-lookup"><span data-stu-id="8227b-115">Since the Intel and Internet byte orders are different, the conversions described in the preceding are unavoidable.</span></span> <span data-ttu-id="8227b-116">應用程式寫入器的匯，應該使用 Winsock 提供的標準轉換函式，而不是撰寫自己的轉換程式碼，因為未來的 Winsock 執行可能會在主機順序與網路位元組順序相同的系統上執行。</span><span class="sxs-lookup"><span data-stu-id="8227b-116">Application writers are cautioned that they should use the standard conversion functions provided as part of Winsock rather than writing their own conversion code since future implementations of Winsock are likely to run on systems for which the host order is identical to the network byte order.</span></span> <span data-ttu-id="8227b-117">只有在主機和網路位元組順序之間使用標準轉換函式的應用程式，才有可能是可移植的。</span><span class="sxs-lookup"><span data-stu-id="8227b-117">Only applications that use the standard conversion functions between host and network byte order are likely to be portable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8227b-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="8227b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8227b-119">**getpeername**</span><span class="sxs-lookup"><span data-stu-id="8227b-119">**getpeername**</span></span>](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[<span data-ttu-id="8227b-120">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="8227b-120">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[<span data-ttu-id="8227b-121">**htonl**</span><span class="sxs-lookup"><span data-stu-id="8227b-121">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="8227b-122">**htons**</span><span class="sxs-lookup"><span data-stu-id="8227b-122">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="8227b-123">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="8227b-123">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="8227b-124">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="8227b-124">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="8227b-125">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="8227b-125">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="8227b-126">**sockaddr**</span><span class="sxs-lookup"><span data-stu-id="8227b-126">**sockaddr**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="8227b-127">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="8227b-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="8227b-128">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="8227b-128">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="8227b-129">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="8227b-129">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="8227b-130">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="8227b-130">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="8227b-131">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="8227b-131">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



