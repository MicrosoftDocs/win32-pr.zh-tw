---
description: 許多形式的驗證都是以實體可證明其身分識別的概念為基礎，如果它可以證明它知道只有它知道的金鑰（例如密碼）。
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: 金鑰驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193084"
---
# <a name="key-authentication"></a><span data-ttu-id="24b4e-103">金鑰驗證</span><span class="sxs-lookup"><span data-stu-id="24b4e-103">Key Authentication</span></span>

<span data-ttu-id="24b4e-104">許多形式的驗證都是以實體可證明其身分識別的概念為基礎，如果它可以證明它知道只有它知道的金鑰（例如密碼）。</span><span class="sxs-lookup"><span data-stu-id="24b4e-104">Many forms of authentication are based on the idea that an entity can prove its identity if it can prove it knows a key, such as a password, that only it can know.</span></span>

<span data-ttu-id="24b4e-105">依賴秘密的驗證技術（例如密碼）必須要有一種方法來防止秘密成為公開知識。</span><span class="sxs-lookup"><span data-stu-id="24b4e-105">Authentication techniques that rely on a secret, such as a password, need to have a way to keep the secret from becoming public knowledge.</span></span> <span data-ttu-id="24b4e-106">密碼擁有者無法向上移至大門並提供密碼。</span><span class="sxs-lookup"><span data-stu-id="24b4e-106">A password owner cannot walk up to a door and give the password.</span></span> <span data-ttu-id="24b4e-107">Doorkeeper 以外的人可能正在接聽;或者它可能是錯誤的門。</span><span class="sxs-lookup"><span data-stu-id="24b4e-107">Someone besides the doorkeeper might be listening; or it might be the wrong door.</span></span> <span data-ttu-id="24b4e-108">為了保留秘密，必須有方法證明使用者知道密碼，而不會洩漏密碼。</span><span class="sxs-lookup"><span data-stu-id="24b4e-108">In order to keep a secret, there must be a way to prove a user knows the password without revealing the password.</span></span> <span data-ttu-id="24b4e-109">這是秘密金鑰驗證背後的概念，也就是在 [*Kerberos 通訊協定*](../secgloss/k-gly.md)中使用的一種驗證方法。</span><span class="sxs-lookup"><span data-stu-id="24b4e-109">That is the idea behind secret key authentication, a method of verification used throughout the [*Kerberos protocol*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="24b4e-110">請注意，秘密金鑰驗證中的「秘密」是指驗證程式是在「秘密」中進行，亦即，實際上不會洩漏金鑰的內容。</span><span class="sxs-lookup"><span data-stu-id="24b4e-110">Notice that the "secret" in secret key authentication is that the authentication process takes place "in secret;" that is, without ever actually revealing the content of the key.</span></span>

<span data-ttu-id="24b4e-111">若要讓秘密金鑰驗證正常運作，交易的雙方必須共用密碼編譯 [*工作階段金鑰*](../secgloss/s-gly.md) ，也就是秘密，而且沒有人知道。</span><span class="sxs-lookup"><span data-stu-id="24b4e-111">For secret key authentication to work, the two parties to a transaction must share a cryptographic [*session key*](../secgloss/s-gly.md) which is also secret, known only to them and to no others.</span></span> <span data-ttu-id="24b4e-112">金鑰為 [*對稱*](../secgloss/s-gly.md)式;也就是說，它是用於加密和解密的單一金鑰。</span><span class="sxs-lookup"><span data-stu-id="24b4e-112">The key is [*symmetric*](../secgloss/s-gly.md); that is, it is a single key used for both encryption and decryption.</span></span> <span data-ttu-id="24b4e-113">驗證程式中的一方會藉由加密訊息來證明其金鑰的知識。</span><span class="sxs-lookup"><span data-stu-id="24b4e-113">One party in the authentication process proves its knowledge of the key by encrypting a message.</span></span> <span data-ttu-id="24b4e-114">另一方藉由解密訊息來證明其金鑰的知識。</span><span class="sxs-lookup"><span data-stu-id="24b4e-114">The other party proves its knowledge of the key by decrypting the message.</span></span>

 

 
