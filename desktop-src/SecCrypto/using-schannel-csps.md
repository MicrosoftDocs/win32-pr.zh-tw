---
description: SSL 通訊協定引擎 (Schannel) 在執行密碼編譯作業時，會使用 (CSP) 的密碼編譯服務提供者。 密碼編譯應用程式可以使用 >PROV \_ RSA \_ SCHANNEL 和 >prov DH 安全通道 \_ \_ 提供者來呼叫 CryptAcquireCoNtext。
ms.assetid: ad1eabf1-23bc-4d23-8f8b-13f0bda95120
title: 使用 Schannel Csp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289ed57d9f312ee1ef57aecf7534a8d585859126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993004"
---
# <a name="using-schannel-csps"></a><span data-ttu-id="b951f-104">使用 Schannel Csp</span><span class="sxs-lookup"><span data-stu-id="b951f-104">Using Schannel CSPs</span></span>

<span data-ttu-id="b951f-105">SSL 通訊協定引擎 ([*Schannel*](../secgloss/s-gly.md)) 在執行密碼編譯作業時，會使用 (CSP) 的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="b951f-105">The SSL protocol engine ([*Schannel*](../secgloss/s-gly.md)) uses a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) when performing cryptographic operations.</span></span> <span data-ttu-id="b951f-106">密碼編譯應用程式[](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)可以使用 >prov \_ RSA \_ schannel 和 >prov DH 安全通道 \_ \_ 提供者來呼叫 CryptAcquireCoNtext。</span><span class="sxs-lookup"><span data-stu-id="b951f-106">Cryptographic applications can call [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) using the PROV\_RSA\_SCHANNEL and PROV\_DH\_SCHANNEL providers.</span></span>

<span data-ttu-id="b951f-107">本節定義 RSA 和 Diffie-Hellman Schannel [*CSP 類型*](../secgloss/c-gly.md) ，並描述 CSP 必須支援的功能，以與 Schannel.dll 的密碼編譯通訊協定引擎相容。</span><span class="sxs-lookup"><span data-stu-id="b951f-107">This section defines the RSA and Diffie-Hellman Schannel [*CSP types*](../secgloss/c-gly.md) and describes the functionality that a CSP must support to be compatible with Schannel.dll, the cryptographic protocol engine.</span></span> <span data-ttu-id="b951f-108">通訊協定引擎是一種程式，可在用戶端與伺服器應用程式之間建立安全通道。</span><span class="sxs-lookup"><span data-stu-id="b951f-108">A protocol engine is a program that establishes a secure communications channel between a client and server application.</span></span>

<span data-ttu-id="b951f-109">應用程式不應該嘗試使用本檔中的資訊，直接使用 >PROV \_ RSA \_ SCHANNEL 或 >prov \_ DH \_ schannel。</span><span class="sxs-lookup"><span data-stu-id="b951f-109">Applications should not attempt to use information in this documentation to use PROV\_RSA\_SCHANNEL or PROV\_DH\_SCHANNEL directly.</span></span> <span data-ttu-id="b951f-110">相反地，本檔說明 CSP 開發人員和廠商必須撰寫與 Microsoft Schannel 提供者相容的安全通道 Csp。</span><span class="sxs-lookup"><span data-stu-id="b951f-110">Rather, this documentation explains how CSP developers and vendors must write Schannel CSPs that are compatible with Microsoft Schannel providers.</span></span>

<span data-ttu-id="b951f-111">本檔旨在協助 CSP 開發人員執行相容的 RSA 或 Diffie-Hellman Schannel Csp。</span><span class="sxs-lookup"><span data-stu-id="b951f-111">This documentation is intended to help CSP developers implement compatible RSA or Diffie-Hellman Schannel CSPs.</span></span> <span data-ttu-id="b951f-112">開發人員會假設您已熟悉 [*安全通訊端層*](../secgloss/s-gly.md) (SSL) 通訊協定3.0 版、 [*公開金鑰*](../secgloss/p-gly.md) 密碼編譯、 [*數位憑證*](../secgloss/d-gly.md)和 CryptoAPI 函數集。</span><span class="sxs-lookup"><span data-stu-id="b951f-112">Developers are assumed to be familiar with the [*Secure Socket Layer*](../secgloss/s-gly.md) (SSL) protocol version 3.0, [*public key*](../secgloss/p-gly.md) cryptography, [*digital certificates*](../secgloss/d-gly.md), and the CryptoAPI function set.</span></span> <span data-ttu-id="b951f-113">建議您閱讀這些主題的新開發人員，以閱讀此 SDK 中的 SSL 通訊協定3.0 規格和 [密碼編譯基本](cryptography-essentials.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="b951f-113">Developers new to these topics are advised to read the SSL Protocol 3.0 specification and the [Cryptography Essentials](cryptography-essentials.md) documentation in this SDK.</span></span> <span data-ttu-id="b951f-114">此外，RSA 和 Diffie-Hellman CSP 開發人員必須知道 [*傳輸層安全性*](../secgloss/t-gly.md) (TLS) 通訊協定規格，以及相關的 RSA 和 [*diffie-hellman 演算法*](../secgloss/d-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="b951f-114">In addition, RSA and Diffie-Hellman CSP developers must know [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) protocol specifications along with the relevant RSA and [*Diffie-Hellman algorithms*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="b951f-115">如需 Microsoft 通訊協定引擎使用的範例，請參閱 [建立主要金鑰](creating-the-master-key.md)。</span><span class="sxs-lookup"><span data-stu-id="b951f-115">For an example used by a Microsoft protocol engine, see [Creating the Master Key](creating-the-master-key.md).</span></span> <span data-ttu-id="b951f-116">在此範例中，對密碼編譯函式的呼叫會導致呼叫由 CSP 必須實行的 CP 函式。</span><span class="sxs-lookup"><span data-stu-id="b951f-116">The calls to cryptography functions in this example result in calls to CP functions that a CSP must implement.</span></span> <span data-ttu-id="b951f-117">若要撰寫相容的 CSP，開發人員必須瞭解 SSL 3.0 規格，並將該知識與此範例中所使用的通訊協定引擎程式碼的理解進行結合。</span><span class="sxs-lookup"><span data-stu-id="b951f-117">To write a compatible CSP, a developer must understand the SSL 3.0 specification and combine that knowledge with an understanding of the protocol engine code similar to that used in this example.</span></span>

<span data-ttu-id="b951f-118">由於使用私用通訊技術通訊協定的未來預期會很短，因此新的 Csp 開發人員不需要支援此通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b951f-118">Because use of the Private Communications Technology protocol is expected to be minimal in the future, developers of new CSPs need not support this protocol.</span></span> <span data-ttu-id="b951f-119">安全通道通訊協定引擎為了回溯相容性而完全支援。</span><span class="sxs-lookup"><span data-stu-id="b951f-119">The Schannel protocol engine supports it strictly for backward compatibility.</span></span>

 

 
