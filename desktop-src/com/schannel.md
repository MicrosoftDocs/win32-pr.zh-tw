---
title: Schannel
description: 安全通道 (Schannel) 安全性套件，其驗證服務識別碼為 RPC \_ C \_ 驗證 GSS 安全通道 \_ \_ ，支援下列以公開金鑰為基礎的通訊協定： SSL (安全通訊端層) 2.0 和3.0 版、傳輸層安全性 (TLS) 1.0 和私用通訊技術 (PCT) 1.0。 TLS 1.0 是一種標準化、稍微修改的 SSL 3.0 版本，由網際網路工程任務推動小組 (IETF) 在檔 RFC 2246 中的1月1999日。 由於 TLS 已標準化，因此我們鼓勵開發人員使用 TLS，而不是使用 SSL。 PCT 是為了提供回溯相容性而包含，不應該用於新的開發。 使用安全通道安全性套件時，DCOM 會根據用戶端和伺服器的功能，自動協調最佳的通訊協定。
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc9f82a05d1542e7585426128f10cdf452d31d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316570"
---
# <a name="schannel"></a><span data-ttu-id="e328b-107">Schannel</span><span class="sxs-lookup"><span data-stu-id="e328b-107">Schannel</span></span>

<span data-ttu-id="e328b-108">安全通道 (Schannel) 安全性封裝，其驗證服務識別碼為 RPC \_ C \_ 驗證 GSS 安全通道 \_ \_ ，支援下列以公開金鑰為基礎的通訊協定： SSL (安全通訊端層) 2.0 和3.0 版、傳輸層安全性 (TLS) 1.0 和私用通訊技術 (PCT) 1.0。</span><span class="sxs-lookup"><span data-stu-id="e328b-108">The Secure Channel (Schannel) security package, whose authentication service identifier is RPC\_C\_AUTHN\_GSS\_SCHANNEL, supports the following public-key based protocols: SSL (Secure Sockets Layer) versions 2.0 and 3.0, Transport Layer Security (TLS) 1.0, and Private Communication Technology (PCT) 1.0.</span></span> <span data-ttu-id="e328b-109">TLS 1.0 是一種標準化、稍微修改的 SSL 3.0 版本，由網際網路工程任務推動小組 (IETF) 在檔 [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt)中的1月1999日。</span><span class="sxs-lookup"><span data-stu-id="e328b-109">TLS 1.0 is a standardized, slightly modified version of SSL 3.0 that was issued by the Internet Engineering Task Force (IETF) in January 1999, in document [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt).</span></span> <span data-ttu-id="e328b-110">由於 TLS 已標準化，因此我們鼓勵開發人員使用 TLS，而不是使用 SSL。</span><span class="sxs-lookup"><span data-stu-id="e328b-110">Because TLS has been standardized, developers are encouraged to use TLS rather than SSL.</span></span> <span data-ttu-id="e328b-111">PCT 是為了提供回溯相容性而包含，不應該用於新的開發。</span><span class="sxs-lookup"><span data-stu-id="e328b-111">PCT is included for backward compatibility only and should not be used for new development.</span></span> <span data-ttu-id="e328b-112">使用安全通道安全性套件時，DCOM 會根據用戶端和伺服器的功能，自動協調最佳的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e328b-112">When the Schannel security package is used, DCOM automatically negotiates the best protocol, depending on the client and server capabilities.</span></span>

<span data-ttu-id="e328b-113">下列主題簡要說明 TLS 通訊協定以及它與 DCOM 的搭配運作方式。</span><span class="sxs-lookup"><span data-stu-id="e328b-113">The following topics briefly describe the TLS protocol and how it works with DCOM.</span></span>

