---
description: Schannel 支援傳輸層安全性 (TLS) 通訊協定的1.0、1.1 和1.2 版。
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: 傳輸層安全性通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994430"
---
# <a name="transport-layer-security-protocol"></a><span data-ttu-id="3aae4-103">傳輸層安全性通訊協定</span><span class="sxs-lookup"><span data-stu-id="3aae4-103">Transport Layer Security Protocol</span></span>

<span data-ttu-id="3aae4-104">Schannel 支援 [*傳輸層安全性 (TLS) 通訊協定*](../secgloss/t-gly.md)的1.0、1.1 和1.2 版。</span><span class="sxs-lookup"><span data-stu-id="3aae4-104">Schannel supports versions 1.0, 1.1, and 1.2 of the [*Transport Layer Security (TLS) protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="3aae4-105">此通訊協定是一種業界標準，其設計目的是要保護透過網際網路所傳達資訊的隱私權。</span><span class="sxs-lookup"><span data-stu-id="3aae4-105">This protocol is an industry standard designed to protect the privacy of information communicated over the Internet.</span></span> <span data-ttu-id="3aae4-106">TLS 假設連接導向傳輸（通常是 TCP）正在使用中。</span><span class="sxs-lookup"><span data-stu-id="3aae4-106">TLS assumes that a connection-oriented transport, typically TCP, is in use.</span></span> <span data-ttu-id="3aae4-107">TLS 通訊協定可讓用戶端/伺服器應用程式偵測下列安全性風險：</span><span class="sxs-lookup"><span data-stu-id="3aae4-107">The TLS protocol allows client/server applications to detect the following security risks:</span></span>

-   <span data-ttu-id="3aae4-108">訊息篡改</span><span class="sxs-lookup"><span data-stu-id="3aae4-108">Message tampering</span></span>
-   <span data-ttu-id="3aae4-109">訊息攔截</span><span class="sxs-lookup"><span data-stu-id="3aae4-109">Message interception</span></span>
-   <span data-ttu-id="3aae4-110">訊息偽造</span><span class="sxs-lookup"><span data-stu-id="3aae4-110">Message forgery</span></span>

<span data-ttu-id="3aae4-111">您可以從 IETF 網站取得 TLS 通訊協定的完整規格： [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) 。</span><span class="sxs-lookup"><span data-stu-id="3aae4-111">The full specification of the TLS Protocol is available from the IETF website: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="organization-of-tls"></a><span data-ttu-id="3aae4-112">TLS 的組織</span><span class="sxs-lookup"><span data-stu-id="3aae4-112">Organization of TLS</span></span>

<span data-ttu-id="3aae4-113">下列步驟牽涉到使用 TLS 進行用戶端/伺服器通訊：</span><span class="sxs-lookup"><span data-stu-id="3aae4-113">The following steps are involved in using TLS for client/server communication:</span></span>

 <span data-ttu-id="3aae4-114">**使用 TLS 進行用戶端/伺服器通訊**</span><span class="sxs-lookup"><span data-stu-id="3aae4-114">**To use TLS for client/server communication**</span></span>

1.  <span data-ttu-id="3aae4-115">交握和加密套件協商</span><span class="sxs-lookup"><span data-stu-id="3aae4-115">Handshake and cipher suite negotiation</span></span>
2.  <span data-ttu-id="3aae4-116">合作物件的驗證</span><span class="sxs-lookup"><span data-stu-id="3aae4-116">Authentication of parties</span></span>
3.  <span data-ttu-id="3aae4-117">與金鑰相關的資訊交換</span><span class="sxs-lookup"><span data-stu-id="3aae4-117">Key-related information exchange</span></span>
4.  <span data-ttu-id="3aae4-118">應用程式資料交換</span><span class="sxs-lookup"><span data-stu-id="3aae4-118">Application data exchange</span></span>

<span data-ttu-id="3aae4-119">組成 TLS 的步驟分為兩種通訊協定，可同時提供連接安全性：</span><span class="sxs-lookup"><span data-stu-id="3aae4-119">The steps that make up TLS are divided into two protocols that, together, provide connection security:</span></span>

-   <span data-ttu-id="3aae4-120">[TLS 交握通訊協定](tls-handshake-protocol.md)- (步驟1– 3) </span><span class="sxs-lookup"><span data-stu-id="3aae4-120">[TLS Handshake Protocol](tls-handshake-protocol.md)— (steps 1 – 3)</span></span>
-   <span data-ttu-id="3aae4-121">[TLS 記錄通訊協定](tls-record-protocol.md)- (步驟 4) </span><span class="sxs-lookup"><span data-stu-id="3aae4-121">[TLS Record Protocol](tls-record-protocol.md)— (step 4)</span></span>

## <a name="sspi-with-tls-implementations"></a><span data-ttu-id="3aae4-122">使用 TLS 的 SSPI</span><span class="sxs-lookup"><span data-stu-id="3aae4-122">SSPI with TLS implementations</span></span>

<span data-ttu-id="3aae4-123">由於 TLS 沒有 GSSAPI 規格，因此 TLS 實施者可能不熟悉 SSPI 功能。</span><span class="sxs-lookup"><span data-stu-id="3aae4-123">Because TLS does not have a GSSAPI specification, TLS implementers may not be familiar with the SSPI functions.</span></span> <span data-ttu-id="3aae4-124">應用程式會呼叫 SSPI 函式來列舉可用的套件、建立及處理認證的控制碼、建立安全性內容，以及確保訊息完整性的隱私權。</span><span class="sxs-lookup"><span data-stu-id="3aae4-124">Applications call the SSPI functions to enumerate available packages, create and work with handles to credentials, create security contexts and ensure message integrity privacy.</span></span>

<span data-ttu-id="3aae4-125">若要支援使用者模式應用程式所使用的 SSPI 函式，TLS 實現（例如 schannel.dll）必須支援由 [使用者模式 SSP/ap 所執行](/windows/desktop/SecAuthN/authentication-functions) 之函式中所列的函式。</span><span class="sxs-lookup"><span data-stu-id="3aae4-125">To support the SSPI functions used by user mode applications, the functions listed in [Functions Implemented by User-mode SSP/APs](/windows/desktop/SecAuthN/authentication-functions) need to be supported by TLS implementations such as schannel.dll.</span></span>

<span data-ttu-id="3aae4-126">如需 SSPI 函數和 SSP 函數的詳細資訊，請參閱 [驗證](authentication-functions.md)函式。</span><span class="sxs-lookup"><span data-stu-id="3aae4-126">For details about the SSPI functions and SSP functions, see [Authentication Functions](authentication-functions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3aae4-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="3aae4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aae4-128">TLS 加密套件</span><span class="sxs-lookup"><span data-stu-id="3aae4-128">TLS Cipher Suites</span></span>](tls-cipher-suites.md)
</dt> <dt>

[<span data-ttu-id="3aae4-129">TLS 與 SSL 的比較</span><span class="sxs-lookup"><span data-stu-id="3aae4-129">TLS vs. SSL</span></span>](tls-versus-ssl.md)
</dt> </dl>

 

 
