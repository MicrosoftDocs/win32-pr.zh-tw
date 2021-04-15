---
description: Windows 通訊端2不會假設所有通訊協定的網路位元組順序都相同。
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: 擴充 Byte-Order 轉換常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511449"
---
# <a name="extended-byte-order-conversion-routines"></a><span data-ttu-id="6eae6-103">擴充 Byte-Order 轉換常式</span><span class="sxs-lookup"><span data-stu-id="6eae6-103">Extended Byte-Order Conversion Routines</span></span>

<span data-ttu-id="6eae6-104">Windows 通訊端2不會假設所有通訊協定的網路位元組順序都相同。</span><span class="sxs-lookup"><span data-stu-id="6eae6-104">Windows Sockets 2 does not assume that the network byte order for all protocols is the same.</span></span> <span data-ttu-id="6eae6-105">提供一組轉換常式，以將16位和32位的數量轉換成網路位元組順序。</span><span class="sxs-lookup"><span data-stu-id="6eae6-105">A set of conversion routines is supplied for converting 16-bit and 32-bit quantities to and from network byte order.</span></span> <span data-ttu-id="6eae6-106">這些常式會以具有與其相關聯之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構的通訊端控制碼作為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="6eae6-106">These routines take as an input parameter the socket handle that has a [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure associated with it.</span></span> <span data-ttu-id="6eae6-107">**WSAPROTOCOL \_ 資訊** 結構的 **NetworkByteOrder** 成員會指定所需的網路位元組順序 (目前是位元組由大到小或由小到大的) 。</span><span class="sxs-lookup"><span data-stu-id="6eae6-107">The **NetworkByteOrder** member of the **WSAPROTOCOL\_INFO** structure specifies the desired network byte order (currently either big-endian or little-endian).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6eae6-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="6eae6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eae6-109">**htonl**</span><span class="sxs-lookup"><span data-stu-id="6eae6-109">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="6eae6-110">**htons**</span><span class="sxs-lookup"><span data-stu-id="6eae6-110">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="6eae6-111">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="6eae6-111">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="6eae6-112">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="6eae6-112">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="6eae6-113">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="6eae6-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="6eae6-114">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="6eae6-114">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="6eae6-115">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="6eae6-115">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="6eae6-116">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="6eae6-116">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="6eae6-117">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="6eae6-117">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="6eae6-118">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="6eae6-118">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[<span data-ttu-id="6eae6-119">**WSAPROTOCOL \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6eae6-119">**WSAPROTOCOL\_INFO**</span></span>](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