-   [<span data-ttu-id="e328b-114">使用 TLS 的時機</span><span class="sxs-lookup"><span data-stu-id="e328b-114">When to Use TLS</span></span>](#when-to-use-tls)
-   [<span data-ttu-id="e328b-115">TLS 如何運作的簡短總覽</span><span class="sxs-lookup"><span data-stu-id="e328b-115">Brief Overview of How TLS Works</span></span>](#brief-overview-of-how-tls-works)
-   [<span data-ttu-id="e328b-116">X.509 憑證</span><span class="sxs-lookup"><span data-stu-id="e328b-116">X.509 Certificates</span></span>](#x509-certificates)
    -   [<span data-ttu-id="e328b-117">用戶端憑證</span><span class="sxs-lookup"><span data-stu-id="e328b-117">Client Certificates</span></span>](#client-certificates)
-   [<span data-ttu-id="e328b-118">使用 COM 中的 TLS</span><span class="sxs-lookup"><span data-stu-id="e328b-118">Using TLS in COM</span></span>](#using-tls-in-com)
    -   [<span data-ttu-id="e328b-119">伺服器如何設定安全性綜合</span><span class="sxs-lookup"><span data-stu-id="e328b-119">How a Server Sets the Security Blanket</span></span>](#how-a-server-sets-the-security-blanket)
    -   [<span data-ttu-id="e328b-120">用戶端如何設定安全性的總</span><span class="sxs-lookup"><span data-stu-id="e328b-120">How a Client Sets the Security Blanket</span></span>](#how-a-client-sets-the-security-blanket)
    -   [<span data-ttu-id="e328b-121">用戶端如何變更安全性的總</span><span class="sxs-lookup"><span data-stu-id="e328b-121">How a Client Changes the Security Blanket</span></span>](#how-a-client-changes-the-security-blanket)
    -   [<span data-ttu-id="e328b-122">範例：用戶端變更安全性的總</span><span class="sxs-lookup"><span data-stu-id="e328b-122">Example: Client Changes the Security Blanket</span></span>](#example-client-changes-the-security-blanket)
-   [<span data-ttu-id="e328b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e328b-123">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="e328b-124">在這些章節中，TLS 通訊協定的所有相關資訊也適用于 SSL 和 PCT 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e328b-124">All the information about the TLS protocol in these sections also applies to the SSL and PCT protocols.</span></span>

 

## <a name="when-to-use-tls"></a><span data-ttu-id="e328b-125">使用 TLS 的時機</span><span class="sxs-lookup"><span data-stu-id="e328b-125">When to Use TLS</span></span>

<span data-ttu-id="e328b-126">當伺服器需要向匿名用戶端證明其身分識別時，TLS 是唯一可用的安全性選項。</span><span class="sxs-lookup"><span data-stu-id="e328b-126">TLS is the only security option available when servers need to prove their identity to anonymous clients.</span></span> <span data-ttu-id="e328b-127">這對於想要參與電子商務的網站來說特別重要，因為它可協助保護機密資訊的傳輸，例如信用卡號碼。</span><span class="sxs-lookup"><span data-stu-id="e328b-127">This is particularly important for websites that want to participate in e-commerce because it helps protect the transmission of sensitive information such as credit card numbers.</span></span> <span data-ttu-id="e328b-128">TLS 可確保電子商務客戶可以確定其執行業務的人員，因為它們會獲得伺服器身分識別的證明。</span><span class="sxs-lookup"><span data-stu-id="e328b-128">TLS assures that the e-commerce customers can be certain of whom they are doing business with because they are given proof of the server's identity.</span></span> <span data-ttu-id="e328b-129">它也讓電子商務伺服器的效率不需要自行驗證其每個客戶的身分識別。</span><span class="sxs-lookup"><span data-stu-id="e328b-129">It also gives the e-commerce server the efficiency of not having to concern itself with authenticating the identity of each of its customers.</span></span>

<span data-ttu-id="e328b-130">TLS 要求所有伺服器向用戶端證明其身分識別。</span><span class="sxs-lookup"><span data-stu-id="e328b-130">TLS requires that all servers prove their identity to clients.</span></span> <span data-ttu-id="e328b-131">此外，TLS 提供讓用戶端向伺服器證明其身分識別的選項。</span><span class="sxs-lookup"><span data-stu-id="e328b-131">Additionally, TLS provides the option of having clients prove their identity to servers.</span></span> <span data-ttu-id="e328b-132">此相互驗證有助於限制大型公司內部網路中特定網頁的存取。</span><span class="sxs-lookup"><span data-stu-id="e328b-132">This mutual authentication can be useful in restricting the access of certain webpages in a large corporate intranet.</span></span>

<span data-ttu-id="e328b-133">TLS 支援最強的驗證層級，並提供開放的架構，可讓加密強度隨著時間增加，以跟上技術創新。</span><span class="sxs-lookup"><span data-stu-id="e328b-133">TLS supports the strongest authentication levels and offers an open architecture that permits encryption strength to increase over time to keep up with technological innovation.</span></span> <span data-ttu-id="e328b-134">對於傳輸中資料所需的最高層級安全性環境而言，TLS 是最好的選擇。</span><span class="sxs-lookup"><span data-stu-id="e328b-134">TLS is the best choice for environments where the highest level of security is desired for the data in transit.</span></span>

## <a name="brief-overview-of-how-tls-works"></a><span data-ttu-id="e328b-135">TLS 如何運作的簡短總覽</span><span class="sxs-lookup"><span data-stu-id="e328b-135">Brief Overview of How TLS Works</span></span>

<span data-ttu-id="e328b-136">TLS 是建立在公開金鑰基礎結構 (PKI) ，其使用公開/私密金鑰組來啟用資料加密和建立資料完整性，並使用 x.509 憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e328b-136">TLS is built upon a public key infrastructure (PKI), which uses public/private key pairs for enabling data encryption and establishing data integrity, and uses X.509 certificates for authentication.</span></span>

<span data-ttu-id="e328b-137">許多安全性通訊協定（例如 Kerberos v5 通訊協定）相依于單一金鑰來加密和解密資料。</span><span class="sxs-lookup"><span data-stu-id="e328b-137">Many security protocols, such as the Kerberos v5 protocol, depend on a single key to both encrypt and decrypt data.</span></span> <span data-ttu-id="e328b-138">因此，這類通訊協定取決於加密金鑰的安全交換;在 Kerberos 通訊協定中，這是透過從金鑰發佈中心 (KDC) 取得的票證來完成。</span><span class="sxs-lookup"><span data-stu-id="e328b-138">Such protocols therefore depend on the secure exchange of encryption keys; in the Kerberos protocol, this is done through tickets obtained from the Key Distribution Center (KDC).</span></span> <span data-ttu-id="e328b-139">如此一來，使用 Kerberos 通訊協定的每個人都必須向 KDC 註冊，這對電子商務 web 伺服器來說是一項不實際的限制，旨在吸引全球數百萬名客戶。</span><span class="sxs-lookup"><span data-stu-id="e328b-139">This requires that everyone using the Kerberos protocol be registered with the KDC, which would be an impractical limitation for an e-commerce web server that is intended to attract millions of customers from around the world.</span></span> <span data-ttu-id="e328b-140">因此，TLS 會依賴 PKI，這會使用兩個金鑰來進行資料 encryptionâ。」當其中一個索引鍵加密資料時，只有配對的另一個索引鍵可以解密。</span><span class="sxs-lookup"><span data-stu-id="e328b-140">TLS therefore relies upon a PKI, which uses two keys for data encryptionâ€”when one key of the pair encrypts the data, only the other key of the pair can decrypt it.</span></span> <span data-ttu-id="e328b-141">這項設計的主要優點是可以執行加密，而不需要安全地交換加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="e328b-141">The principle benefit of this design is that encryption can be performed without requiring the secure exchange of encryption keys.</span></span>

<span data-ttu-id="e328b-142">PKI 使用的技巧是，其中一個金鑰會保留為私用，而且僅適用于它所註冊的主體，而另一個金鑰則公開給任何人存取。</span><span class="sxs-lookup"><span data-stu-id="e328b-142">A PKI uses a technique where one of the keys is kept private and is available only to the principal to whom it is registered, while the other key is made public for anyone to access.</span></span> <span data-ttu-id="e328b-143">如果有人想要將私用訊息傳送給金鑰組的擁有者，可以使用公開金鑰來加密訊息，而只有私密金鑰可以用來解密訊息。</span><span class="sxs-lookup"><span data-stu-id="e328b-143">If someone wants to send a private message to the owner of a key pair, the message can be encrypted with the public key and only the private key can be used to decrypt the message.</span></span>

<span data-ttu-id="e328b-144">金鑰組也用來驗證所傳送資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="e328b-144">Key pairs are also used to verify the integrity of the data being sent.</span></span> <span data-ttu-id="e328b-145">若要這樣做，金鑰組的擁有者可以在傳送數位簽章之前，先將數位簽章附加至資料。</span><span class="sxs-lookup"><span data-stu-id="e328b-145">To do this, the owner of the key pair can attach a digital signature to the data before sending it.</span></span> <span data-ttu-id="e328b-146">建立數位簽章牽涉到計算資料的雜湊，並使用私密金鑰來加密雜湊。</span><span class="sxs-lookup"><span data-stu-id="e328b-146">Creating a digital signature involves calculating a hash of the data and encrypting the hash with the private key.</span></span> <span data-ttu-id="e328b-147">使用公開金鑰解密數位簽章的任何人都可以確保數位簽章只能來自擁有私密金鑰的人員。</span><span class="sxs-lookup"><span data-stu-id="e328b-147">Anyone who uses the public key to decrypt the digital signature is assured that the digital signature must have come only from the person who owns the private key.</span></span> <span data-ttu-id="e328b-148">此外，收件者也可以使用與寄件者相同的演算法來計算資料的雜湊，而且如果匯出的雜湊符合數位簽章中傳送的雜湊，則收件者可以確定資料經過數位簽署之後不會修改。</span><span class="sxs-lookup"><span data-stu-id="e328b-148">Additionally, the recipient can calculate a hash of the data using the same algorithm as the sender, and if the calculated hash matches the one sent in the digital signature, the recipient can be certain that the data was not modified after it was digitally signed.</span></span>

<span data-ttu-id="e328b-149">使用 PKI 進行大量資料加密的其中一個缺點是其效能相對較慢。</span><span class="sxs-lookup"><span data-stu-id="e328b-149">One disadvantage of using a PKI for high-volume data encryption is its relatively slow performance.</span></span> <span data-ttu-id="e328b-150">由於涉及大量的數學運算，使用與金鑰組相依的非對稱式加密來加密和解密資料的速度，最高可達1000倍，但使用只依賴單一金鑰的對稱式加密和解密。</span><span class="sxs-lookup"><span data-stu-id="e328b-150">Because of the intensive mathematics involved, encryption and decryption of data using an asymmetric cipher that depends on a key pair can be up to 1,000 times slower than encryption and decryption using a symmetric cipher that depends only on a single key.</span></span> <span data-ttu-id="e328b-151">因此，TLS 只會使用 PKI 來產生數位簽章，以及協調用戶端和伺服器將用來進行大量資料加密和解密的會話特定單一金鑰。</span><span class="sxs-lookup"><span data-stu-id="e328b-151">TLS therefore uses a PKI only for generating digital signatures and for negotiating the session-specific single key that will be used by both the client and the server for bulk data encryption and decryption.</span></span> <span data-ttu-id="e328b-152">TLS 支援各種不同的單一金鑰組稱式加密，未來可能會新增額外的密碼。</span><span class="sxs-lookup"><span data-stu-id="e328b-152">TLS supports a wide variety of single-key symmetric ciphers, and additional ciphers may be added in the future.</span></span>

<span data-ttu-id="e328b-153">如需 TLS 交握通訊協定的詳細資訊，請參閱 [Tls 交握通訊協定](/windows/desktop/SecAuthN/tls-handshake-protocol)。</span><span class="sxs-lookup"><span data-stu-id="e328b-153">For more information about the TLS handshake protocol, see [TLS Handshake Protocol](/windows/desktop/SecAuthN/tls-handshake-protocol).</span></span>

<span data-ttu-id="e328b-154">如需 TLS 通訊協定背後密碼編譯的詳細資訊，請參閱 [密碼編譯基本](/windows/desktop/SecCrypto/cryptography-essentials)資訊。</span><span class="sxs-lookup"><span data-stu-id="e328b-154">For more details regarding the cryptography behind the TLS protocol, see [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).</span></span>

## <a name="x509-certificates"></a><span data-ttu-id="e328b-155">X.509 憑證</span><span class="sxs-lookup"><span data-stu-id="e328b-155">X.509 Certificates</span></span>

<span data-ttu-id="e328b-156">PKI 必須處理的重大問題，就是能夠信任所使用公開金鑰的真實性。</span><span class="sxs-lookup"><span data-stu-id="e328b-156">A critical issue that must be handled by a PKI is the ability to trust the authenticity of the public key that is being used.</span></span> <span data-ttu-id="e328b-157">當您使用發行給公司的公開金鑰，而該公司想要與公司合作時，您會想要確定金鑰實際上屬於公司，而不是想要探索您的信用卡號碼的竊賊。</span><span class="sxs-lookup"><span data-stu-id="e328b-157">When you use a public key issued to a company that you want to do business with, you want to be certain that the key actually belongs to the company rather than to a thief who wants to discover your credit card number.</span></span>

<span data-ttu-id="e328b-158">為了保證持有金鑰組之主體的身分識別，主體是由憑證授權單位單位 (CA) 發出的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="e328b-158">To guarantee the identity of a principal holding a key pair, the principal is issued an X.509 certificate by a certification authority (CA).</span></span> <span data-ttu-id="e328b-159">此憑證包含可識別主體的資訊、包含主體的公開金鑰，且由 CA 進行數位簽署。</span><span class="sxs-lookup"><span data-stu-id="e328b-159">This certificate contains information that identifies the principal, contains the principal's public key, and is digitally signed by the CA.</span></span> <span data-ttu-id="e328b-160">此數位簽章表示 CA 認為憑證中包含的公開金鑰確實屬於憑證所識別的主體。</span><span class="sxs-lookup"><span data-stu-id="e328b-160">This digital signature indicates that the CA believes that the public key contained in the certificate truly belongs to the principal identified by the certificate.</span></span>

<span data-ttu-id="e328b-161">那麼，您該如何信任 CA 呢？</span><span class="sxs-lookup"><span data-stu-id="e328b-161">And how do you trust the CA?</span></span> <span data-ttu-id="e328b-162">因為 CA 本身會保存由較高層級 CA 簽署的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="e328b-162">Because the CA itself holds an X.509 certificate that has been signed by a higher-level CA.</span></span> <span data-ttu-id="e328b-163">這一鏈的憑證簽章會繼續進行，直到到達根 CA，也就是簽署本身憑證的 CA。</span><span class="sxs-lookup"><span data-stu-id="e328b-163">This chain of certificate signatures continues until it reaches a root CA, which is a CA that signs its own certificates.</span></span> <span data-ttu-id="e328b-164">如果您信任憑證根 CA 的完整性，您應該能夠信任憑證本身的真實性。</span><span class="sxs-lookup"><span data-stu-id="e328b-164">If you trust the integrity of the root CA of a certificate, you should be able to trust the authenticity of the certificate itself.</span></span> <span data-ttu-id="e328b-165">因此，挑選您願意信任的根 Ca 是系統管理員的重要責任。</span><span class="sxs-lookup"><span data-stu-id="e328b-165">Therefore, picking root CAs that you are willing to trust is an important duty for a system administrator.</span></span>

### <a name="client-certificates"></a><span data-ttu-id="e328b-166">用戶端憑證</span><span class="sxs-lookup"><span data-stu-id="e328b-166">Client Certificates</span></span>

<span data-ttu-id="e328b-167">當安全性傳輸層通訊協定第一次出現時，其主要目的是保證用戶端連線至真實的伺服器，並在傳輸時保護資料的隱私權。</span><span class="sxs-lookup"><span data-stu-id="e328b-167">When security transport-layer protocols first emerged, their primary purpose was to guarantee that a client was connecting to an authentic server and help protect the privacy of data while in transit.</span></span> <span data-ttu-id="e328b-168">不過，SSL 3.0 和 TLS 1.0 也支援在通訊協定交握期間傳輸用戶端的憑證。</span><span class="sxs-lookup"><span data-stu-id="e328b-168">However, SSL 3.0 and TLS 1.0 also include support for the transmission of a client's certificate during the protocol's handshake.</span></span> <span data-ttu-id="e328b-169">這項選用功能可啟用用戶端和伺服器的相互驗證。</span><span class="sxs-lookup"><span data-stu-id="e328b-169">This optional feature enables the mutual authentication of the client and server.</span></span>

<span data-ttu-id="e328b-170">您應該在應用程式的內容中，決定是否要使用用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="e328b-170">The decision of whether to use a client certificate should be made in the context of the application.</span></span> <span data-ttu-id="e328b-171">如果主要需求是驗證服務器，就不需要用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="e328b-171">Client certificates are unnecessary if the primary requirement is authenticating the server.</span></span> <span data-ttu-id="e328b-172">但是，如果用戶端驗證是必要的，則可以使用用戶端的憑證，而不是依賴應用程式內的自訂驗證。</span><span class="sxs-lookup"><span data-stu-id="e328b-172">However, if client authentication is essential, a client's certificate can be used rather than relying on custom authentication within the application.</span></span> <span data-ttu-id="e328b-173">使用用戶端憑證優於自訂驗證，因為它會為使用者提供單一登入案例。</span><span class="sxs-lookup"><span data-stu-id="e328b-173">Using client certificates is preferable over custom authentication because it gives users a single sign-on scenario.</span></span>

## <a name="using-tls-in-com"></a><span data-ttu-id="e328b-174">使用 COM 中的 TLS</span><span class="sxs-lookup"><span data-stu-id="e328b-174">Using TLS in COM</span></span>

<span data-ttu-id="e328b-175">TLS 僅支援模擬 (RPC \_ C \_ IMP \_ 層級模擬 \_) 的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="e328b-175">TLS supports only the impersonate (RPC\_C\_IMP\_LEVEL\_IMPERSONATE) level of impersonation.</span></span> <span data-ttu-id="e328b-176">如果 COM 將 TLS 協商為 proxy 上的驗證服務，則不論進程預設值為何，COM 都會將模擬等級設定為模擬。</span><span class="sxs-lookup"><span data-stu-id="e328b-176">If COM negotiates TLS as the authentication service on a proxy, COM will set the impersonation level to impersonate regardless of the process default.</span></span> <span data-ttu-id="e328b-177">為了讓模擬在 TLS 中正常運作，用戶端必須提供 x.509 憑證給伺服器，且伺服器必須將該憑證對應到伺服器上的特定使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="e328b-177">For impersonation to work properly in TLS, the client must provide an X.509 certificate to the server and the server must have that certificate mapped to a particular user account on the server.</span></span> <span data-ttu-id="e328b-178">如需詳細資訊，請參閱將 [憑證對應至使用者帳戶的逐步指南](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates)。</span><span class="sxs-lookup"><span data-stu-id="e328b-178">For more information, see the [Step-by-Step Guide to Mapping Certificates to User Accounts](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates).</span></span>

<span data-ttu-id="e328b-179">TLS 不支援 [掩蓋](cloaking.md)。</span><span class="sxs-lookup"><span data-stu-id="e328b-179">TLS does not support [cloaking](cloaking.md).</span></span> <span data-ttu-id="e328b-180">如果在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 或 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) 呼叫中指定了遮蓋旗標和 TLS，將會 \_ 傳回 E INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="e328b-180">If a cloaking flag and TLS are specified in a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or a [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) call, E\_INVALIDARG will be returned.</span></span>

<span data-ttu-id="e328b-181">當驗證層級設定為 [無] 時，TLS 無法運作。</span><span class="sxs-lookup"><span data-stu-id="e328b-181">TLS does not work with the authentication level set to None.</span></span> <span data-ttu-id="e328b-182">用戶端與伺服器之間的交握會檢查每個設定的驗證層級，並為連線選擇較高的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="e328b-182">The handshake between the client and server examines the authentication level set by each and chooses the higher security setting for the connection.</span></span>

<span data-ttu-id="e328b-183">您可以藉由呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 和 [**COSETPROXYBLANKET**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)來設定 TLS 的安全性參數。</span><span class="sxs-lookup"><span data-stu-id="e328b-183">The security parameters for TLS can be set by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="e328b-184">下列各節說明進行這些呼叫時所牽涉到的細微差異。</span><span class="sxs-lookup"><span data-stu-id="e328b-184">The following sections describe the nuances involved in making those calls.</span></span>

### <a name="how-a-server-sets-the-security-blanket"></a><span data-ttu-id="e328b-185">伺服器如何設定安全性綜合</span><span class="sxs-lookup"><span data-stu-id="e328b-185">How a Server Sets the Security Blanket</span></span>

<span data-ttu-id="e328b-186">如果伺服器想要使用 TLS，它必須 \_ \_ \_ 在 CoInitializeSecurity 的 asAuthSvc 參數中指定 Schannel (RPC C 驗證 GSS \_ Schannel) 作為驗證服務。 [](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)</span><span class="sxs-lookup"><span data-stu-id="e328b-186">If a server wants to use TLS, it must specify Schannel (RPC\_C\_AUTHN\_GSS\_SCHANNEL) as an authentication service in the *asAuthSvc* parameter of [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="e328b-187">為了防止用戶端使用較不安全的驗證服務連接到伺服器，伺服器在呼叫 **CoInitializeSecurity** 時，只能將 Schannel 指定為驗證服務。</span><span class="sxs-lookup"><span data-stu-id="e328b-187">To prevent clients from connecting to the server by using a less secure authentication service, the server should specify only Schannel as an authentication service when it calls **CoInitializeSecurity**.</span></span> <span data-ttu-id="e328b-188">伺服器在呼叫 **CoInitializeSecurity** 之後，就無法變更安全性的總。</span><span class="sxs-lookup"><span data-stu-id="e328b-188">The server cannot change the security blanket after it has called **CoInitializeSecurity**.</span></span>

<span data-ttu-id="e328b-189">若要使用 TLS，當伺服器呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時，應該指定下列參數：</span><span class="sxs-lookup"><span data-stu-id="e328b-189">To use TLS, the following parameters should be specified when a server calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

-   <span data-ttu-id="e328b-190">*pVoid* 應該是 [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) 物件的指標或 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)的指標。</span><span class="sxs-lookup"><span data-stu-id="e328b-190">*pVoid* should be either a pointer to an [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) object or a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor).</span></span> <span data-ttu-id="e328b-191">它不能是 **Null** 或 AppID 的指標。</span><span class="sxs-lookup"><span data-stu-id="e328b-191">It should not be **NULL** or a pointer to an AppID.</span></span>
-   <span data-ttu-id="e328b-192">*cAuthSvc* 不可為0或-1。</span><span class="sxs-lookup"><span data-stu-id="e328b-192">*cAuthSvc* cannot be 0 or -1.</span></span> <span data-ttu-id="e328b-193">當 *cAuthSvc* 為-1 時，COM 伺服器絕不會選擇 Schannel。</span><span class="sxs-lookup"><span data-stu-id="e328b-193">COM servers never chooses Schannel when *cAuthSvc* is -1.</span></span>
-   <span data-ttu-id="e328b-194">*asAuthSvc* 必須將 Schannel 指定為可能的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="e328b-194">*asAuthSvc* must specify Schannel as a possible authentication service.</span></span> <span data-ttu-id="e328b-195">這是藉由為 [**唯一 \_ 驗證 \_ 清單**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list)的 Schannel 成員設定下列 [**唯一 \_ 驗證 \_ 服務**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)參數來完成的：</span><span class="sxs-lookup"><span data-stu-id="e328b-195">This is done by setting the following [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) parameters for the Schannel member of the [**SOLE\_AUTHENTICATION\_LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list):</span></span>
    -   <span data-ttu-id="e328b-196">*dwAuthnSvc* 必須是 RPC \_ C \_ 驗證 \_ GSS \_ SCHANNEL。</span><span class="sxs-lookup"><span data-stu-id="e328b-196">*dwAuthnSvc* must be RPC\_C\_AUTHN\_GSS\_SCHANNEL.</span></span>
    -   <span data-ttu-id="e328b-197">*dwAuthzSvc* 應為「RPC \_ C \_ 授權無」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e328b-197">*dwAuthzSvc* should be RPC\_C\_AUTHZ\_NONE.</span></span> <span data-ttu-id="e328b-198">目前會忽略它。</span><span class="sxs-lookup"><span data-stu-id="e328b-198">Currently, it is ignored.</span></span>
    -   <span data-ttu-id="e328b-199">*pPrincipalName* 必須是指向憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)的指標，轉換成 OLECHAR 的指標，代表伺服器的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="e328b-199">*pPrincipalName* must be a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), cast as a pointer to OLECHAR, which represents the server's X.509 certificate.</span></span>
-   <span data-ttu-id="e328b-200">*dwAuthnLevel* 指出將從用戶端接收成功連線的最小驗證等級。</span><span class="sxs-lookup"><span data-stu-id="e328b-200">*dwAuthnLevel* indicates the minimum authentication level that will be accepted from clients for a successful connection.</span></span> <span data-ttu-id="e328b-201">不可為 RPC \_ C \_ 驗證 \_ 層級 \_ 無。</span><span class="sxs-lookup"><span data-stu-id="e328b-201">It cannot be RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>
-   <span data-ttu-id="e328b-202">*dwCapabilities* 不應 \_ 設定 EOAC APPID 旗標。</span><span class="sxs-lookup"><span data-stu-id="e328b-202">*dwCapabilities* should not have the EOAC\_APPID flag set.</span></span> <span data-ttu-id="e328b-203">\_ \_ 如果 *pVoid* 指向 [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol)物件，則應設定 EOAC 存取控制旗標; *pVoid* 指向安全描述項時，不應設定此旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e328b-203">The EOAC\_ACCESS\_CONTROL flag should be set if *pVoid* points to an [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) object; it should not be set if *pVoid* points to a SECURITY\_DESCRIPTOR.</span></span> <span data-ttu-id="e328b-204">如需其他可能設定的旗標，請參閱 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)。</span><span class="sxs-lookup"><span data-stu-id="e328b-204">For other flags that may be set, see [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="e328b-205">如需使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的詳細資訊，請參閱使用 [CoInitializeSecurity 設定 Processwide 安全性](setting-processwide-security-with-coinitializesecurity.md)。</span><span class="sxs-lookup"><span data-stu-id="e328b-205">For more information about using [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).</span></span>

### <a name="how-a-client-sets-the-security-blanket"></a><span data-ttu-id="e328b-206">用戶端如何設定安全性的總</span><span class="sxs-lookup"><span data-stu-id="e328b-206">How a Client Sets the Security Blanket</span></span>

<span data-ttu-id="e328b-207">如果用戶端想要使用 TLS，它必須在 \_ \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的 *pAuthList* 參數中，于其驗證服務清單中指定 schannel (RPC C 驗證 GSS Schannel) 。</span><span class="sxs-lookup"><span data-stu-id="e328b-207">If a client wants to use TLS, it must specify Schannel (RPC\_C\_AUTHN\_GSS\_SCHANNEL) in its list of authentication services in the *pAuthList* parameter of [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="e328b-208">如果在呼叫 **CoInitializeSecurity** 時未將 schannel 指定為可能的驗證服務，則在稍後呼叫 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (或 [**IClientSecurity：：) SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) 時，如果嘗試將 schannel 指定為驗證服務，將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e328b-208">If Schannel is not specified as a possible authentication service when **CoInitializeSecurity** is called, a later call to [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (or [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)) will fail if it tries to specify Schannel as the authentication service.</span></span>

<span data-ttu-id="e328b-209">當用戶端呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時，應該指定下列參數：</span><span class="sxs-lookup"><span data-stu-id="e328b-209">The following parameters should be specified when a client calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

-   <span data-ttu-id="e328b-210">*dwAuthnLevel* 指定用戶端想要使用的預設驗證層級。</span><span class="sxs-lookup"><span data-stu-id="e328b-210">*dwAuthnLevel* specifies the default authentication level that the client wants to use.</span></span> <span data-ttu-id="e328b-211">不可為 RPC \_ C \_ 驗證 \_ 層級 \_ 無。</span><span class="sxs-lookup"><span data-stu-id="e328b-211">It cannot be RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>
-   <span data-ttu-id="e328b-212">*dwImpLevel* 必須是 RPC \_ C \_ IMP \_ 層級模擬 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e328b-212">*dwImpLevel* must be RPC\_C\_IMP\_LEVEL\_IMPERSONATE.</span></span>
-   <span data-ttu-id="e328b-213">*pAuthList* 必須以下列 [**唯一的 \_ 驗證 \_ 資訊**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) 參數作為清單的成員：</span><span class="sxs-lookup"><span data-stu-id="e328b-213">*pAuthList* must have the following [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) parameters as a member of the list:</span></span>
    -   <span data-ttu-id="e328b-214">*dwAuthnSvc* 必須是 RPC \_ C \_ 驗證 \_ GSS \_ SCHANNEL。</span><span class="sxs-lookup"><span data-stu-id="e328b-214">*dwAuthnSvc* must be RPC\_C\_AUTHN\_GSS\_SCHANNEL.</span></span>
    -   <span data-ttu-id="e328b-215">*dwAuthzSvc* 必須是 RPC \_ C \_ 授權 \_ 無。</span><span class="sxs-lookup"><span data-stu-id="e328b-215">*dwAuthzSvc* must be RPC\_C\_AUTHZ\_NONE.</span></span>
    -   <span data-ttu-id="e328b-216">*pAuthInfo* 是指向憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)的指標，轉換為 void 的指標，代表用戶端的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="e328b-216">*pAuthInfo* is a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), cast as a pointer to void, which represents the client's X.509 certificate.</span></span> <span data-ttu-id="e328b-217">如果用戶端沒有憑證，或不想將其憑證出示給伺服器， *pAuthInfo* 必須是 **Null** ，且伺服器會嘗試匿名連接。</span><span class="sxs-lookup"><span data-stu-id="e328b-217">If the client does not have a certificate or does not wish to present its certificate to the server, *pAuthInfo* must be **NULL** and an anonymous connection will be attempted with the server.</span></span>
-   <span data-ttu-id="e328b-218">*dwCapabilities* 是一組表示額外用戶端功能的旗標。</span><span class="sxs-lookup"><span data-stu-id="e328b-218">*dwCapabilities* is a set of flags that indicate additional client capabilities.</span></span> <span data-ttu-id="e328b-219">如需應設定哪些旗標的詳細資訊，請參閱 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 。</span><span class="sxs-lookup"><span data-stu-id="e328b-219">See [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) for information about which flags should be set.</span></span>

<span data-ttu-id="e328b-220">如需使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的詳細資訊，請參閱使用 [CoInitializeSecurity 設定 Processwide 安全性](setting-processwide-security-with-coinitializesecurity.md)。</span><span class="sxs-lookup"><span data-stu-id="e328b-220">For more information about using [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).</span></span>

### <a name="how-a-client-changes-the-security-blanket"></a><span data-ttu-id="e328b-221">用戶端如何變更安全性的總</span><span class="sxs-lookup"><span data-stu-id="e328b-221">How a Client Changes the Security Blanket</span></span>

<span data-ttu-id="e328b-222">如果用戶端想要使用 TLS，但在呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)之後變更安全性階層，則必須呼叫 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) 或 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) ，並以與 **CoInitializeSecurity** 呼叫中使用的參數類似，但有下列差異：</span><span class="sxs-lookup"><span data-stu-id="e328b-222">If a client wants to use TLS but change the security blanket after calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), it must call either [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) or [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) with parameters similar to those used in the call to **CoInitializeSecurity**, with the following differences:</span></span>

-   <span data-ttu-id="e328b-223">*pServerPrincName* 以 msstd 或 fullsic 格式表示伺服器的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="e328b-223">*pServerPrincName* indicates the principal name of the server, in either msstd or fullsic format.</span></span> <span data-ttu-id="e328b-224">如需這些格式的詳細資訊，請參閱 [主體名稱](/windows/desktop/Rpc/principal-names)。</span><span class="sxs-lookup"><span data-stu-id="e328b-224">For information on these formats, see [Principal Names](/windows/desktop/Rpc/principal-names).</span></span> <span data-ttu-id="e328b-225">如果用戶端有伺服器的 x.509 憑證，它可以藉由呼叫 [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname)來尋找主體名稱。</span><span class="sxs-lookup"><span data-stu-id="e328b-225">If the client has the server's X.509 certificate, it can find the principal name by calling [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname).</span></span>
-   <span data-ttu-id="e328b-226">*pAuthInfo* 是一種指向憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)的指標，轉換為 RPC AUTH 身分 \_ \_ 識別控制碼的指標 \_ ，代表用戶端的 x.509 憑證。</span><span class="sxs-lookup"><span data-stu-id="e328b-226">*pAuthInfo* is a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context), cast as a pointer to RPC\_AUTH\_IDENTITY\_HANDLE, which represents the client's X.509 certificate.</span></span> <span data-ttu-id="e328b-227">如果用戶端沒有憑證，或不想將其憑證出示給伺服器， *pAuthInfo* 必須是 **Null** ，且伺服器會嘗試匿名連接。</span><span class="sxs-lookup"><span data-stu-id="e328b-227">If the client does not have a certificate or does not wish to present its certificate to the server, *pAuthInfo* must be **NULL** and an anonymous connection will be attempted with the server.</span></span>
-   <span data-ttu-id="e328b-228">*dwCapabilities* 包含表示額外用戶端功能的旗標。</span><span class="sxs-lookup"><span data-stu-id="e328b-228">*dwCapabilities* consists of flags that indicate additional client capabilities.</span></span> <span data-ttu-id="e328b-229">只有四個旗標可以用來變更安全性的總設定： EOAC \_ 預設值、EOAC \_ 相互 \_ 驗證、EOAC \_ 任何 \_ 授權單位 (此旗標已淘汰) ，而且 EOAC \_ 設為 \_ FULLSIC。</span><span class="sxs-lookup"><span data-stu-id="e328b-229">Only four flags can be used to change security blanket settings: EOAC\_DEFAULT, EOAC\_MUTUAL\_AUTH, EOAC\_ANY\_AUTHORITY (this flag is deprecated), and EOAC\_MAKE\_FULLSIC.</span></span> <span data-ttu-id="e328b-230">如需詳細資訊，請參閱 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)。</span><span class="sxs-lookup"><span data-stu-id="e328b-230">For more information, see [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="e328b-231">如需使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)的詳細資訊，請參閱在 [介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)。</span><span class="sxs-lookup"><span data-stu-id="e328b-231">For more information about using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), see [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

### <a name="example-client-changes-the-security-blanket"></a><span data-ttu-id="e328b-232">範例：用戶端變更安全性的總</span><span class="sxs-lookup"><span data-stu-id="e328b-232">Example: Client Changes the Security Blanket</span></span>

<span data-ttu-id="e328b-233">下列範例會示範用戶端如何變更安全性，以容納來自伺服器的要求，以提供其 x.509 憑證給用戶端。</span><span class="sxs-lookup"><span data-stu-id="e328b-233">The following example demonstrates how a client can change the security blanket to accommodate a request from the server for the client to provide its X.509 certificate.</span></span> <span data-ttu-id="e328b-234">為了簡潔起見，已省略錯誤處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="e328b-234">Error handling code is omitted for brevity.</span></span>


```C++
void ClientChangesSecurity ()
{
  HCRYPTPROV                   provider           = 0;
  HCERTSTORE                   cert_store         = NULL;
  PCCERT_CONTEXT               client_cert        = NULL;
  PCCERT_CONTEXT               server_cert        = NULL;
  WCHAR                        *server_princ_name = NULL;
  ISecret                      *pSecret           = NULL;
  MULTI_QI                     server_instance;
  COSERVERINFO                 server_machine;
  SOLE_AUTHENTICATION_LIST     auth_list;
  SOLE_AUTHENTICATION_INFO     auth_info[1];



  // Specify all the authentication info. 
  // The client is willing to connect using SChannel,
  //   with no client certificate.
  auth_list.cAuthInfo     = 1;
  auth_list.aAuthInfo     = auth_info;
  auth_info[0].dwAuthnSvc = RPC_C_AUTHN_GSS_SCHANNEL;
  auth_info[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
  auth_info[0].pAuthInfo  = NULL;  // No certificate

  // Initialize client security with no client certificate.
  CoInitializeSecurity( NULL, -1, NULL, NULL,
                        RPC_C_AUTHN_LEVEL_PKT,
                        RPC_C_IMP_LEVEL_IMPERSONATE, &auth_list,
                        EOAC_NONE, NULL );
  
  // Specify info for the proxy.
  server_instance = {&IID_ISecret, NULL, S_OK};
  server_machine  = {0, L"ServerMachineName", NULL, 0};
  
  // Create a proxy.
  CoCreateInstanceEx( CLSID_Secret, NULL, CLSCTX_REMOTE_SERVER, 
                      &server_machine, 1, &server_instance);
  pSecret = (ISecret *) server_instance.pItf;

  //** The client obtained the server's certificate during the handshake.
  //** The server requests a certificate from the client.

  // Get the default certificate provider.
  CryptAcquireContext( &provider, NULL, NULL, PROV_RSA_SCHANNEL, 0 );

  // Open the certificate store.
  cert_store = CertOpenSystemStore( provider, L"my" );

  // Find the client's certificate.
  client_cert = 
    CertFindCertificateInStore( cert_store,
                                X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                                0,
                                CERT_FIND_SUBJECT_STR,
                                L"ClientName",  // Use the principal name
                                NULL );

  // Find the fullsic principal name of the server.
  RpcCertGeneratePrincipalName( server_cert, RPC_C_FULL_CERT_CHAIN, 
                                &server_princ_name );

  // Change the client's security: 
  // Increase the authentication level and attach a certificate.
  CoSetProxyBlanket( pSecret, RPC_C_AUTHN_GSS_SCHANNEL,
                     RPC_C_AUTHZ_NONE,
                     server_princ_name, RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
                     RPC_C_IMP_LEVEL_IMPERSONATE, 
                     (RPC_AUTH_IDENTITY_HANDLE *) client_cert,
                     EOAC_NONE );

  cleanup:
  if (server_princ_name != NULL)
    RpcStringFree( &server_princ_name );
  if (client_cert != NULL)
    CertFreeCertificateContext(client_cert);
  if (server_cert != NULL)
    CertFreeCertificateContext(server_cert);
  if (cert_store != NULL)
    CertCloseStore( cert_store, CERT_CLOSE_STORE_CHECK_FLAG );
  if (provider != 0 )
    CryptReleaseContext( provider, 0 );
  if (pSecret != NULL)
    pSecret->Release();
  CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="e328b-235">相關主題</span><span class="sxs-lookup"><span data-stu-id="e328b-235">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e328b-236">COM 和安全性封裝</span><span class="sxs-lookup"><span data-stu-id="e328b-236">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 