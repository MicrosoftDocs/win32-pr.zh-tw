---
description: 下表列出 Microsoft DSS 密碼編譯提供者所支援的演算法。
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: DSS 提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0bd9346da7a9ab1490e2646d9d2559c07359b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987530"
---
# <a name="dss-provider-algorithms"></a><span data-ttu-id="a62a7-103">DSS 提供者演算法</span><span class="sxs-lookup"><span data-stu-id="a62a7-103">DSS Provider Algorithms</span></span>

<span data-ttu-id="a62a7-104">下表列出 Microsoft DSS 密碼編譯提供者所支援的演算法。</span><span class="sxs-lookup"><span data-stu-id="a62a7-104">The following table lists the algorithms supported by the Microsoft DSS Cryptographic Provider.</span></span>



| <span data-ttu-id="a62a7-105">演算法識別碼</span><span class="sxs-lookup"><span data-stu-id="a62a7-105">Algorithm ID</span></span>    | <span data-ttu-id="a62a7-106">描述</span><span class="sxs-lookup"><span data-stu-id="a62a7-106">Description</span></span>                                 | <span data-ttu-id="a62a7-107">註解</span><span class="sxs-lookup"><span data-stu-id="a62a7-107">Comments</span></span>                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a62a7-108">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="a62a7-108">CALG\_MD5</span></span>       | <span data-ttu-id="a62a7-109">MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="a62a7-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="a62a7-110">僅提供給雜湊之用。</span><span class="sxs-lookup"><span data-stu-id="a62a7-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="a62a7-111">CALG \_ SHA</span><span class="sxs-lookup"><span data-stu-id="a62a7-111">CALG\_SHA</span></span>       | <span data-ttu-id="a62a7-112">SHA 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="a62a7-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="a62a7-113">必須用於 DSS 簽章。</span><span class="sxs-lookup"><span data-stu-id="a62a7-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="a62a7-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="a62a7-114">CALG\_SHA1</span></span>      | <span data-ttu-id="a62a7-115">與 CALG \_ SHA 相同。</span><span class="sxs-lookup"><span data-stu-id="a62a7-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="a62a7-116">不加評論。</span><span class="sxs-lookup"><span data-stu-id="a62a7-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="a62a7-117">CALG \_ DSS \_ SIGN</span><span class="sxs-lookup"><span data-stu-id="a62a7-117">CALG\_DSS\_SIGN</span></span> | <span data-ttu-id="a62a7-118">DSS 公開/私密金鑰簽章演算法。</span><span class="sxs-lookup"><span data-stu-id="a62a7-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="a62a7-119">金鑰長度：可設定為64位遞增的512位到1024位。</span><span class="sxs-lookup"><span data-stu-id="a62a7-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="a62a7-120">預設金鑰長度：1024位。</span><span class="sxs-lookup"><span data-stu-id="a62a7-120">Default key length: 1,024 bits.</span></span><br/> |



 

 

 




