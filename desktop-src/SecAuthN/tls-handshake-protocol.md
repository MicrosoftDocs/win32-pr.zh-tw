---
description: 傳輸層安全性 (TLS) 交握通訊協定負責建立或繼續安全會話所需的驗證和金鑰交換。
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: TLS 交握通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7cfa9e9db54a6035abe147ce00bbde59bcc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997875"
---
# <a name="tls-handshake-protocol"></a><span data-ttu-id="a7cd1-103">TLS 交握通訊協定</span><span class="sxs-lookup"><span data-stu-id="a7cd1-103">TLS Handshake Protocol</span></span>

<span data-ttu-id="a7cd1-104">[*傳輸層安全性*](../secgloss/t-gly.md) (TLS) 交握通訊協定負責建立或繼續安全會話所需的驗證和金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-104">The [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Handshake Protocol is responsible for the authentication and key exchange necessary to establish or resume secure sessions.</span></span> <span data-ttu-id="a7cd1-105">建立安全 [*會話*](../secgloss/s-gly.md)時，交握通訊協定會管理下列各項：</span><span class="sxs-lookup"><span data-stu-id="a7cd1-105">When establishing a secure [*session*](../secgloss/s-gly.md), the Handshake Protocol manages the following:</span></span>

-   <span data-ttu-id="a7cd1-106">加密套件協商</span><span class="sxs-lookup"><span data-stu-id="a7cd1-106">Cipher suite negotiation</span></span>
-   <span data-ttu-id="a7cd1-107">伺服器驗證和用戶端（選擇性）</span><span class="sxs-lookup"><span data-stu-id="a7cd1-107">Authentication of the server and optionally, the client</span></span>
-   <span data-ttu-id="a7cd1-108">工作階段金鑰資訊交換。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-108">Session key information exchange.</span></span>

## <a name="cipher-suite-negotiation"></a><span data-ttu-id="a7cd1-109">加密套件協商</span><span class="sxs-lookup"><span data-stu-id="a7cd1-109">Cipher Suite Negotiation</span></span>

<span data-ttu-id="a7cd1-110">用戶端和伺服器會建立連絡人，並選擇將在整個訊息交換中使用的密碼套件。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-110">The client and server make contact and choose the cipher suite that will be used throughout their message exchange.</span></span>

## <a name="authentication"></a><span data-ttu-id="a7cd1-111">驗證</span><span class="sxs-lookup"><span data-stu-id="a7cd1-111">Authentication</span></span>

<span data-ttu-id="a7cd1-112">在 TLS 中，伺服器會向用戶端證明其身分識別。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-112">In TLS, a server proves its identity to the client.</span></span> <span data-ttu-id="a7cd1-113">用戶端也可能需要向伺服器證明其身分識別。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-113">The client might also need to prove its identity to the server.</span></span> <span data-ttu-id="a7cd1-114">PKI （ [*公開/私密金鑰*](../secgloss/p-gly.md)組的使用）是此驗證的基礎。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-114">PKI, the use of [*public/private key pairs*](../secgloss/p-gly.md), is the basis of this authentication.</span></span> <span data-ttu-id="a7cd1-115">用於驗證的確切方法取決於經過協商的密碼套件。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-115">The exact method used for authentication is determined by the cipher suite negotiated.</span></span>

## <a name="key-exchange"></a><span data-ttu-id="a7cd1-116">金鑰交換</span><span class="sxs-lookup"><span data-stu-id="a7cd1-116">Key Exchange</span></span>

