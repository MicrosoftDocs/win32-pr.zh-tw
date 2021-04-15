---
description: 主要金鑰是衍生其他金鑰的主要資料材質。
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: 建立主要金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511175"
---
# <a name="creating-the-master-key"></a><span data-ttu-id="68128-103">建立主要金鑰</span><span class="sxs-lookup"><span data-stu-id="68128-103">Creating the Master Key</span></span>

<span data-ttu-id="68128-104">[*主要金鑰*](../secgloss/m-gly.md)是衍生其他金鑰的主要資料材質。</span><span class="sxs-lookup"><span data-stu-id="68128-104">A [*master key*](../secgloss/m-gly.md) is key data material from which other keys are derived.</span></span> <span data-ttu-id="68128-105">根據所使用的通訊協定和加密套件，主要金鑰的長度可以是5到48個位元組。</span><span class="sxs-lookup"><span data-stu-id="68128-105">Depending on the protocol and cipher suite used, the master key can be from 5 to 48 bytes in length.</span></span> <span data-ttu-id="68128-106">針對 [*rsa*](../secgloss/r-gly.md)安全通道 / [](../secgloss/s-gly.md) CSP，主要金鑰是由用戶端所建立，並傳輸至 RSA 信封中的伺服器。</span><span class="sxs-lookup"><span data-stu-id="68128-106">For the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) CSP, the master key is created by the client-side and transferred to the server in an RSA envelope.</span></span> <span data-ttu-id="68128-107">若是 [*Diffie-hellman*](../secgloss/d-gly.md)/Schannel CSP，主要金鑰是藉由執行 Diffie-Hellman 金鑰交換來建立。</span><span class="sxs-lookup"><span data-stu-id="68128-107">For a [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel CSP, the master key is created by performing a Diffie-Hellman key exchange.</span></span>

<span data-ttu-id="68128-108">以下示範建立和交換主要金鑰的程式碼：</span><span class="sxs-lookup"><span data-stu-id="68128-108">Code for creating and exchanging master keys is demonstrated in:</span></span>

-   [<span data-ttu-id="68128-109">用來建立主要金鑰的 diffie-hellman 用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="68128-109">Diffie-Hellman Client Code for Creating the Master Key</span></span>](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="68128-110">建立主要金鑰的 diffie-hellman 伺服器程式碼</span><span class="sxs-lookup"><span data-stu-id="68128-110">Diffie-Hellman Server Code for Creating the Master Key</span></span>](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="68128-111">用來建立主要金鑰的 RSA 用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="68128-111">RSA Client Code for Creating the Master Key</span></span>](rsa-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="68128-112">用來建立主要金鑰的 RSA 伺服器程式碼</span><span class="sxs-lookup"><span data-stu-id="68128-112">RSA Server Code for Creating the Master Key</span></span>](rsa-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="68128-113">指定演算法</span><span class="sxs-lookup"><span data-stu-id="68128-113">Specifying the Algorithms</span></span>](specifying-the-algorithms.md)

 

 
