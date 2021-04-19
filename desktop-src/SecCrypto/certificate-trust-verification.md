---
description: 簽署訊息的收件者與訊息的簽署者之間必須存在信任。
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: 憑證信任驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980580"
---
# <a name="certificate-trust-verification"></a><span data-ttu-id="9ca27-103">憑證信任驗證</span><span class="sxs-lookup"><span data-stu-id="9ca27-103">Certificate Trust Verification</span></span>

<span data-ttu-id="9ca27-104">簽署訊息的收件者與訊息的簽署者之間必須存在信任。</span><span class="sxs-lookup"><span data-stu-id="9ca27-104">A trust must exist between the recipient of a signed message and the signer of the message.</span></span> <span data-ttu-id="9ca27-105">建立此信任的其中一種方法是透過 [*憑證*](../secgloss/c-gly.md)，這是一份電子檔，可驗證實體或人員是否為他們宣稱的身分。</span><span class="sxs-lookup"><span data-stu-id="9ca27-105">One method of establishing this trust is through a [*certificate*](../secgloss/c-gly.md), an electronic document verifying that entities or persons are who they claim to be.</span></span> <span data-ttu-id="9ca27-106">憑證會由其他雙方所信任的協力廠商發行至實體。</span><span class="sxs-lookup"><span data-stu-id="9ca27-106">A certificate is issued to an entity by a third party that is trusted by both of the other parties.</span></span> <span data-ttu-id="9ca27-107">因此，簽署訊息的每個收件者都會決定簽署者憑證的簽發者是否值得信任。</span><span class="sxs-lookup"><span data-stu-id="9ca27-107">So, each recipient of a signed message decides if the issuer of the signer's certificate is trustworthy.</span></span> <span data-ttu-id="9ca27-108">[*CryptoAPI*](../secgloss/c-gly.md) 已實行一種方法，可讓應用程式開發人員建立應用程式，以根據預先定義的受信任憑證或 [*根*](../secgloss/r-gly.md)清單來自動驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="9ca27-108">[*CryptoAPI*](../secgloss/c-gly.md) has implemented a methodology to allow application developers to create applications that automatically verify certificates against a predefined list of trusted certificates or [*roots*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="9ca27-109">這份受信任的實體清單 (稱為主體) 稱為「 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 。</span><span class="sxs-lookup"><span data-stu-id="9ca27-109">This list of trusted entities (called subjects) is called a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

<span data-ttu-id="9ca27-110">下列使用 CTL 的範例牽涉到內部網路 (內部網路) 系統管理員想要控制哪些外部來源受到信任。</span><span class="sxs-lookup"><span data-stu-id="9ca27-110">The following example of using a CTL involves an intranet (intra-company network) administrator who wants to control just which outside sources are trusted.</span></span> <span data-ttu-id="9ca27-111">在此情況下，系統管理員可以建立受信任的憑證或根清單、簽署它，然後以 CTL 的形式將清單提供給網路上的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="9ca27-111">In this case, the administrator can create a list of trusted certificates or roots, sign it, and make the list available to all clients on the network in the form of a CTL.</span></span> <span data-ttu-id="9ca27-112">設計用來使用這項 CryptoAPI 功能的應用程式，只會接受已簽署的訊息，或是由清單中的實體所簽署的已下載軟體。</span><span class="sxs-lookup"><span data-stu-id="9ca27-112">An application designed to use this CryptoAPI functionality would then only accept signed messages or downloaded software that was signed by entities on the list.</span></span>

<span data-ttu-id="9ca27-113">如需這些函式的清單，請參閱 [憑證驗證功能](cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="9ca27-113">For a list of these functions, see [Certificate Verification Functions](cryptography-functions.md).</span></span>

 

 
