---
description: 登入網路時，會使用 Kerberos 驗證套件;本機登入是由 MSV1 \_ 0 處理。
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: Kerberos SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026871"
---
# <a name="kerberos-sspap"></a><span data-ttu-id="90a56-103">Kerberos SSP/AP</span><span class="sxs-lookup"><span data-stu-id="90a56-103">Kerberos SSP/AP</span></span>

<span data-ttu-id="90a56-104">登入網路時，會使用 [*Kerberos*](../secgloss/k-gly.md) 驗證套件;本機登入是由 MSV1 \_ 0 處理。</span><span class="sxs-lookup"><span data-stu-id="90a56-104">The [*Kerberos*](../secgloss/k-gly.md) authentication package is used when logging on to a network; local logons are handled by MSV1\_0.</span></span>

<span data-ttu-id="90a56-105">當使用者使用網路帳戶登入時，Kerberos 預設會嘗試連線到網域控制站上的 Kerberos [*金鑰發佈中心*](../secgloss/k-gly.md) (KDC) ，並使用使用者提供的登入資料， (TGT) 取得票證授權票證。</span><span class="sxs-lookup"><span data-stu-id="90a56-105">When a user logs on using a network account, by default, Kerberos attempts to connect to the Kerberos [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) on the domain controller and obtain a ticket granting ticket (TGT) by using the logon data supplied by the user.</span></span>

<span data-ttu-id="90a56-106">如果無法使用 Kerberos KDC，Windows 會使用 MSV1 \_ 0 和傳遞驗證，如 [MSV1 \_ 0 authentication 套件](msv1-0-authentication-package.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="90a56-106">If a Kerberos KDC is not available, Windows uses MSV1\_0 and pass-through authentication as described in [MSV1\_0 Authentication Package](msv1-0-authentication-package.md).</span></span>

<span data-ttu-id="90a56-107">Kerberos 驗證套件支援 Kerberos 通訊協定的第5版（修訂版6）。</span><span class="sxs-lookup"><span data-stu-id="90a56-107">The Kerberos authentication package supports version 5, revision 6 of the Kerberos protocol.</span></span> <span data-ttu-id="90a56-108">此通訊協定是以網際網路 [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)為基礎。</span><span class="sxs-lookup"><span data-stu-id="90a56-108">This protocol is based on Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt).</span></span> <span data-ttu-id="90a56-109">如需詳細資訊，請參閱 IETF 網站：</span><span class="sxs-lookup"><span data-stu-id="90a56-109">For more information, see the IETF website:</span></span>

[https://www.ietf.org](https://www.ietf.org/)

<span data-ttu-id="90a56-110">如需有關 Kerberos 的詳細資訊，請參閱 [Microsoft kerberos](microsoft-kerberos.md)。</span><span class="sxs-lookup"><span data-stu-id="90a56-110">For more information about Kerberos, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

## <a name="kerberos-credential-formats"></a><span data-ttu-id="90a56-111">Kerberos 認證格式</span><span class="sxs-lookup"><span data-stu-id="90a56-111">Kerberos Credential Formats</span></span>

<span data-ttu-id="90a56-112">Kerberos 驗證套件在成功登入之後所指派的使用者 [*認證*](../secgloss/c-gly.md) 是票證和暫時加密金鑰，通常稱為 [*工作階段金鑰*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="90a56-112">The user [*credentials*](../secgloss/c-gly.md) assigned by the Kerberos authentication package after a successful logon attempt are a ticket and a temporary encryption key, often called a [*session key*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="90a56-113">票證包含用戶端認證和工作階段金鑰的加密複本。</span><span class="sxs-lookup"><span data-stu-id="90a56-113">The ticket contains both an encrypted copy of the client's credentials and the session key.</span></span>

 

 
