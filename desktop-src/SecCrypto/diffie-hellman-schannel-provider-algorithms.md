---
description: Diffie-Hellman 演算法的目的是要讓兩部或多部主機建立和共用相同的秘密加密金鑰，只要透過不安全的網路共用資訊就可以了。
ms.assetid: f89a1268-e364-41ec-a6a8-1f6331dbb787
title: Diffie-hellman/Schannel 提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4fb88e3a50e15a6690340ab3fbcee91da1193a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321032"
---
# <a name="diffie-hellmanschannel-provider-algorithms"></a><span data-ttu-id="ac175-103">Diffie-hellman/Schannel 提供者演算法</span><span class="sxs-lookup"><span data-stu-id="ac175-103">Diffie-Hellman/Schannel Provider Algorithms</span></span>

<span data-ttu-id="ac175-104">Diffie-Hellman 演算法的目的是要讓兩部或多部主機建立和共用相同的秘密加密金鑰，只要透過不安全的網路共用資訊就可以了。</span><span class="sxs-lookup"><span data-stu-id="ac175-104">The purpose of the Diffie-Hellman algorithm is to make it possible for two or more hosts to create and share an identical, secret encryption key, by simply sharing information over a network that is not secure.</span></span> <span data-ttu-id="ac175-105">透過網路共用的資訊是以一些常數值和 D-H 公開金鑰的形式呈現。</span><span class="sxs-lookup"><span data-stu-id="ac175-105">The information that gets shared over the network is in the form of a couple of constant values, and a D-H public key.</span></span>

<span data-ttu-id="ac175-106">Microsoft [*diffie-hellman*](../secgloss/d-gly.md) / [*Schannel*](../secgloss/s-gly.md)密碼編譯提供者支援下列演算法。</span><span class="sxs-lookup"><span data-stu-id="ac175-106">The Microsoft [*Diffie-Hellman*](../secgloss/d-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider supports the following algorithms.</span></span>



| <span data-ttu-id="ac175-107">演算法識別碼</span><span class="sxs-lookup"><span data-stu-id="ac175-107">Algorithm ID</span></span>                  | <span data-ttu-id="ac175-108">描述</span><span class="sxs-lookup"><span data-stu-id="ac175-108">Description</span></span>                                                                                                                                           | <span data-ttu-id="ac175-109">註解</span><span class="sxs-lookup"><span data-stu-id="ac175-109">Comments</span></span>                                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac175-110">CALG \_ DH \_ SF</span><span class="sxs-lookup"><span data-stu-id="ac175-110">CALG\_DH\_SF</span></span>                  | <span data-ttu-id="ac175-111">Diffie-Hellman 儲存和轉寄 [*金鑰交換演算法*](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="ac175-111">Diffie-Hellman store and forward [*key exchange algorithm*](../secgloss/k-gly.md)</span></span> | <span data-ttu-id="ac175-112">金鑰長度：可設定為8位遞增的384位到512位。</span><span class="sxs-lookup"><span data-stu-id="ac175-112">Key length: Can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="ac175-113">預設金鑰長度：512位。</span><span class="sxs-lookup"><span data-stu-id="ac175-113">Default key length: 512 bits.</span></span><br/> |
| <span data-ttu-id="ac175-114">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="ac175-114">CALG\_MD5</span></span>                     | <span data-ttu-id="ac175-115">MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="ac175-115">MD5 hashing algorithm.</span></span>                                                                                                                                | <span data-ttu-id="ac175-116">僅提供給雜湊之用。</span><span class="sxs-lookup"><span data-stu-id="ac175-116">Provided only for hashing.</span></span>                                                                                 |
| <span data-ttu-id="ac175-117">CALG \_ DH \_ EPHEM</span><span class="sxs-lookup"><span data-stu-id="ac175-117">CALG\_DH\_EPHEM</span></span>               | <span data-ttu-id="ac175-118">暫時的 D-H 金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="ac175-118">Ephemeral D-H key exchange.</span></span>                                                                                                                           | <span data-ttu-id="ac175-119">金鑰長度：可設定為8位遞增的384位到512位。</span><span class="sxs-lookup"><span data-stu-id="ac175-119">Key length: Can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="ac175-120">預設金鑰長度：512位。</span><span class="sxs-lookup"><span data-stu-id="ac175-120">Default key length: 512 bits.</span></span><br/> |
| <span data-ttu-id="ac175-121">CALG \_ SHA</span><span class="sxs-lookup"><span data-stu-id="ac175-121">CALG\_SHA</span></span>                     | <span data-ttu-id="ac175-122">SHA 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="ac175-122">SHA hashing algorithm.</span></span>                                                                                                                                | <span data-ttu-id="ac175-123">必須用於 DSS 簽章。</span><span class="sxs-lookup"><span data-stu-id="ac175-123">Must be used for DSS signatures.</span></span>                                                                           |
| <span data-ttu-id="ac175-124">CALG \_ RC2</span><span class="sxs-lookup"><span data-stu-id="ac175-124">CALG\_RC2</span></span>                     | <span data-ttu-id="ac175-125">RC2 區塊加密演算法</span><span class="sxs-lookup"><span data-stu-id="ac175-125">RC2 block encryption algorithm</span></span>                                                                                                                        | <span data-ttu-id="ac175-126">金鑰長度：40至88位。</span><span class="sxs-lookup"><span data-stu-id="ac175-126">Key length: 40 to 88 bits.</span></span>                                                                                 |
| <span data-ttu-id="ac175-127">CALG \_ RC4</span><span class="sxs-lookup"><span data-stu-id="ac175-127">CALG\_RC4</span></span>                     | <span data-ttu-id="ac175-128">RC4 串流加密演算法</span><span class="sxs-lookup"><span data-stu-id="ac175-128">RC4 stream encryption algorithm</span></span>                                                                                                                       | <span data-ttu-id="ac175-129">金鑰長度：40至88位。</span><span class="sxs-lookup"><span data-stu-id="ac175-129">Key length: 40 to 88 bits.</span></span>                                                                                 |
| <span data-ttu-id="ac175-130">CALG \_ CYLINK \_ MEK</span><span class="sxs-lookup"><span data-stu-id="ac175-130">CALG\_CYLINK\_ MEK</span></span><br/> | <span data-ttu-id="ac175-131">DES 變異加密演算法</span><span class="sxs-lookup"><span data-stu-id="ac175-131">DES variant encryption algorithm</span></span>                                                                                                                      | <span data-ttu-id="ac175-132">金鑰長度：40位。</span><span class="sxs-lookup"><span data-stu-id="ac175-132">Key length: 40 bits.</span></span>                                                                                       |



 

 

 
