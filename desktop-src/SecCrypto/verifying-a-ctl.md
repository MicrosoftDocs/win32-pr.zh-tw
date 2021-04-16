---
description: 若要讓 interloper 更難將假憑證信任清單替換為現有憑證的 (CTL) ，請在每次使用 CTL 時，確認 CTL 上的簽章。
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: 驗證 CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512404"
---
# <a name="verifying-a-ctl"></a><span data-ttu-id="c75a1-103">驗證 CTL</span><span class="sxs-lookup"><span data-stu-id="c75a1-103">Verifying a CTL</span></span>

<span data-ttu-id="c75a1-104">若要讓 interloper 更難將假 [*憑證信任清單*](../secgloss/c-gly.md) 替換為現有憑證的 (CTL) ，請在每次使用 ctl 時，確認 ctl 上的簽章。</span><span class="sxs-lookup"><span data-stu-id="c75a1-104">To make it more difficult for an interloper to substitute a bogus [*certificate trust list*](../secgloss/c-gly.md) (CTL) for an existing one, verify the signature on the CTL each time the CTL is used.</span></span> <span data-ttu-id="c75a1-105">請勿使用不包含受信任簽章的 CTL。</span><span class="sxs-lookup"><span data-stu-id="c75a1-105">Do not use a CTL that does not contain a trusted signature.</span></span>

<span data-ttu-id="c75a1-106">**驗證 CTL 簽章**</span><span class="sxs-lookup"><span data-stu-id="c75a1-106">**To verify a CTL signature**</span></span>

1.  <span data-ttu-id="c75a1-107">開啟包含所需 CTL 的 [*憑證存放區*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="c75a1-107">Open the [*certificate store*](../secgloss/c-gly.md) containing the desired CTL.</span></span>
2.  <span data-ttu-id="c75a1-108">取得 CTL 的 [**ctl \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="c75a1-108">Get a handle to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) for the CTL.</span></span> <span data-ttu-id="c75a1-109">這可以藉由呼叫將控制碼傳回到 **CTL \_ 內容**（例如 [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)）的任何函式來完成。</span><span class="sxs-lookup"><span data-stu-id="c75a1-109">This can be done by calling any of the functions that return a handle to the **CTL\_CONTEXT**, such as [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
3.  <span data-ttu-id="c75a1-110">呼叫 [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner)，傳遞在 *hCryptMsg* 參數的步驟2中抓取的 [**CTL \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)，此為憑證存放區的控制碼，其中包含 *rghSignerStore* 參數中 ctl 之信任來源的憑證，以及 \_ dwFlags 參數中的 CMSG 受信任 \_ 簽署者 \_ 旗標。 </span><span class="sxs-lookup"><span data-stu-id="c75a1-110">Call [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) retrieved in step 2 in the *hCryptMsg* parameter, a handle to the certificate store containing the certificate of the trusted source for CTLs in the *rghSignerStore* parameter, and the CMSG\_TRUSTED\_SIGNER\_FLAG in the *dwFlags* parameter.</span></span> <span data-ttu-id="c75a1-111">如果函式傳回 **TRUE**，就會驗證簽章，並在 *ppSigner* 參數中傳回 CTL 簽署者 [**PCCERT \_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)的指標。</span><span class="sxs-lookup"><span data-stu-id="c75a1-111">If the function returns **TRUE**, the signature was verified, and a pointer to the CTL signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

 

 
