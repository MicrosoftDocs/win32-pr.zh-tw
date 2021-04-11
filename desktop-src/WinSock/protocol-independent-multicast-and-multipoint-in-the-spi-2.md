---
description: Windows 通訊端 (Winsock) 和通訊協定獨立的 multipoint 和多播功能。
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: 在 SPI 中 Protocol-Independent 多播和 Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115060"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a><span data-ttu-id="7a925-103">在 SPI 中 Protocol-Independent 多播和 Multipoint</span><span class="sxs-lookup"><span data-stu-id="7a925-103">Protocol-Independent Multicast and Multipoint in the SPI</span></span>

<span data-ttu-id="7a925-104">就像 Windows 通訊端2允許以一般方式存取許多傳輸通訊協定的基本資料傳輸功能一樣，它也提供了一般的方式來使用可執行這些功能之傳輸的 multipoint 和多播功能。</span><span class="sxs-lookup"><span data-stu-id="7a925-104">Just as Windows Sockets 2 allows the basic data transport capabilities of numerous transport protocols to be accessed in a generic manner, it also provides a generic way to use multipoint and multicast capabilities of transports that implement these features.</span></span> <span data-ttu-id="7a925-105">為了簡化，此處會使用 *multipoint* 這一詞來參考多播和 multipoint 通訊。</span><span class="sxs-lookup"><span data-stu-id="7a925-105">To simplify, the term *multipoint* is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="7a925-106">目前的 multipoint 執行 (例如，IP 多播、ST-II、T. 120、ATM 單向) 在節點加入 multipoint 會話的方式有很大的差異，不論特定節點是否指定為中央或根節點，以及資料是否要在所有節點之間交換，或只在根節點與不同分葉節點之間進行交換。</span><span class="sxs-lookup"><span data-stu-id="7a925-106">Current multipoint implementations (for example, IP multicast, ST-II, T.120, ATM UNI) vary widely with respect to how nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and various leaf nodes.</span></span> <span data-ttu-id="7a925-107">Windows 通訊端 2 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構是用來宣告通訊協定的 multipoint 屬性。</span><span class="sxs-lookup"><span data-stu-id="7a925-107">The Windows Sockets 2 [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure is used to declare the multipoint attributes of a protocol.</span></span> <span data-ttu-id="7a925-108">藉由檢查這些屬性，程式設計人員將知道使用適用的 Winsock 函式來設定、使用和卸載 multipoint 會話時應遵循的慣例。</span><span class="sxs-lookup"><span data-stu-id="7a925-108">By examining these attributes the programmer will know what conventions to follow in using the applicable Winsock functions to set up, use, and tear down multipoint sessions.</span></span>

<span data-ttu-id="7a925-109">支援多播的 Windows 通訊端2功能可摘要如下：</span><span class="sxs-lookup"><span data-stu-id="7a925-109">The features of Windows Sockets 2 that support multicast can be summarized as follows:</span></span>

-   <span data-ttu-id="7a925-110">[**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中有三個屬性位。</span><span class="sxs-lookup"><span data-stu-id="7a925-110">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="7a925-111">針對 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)的 *dwFlags* 參數定義的四個旗標</span><span class="sxs-lookup"><span data-stu-id="7a925-111">Four flags defined for the *dwFlags* parameter of [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span></span>
-   <span data-ttu-id="7a925-112">一個函式 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)，用於將分葉節點新增至 multipoint 會話。</span><span class="sxs-lookup"><span data-stu-id="7a925-112">One function, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="7a925-113">用於控制 multipoint 回送和建立多播傳輸範圍的兩個 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) 命令代碼。</span><span class="sxs-lookup"><span data-stu-id="7a925-113">Two [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="7a925-114"> (後者對應至 IP 多播的存留時間或 TTL 參數。 ) </span><span class="sxs-lookup"><span data-stu-id="7a925-114">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="7a925-115">在 Windows 通訊端2中包含這些 multipoint 功能，並不會妨礙服務提供者也支援現有的通訊協定相依介面，例如 IP 多播的 Deering 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="7a925-115">The inclusion of these multipoint features in Windows Sockets 2 does not preclude a service provider from also supporting an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

 

 
