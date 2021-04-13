---
description: 許多功能都需要憑證或訊息編碼類型。
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: 憑證和訊息編碼類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468933"
---
# <a name="certificate-and-message-encoding-types"></a><span data-ttu-id="38836-103">憑證和訊息編碼類型</span><span class="sxs-lookup"><span data-stu-id="38836-103">Certificate and Message Encoding Types</span></span>

<span data-ttu-id="38836-104">許多功能都需要憑證或 [*訊息編碼類型*](../secgloss/m-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="38836-104">Many of the functions require certificate or [*message encoding types*](../secgloss/m-gly.md).</span></span> <span data-ttu-id="38836-105">此編碼類型為 **DWORD**，可能包含憑證和訊息編碼類型。</span><span class="sxs-lookup"><span data-stu-id="38836-105">This encoding type is a **DWORD**, possibly containing both the certificate and message encoding types.</span></span> <span data-ttu-id="38836-106">憑證編碼類型會儲存在低序位字組中。</span><span class="sxs-lookup"><span data-stu-id="38836-106">The certificate encoding type is stored in the low-order word.</span></span> <span data-ttu-id="38836-107">訊息編碼類型會儲存在高序位字組中。</span><span class="sxs-lookup"><span data-stu-id="38836-107">The message encoding type is stored in the high-order word.</span></span> <span data-ttu-id="38836-108">某些函數或結構欄位只需要其中一種編碼類型，但一律可接受同時指定這兩種編碼類型。</span><span class="sxs-lookup"><span data-stu-id="38836-108">Some functions or structure fields require only one of the encoding types, but it is always acceptable to specify both encoding types.</span></span> <span data-ttu-id="38836-109">如需同時指定編碼類型的範例，請參閱[ \# 包含和 \# 定義](-includes-and--defines.md)。</span><span class="sxs-lookup"><span data-stu-id="38836-109">For an example specifying both encoding types, see [\#includes and \#defines](-includes-and--defines.md).</span></span>

<span data-ttu-id="38836-110">下列參數命名慣例可用來指出所需的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="38836-110">The following parameter naming convention is used to indicate the encoding types required.</span></span>



| <span data-ttu-id="38836-111">Name</span><span class="sxs-lookup"><span data-stu-id="38836-111">Name</span></span>                       | <span data-ttu-id="38836-112">註解</span><span class="sxs-lookup"><span data-stu-id="38836-112">Comments</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38836-113">*dwMsgAndCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="38836-113">*dwMsgAndCertEncodingType*</span></span> | <span data-ttu-id="38836-114">這兩種編碼類型都是必要的。</span><span class="sxs-lookup"><span data-stu-id="38836-114">Both encoding types are required.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="38836-115">*dwMsgEncodingType*</span><span class="sxs-lookup"><span data-stu-id="38836-115">*dwMsgEncodingType*</span></span>        | <span data-ttu-id="38836-116">只需要訊息編碼類型。</span><span class="sxs-lookup"><span data-stu-id="38836-116">Only the message encoding type is required.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="38836-117">*dwCertEncodingType*</span><span class="sxs-lookup"><span data-stu-id="38836-117">*dwCertEncodingType*</span></span>       | <span data-ttu-id="38836-118">只需要憑證編碼類型。</span><span class="sxs-lookup"><span data-stu-id="38836-118">Only the certificate encoding type is required.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="38836-119">*dwEncodingType*</span><span class="sxs-lookup"><span data-stu-id="38836-119">*dwEncodingType*</span></span>           | <span data-ttu-id="38836-120">需要訊息或憑證編碼類型。</span><span class="sxs-lookup"><span data-stu-id="38836-120">Either a message or certificate encoding type is required.</span></span> <span data-ttu-id="38836-121">如果包含憑證編碼類型的低序位字組為非零值，則會使用它。</span><span class="sxs-lookup"><span data-stu-id="38836-121">If the low-order word containing the certificate encoding type is nonzero, then it is used.</span></span> <span data-ttu-id="38836-122">否則，會使用包含訊息編碼類型的高序位字組。</span><span class="sxs-lookup"><span data-stu-id="38836-122">Otherwise, the high-order word containing the message encoding type is used.</span></span> <span data-ttu-id="38836-123">如果同時指定這兩者，則會使用低序位字組中的憑證編碼類型。</span><span class="sxs-lookup"><span data-stu-id="38836-123">If both are specified, the certificate encoding type in the low-order word is used.</span></span> |



 

<span data-ttu-id="38836-124">下表顯示目前定義的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="38836-124">Currently defined encoding types are shown in the following table.</span></span>



| <span data-ttu-id="38836-125">編碼類型</span><span class="sxs-lookup"><span data-stu-id="38836-125">Encoding type</span></span>          | <span data-ttu-id="38836-126">值</span><span class="sxs-lookup"><span data-stu-id="38836-126">Value</span></span>      |
|------------------------|------------|
| <span data-ttu-id="38836-127">CRYPT \_ ASN \_ 編碼</span><span class="sxs-lookup"><span data-stu-id="38836-127">CRYPT\_ASN\_ENCODING</span></span>   | <span data-ttu-id="38836-128">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38836-128">0x00000001</span></span> |
| <span data-ttu-id="38836-129">X509 \_ ASN \_ 編碼</span><span class="sxs-lookup"><span data-stu-id="38836-129">X509\_ASN\_ENCODING</span></span>    | <span data-ttu-id="38836-130">0x00000001</span><span class="sxs-lookup"><span data-stu-id="38836-130">0x00000001</span></span> |
| <span data-ttu-id="38836-131">PKCS \_ 7 \_ ASN \_ 編碼</span><span class="sxs-lookup"><span data-stu-id="38836-131">PKCS\_7\_ASN\_ENCODING</span></span> | <span data-ttu-id="38836-132">0x00010000</span><span class="sxs-lookup"><span data-stu-id="38836-132">0x00010000</span></span> |



 

 

 
