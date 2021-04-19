---
description: 憑證有相關聯的屬性，例如顯示名稱、描述和允許的用法，可供您查看和編輯。
ms.assetid: 23faaa03-af3e-4497-8607-4e34f8889368
title: 建立、查看及管理憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2136f8cd3ea3af1aab95b3c9c89ddd5787b4cefc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991816"
---
# <a name="creating-viewing-and-managing-certificates"></a><span data-ttu-id="9fc40-103">建立、查看及管理憑證</span><span class="sxs-lookup"><span data-stu-id="9fc40-103">Creating, Viewing, and Managing Certificates</span></span>

<span data-ttu-id="9fc40-104">[*憑證*](../secgloss/c-gly.md) 是唯讀結構。</span><span class="sxs-lookup"><span data-stu-id="9fc40-104">[*Certificates*](../secgloss/c-gly.md) are read-only structures.</span></span> <span data-ttu-id="9fc40-105">您可以查看憑證的內容，但無法修改。</span><span class="sxs-lookup"><span data-stu-id="9fc40-105">The contents of a certificate can be viewed but cannot be modified.</span></span> <span data-ttu-id="9fc40-106">憑證本身的資訊包括憑證的有效性日期、簽發者、主體和公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="9fc40-106">Information in the certificate itself includes the certificate's validity dates, issuer, subject, and the public key.</span></span> <span data-ttu-id="9fc40-107">不過，憑證有相關聯的屬性，例如顯示名稱、描述和允許的用法，可供您查看和編輯。</span><span class="sxs-lookup"><span data-stu-id="9fc40-107">However, certificates have associated properties, such as a display name, description, and allowed uses, that can be viewed and edited.</span></span>

<span data-ttu-id="9fc40-108">本節將示範如何建立測試憑證、查看憑證，以及管理憑證和其他安全性物件。</span><span class="sxs-lookup"><span data-stu-id="9fc40-108">This section demonstrates creating test certificates, viewing certificates, and managing certificates and other security objects.</span></span> <span data-ttu-id="9fc40-109">您可以使用 MakeCert 建立的憑證和 [*軟體發行者憑證*](../secgloss/s-gly.md) (SPCs) ，完全用於測試用途。</span><span class="sxs-lookup"><span data-stu-id="9fc40-109">The certificates and [*Software Publisher Certificates*](../secgloss/s-gly.md) (SPCs) that can be created with MakeCert are strictly for test purposes.</span></span> <span data-ttu-id="9fc40-110">測試 [*根憑證*](../secgloss/r-gly.md) 和測試根目錄 [*私密金鑰*](../secgloss/p-gly.md) 僅供測試之用。</span><span class="sxs-lookup"><span data-stu-id="9fc40-110">A test [*root certificate*](../secgloss/r-gly.md) and a test root [*private key*](../secgloss/p-gly.md) are provided for testing purposes only.</span></span> <span data-ttu-id="9fc40-111">獨立軟體廠商必須從 GTE、VeriSign、Inc. 或其他 [*憑證授權單位*](../secgloss/c-gly.md) 單位取得憑證 (CA) 來簽署將散發至公用的程式碼。</span><span class="sxs-lookup"><span data-stu-id="9fc40-111">Independent software vendors must obtain a certificate from GTE, VeriSign, Inc., or other [*certification authority*](../secgloss/c-gly.md) (CA) to sign code that will be distributed to the public.</span></span>

<span data-ttu-id="9fc40-112">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="9fc40-112">This section includes the following topics:</span></span>

-   [<span data-ttu-id="9fc40-113">使用 MakeCert</span><span class="sxs-lookup"><span data-stu-id="9fc40-113">Using MakeCert</span></span>](using-makecert.md)
-   [<span data-ttu-id="9fc40-114">使用 Cert2spc.exe</span><span class="sxs-lookup"><span data-stu-id="9fc40-114">Using Cert2SPC</span></span>](using-cert2spc.md)
-   [<span data-ttu-id="9fc40-115">使用 Certmgr.msc</span><span class="sxs-lookup"><span data-stu-id="9fc40-115">Using CertMgr</span></span>](using-certmgr.md)

 

 
