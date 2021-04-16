---
description: 當公開金鑰基礎結構中的已發行憑證數目 (PKI) 增加時，單一證書 (頒發機構單位) 可能會變得很難有效追蹤它所發行的憑證。
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: 憑證階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558912"
---
# <a name="certificate-hierarchy"></a><span data-ttu-id="c8866-103">憑證階層</span><span class="sxs-lookup"><span data-stu-id="c8866-103">Certificate Hierarchy</span></span>

<span data-ttu-id="c8866-104">當公開金鑰基礎結構中的已發行憑證數目 (PKI) 增加時，單一證書 (頒發機構單位) 可能會變得很難有效追蹤它所發行的憑證。</span><span class="sxs-lookup"><span data-stu-id="c8866-104">As the number of issued certificates in a public key infrastructure (PKI) increases, it can become difficult for a single certification authority (CA) to effectively track the certificates it has issued.</span></span> <span data-ttu-id="c8866-105">解決此問題的其中一種方式是建立憑證階層，CA 會將憑證頒發給次級授權單位，進而將授權委派給次級授權單位。</span><span class="sxs-lookup"><span data-stu-id="c8866-105">One way to address this is to create a certificate hierarchy in which the CA delegates the authority to issue certificates to subordinate authorities which can, in turn, delegate authority to their subordinates.</span></span> <span data-ttu-id="c8866-106">每個 CA 都會將 CA 憑證簽發給次級，以委派授權單位。</span><span class="sxs-lookup"><span data-stu-id="c8866-106">Each CA delegates authority by issuing a CA certificate to a subordinate.</span></span> <span data-ttu-id="c8866-107">鏈中的初始 CA 稱為「根」（root），而且實體不需要與實體所在的不同 [憑證鏈](about-certificate-chain.md) 上的任何 CA 建立信任關係。</span><span class="sxs-lookup"><span data-stu-id="c8866-107">The initial CA in the chain is called the root, and it is not necessary for an entity to establish trust with any CA that resides on a different [Certificate Chain](about-certificate-chain.md) from that on which the entity resides.</span></span>

<span data-ttu-id="c8866-108">下圖顯示由一個根 CA 組成的憑證階層、兩個附屬於根 CA 的 Ca， (一個用於行銷部門，另一個用於製造部門) ，另一個則是附屬於這些 CA 的 ca。</span><span class="sxs-lookup"><span data-stu-id="c8866-108">The following illustration shows a certificate hierarchy made up of one root CA, two CAs subordinate to the root (one for the marketing department and one for the manufacturing department), and CAs that are subordinate to these.</span></span>

![憑證階層圖](images/certificate-hierarchy.png)

## <a name="related-topics"></a><span data-ttu-id="c8866-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8866-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8866-111">信任模型</span><span class="sxs-lookup"><span data-stu-id="c8866-111">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



