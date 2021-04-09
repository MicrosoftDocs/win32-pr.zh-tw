---
description: 在 Microsoft PKI 中，會將憑證要求從用戶端電腦傳送到憑證授權單位單位 (Ca) 為包含一連串編碼資料結構的二進位字串。
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: 憑證要求編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693004"
---
# <a name="certificate-request-encoding"></a><span data-ttu-id="9aac7-103">憑證要求編碼</span><span class="sxs-lookup"><span data-stu-id="9aac7-103">Certificate Request Encoding</span></span>

<span data-ttu-id="9aac7-104">在 Microsoft PKI 中，會將憑證要求從用戶端電腦傳送到憑證授權單位單位 (Ca) 為包含一連串編碼資料結構的二進位字串。</span><span class="sxs-lookup"><span data-stu-id="9aac7-104">In a Microsoft PKI, certificate requests are sent from client computers to certification authorities (CAs) as a binary string that contains a sequence of encoded data structures.</span></span> <span data-ttu-id="9aac7-105">憑證註冊 API 使用抽象語法標記法 (一)  (asn.1) 來描述及編碼這些結構。</span><span class="sxs-lookup"><span data-stu-id="9aac7-105">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to describe and encode these structures.</span></span> <span data-ttu-id="9aac7-106">基於本檔的目的，您可以在概念上將 asn.1 分為語法規則， (ISO 8824) 來描述資料結構，以及指定資料如何編碼以進行網路傳輸的編碼規則 (ISO 8825) 。</span><span class="sxs-lookup"><span data-stu-id="9aac7-106">For the purposes of this documentation, ASN.1 can be conceptually divided into the syntax rules (ISO 8824) that describe the data structures and the encoding rules (ISO 8825) that specify how the data is to be encoded for network transmission.</span></span> <span data-ttu-id="9aac7-107">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9aac7-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9aac7-108">ASN. 1 語法和編碼簡介</span><span class="sxs-lookup"><span data-stu-id="9aac7-108">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [<span data-ttu-id="9aac7-109">ASN. 1 類型系統</span><span class="sxs-lookup"><span data-stu-id="9aac7-109">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
-   [<span data-ttu-id="9aac7-110">可辨別編碼規則</span><span class="sxs-lookup"><span data-stu-id="9aac7-110">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)

## <a name="related-topics"></a><span data-ttu-id="9aac7-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="9aac7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aac7-112">關於憑證註冊 API</span><span class="sxs-lookup"><span data-stu-id="9aac7-112">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



