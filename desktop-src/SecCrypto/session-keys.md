---
description: 工作階段金鑰是為了在單一通訊會話中使用而產生的金鑰。
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: 工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981035"
---
# <a name="session-keys"></a><span data-ttu-id="e4a04-103">工作階段金鑰</span><span class="sxs-lookup"><span data-stu-id="e4a04-103">Session Keys</span></span>

<span data-ttu-id="e4a04-104">[*工作階段金鑰*](../secgloss/s-gly.md) 是為了在單一通訊會話中使用而產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e4a04-104">[*Session keys*](../secgloss/s-gly.md) are keys that are generated to be used in a single communication session.</span></span> <span data-ttu-id="e4a04-105">工作階段金鑰會經常變更，並在不再需要時捨棄。</span><span class="sxs-lookup"><span data-stu-id="e4a04-105">Session keys are frequently changed and are discarded when they are no longer needed.</span></span> <span data-ttu-id="e4a04-106">例如，TLS 針對每個連線使用不同的工作階段金鑰，而 S/MIME 針對每個電子郵件訊息使用個別的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="e4a04-106">For example, TLS uses a separate session key for each connection and S/MIME uses a separate session key for each email message.</span></span> <span data-ttu-id="e4a04-107">通常會使用 [*對稱金鑰*](../secgloss/s-gly.md) 做為工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="e4a04-107">Typically a [*symmetric key*](../secgloss/s-gly.md) is used as the session key.</span></span>

<span data-ttu-id="e4a04-108">工作階段金鑰是暫時性的。</span><span class="sxs-lookup"><span data-stu-id="e4a04-108">Session keys are volatile.</span></span> <span data-ttu-id="e4a04-109">應用程式可以儲存這些金鑰以供稍後使用，或傳輸給其他使用者。</span><span class="sxs-lookup"><span data-stu-id="e4a04-109">Applications can save these keys for later use or for transmission to other users.</span></span> <span data-ttu-id="e4a04-110">如需詳細資訊，請參閱 [密碼編譯金鑰儲存和交換](cryptographic-key-storage-and-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="e4a04-110">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md).</span></span>

 

 