<span data-ttu-id="a7cd1-117">用戶端和伺服器交換亂數字，以及稱為預先主密碼的特殊數位。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-117">The client and server exchange random numbers and a special number called the Pre-Master Secret.</span></span> <span data-ttu-id="a7cd1-118">這些數位會與其他資料結合，以允許用戶端和伺服器建立其共用密碼，稱為主要密碼。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-118">These numbers are combined with additional data permitting client and server to create their shared secret, called the Master Secret.</span></span> <span data-ttu-id="a7cd1-119">用戶端和伺服器會使用主要密碼來產生寫入 MAC 秘密，也就是用於 [*雜湊*](../secgloss/h-gly.md)的工作階段金鑰，而寫入金鑰是用於加密的 [*工作階段金鑰*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-119">The Master Secret is used by client and server to generate the write MAC secret, which is the session key used for [*hashing*](../secgloss/h-gly.md), and the write key, which is the [*session key*](../secgloss/s-gly.md) used for encryption.</span></span>

## <a name="establishing-a-secure-session-by-using-tls"></a><span data-ttu-id="a7cd1-120">使用 TLS 建立安全會話</span><span class="sxs-lookup"><span data-stu-id="a7cd1-120">Establishing a Secure Session by Using TLS</span></span>

<span data-ttu-id="a7cd1-121">TLS 交握通訊協定牽涉到下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a7cd1-121">The TLS Handshake Protocol involves the following steps:</span></span>

1.  <span data-ttu-id="a7cd1-122">用戶端會將 "Client hello" 訊息傳送至伺服器，以及用戶端的隨機值和支援的加密套件。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-122">The client sends a "Client hello" message to the server, along with the client's random value and supported cipher suites.</span></span>
2.  <span data-ttu-id="a7cd1-123">伺服器會透過傳送 "Server hello" 訊息給用戶端來回應，以及伺服器的隨機值。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-123">The server responds by sending a "Server hello" message to the client, along with the server's random value.</span></span>
3.  <span data-ttu-id="a7cd1-124">伺服器會將其憑證傳送給用戶端進行驗證，而且可能會向用戶端要求憑證。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-124">The server sends its certificate to the client for authentication and may request a certificate from the client.</span></span> <span data-ttu-id="a7cd1-125">伺服器會傳送「伺服器 hello 完成」訊息。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-125">The server sends the "Server hello done" message.</span></span>
4.  <span data-ttu-id="a7cd1-126">如果伺服器已向用戶端要求憑證，用戶端會傳送憑證。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-126">If the server has requested a certificate from the client, the client sends it.</span></span>
5.  <span data-ttu-id="a7cd1-127">用戶端會建立隨機的主要密碼，並使用伺服器憑證的 [*公開金鑰*](../secgloss/p-gly.md) 進行加密，並將加密的主要密碼傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-127">The client creates a random Pre-Master Secret and encrypts it with the [*public key*](../secgloss/p-gly.md) from the server's certificate, sending the encrypted Pre-Master Secret to the server.</span></span>
6.  <span data-ttu-id="a7cd1-128">伺服器會接收預先主要密碼。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-128">The server receives the Pre-Master Secret.</span></span> <span data-ttu-id="a7cd1-129">伺服器和用戶端都會根據前版秘密產生主要密碼和 [*工作階段金鑰*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-129">The server and client each generate the Master Secret and [*session keys*](../secgloss/s-gly.md) based on the Pre-Master Secret.</span></span>
7.  <span data-ttu-id="a7cd1-130">用戶端會將「變更加密規格」通知傳送至伺服器，表示用戶端將會開始使用新的 [*工作階段金鑰*](../secgloss/s-gly.md) 來 [*雜湊*](../secgloss/h-gly.md) 和加密訊息。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-130">The client sends "Change cipher spec" notification to server to indicate that the client will start using the new [*session keys*](../secgloss/s-gly.md) for [*hashing*](../secgloss/h-gly.md) and encrypting messages.</span></span> <span data-ttu-id="a7cd1-131">用戶端也會傳送「用戶端已完成」訊息。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-131">Client also sends "Client finished" message.</span></span>
8.  <span data-ttu-id="a7cd1-132">伺服器會收到「變更加密規格」，並使用 [*工作階段金鑰*](../secgloss/s-gly.md)將其記錄層安全性狀態切換至 [*對稱式加密*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-132">Server receives "Change cipher spec" and switches its record layer security state to [*symmetric encryption*](../secgloss/s-gly.md) using the [*session keys*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="a7cd1-133">伺服器會將「伺服器已完成」訊息傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-133">Server sends "Server finished" message to the client.</span></span>
9.  <span data-ttu-id="a7cd1-134">用戶端和伺服器現在可以透過已建立的安全通道來交換應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-134">Client and server can now exchange application data over the secured channel they have established.</span></span> <span data-ttu-id="a7cd1-135">從用戶端到伺服器以及從伺服器傳送到用戶端的所有訊息都會使用工作階段金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-135">All messages sent from client to server and from server to client are encrypted using session key.</span></span>

## <a name="resuming-a-secure-session-by-using-tls"></a><span data-ttu-id="a7cd1-136">使用 TLS 繼續安全會話</span><span class="sxs-lookup"><span data-stu-id="a7cd1-136">Resuming a Secure Session by Using TLS</span></span>

1.  <span data-ttu-id="a7cd1-137">用戶端會使用要繼續之會話的會話識別碼來傳送 "Client hello" 訊息。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-137">The client sends a "Client hello" message using the Session ID of the session to be resumed.</span></span>
2.  <span data-ttu-id="a7cd1-138">伺服器會檢查其會話快取中是否有相符的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-138">The server checks its session cache for a matching Session ID.</span></span> <span data-ttu-id="a7cd1-139">如果找到相符的，且伺服器能夠繼續會話，則會傳送含有會話識別碼的 "Server hello" 訊息。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-139">If a match is found, and the server is able to resume the session, it sends a "Server hello" message with the Session ID.</span></span>
    > [!Note]  
    > <span data-ttu-id="a7cd1-140">如果找不到會話識別碼相符，伺服器會產生新的會話識別碼，而 TLS 用戶端和伺服器會執行完整的交握。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-140">If a session ID match is not found, the server generates a new session ID and the TLS client and server perform a full handshake.</span></span>

     

3.  <span data-ttu-id="a7cd1-141">用戶端和伺服器必須交換「變更加密規格」訊息，並傳送「用戶端已完成」和「伺服器已完成」訊息。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-141">Client and server must exchange "Change cipher spec" messages and send "Client finished" and "Server finished" messages.</span></span>
4.  <span data-ttu-id="a7cd1-142">用戶端和伺服器現在可以透過安全通道恢復應用程式資料交換。</span><span class="sxs-lookup"><span data-stu-id="a7cd1-142">Client and server can now resume application data exchange over the secure channel.</span></span>

 

 
