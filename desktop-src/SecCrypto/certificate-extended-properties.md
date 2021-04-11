---
description: 憑證中的資料、憑證撤銷清單 (CRL) 或憑證信任清單 (CTL) 內容（包括任何擴充功能）都是唯讀的，而且無法變更。
ms.assetid: a9958c59-dc89-4d59-8ad3-6651ea4a1e56
title: 憑證擴充屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29853736433cb143a201ca352fceff0141cc96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114936"
---
# <a name="certificate-extended-properties"></a><span data-ttu-id="1c313-103">憑證擴充屬性</span><span class="sxs-lookup"><span data-stu-id="1c313-103">Certificate Extended Properties</span></span>

<span data-ttu-id="1c313-104">[*憑證*](../secgloss/c-gly.md)中的資料、[*憑證撤銷清單*](../secgloss/c-gly.md) (CRL) 或 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) [*內容*](../secgloss/c-gly.md)（包括任何擴充功能）都是唯讀的，而且無法變更。</span><span class="sxs-lookup"><span data-stu-id="1c313-104">The data in a [*certificate*](../secgloss/c-gly.md), [*certificate revocation list*](../secgloss/c-gly.md) (CRL), or [*certificate trust list*](../secgloss/c-gly.md) (CTL) [*context*](../secgloss/c-gly.md), including any extensions, is read-only and cannot be changed.</span></span> <span data-ttu-id="1c313-105">不過，在 Microsoft 平臺上，CryptoAPI 憑證也有可新增和變更的動態擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="1c313-105">However, on Microsoft platforms, CryptoAPI certificates also have dynamic extended properties that can be added and changed.</span></span>

> [!Note]  
> <span data-ttu-id="1c313-106">擴充屬性會與憑證相關聯，而且不是證書 [*頒發機構*](../secgloss/c-gly.md) 單位所簽發的憑證 (CA) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1c313-106">Extended properties are associated with a certificate and are not part of a certificate as issued by a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span> <span data-ttu-id="1c313-107">在非 Microsoft 平臺上使用擴充屬性時，憑證上無法使用它。</span><span class="sxs-lookup"><span data-stu-id="1c313-107">Extended properties are not available on a certificate when it is used on a non-Microsoft platform.</span></span>

 

<span data-ttu-id="1c313-108">這些屬性包含下列資料：</span><span class="sxs-lookup"><span data-stu-id="1c313-108">These properties include data that:</span></span>

-   <span data-ttu-id="1c313-109">適用于與憑證搭配使用的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="1c313-109">Pertains to the private key to be used with the certificate.</span></span>
-   <span data-ttu-id="1c313-110">表示要在憑證上執行的雜湊類型。</span><span class="sxs-lookup"><span data-stu-id="1c313-110">Indicates the type of hashes to be performed on the certificate.</span></span>
-   <span data-ttu-id="1c313-111">提供與憑證相關聯的使用者定義資訊。</span><span class="sxs-lookup"><span data-stu-id="1c313-111">Provides user-defined information associated with the certificate.</span></span>

<span data-ttu-id="1c313-112">在 Microsoft 平臺上，這些屬性的值會附加至憑證，並隨之移動。</span><span class="sxs-lookup"><span data-stu-id="1c313-112">On Microsoft platforms, values for these properties are attached to and move with the certificate.</span></span> <span data-ttu-id="1c313-113">目前使用屬性識別碼識別的預先定義屬性包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="1c313-113">Currently predefined properties identified with property IDs include the following properties:</span></span>

-   <span data-ttu-id="1c313-114">這些屬性會將憑證系結至特定的 CSP，並將該 CSP 內的特定私密金鑰系結至特定的私密金鑰：</span><span class="sxs-lookup"><span data-stu-id="1c313-114">These properties tie a certificate to a particular CSP and, within that CSP, to a particular private key:</span></span>
    -   <span data-ttu-id="1c313-115">CERT \_ KEY \_ >PROV \_ 句 \_ 柄 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="1c313-115">CERT\_KEY\_PROV\_HANDLE\_PROP\_ID</span></span>
    -   <span data-ttu-id="1c313-116">CERT \_ KEY \_ >PROV \_ INFO \_ 資訊 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="1c313-116">CERT\_KEY\_PROV\_INFO\_PROP\_ID</span></span>
    -   <span data-ttu-id="1c313-117">CERT \_ KEY \_ CONTEXT \_ 內容 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="1c313-117">CERT\_KEY\_CONTEXT\_PROP\_ID</span></span>
-   <span data-ttu-id="1c313-118">這些屬性工作表示執行雜湊作業時要使用的雜湊演算法：</span><span class="sxs-lookup"><span data-stu-id="1c313-118">These properties indicate the hashing algorithm to be used when a hashing operation is performed:</span></span>
    -   <span data-ttu-id="1c313-119">CERT \_ SHA1 \_ 雜湊的 \_ \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="1c313-119">CERT\_SHA1\_HASH\_PROP\_ID</span></span>
    -   <span data-ttu-id="1c313-120">CERT \_ MD5 \_ 雜湊的 \_ \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="1c313-120">CERT\_MD5\_HASH\_PROP\_ID</span></span>

<span data-ttu-id="1c313-121">如需目前定義之擴充憑證屬性的完整清單，以及每個屬性的意義與用法說明，請參閱 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 和 [**CertSetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)。</span><span class="sxs-lookup"><span data-stu-id="1c313-121">For complete lists of currently defined extended certificate properties and descriptions of the meaning and use of each property, see [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c313-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="1c313-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c313-123">**CertGetCRLCoNtextProperty**</span><span class="sxs-lookup"><span data-stu-id="1c313-123">**CertGetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="1c313-124">**CertGetCTLCoNtextProperty**</span><span class="sxs-lookup"><span data-stu-id="1c313-124">**CertGetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)
</dt> <dt>

[<span data-ttu-id="1c313-125">**CertSetCRLCoNtextProperty**</span><span class="sxs-lookup"><span data-stu-id="1c313-125">**CertSetCRLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)
</dt> <dt>

[<span data-ttu-id="1c313-126">**CertSetCTLCoNtextProperty**</span><span class="sxs-lookup"><span data-stu-id="1c313-126">**CertSetCTLContextProperty**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)
</dt> </dl>

 

 
