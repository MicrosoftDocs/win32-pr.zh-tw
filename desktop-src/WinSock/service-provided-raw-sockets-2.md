---
description: 原始通訊端是允許存取基礎傳輸提供者的通訊端類型。 不建議將應用程式移植到 Winsock 時使用原始通訊端的原因有好幾種。
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: 原始通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114908"
---
# <a name="raw-sockets"></a><span data-ttu-id="45175-104">原始通訊端</span><span class="sxs-lookup"><span data-stu-id="45175-104">Raw Sockets</span></span>

<span data-ttu-id="45175-105">原始通訊端是允許存取基礎傳輸提供者的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="45175-105">A raw socket is a type of socket that allows access to the underlying transport provider.</span></span> <span data-ttu-id="45175-106">不建議將應用程式移植到 Winsock 時使用原始通訊端的原因有好幾種。</span><span class="sxs-lookup"><span data-stu-id="45175-106">The use of raw sockets when porting applications to Winsock is not recommended for several reasons.</span></span>

<span data-ttu-id="45175-107">Windows 通訊端規格不會要求 Winsock 服務提供者支援原始通訊端，也就是 **SOCK \_ 原始** 類型的通訊端。</span><span class="sxs-lookup"><span data-stu-id="45175-107">The Windows Sockets specification does not mandate that a Winsock service provider support raw sockets, that is, sockets of type **SOCK\_RAW**.</span></span> <span data-ttu-id="45175-108">不過，建議服務提供者提供原始通訊端支援。</span><span class="sxs-lookup"><span data-stu-id="45175-108">However, service providers are encouraged to supply raw socket support.</span></span> <span data-ttu-id="45175-109">想要使用原始通訊端的 Windows 通訊端相容應用程式應該嘗試使用 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 呼叫來開啟通訊端，如果它失敗，請嘗試使用另一個通訊端類型或指出使用者失敗。</span><span class="sxs-lookup"><span data-stu-id="45175-109">A Windows Sockets-compliant application that wishes to use raw sockets should attempt to open the socket with the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call, and if it fails either attempt to use another socket type or indicate the failure to the user.</span></span>

<span data-ttu-id="45175-110">在 Windows 7、Windows Server 2008 R2、Windows Vista 和 Windows XP （含 Service Pack 2）上 (SP2) ，透過原始通訊端傳送流量的能力已受到數種限制。</span><span class="sxs-lookup"><span data-stu-id="45175-110">On Windows 7, Windows Server 2008 R2, Windows Vista, and Windows XP with Service Pack 2 (SP2), the ability to send traffic over raw sockets has been restricted in several ways.</span></span> <span data-ttu-id="45175-111">如需詳細資訊，請參閱 [Tcp/ip 原始通訊端](tcp-ip-raw-sockets-2.md)。</span><span class="sxs-lookup"><span data-stu-id="45175-111">For more information, see [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45175-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="45175-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45175-113">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="45175-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="45175-114">**插座**</span><span class="sxs-lookup"><span data-stu-id="45175-114">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="45175-115">TCP/IP 原始通訊端</span><span class="sxs-lookup"><span data-stu-id="45175-115">TCP/IP Raw Sockets</span></span>](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[<span data-ttu-id="45175-116">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="45175-116">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



