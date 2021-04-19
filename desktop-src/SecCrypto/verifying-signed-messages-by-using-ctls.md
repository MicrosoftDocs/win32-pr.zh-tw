---
description: 使用憑證信任清單 () Ctl 的優點之一，就是可以將應用程式設計成可以根據信任的憑證自動驗證已簽署的訊息，而不需要竟然想使用者的對話方塊。
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: 使用 Ctl 驗證已簽署的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971822"
---
# <a name="verifying-signed-messages-by-using-ctls"></a><span data-ttu-id="fbf33-103">使用 Ctl 驗證已簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="fbf33-103">Verifying Signed Messages by Using CTLs</span></span>

<span data-ttu-id="fbf33-104">使用 [*憑證信任清單*](../secgloss/c-gly.md) () ctl 的優點之一，就是可以將應用程式設計成可以根據信任的憑證自動驗證已簽署的訊息，而不需要竟然想使用者的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fbf33-104">One of the advantages of using [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) is that applications can be designed that can automatically verify signed messages against trusted certificates without bothering the user with dialog boxes.</span></span> <span data-ttu-id="fbf33-105">它也可讓網路系統管理員控制來源受到信任。</span><span class="sxs-lookup"><span data-stu-id="fbf33-105">It also gives a network administrator control sources to be trusted.</span></span>

<span data-ttu-id="fbf33-106">您可以使用下列程式，透過 CTL 驗證已簽署訊息的簽章。</span><span class="sxs-lookup"><span data-stu-id="fbf33-106">The following procedure can be used to verify the signature of a signed message by using a CTL.</span></span>

<span data-ttu-id="fbf33-107">**使用 CTL 驗證已簽署的訊息**</span><span class="sxs-lookup"><span data-stu-id="fbf33-107">**To verify a signed message by using a CTL**</span></span>

1.  <span data-ttu-id="fbf33-108">解碼訊息，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fbf33-108">Decode the message as follows:</span></span>

    1.  <span data-ttu-id="fbf33-109">取得已接收訊息的指標， (編碼的 [*BLOB*](../secgloss/b-gly.md)) 。</span><span class="sxs-lookup"><span data-stu-id="fbf33-109">Get a pointer to the received message (the encoded [*BLOB*](../secgloss/b-gly.md)).</span></span>
    2.  <span data-ttu-id="fbf33-110">呼叫 [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)，傳遞必要的引數。</span><span class="sxs-lookup"><span data-stu-id="fbf33-110">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
    3.  <span data-ttu-id="fbf33-111">呼叫 [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) 一次，並傳入步驟 b 中抓取的控制碼，以及要解碼之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="fbf33-111">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step b and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="fbf33-112">這會根據訊息類型，對訊息採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="fbf33-112">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>

2.  <span data-ttu-id="fbf33-113">確認已解碼、已簽署訊息的簽章，並取得簽署者憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。</span><span class="sxs-lookup"><span data-stu-id="fbf33-113">Verify the signature of the decoded, signed message, and get a pointer to the signer's [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

    <span data-ttu-id="fbf33-114">這可以藉由呼叫 [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner)來完成，並傳遞在步驟1c 中取出的訊息控制碼做為 *hCryptMsg* 參數。</span><span class="sxs-lookup"><span data-stu-id="fbf33-114">This can be done by calling [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the message handle retrieved in step 1c as the *hCryptMsg* parameter.</span></span> <span data-ttu-id="fbf33-115">如果函式呼叫傳回 **TRUE**，就會驗證簽章，並在 *ppSigner* 參數中傳回簽署者 [**PCCERT \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。</span><span class="sxs-lookup"><span data-stu-id="fbf33-115">If the function call returns **TRUE**, the signature was verified, and a pointer to the signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

3.  <span data-ttu-id="fbf33-116">確認簽署者是受信任的來源，如下所示：</span><span class="sxs-lookup"><span data-stu-id="fbf33-116">Confirm that the signer is a trusted source as follows:</span></span>

    1.  <span data-ttu-id="fbf33-117">開啟包含適當 CTL 的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="fbf33-117">Open the certificate store containing the appropriate CTL.</span></span>
    2.  <span data-ttu-id="fbf33-118">藉由呼叫 [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)來取得 [**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)的指標。</span><span class="sxs-lookup"><span data-stu-id="fbf33-118">Get a pointer to the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) by calling [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
    3.  <span data-ttu-id="fbf33-119">若要確認簽署者是受信任的來源，請呼叫 [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)，並傳遞在上一個步驟的 *pCtlCoNtext* 參數中所抓取的指標、 \_ \_ dwSubjectType 參數中的 CTL 憑證主體 \_ 類型，以及在 *pvSubject* 參數的步驟2中抓取的憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)指標。 </span><span class="sxs-lookup"><span data-stu-id="fbf33-119">To confirm that the signer is a trusted source, call [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), passing the pointer retrieved in the previous step in the *pCtlContext* parameter, CTL\_CERT\_SUBJECT\_TYPE in the *dwSubjectType* parameter, and the pointer to the [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) retrieved in step 2 in the *pvSubject* parameter.</span></span> <span data-ttu-id="fbf33-120">如果函式呼叫傳回 **TRUE**，則傳遞至函式的憑證 **\_ 內容** 是 CTL 中受信任的來源。</span><span class="sxs-lookup"><span data-stu-id="fbf33-120">If the function call returns **TRUE**, the **CERT\_CONTEXT** passed to the function is a trusted source in the CTL.</span></span>

 

 
