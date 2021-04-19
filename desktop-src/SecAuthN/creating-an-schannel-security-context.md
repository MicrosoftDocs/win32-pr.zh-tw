---
description: 說明如何建立安全性內容，以保護用戶端與伺服器之間的通訊。
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: 建立 Schannel 安全性內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986928"
---
# <a name="creating-an-schannel-security-context"></a><span data-ttu-id="06b56-103">建立 Schannel 安全性內容</span><span class="sxs-lookup"><span data-stu-id="06b56-103">Creating an Schannel Security Context</span></span>

<span data-ttu-id="06b56-104">若要建立可保護用戶端和伺服器之間通訊的 [*安全性內容*](/windows/desktop/SecGloss/s-gly) ，這兩者都必須參與下列資訊交換流程：</span><span class="sxs-lookup"><span data-stu-id="06b56-104">To establish a [*security context*](/windows/desktop/SecGloss/s-gly) that will protect communications between a client and server, both must participate in the following information exchange process:</span></span>

## <a name="client"></a><span data-ttu-id="06b56-105">用戶端</span><span class="sxs-lookup"><span data-stu-id="06b56-105">Client</span></span>

1.  <span data-ttu-id="06b56-106">用戶端會呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函數。</span><span class="sxs-lookup"><span data-stu-id="06b56-106">The client calls the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>
2.  <span data-ttu-id="06b56-107">Schannel 會根據所選安全性通訊協定的規則開始建立安全性內容。</span><span class="sxs-lookup"><span data-stu-id="06b56-107">Schannel begins creating a security context according to the rules of the selected security protocol.</span></span> <span data-ttu-id="06b56-108">函數的傳回碼會指出用戶端是否必須再次呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="06b56-108">The function's return code indicates whether the client must call the function again.</span></span> <span data-ttu-id="06b56-109">[**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 可能會傳回代表內容的權杖。</span><span class="sxs-lookup"><span data-stu-id="06b56-109">[**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) may return a token that represents the context.</span></span>
3.  <span data-ttu-id="06b56-110">如果傳回權杖，用戶端會將它傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="06b56-110">If a token was returned, the client sends it to the server.</span></span>
4.  <span data-ttu-id="06b56-111">[**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)傳回 SEC \_ E OK 時 \_ ，用戶端就完成了。</span><span class="sxs-lookup"><span data-stu-id="06b56-111">When [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) returns SEC\_E\_OK, the client is done.</span></span> <span data-ttu-id="06b56-112">如果函式傳回每 \_ 秒 \_ 繼續 \_ 需要的時間，用戶端必須等待伺服器傳送權杖給它。</span><span class="sxs-lookup"><span data-stu-id="06b56-112">If the function returns SEC\_I\_CONTINUE\_NEEDED, the client must wait for the server to send it a token.</span></span> <span data-ttu-id="06b56-113">當用戶端具有來自伺服器的權杖時，它必須再次呼叫 **InitializeSecurityCoNtext (一般)** [*函數*](/windows/desktop/SecGloss/c-gly) 。</span><span class="sxs-lookup"><span data-stu-id="06b56-113">When the client has the token from the server, it must call the **InitializeSecurityContext (General)** [*function*](/windows/desktop/SecGloss/c-gly) again.</span></span> <span data-ttu-id="06b56-114"> (返回步驟 2. ) </span><span class="sxs-lookup"><span data-stu-id="06b56-114">(Return to step 2.)</span></span>

## <a name="server"></a><span data-ttu-id="06b56-115">伺服器</span><span class="sxs-lookup"><span data-stu-id="06b56-115">Server</span></span>

