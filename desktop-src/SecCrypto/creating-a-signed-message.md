---
description: 描述建立已簽署訊息時必須完成的工作。
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: 建立已簽署的訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193459"
---
# <a name="creating-a-signed-message"></a><span data-ttu-id="ba268-103">建立已簽署的訊息</span><span class="sxs-lookup"><span data-stu-id="ba268-103">Creating a Signed Message</span></span>

<span data-ttu-id="ba268-104">下圖說明建立已簽署訊息時必須完成的工作。</span><span class="sxs-lookup"><span data-stu-id="ba268-104">The following illustration depicts the tasks that must be accomplished to create a signed message.</span></span> <span data-ttu-id="ba268-105">這些步驟如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="ba268-105">The steps are listed following the illustration.</span></span>

![簽署訊息](images/signdmsg.png)

<span data-ttu-id="ba268-107">**若要建立已簽署的訊息**</span><span class="sxs-lookup"><span data-stu-id="ba268-107">**To create a signed message**</span></span>

1.  <span data-ttu-id="ba268-108">視需要建立資料 (，) 並取得其指標。</span><span class="sxs-lookup"><span data-stu-id="ba268-108">Create the data (if necessary) and get a pointer to it.</span></span>
2.  <span data-ttu-id="ba268-109">開啟包含簽署者憑證的 [*憑證存放區*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="ba268-109">Open a [*certificate store*](../secgloss/c-gly.md) that contains the signer's certificate.</span></span>
3.  <span data-ttu-id="ba268-110">取得憑證的 [*私密金鑰*](../secgloss/p-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="ba268-110">Get the [*private key*](../secgloss/p-gly.md) for the certificate.</span></span> <span data-ttu-id="ba268-111">在使用憑證之前，必須先在憑證上設定屬性，以將憑證系結至特定的 [*csp*](../secgloss/c-gly.md)，並將該 csp 內的憑證系結至特定的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="ba268-111">A property must be set on the certificate before using it, to tie a certificate to a particular [*CSP*](../secgloss/c-gly.md), and, within that CSP, to a particular private key.</span></span> <span data-ttu-id="ba268-112">這需要設定一次。</span><span class="sxs-lookup"><span data-stu-id="ba268-112">This needs to be set once.</span></span>
4.  <span data-ttu-id="ba268-113">選擇摘要作業的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="ba268-113">Choose a hashing algorithm for the digest operation.</span></span> <span data-ttu-id="ba268-114">我們建議您從可設定的位置選取雜湊演算法，以在不需要變更程式碼的情況下進行更新。</span><span class="sxs-lookup"><span data-stu-id="ba268-114">We recommend that the hashing algorithm be selected from a configurable location that can be subsequently updated without requiring changes to code.</span></span>
5.  <span data-ttu-id="ba268-115">使用雜湊演算法，透過雜湊函數傳送資料，藉此建立資料的 [*雜湊*](../secgloss/h-gly.md) (摘要) 。</span><span class="sxs-lookup"><span data-stu-id="ba268-115">Send the data through the hashing function by using the hashing algorithm, thus creating a [*hash*](../secgloss/h-gly.md) (digest) of the data.</span></span>
6.  <span data-ttu-id="ba268-116">使用透過憑證上的屬性取得的 [*私密金鑰*](../secgloss/p-gly.md) ，加密摘要，建立簽章。</span><span class="sxs-lookup"><span data-stu-id="ba268-116">Using the [*private key*](../secgloss/p-gly.md) obtained through the property on the certificate, encrypt the digest, creating the signature.</span></span>
7.  <span data-ttu-id="ba268-117">在簽署的訊息中包含下列內容：</span><span class="sxs-lookup"><span data-stu-id="ba268-117">Include the following in the signed message:</span></span>

    -   <span data-ttu-id="ba268-118">簽署的資料</span><span class="sxs-lookup"><span data-stu-id="ba268-118">The signed data</span></span>
    -   <span data-ttu-id="ba268-119">雜湊演算法</span><span class="sxs-lookup"><span data-stu-id="ba268-119">The hash algorithm</span></span>
    -   <span data-ttu-id="ba268-120">簽章</span><span class="sxs-lookup"><span data-stu-id="ba268-120">The signature</span></span>
    -   <span data-ttu-id="ba268-121">簽署者識別碼 (憑證簽發者和序號) </span><span class="sxs-lookup"><span data-stu-id="ba268-121">The signer identifier (certificate issuer and serial number)</span></span>
    -   <span data-ttu-id="ba268-122">簽署者的憑證 (選用) </span><span class="sxs-lookup"><span data-stu-id="ba268-122">The signer's certificate (optional)</span></span>

<span data-ttu-id="ba268-123">如需詳細的程式和範例，請參閱 [簽署資料](procedure-for-signing-data.md) 的 [程式和範例 C 程式：簽署訊息和驗證訊息簽](example-c-program-signing-a-message-and-verifying-a-message-signature.md)章。</span><span class="sxs-lookup"><span data-stu-id="ba268-123">For a detailed procedure and example, see [Procedure for Signing Data](procedure-for-signing-data.md) and [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
