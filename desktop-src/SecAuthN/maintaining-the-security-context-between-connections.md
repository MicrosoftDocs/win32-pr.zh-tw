---
description: 為了減少網域控制站的流量並改善效能，Microsoft Digest 的用戶端會快取伺服器驗證成功後所接收的資訊。
ms.assetid: cd928266-889a-494c-a94b-4ea7b1dcc241
title: 維護連接間的安全性內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb450dde789f17f46397cb56fe74b94adcf8ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319835"
---
# <a name="maintaining-the-security-context-between-connections"></a><span data-ttu-id="c64b0-103">維護連接間的安全性內容</span><span class="sxs-lookup"><span data-stu-id="c64b0-103">Maintaining the Security Context Between Connections</span></span>

<span data-ttu-id="c64b0-104">為了減少網域控制站的流量並改善效能，Microsoft Digest 的用戶端會快取伺服器驗證成功後所接收的資訊。</span><span class="sxs-lookup"><span data-stu-id="c64b0-104">To reduce domain controller traffic and improve performance, the client-side of Microsoft Digest caches information received after successful authentication with a server.</span></span> <span data-ttu-id="c64b0-105">用戶端應用程式只需要將控制碼快取到已建立的 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="c64b0-105">Client applications need only cache the handle to the [*security context*](../secgloss/s-gly.md) that has been established.</span></span> <span data-ttu-id="c64b0-106">下表說明安全性封裝所快取的資訊。</span><span class="sxs-lookup"><span data-stu-id="c64b0-106">The following table describes information cached by the security package.</span></span>



| <span data-ttu-id="c64b0-107">資訊</span><span class="sxs-lookup"><span data-stu-id="c64b0-107">Information</span></span>                                                       | <span data-ttu-id="c64b0-108">描述</span><span class="sxs-lookup"><span data-stu-id="c64b0-108">Description</span></span>                                                                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c64b0-109">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="c64b0-109">Server name</span></span>                                                       | <span data-ttu-id="c64b0-110">已成功建立使用者安全性內容的伺服器。</span><span class="sxs-lookup"><span data-stu-id="c64b0-110">The server that has successfully created a security context for the user.</span></span>                                                                           |
| <span data-ttu-id="c64b0-111">領域/網域</span><span class="sxs-lookup"><span data-stu-id="c64b0-111">Realm/Domain</span></span>                                                      | <span data-ttu-id="c64b0-112">成功驗證時所使用的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="c64b0-112">The domain name used in the successful authentication.</span></span>                                                                                              |
| [<span data-ttu-id="c64b0-113">*Nonce*</span><span class="sxs-lookup"><span data-stu-id="c64b0-113">*Nonce*</span></span>](../secgloss/n-gly.md) | <span data-ttu-id="c64b0-114">與成功驗證相關聯的伺服器 nonce。</span><span class="sxs-lookup"><span data-stu-id="c64b0-114">A server nonce that is associated with the successful authentication.</span></span>                                                                               |
| <span data-ttu-id="c64b0-115">Nonce 計數</span><span class="sxs-lookup"><span data-stu-id="c64b0-115">Nonce count</span></span>                                                       | <span data-ttu-id="c64b0-116">用戶端在伺服器要求中包含 nonce 的次數。</span><span class="sxs-lookup"><span data-stu-id="c64b0-116">The number of times the client has included the nonce in requests to the server.</span></span> <span data-ttu-id="c64b0-117">這是用於重新執行偵測。</span><span class="sxs-lookup"><span data-stu-id="c64b0-117">This is used for replay-detection.</span></span>                                 |
| <span data-ttu-id="c64b0-118">不透明的值</span><span class="sxs-lookup"><span data-stu-id="c64b0-118">Opaque value</span></span>                                                      | <span data-ttu-id="c64b0-119">驗證成功之後，針對不透明指示詞傳回的值。</span><span class="sxs-lookup"><span data-stu-id="c64b0-119">The value returned for the opaque directive after a successful authentication.</span></span> <span data-ttu-id="c64b0-120">此值包含使用者安全性內容的參考。</span><span class="sxs-lookup"><span data-stu-id="c64b0-120">This value contains a reference to the security context of the user.</span></span> |



 

<span data-ttu-id="c64b0-121">當用戶端將訊息傳送到伺服器時，伺服器必須判斷用戶端是否有現有的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="c64b0-121">When a client sends a message to a server, the server must determine whether the client has an existing security context.</span></span> <span data-ttu-id="c64b0-122">若要這樣做，伺服器會將每個用戶端要求傳遞給 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數。</span><span class="sxs-lookup"><span data-stu-id="c64b0-122">To do this, the server passes each client request to the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span> <span data-ttu-id="c64b0-123">此函式會從要求中解壓縮不透明指示詞的值（如果有的話），並使用它來查閱用戶端的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="c64b0-123">This function extracts the value of the opaque directive from the request, if present, and uses it to look up the client's security context.</span></span> <span data-ttu-id="c64b0-124">如果找到安全性內容，則會將內容控制碼傳回給伺服器。</span><span class="sxs-lookup"><span data-stu-id="c64b0-124">If the security context is found, the handle of the context is returned to the server.</span></span> <span data-ttu-id="c64b0-125">如需相關資訊，請參閱 [驗證後續要求](authenticating-subsequent-requests-using-microsoft-digest.md)。</span><span class="sxs-lookup"><span data-stu-id="c64b0-125">For related information, see [Authenticating Subsequent Requests](authenticating-subsequent-requests-using-microsoft-digest.md).</span></span>

<span data-ttu-id="c64b0-126">作為偵測詐騙和重新執行攻擊的方法，用戶端會呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式，該函式會使用安全性內容來簽署訊息。</span><span class="sxs-lookup"><span data-stu-id="c64b0-126">As a means of detecting spoofing and replay attacks, the client calls the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function which uses a security context to sign a message.</span></span> <span data-ttu-id="c64b0-127">當使用 **MakeSignature** 函數來保護訊息時，伺服器會使用 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函式搭配快取的內容，以驗證訊息的來源和 [*完整性*](../secgloss/i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c64b0-127">When messages are protected using the **MakeSignature** function, the server uses the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function with the cached context to verify the message's origin and [*integrity*](../secgloss/i-gly.md).</span></span> <span data-ttu-id="c64b0-128">如需詳細資訊，請參閱 [保護訊息](protecting-messages-using-microsoft-digest.md)。</span><span class="sxs-lookup"><span data-stu-id="c64b0-128">For more information, see [Protecting Messages](protecting-messages-using-microsoft-digest.md).</span></span>

 

 
