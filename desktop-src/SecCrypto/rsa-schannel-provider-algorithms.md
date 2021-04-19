---
description: Microsoft RSA/Schannel 密碼編譯提供者可能會支援演算法。
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: RSA/Schannel 提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973295"
---
# <a name="rsaschannel-provider-algorithms"></a><span data-ttu-id="d5d05-103">RSA/Schannel 提供者演算法</span><span class="sxs-lookup"><span data-stu-id="d5d05-103">RSA/Schannel Provider Algorithms</span></span>

<span data-ttu-id="d5d05-104">Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md)密碼編譯提供者可能支援下列演算法。</span><span class="sxs-lookup"><span data-stu-id="d5d05-104">The following algorithms might be supported by the Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.</span></span>



| <span data-ttu-id="d5d05-105">演算法識別碼</span><span class="sxs-lookup"><span data-stu-id="d5d05-105">Algorithm ID</span></span>    | <span data-ttu-id="d5d05-106">描述</span><span class="sxs-lookup"><span data-stu-id="d5d05-106">Description</span></span>                                                                                                                         | <span data-ttu-id="d5d05-107">註解</span><span class="sxs-lookup"><span data-stu-id="d5d05-107">Comments</span></span>                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d05-108">CALG \_ RSA \_ KEYX</span><span class="sxs-lookup"><span data-stu-id="d5d05-108">CALG\_RSA\_KEYX</span></span> | <span data-ttu-id="d5d05-109">RSA 公開金鑰 [*金鑰交換演算法*](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="d5d05-109">RSA public key [*key exchange algorithm*](../secgloss/k-gly.md)</span></span> | <span data-ttu-id="d5d05-110">金鑰長度：可設定為8位遞增的384位到16384位。</span><span class="sxs-lookup"><span data-stu-id="d5d05-110">Key length: Can be set, 384 bits to 16,384 bits in 8 bit increments.</span></span> <span data-ttu-id="d5d05-111">預設金鑰長度：1024位。</span><span class="sxs-lookup"><span data-stu-id="d5d05-111">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="d5d05-112">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="d5d05-112">CALG\_MD5</span></span>       | <span data-ttu-id="d5d05-113">MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="d5d05-113">MD5 hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="d5d05-114">僅提供給雜湊之用。</span><span class="sxs-lookup"><span data-stu-id="d5d05-114">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="d5d05-115">CALG \_ SHA</span><span class="sxs-lookup"><span data-stu-id="d5d05-115">CALG\_SHA</span></span>       | <span data-ttu-id="d5d05-116">SHA 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="d5d05-116">SHA hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="d5d05-117">必須用於 DSS 簽章。</span><span class="sxs-lookup"><span data-stu-id="d5d05-117">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="d5d05-118">CALG \_ RC2</span><span class="sxs-lookup"><span data-stu-id="d5d05-118">CALG\_RC2</span></span>       | <span data-ttu-id="d5d05-119">RC2 區塊加密演算法。</span><span class="sxs-lookup"><span data-stu-id="d5d05-119">RC2 block encryption algorithm.</span></span>                                                                                                     | <span data-ttu-id="d5d05-120">金鑰長度：40至88位</span><span class="sxs-lookup"><span data-stu-id="d5d05-120">Key length: 40 to 88 bits</span></span>                                                                                       |
| <span data-ttu-id="d5d05-121">CALG \_ RC4</span><span class="sxs-lookup"><span data-stu-id="d5d05-121">CALG\_RC4</span></span>       | <span data-ttu-id="d5d05-122">RC4 資料流程加密演算法。</span><span class="sxs-lookup"><span data-stu-id="d5d05-122">RC4 stream encryption algorithm.</span></span>                                                                                                    | <span data-ttu-id="d5d05-123">金鑰長度：40至88位</span><span class="sxs-lookup"><span data-stu-id="d5d05-123">Key length: 40 to 88 bits</span></span>                                                                                       |



 

 

 
