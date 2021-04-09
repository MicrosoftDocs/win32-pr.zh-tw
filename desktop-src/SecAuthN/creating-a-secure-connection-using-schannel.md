---
description: 如何使用 Schannel 建立安全的連接。
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: 使用 Schannel 建立安全連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693503"
---
# <a name="creating-a-secure-connection-using-schannel"></a><span data-ttu-id="df407-103">使用 Schannel 建立安全連線</span><span class="sxs-lookup"><span data-stu-id="df407-103">Creating a Secure Connection Using Schannel</span></span>

<span data-ttu-id="df407-104">Schannel [*安全性封裝*](/windows/desktop/SecGloss/s-gly) 可讓您存取四種 [*安全性通訊協定*](/windows/desktop/SecGloss/s-gly)：</span><span class="sxs-lookup"><span data-stu-id="df407-104">The Schannel [*security package*](/windows/desktop/SecGloss/s-gly) provides access to four [*security protocols*](/windows/desktop/SecGloss/s-gly):</span></span>

-   [<span data-ttu-id="df407-105">傳輸層安全性 (TLS 1.2) </span><span class="sxs-lookup"><span data-stu-id="df407-105">Transport Layer Security (TLS 1.2)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="df407-106">傳輸層安全性 (TLS 1.1) </span><span class="sxs-lookup"><span data-stu-id="df407-106">Transport Layer Security (TLS 1.1)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="df407-107">傳輸層安全性 (TLS 1.0) </span><span class="sxs-lookup"><span data-stu-id="df407-107">Transport Layer Security (TLS 1.0)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="df407-108">安全通訊端層 (SSL 3.0) </span><span class="sxs-lookup"><span data-stu-id="df407-108">Secure Sockets Layer (SSL 3.0)</span></span>](secure-sockets-layer-protocol.md)
-   [<span data-ttu-id="df407-109">安全通訊端層 (SSL 2.0) </span><span class="sxs-lookup"><span data-stu-id="df407-109">Secure Sockets Layer (SSL 2.0)</span></span>](secure-sockets-layer-protocol.md)

> [!Note]  
> <span data-ttu-id="df407-110">PCT 和 SSL 2.0 通訊協定已被 TLS 通訊協定取代，且不應該用於新的開發。</span><span class="sxs-lookup"><span data-stu-id="df407-110">The PCT and SSL 2.0 protocols have been superseded by the TLS protocol and should not be used for new development.</span></span>

 

<span data-ttu-id="df407-111">**設定用戶端與伺服器之間的安全連線**</span><span class="sxs-lookup"><span data-stu-id="df407-111">**To set up a secure connection between a client and server**</span></span>

1.  <span data-ttu-id="df407-112">取得安全通道認證 (取得) 的 [Schannel 認證](obtaining-schannel-credentials.md) 。</span><span class="sxs-lookup"><span data-stu-id="df407-112">Obtain Schannel credentials ([Obtaining Schannel Credentials](obtaining-schannel-credentials.md)).</span></span>
2.  <span data-ttu-id="df407-113">建立 Schannel 安全性內容 ([建立安全通道安全性內容](creating-an-schannel-security-context.md)) 。</span><span class="sxs-lookup"><span data-stu-id="df407-113">Create an Schannel security context ([Creating an Schannel Security Context](creating-an-schannel-security-context.md)).</span></span>

<span data-ttu-id="df407-114">建立連線之後，您可以取得其屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="df407-114">After a connection is established, you can retrieve information about its attributes.</span></span> <span data-ttu-id="df407-115">如需詳細資訊，請參閱 [取得 Schannel 連接的相關資訊](getting-information-about-schannel-connections.md)。</span><span class="sxs-lookup"><span data-stu-id="df407-115">For details, see [Getting Information About Schannel Connections](getting-information-about-schannel-connections.md).</span></span>

<span data-ttu-id="df407-116">如果您在建立連線之後，應用程式的安全性需求變更或連接已遺失，您就可以重新協商連接。</span><span class="sxs-lookup"><span data-stu-id="df407-116">If, after you have established a connection, the security requirements of your application change or the connection is lost, you can renegotiate the connection.</span></span> <span data-ttu-id="df407-117">如需詳細資訊，請參閱 [重新交涉 Schannel 連接](renegotiating-an-schannel-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="df407-117">For details, see [Renegotiating an Schannel Connection](renegotiating-an-schannel-connection.md).</span></span>

<span data-ttu-id="df407-118">當您完成使用 Schannel 連接時，必須執行必要的清除。</span><span class="sxs-lookup"><span data-stu-id="df407-118">When you have finished using an Schannel connection, you must perform the necessary cleanup.</span></span> <span data-ttu-id="df407-119">如需詳細資訊，請參閱 [關閉 Schannel 連接](shutting-down-an-schannel-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="df407-119">For details, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span>

<span data-ttu-id="df407-120">如需平臺軟體發展工具組隨附的範例 (SDK) （示範 Schannel [*安全性封裝*](/windows/desktop/SecGloss/s-gly)）的相關資訊，請參閱使用 SCHANNEL 的 PSDK 範例。</span><span class="sxs-lookup"><span data-stu-id="df407-120">For information about samples shipped with the Platform Software Development Kit (SDK) that demonstrate the Schannel [*security package*](/windows/desktop/SecGloss/s-gly), see the PSDK samples using Schannel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df407-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="df407-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df407-122">指定 Schannel 密碼和加密的強度</span><span class="sxs-lookup"><span data-stu-id="df407-122">Specifying Schannel Ciphers and Cipher Strengths</span></span>](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
