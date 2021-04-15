---
description: 抽象語法標記法 (一)  (asn.1) 會定義下列規則集，以管理在電腦之間傳送的資料結構如何進行編碼和解碼。
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: 可辨別編碼規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511996"
---
# <a name="distinguished-encoding-rules"></a><span data-ttu-id="bd79a-103">可辨別編碼規則</span><span class="sxs-lookup"><span data-stu-id="bd79a-103">Distinguished Encoding Rules</span></span>

<span data-ttu-id="bd79a-104">抽象語法標記法 (一)  (asn.1) 會定義下列規則集，以管理在電腦之間傳送的資料結構如何進行編碼和解碼。</span><span class="sxs-lookup"><span data-stu-id="bd79a-104">Abstract Syntax Notation One (ASN.1) defines the following rule sets that govern how data structures that are being sent between computers are encoded and decoded.</span></span>

-   <span data-ttu-id="bd79a-105"> (BER) 的基本編碼規則</span><span class="sxs-lookup"><span data-stu-id="bd79a-105">Basic Encoding Rules (BER)</span></span>
-   <span data-ttu-id="bd79a-106">標準編碼規則 (CER) </span><span class="sxs-lookup"><span data-stu-id="bd79a-106">Canonical Encoding Rules (CER)</span></span>
-   <span data-ttu-id="bd79a-107">可辨別編碼規則 (DER) </span><span class="sxs-lookup"><span data-stu-id="bd79a-107">Distinguished Encoding Rules (DER)</span></span>
-   <span data-ttu-id="bd79a-108">每個)  (壓縮的編碼規則</span><span class="sxs-lookup"><span data-stu-id="bd79a-108">Packed Encoding Rules (PER)</span></span>

<span data-ttu-id="bd79a-109">原始規則集是由 BER 規格所定義。</span><span class="sxs-lookup"><span data-stu-id="bd79a-109">The original rule set was defined by the BER specification.</span></span> <span data-ttu-id="bd79a-110">CER 和 DER 之後是以 BER 的特製化子集的方式開發。</span><span class="sxs-lookup"><span data-stu-id="bd79a-110">CER and DER were developed later as specialized subsets of BER.</span></span> <span data-ttu-id="bd79a-111">針對使用 BER 或其變體傳輸資料所需的頻寬量，以回應用心發問也。</span><span class="sxs-lookup"><span data-stu-id="bd79a-111">PER was developed in response to criticisms about the amount of bandwidth required to transmit data using BER or its variants.</span></span> <span data-ttu-id="bd79a-112">每個可節省大量費用。</span><span class="sxs-lookup"><span data-stu-id="bd79a-112">PER provides a significant savings.</span></span>

<span data-ttu-id="bd79a-113">為了滿足 x.509 規格的安全資料傳輸需求而建立了 DER。</span><span class="sxs-lookup"><span data-stu-id="bd79a-113">DER was created to satisfy the requirements of the X.509 specification for secure data transfer.</span></span> <span data-ttu-id="bd79a-114">憑證註冊 API 會以獨佔方式使用 DER。</span><span class="sxs-lookup"><span data-stu-id="bd79a-114">The Certificate Enrollment API uses DER exclusively.</span></span> <span data-ttu-id="bd79a-115">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="bd79a-115">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="bd79a-116">DER 傳送語法</span><span class="sxs-lookup"><span data-stu-id="bd79a-116">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
-   [<span data-ttu-id="bd79a-117">以 DER 編碼的 ASN. 1 類型</span><span class="sxs-lookup"><span data-stu-id="bd79a-117">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a><span data-ttu-id="bd79a-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd79a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd79a-119">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="bd79a-119">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="bd79a-120">憑證要求編碼</span><span class="sxs-lookup"><span data-stu-id="bd79a-120">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="bd79a-121">ASN. 1 語法和編碼簡介</span><span class="sxs-lookup"><span data-stu-id="bd79a-121">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



