---
description: 當 SSP/AP 安全性封裝作為驗證套件運作時，它會載入到本地安全機構 (LSA) 的進程空間中，並被視為在 LSA 模式中。
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: LSA 模式與使用者模式的比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027252"
---
# <a name="lsa-mode-vs-user-mode"></a><span data-ttu-id="5b863-103">LSA 模式與使用者模式的比較</span><span class="sxs-lookup"><span data-stu-id="5b863-103">LSA Mode vs. User Mode</span></span>

<span data-ttu-id="5b863-104">當 SSP/AP [*安全性封裝*](../secgloss/s-gly.md) 作為 [*驗證套件*](../secgloss/a-gly.md)運作時，它會載入到 [*本地安全機構*](../secgloss/l-gly.md) (lsa) 的進程空間中，並被視為在 lsa 模式中。</span><span class="sxs-lookup"><span data-stu-id="5b863-104">When an SSP/AP [*security package*](../secgloss/s-gly.md) is functioning as an [*authentication package*](../secgloss/a-gly.md), it is loaded into the process space of the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) and is said to be in LSA mode.</span></span> <span data-ttu-id="5b863-105">使用 [LSA 登入功能](authentication-functions.md)的登入應用程式存取驗證套件功能。</span><span class="sxs-lookup"><span data-stu-id="5b863-105">Logon applications access authentication package functionality using the [LSA Logon Functions](authentication-functions.md).</span></span> <span data-ttu-id="5b863-106">開發人員可以使用 LSA 支援函式，僅適用于 LSA 模式安全性封裝，以執行比先前支援更複雜的驗證套件。</span><span class="sxs-lookup"><span data-stu-id="5b863-106">Developers can use LSA support functions available only to LSA-mode security packages to implement more sophisticated authentication packages than previously supported.</span></span>

<span data-ttu-id="5b863-107">當 [*安全性封裝*](../secgloss/s-gly.md) 提供安全性服務給用戶端/伺服器應用程式時，它會載入至用戶端和伺服器進程，而且會被視為使用者模式。</span><span class="sxs-lookup"><span data-stu-id="5b863-107">When a [*security package*](../secgloss/s-gly.md) provides security services to a client/server application, it is loaded into the client and server processes and is said to be in user mode.</span></span> <span data-ttu-id="5b863-108">用戶端/伺服器應用程式會使用 Microsoft [*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 來存取安全性套件的安全性支援服務。</span><span class="sxs-lookup"><span data-stu-id="5b863-108">Client/server applications access the security package's security support services using Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).</span></span>

<span data-ttu-id="5b863-109">SSP/Ap 的 LSA 支援包含可讓安全性封裝的 LSA 模式和使用者模式實例用來進行通訊的功能。</span><span class="sxs-lookup"><span data-stu-id="5b863-109">LSA support for SSP/APs includes functions that the LSA-mode and user-mode instances of a security package can use to communicate.</span></span> <span data-ttu-id="5b863-110">此外，安全性封裝的使用者模式實例可以將所選要求的資訊委派給該封裝的 LSA 模式實例。</span><span class="sxs-lookup"><span data-stu-id="5b863-110">Additionally, the user-mode instance of a security package can delegate selected requests for information to the LSA-mode instance of the package.</span></span>

<span data-ttu-id="5b863-111">如需有關如何針對每個模式初始化安全性封裝的詳細資訊，請參閱 [LSA 模式初始化](lsa-mode-initialization.md) 和 [使用者模式初始化](user-mode-initialization.md)。</span><span class="sxs-lookup"><span data-stu-id="5b863-111">For details about how security packages are initialized for each mode, see [LSA-mode Initialization](lsa-mode-initialization.md) and [User-mode Initialization](user-mode-initialization.md).</span></span>

 

 
