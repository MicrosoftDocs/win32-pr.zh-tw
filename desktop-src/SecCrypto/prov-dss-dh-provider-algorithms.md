---
description: Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者所支援的演算法。
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: PROV_DSS_DH 提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978194"
---
# <a name="prov_dss_dh-provider-algorithms"></a><span data-ttu-id="49cd0-103">>PROV \_ DSS \_ DH 提供者演算法</span><span class="sxs-lookup"><span data-stu-id="49cd0-103">PROV\_DSS\_DH Provider Algorithms</span></span>

<span data-ttu-id="49cd0-104">下表列出 Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者所支援的演算法。</span><span class="sxs-lookup"><span data-stu-id="49cd0-104">The following table lists the algorithms supported by the Microsoft Base DSS and Diffie-Hellman Cryptographic Provider.</span></span>



| <span data-ttu-id="49cd0-105">演算法識別碼</span><span class="sxs-lookup"><span data-stu-id="49cd0-105">Algorithm ID</span></span>      | <span data-ttu-id="49cd0-106">描述</span><span class="sxs-lookup"><span data-stu-id="49cd0-106">Description</span></span>                                 | <span data-ttu-id="49cd0-107">註解</span><span class="sxs-lookup"><span data-stu-id="49cd0-107">Comments</span></span>                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49cd0-108">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="49cd0-108">CALG\_MD5</span></span>         | <span data-ttu-id="49cd0-109">MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="49cd0-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="49cd0-110">僅提供給雜湊之用。</span><span class="sxs-lookup"><span data-stu-id="49cd0-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="49cd0-111">CALG \_ SHA</span><span class="sxs-lookup"><span data-stu-id="49cd0-111">CALG\_SHA</span></span>         | <span data-ttu-id="49cd0-112">SHA 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="49cd0-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="49cd0-113">必須用於 DSS 簽章。</span><span class="sxs-lookup"><span data-stu-id="49cd0-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="49cd0-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="49cd0-114">CALG\_SHA1</span></span>        | <span data-ttu-id="49cd0-115">與 CALG \_ SHA 相同。</span><span class="sxs-lookup"><span data-stu-id="49cd0-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="49cd0-116">不加評論。</span><span class="sxs-lookup"><span data-stu-id="49cd0-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="49cd0-117">CALG \_ DSS \_ SIGN</span><span class="sxs-lookup"><span data-stu-id="49cd0-117">CALG\_DSS\_SIGN</span></span>   | <span data-ttu-id="49cd0-118">DSS 公開/私密金鑰簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="49cd0-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="49cd0-119">金鑰長度：可設定為64位遞增的512位到1024位。</span><span class="sxs-lookup"><span data-stu-id="49cd0-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="49cd0-120">預設金鑰長度：1024位。</span><span class="sxs-lookup"><span data-stu-id="49cd0-120">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="49cd0-121">CALG \_ DH \_ SF</span><span class="sxs-lookup"><span data-stu-id="49cd0-121">CALG\_DH\_SF</span></span>      | <span data-ttu-id="49cd0-122">儲存和轉寄 D-H 金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="49cd0-122">Store and Forward D-H key exchange.</span></span>         | <span data-ttu-id="49cd0-123">金鑰長度：可設定為8位遞增的384位到512位。</span><span class="sxs-lookup"><span data-stu-id="49cd0-123">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="49cd0-124">預設金鑰長度：512位。</span><span class="sxs-lookup"><span data-stu-id="49cd0-124">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="49cd0-125">CALG \_ DH \_ EPHEM</span><span class="sxs-lookup"><span data-stu-id="49cd0-125">CALG\_DH\_EPHEM</span></span>   | <span data-ttu-id="49cd0-126">暫時的 D-H 金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="49cd0-126">Ephemeral D-H key exchange.</span></span>                 | <span data-ttu-id="49cd0-127">金鑰長度：可設定為8位遞增的384位到512位。</span><span class="sxs-lookup"><span data-stu-id="49cd0-127">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="49cd0-128">預設金鑰長度：512位。</span><span class="sxs-lookup"><span data-stu-id="49cd0-128">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="49cd0-129">CALG \_ CYLINK \_ MEK</span><span class="sxs-lookup"><span data-stu-id="49cd0-129">CALG\_CYLINK\_MEK</span></span> | <span data-ttu-id="49cd0-130">DES 金鑰的40位變異。</span><span class="sxs-lookup"><span data-stu-id="49cd0-130">A 40-bit variant of a DES key.</span></span>              | <span data-ttu-id="49cd0-131">金鑰長度：40位。</span><span class="sxs-lookup"><span data-stu-id="49cd0-131">Key Length: 40 bits.</span></span>                                                                                            |



 

 

 