1.  <span data-ttu-id="06b56-116">伺服器會等候用戶端傳送包含安全性權杖的訊息。</span><span class="sxs-lookup"><span data-stu-id="06b56-116">The server waits for a client to send a message that contains a security token.</span></span> <span data-ttu-id="06b56-117">伺服器會將接收自用戶端的權杖傳遞至 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函式。</span><span class="sxs-lookup"><span data-stu-id="06b56-117">The server passes the token received from the client into the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>
2.  <span data-ttu-id="06b56-118">Schannel 是以權杖所代表的部分安全性內容為基礎。</span><span class="sxs-lookup"><span data-stu-id="06b56-118">Schannel builds on the partial security context represented by the token.</span></span> <span data-ttu-id="06b56-119">Schannel 會將權杖傳回給伺服器，並傳回指出伺服器是否必須再次呼叫函式的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="06b56-119">Schannel returns a token to the server, and a return code indicating whether the server must call the function again.</span></span>
3.  <span data-ttu-id="06b56-120">如果傳回了權杖，伺服器會將它傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="06b56-120">If a token was returned, the server sends it to the client.</span></span>
4.  <span data-ttu-id="06b56-121">當 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 傳回 SEC \_ E \_ OK 時，伺服器就完成了。</span><span class="sxs-lookup"><span data-stu-id="06b56-121">When [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) returns SEC\_E\_OK, the server is done.</span></span> <span data-ttu-id="06b56-122">如果函式傳回每 \_ 秒 \_ 繼續需要的時間，則 \_ 伺服器必須等待用戶端傳送權杖給它。</span><span class="sxs-lookup"><span data-stu-id="06b56-122">If the function returns SEC\_I\_CONTINUE\_NEEDED, then the server must wait for the client to send it a token.</span></span> <span data-ttu-id="06b56-123">當伺服器具有來自用戶端的權杖時，它必須再次呼叫 **AcceptSecurityCoNtext (一般)** 函數。</span><span class="sxs-lookup"><span data-stu-id="06b56-123">When the server has the token from the client, it must call the **AcceptSecurityContext (General)** function again.</span></span> <span data-ttu-id="06b56-124"> (返回步驟 2. ) </span><span class="sxs-lookup"><span data-stu-id="06b56-124">(Return to step 2.)</span></span>

<span data-ttu-id="06b56-125">如果任一個函式傳回 SEC E OK 以外的值 \_ \_ ， \_ \_ 就會繼續 \_ 需要 sec 或 sec \_ e \_ 未完成 \_ 的訊息 (請參閱下列段落) 發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="06b56-125">If either function returns a value other than SEC\_E\_OK, SEC\_I\_CONTINUE\_NEEDED, or SEC\_E\_INCOMPLETE\_MESSAGE (see the following paragraph) an error has occurred.</span></span> <span data-ttu-id="06b56-126">用戶端和伺服器應呼叫 [**DeleteSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) 函數，以刪除部分建立的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="06b56-126">The client and server should call the [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) function to delete the partially established security context.</span></span>

<span data-ttu-id="06b56-127">可以改變用戶端和伺服器處理的特殊案例，就是從其他一方傳送太少或太多的資訊給用戶端或伺服器。</span><span class="sxs-lookup"><span data-stu-id="06b56-127">A special case that can alter client and server processing is when too little or too much information is sent to the client or server from the other party.</span></span> <span data-ttu-id="06b56-128">如果資訊太少，這兩個函式會傳回 SEC \_ E \_ 未完成 \_ 的訊息。</span><span class="sxs-lookup"><span data-stu-id="06b56-128">In the case of too little information, both functions return SEC\_E\_INCOMPLETE\_MESSAGE.</span></span> <span data-ttu-id="06b56-129">如需辨識和處理不足或超過資訊的相關資訊，請參閱 [Schannel 傳回的額外緩衝區](extra-buffers-returned-by-schannel.md)。</span><span class="sxs-lookup"><span data-stu-id="06b56-129">For information about recognizing and handling insufficient or excess information, see [Extra buffers Returned by Schannel](extra-buffers-returned-by-schannel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06b56-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="06b56-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06b56-131">使用 Schannel 執行驗證</span><span class="sxs-lookup"><span data-stu-id="06b56-131">Performing Authentication Using Schannel</span></span>](performing-authentication-using-schannel.md)
</dt> <dt>

[<span data-ttu-id="06b56-132">對應憑證</span><span class="sxs-lookup"><span data-stu-id="06b56-132">Mapping Certificates</span></span>](mapping-certificates.md)
</dt> <dt>

[<span data-ttu-id="06b56-133">手動驗證 Schannel 認證</span><span class="sxs-lookup"><span data-stu-id="06b56-133">Manually Validating Schannel Credentials</span></span>](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
