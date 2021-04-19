---
title: COM 和安全性封裝
description: Windows 支援 NTLMSSP (LAN Manager 安全性支援提供者) 、Kerberos v5 驗證通訊協定，以及安全通道安全性套件，可提供 PCT 1.0、SSL 2.0、SSL 3.0 和 TLS 1.0 通訊協定。
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968213"
---
# <a name="com-and-security-packages"></a><span data-ttu-id="af2d2-103">COM 和安全性封裝</span><span class="sxs-lookup"><span data-stu-id="af2d2-103">COM and Security Packages</span></span>

<span data-ttu-id="af2d2-104">Windows 支援 NTLMSSP (LAN Manager 安全性支援提供者) 、Kerberos v5 驗證通訊協定，以及安全通道安全性套件，可提供 PCT 1.0、SSL 2.0、SSL 3.0 和 TLS 1.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="af2d2-104">Windows supports NTLMSSP (LAN Manager Security Support Provider), the Kerberos v5 authentication protocol, and the Schannel security package, which provides the PCT 1.0, SSL 2.0, SSL 3.0, and TLS 1.0 protocols.</span></span> <span data-ttu-id="af2d2-105">此外，也支援使用 Snego 來檢查可用的安全性套件，並選取最適當的套件。</span><span class="sxs-lookup"><span data-stu-id="af2d2-105">Also supported is Snego, which checks for available security packages and selects the most appropriate one.</span></span>

<span data-ttu-id="af2d2-106">下表顯示各種安全性封裝所支援的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="af2d2-106">The following table shows the levels of authentication supported by the various security packages.</span></span>



| <span data-ttu-id="af2d2-107">伺服器/用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="af2d2-107">Server/Client Authentication</span></span>                                                                                           | <span data-ttu-id="af2d2-108">安全性套件支援</span><span class="sxs-lookup"><span data-stu-id="af2d2-108">Security Package Support</span></span>                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="af2d2-109">兩者都不能取得其他的名稱。</span><span class="sxs-lookup"><span data-stu-id="af2d2-109">Neither can get the name of the other.</span></span><br/>                                                                      | <span data-ttu-id="af2d2-110">無</span><span class="sxs-lookup"><span data-stu-id="af2d2-110">None</span></span><br/>                                                  |
| <span data-ttu-id="af2d2-111">用戶端可以驗證服務器，但不是反之亦然。</span><span class="sxs-lookup"><span data-stu-id="af2d2-111">The client can authenticate the server, but not vice versa.</span></span><br/>                                                 | <span data-ttu-id="af2d2-112">Schannel</span><span class="sxs-lookup"><span data-stu-id="af2d2-112">Schannel</span></span><br/>                                              |
| <span data-ttu-id="af2d2-113">用戶端無法探索伺服器，但是伺服器可以取得用戶端的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="af2d2-113">The client cannot discover the server, but the server can get the user ID of the client.</span></span><br/>                    | <span data-ttu-id="af2d2-114">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="af2d2-114">NTLMSSP</span></span><br/>                                               |
| <span data-ttu-id="af2d2-115">相互驗證：如果授與許可權，用戶端和伺服器都可以知道另一個的名稱。</span><span class="sxs-lookup"><span data-stu-id="af2d2-115">Mutual authentication: Both the client and server can know the name of the other, if permission is granted.</span></span><br/> | <span data-ttu-id="af2d2-116">NTLMSSP (本機) 、Kerberos v5 通訊協定和 Schannel</span><span class="sxs-lookup"><span data-stu-id="af2d2-116">NTLMSSP (locally), Kerberos v5 protocol, and Schannel</span></span><br/> |



 

<span data-ttu-id="af2d2-117">如需這些安全性封裝的詳細資訊，請參閱本節中的下列主題：</span><span class="sxs-lookup"><span data-stu-id="af2d2-117">For more information about these security packages, see the following topics in this section:</span></span>

-   [<span data-ttu-id="af2d2-118">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="af2d2-118">NTLMSSP</span></span>](ntlmssp.md)
-   [<span data-ttu-id="af2d2-119">Kerberos v5 通訊協定</span><span class="sxs-lookup"><span data-stu-id="af2d2-119">Kerberos v5 Protocol</span></span>](kerberos-v5-protocol.md)
-   [<span data-ttu-id="af2d2-120">頻道</span><span class="sxs-lookup"><span data-stu-id="af2d2-120">Schannel</span></span>](schannel.md)
-   [<span data-ttu-id="af2d2-121">Snego</span><span class="sxs-lookup"><span data-stu-id="af2d2-121">Snego</span></span>](snego.md)

## <a name="related-topics"></a><span data-ttu-id="af2d2-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="af2d2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2d2-123">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="af2d2-123">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 





