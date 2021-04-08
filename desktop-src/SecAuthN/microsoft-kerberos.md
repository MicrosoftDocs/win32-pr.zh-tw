---
description: Kerberos 通訊協定會定義用戶端如何與網路驗證服務 \[ 平臺軟體發展工具組 (SDK) 互動 \] 。
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos (英文)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03787bcc65959838ea02c49958d9ca4e0405649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943370"
---
# <a name="microsoft-kerberos"></a><span data-ttu-id="718f4-103">Microsoft Kerberos (英文)</span><span class="sxs-lookup"><span data-stu-id="718f4-103">Microsoft Kerberos</span></span>

<span data-ttu-id="718f4-104">[*Kerberos 通訊協定*](../secgloss/k-gly.md)會定義用戶端與網路驗證服務的互動方式。</span><span class="sxs-lookup"><span data-stu-id="718f4-104">The [*Kerberos protocol*](../secgloss/k-gly.md) defines how clients interact with a network authentication service.</span></span> <span data-ttu-id="718f4-105">用戶端從 Kerberos 金鑰發佈中心 (KDC) 取得票證，並在建立連線時將這些票證呈交給伺服器。</span><span class="sxs-lookup"><span data-stu-id="718f4-105">Clients obtain tickets from the Kerberos Key Distribution Center (KDC), and they present these tickets to servers when connections are established.</span></span> <span data-ttu-id="718f4-106">Kerberos 票證代表用戶端的網路 [*認證*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="718f4-106">Kerberos tickets represent the client's network [*credentials*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="718f4-107">本節中的資訊提供在驗證程式中使用 Kerberos 通訊協定的理論背景。</span><span class="sxs-lookup"><span data-stu-id="718f4-107">Information in this section provides theoretical background on the use of the Kerberos protocol in an authentication process.</span></span> <span data-ttu-id="718f4-108">這是可讓開發人員瞭解在使用 Kerberos 第5版通訊協定的 SSPI 進程中幕後發生什麼事的背景資訊。</span><span class="sxs-lookup"><span data-stu-id="718f4-108">This is background information that can add to a developer's understanding of what is happening behind the scenes in an SSPI process that uses the Kerberos Version 5 protocol.</span></span>

<span data-ttu-id="718f4-109">Kerberos 驗證通訊協定會在建立安全的網路連接之前，提供實體之間的相互驗證機制。</span><span class="sxs-lookup"><span data-stu-id="718f4-109">The Kerberos authentication protocol provides a mechanism for mutual authentication between entities before a secure network connection is established.</span></span> <span data-ttu-id="718f4-110">在這整份檔中，這兩個實體稱為用戶端和伺服器，即使可以在伺服器之間建立安全的網路連接也是一樣。</span><span class="sxs-lookup"><span data-stu-id="718f4-110">Throughout this documentation, the two entities are called the client and the server even though secure network connections can be made between servers.</span></span> <span data-ttu-id="718f4-111">用戶端和伺服器也可以稱為 [*安全性主體*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="718f4-111">Both client and server can also be referred to as [*security principals*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="718f4-112">Kerberos 通訊協定會假設用戶端和伺服器之間的交易會在開啟的網路上進行，其中大部分的用戶端和許多伺服器並不安全，而且透過網路移動的封包也可以進行監視和修改。</span><span class="sxs-lookup"><span data-stu-id="718f4-112">The Kerberos protocol assumes that transactions between clients and servers take place on an open network where most clients and many servers are not physically secure, and packets traveling along the network can be monitored and modified at will.</span></span> <span data-ttu-id="718f4-113">假設的環境就像是現今的網際網路，攻擊者可以輕鬆地將它視為用戶端或伺服器，而且可以輕易竊聽或篡改合法用戶端與伺服器之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="718f4-113">The assumed environment is like today's Internet where an attacker can easily pose as either a client or a server, and can readily eavesdrop on or tamper with communications between legitimate clients and servers.</span></span>

<span data-ttu-id="718f4-114">本節提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="718f4-114">This section provides the following information:</span></span>

-   [<span data-ttu-id="718f4-115">基本驗證概念</span><span class="sxs-lookup"><span data-stu-id="718f4-115">Basic Authentication Concepts</span></span>](basic-authentication-concepts.md)
-   [<span data-ttu-id="718f4-116">Kerberos Subprotocols</span><span class="sxs-lookup"><span data-stu-id="718f4-116">Kerberos Subprotocols</span></span>](kerberos-subprotocols.md)
-   [<span data-ttu-id="718f4-117">Kerberos 模型</span><span class="sxs-lookup"><span data-stu-id="718f4-117">Kerberos Model</span></span>](kerberos-components.md)
-   [<span data-ttu-id="718f4-118">SSPI/Kerberos 與 GSSAPI 的互通性</span><span class="sxs-lookup"><span data-stu-id="718f4-118">SSPI/Kerberos Interoperability with GSSAPI</span></span>](sspi-kerberos-interoperability-with-gssapi.md)

<span data-ttu-id="718f4-119">您的應用程式不應直接存取 Kerberos [*安全性套件*](../secgloss/s-gly.md) ;相反地，它應該使用 [*Negotiate*](../secgloss/n-gly.md) 安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="718f4-119">Your application should not access the Kerberos [*security package*](../secgloss/s-gly.md) directly; instead, it should use the [*Negotiate*](../secgloss/n-gly.md) security package.</span></span> <span data-ttu-id="718f4-120">Negotiate 可讓您的應用程式利用更高階的 [*安全性通訊協定*](../secgloss/s-gly.md) （如果驗證所含的系統支援的話）。</span><span class="sxs-lookup"><span data-stu-id="718f4-120">Negotiate allows your application to take advantage of more advanced [*security protocols*](../secgloss/s-gly.md) if they are supported by the systems involved in the authentication.</span></span> <span data-ttu-id="718f4-121">目前，協商安全性封裝會在 [*Kerberos*](../secgloss/k-gly.md) 和 NTLM 之間進行選取。</span><span class="sxs-lookup"><span data-stu-id="718f4-121">Currently, the Negotiate security package selects between [*Kerberos*](../secgloss/k-gly.md) and NTLM.</span></span> <span data-ttu-id="718f4-122">除非其中一個與驗證相關的系統無法使用，否則 Negotiate 會選取 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="718f4-122">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication.</span></span>

 

 
