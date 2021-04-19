---
description: CAPICOM \_ 雜湊 \_ 演算法列舉會定義雜湊演算法。
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: 'CAPICOM_HASH_ALGORITHM 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989796"
---
# <a name="capicom_hash_algorithm-enumeration"></a><span data-ttu-id="824c2-103">CAPICOM \_ 雜湊 \_ 演算法列舉</span><span class="sxs-lookup"><span data-stu-id="824c2-103">CAPICOM\_HASH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="824c2-104">**CAPICOM \_ 雜湊 \_ 演算法** 列舉會定義雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="824c2-104">The **CAPICOM\_HASH\_ALGORITHM** enumeration defines a hash algorithm.</span></span>

## <a name="members"></a><span data-ttu-id="824c2-105">成員</span><span class="sxs-lookup"><span data-stu-id="824c2-105">Members</span></span>



| <span data-ttu-id="824c2-106">member</span><span class="sxs-lookup"><span data-stu-id="824c2-106">Member</span></span>                                 | <span data-ttu-id="824c2-107">描述</span><span class="sxs-lookup"><span data-stu-id="824c2-107">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="824c2-108">值</span><span class="sxs-lookup"><span data-stu-id="824c2-108">Value</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="824c2-109">**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="824c2-109">**CAPICOM\_HASH\_ALGORITHM\_SHA1**</span></span>     | <span data-ttu-id="824c2-110"> (SHA) 的 [*安全雜湊演算法*](../secgloss/s-gly.md)，會產生160位訊息摘要。</span><span class="sxs-lookup"><span data-stu-id="824c2-110">[*Secure Hash Algorithm*](../secgloss/s-gly.md) (SHA) that generates a 160-bit message digest.</span></span><br/> | <span data-ttu-id="824c2-111">0</span><span class="sxs-lookup"><span data-stu-id="824c2-111">0</span></span>     |
| <span data-ttu-id="824c2-112">**CAPICOM \_ 雜湊 \_ 演算法 \_ MD2**</span><span class="sxs-lookup"><span data-stu-id="824c2-112">**CAPICOM\_HASH\_ALGORITHM\_MD2**</span></span>      | <span data-ttu-id="824c2-113">MD2 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="824c2-113">MD2 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="824c2-114">1</span><span class="sxs-lookup"><span data-stu-id="824c2-114">1</span></span>     |
| <span data-ttu-id="824c2-115">**CAPICOM \_ 雜湊 \_ 演算法 \_ MD4**</span><span class="sxs-lookup"><span data-stu-id="824c2-115">**CAPICOM\_HASH\_ALGORITHM\_MD4**</span></span>      | <span data-ttu-id="824c2-116">MD4 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="824c2-116">MD4 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="824c2-117">2</span><span class="sxs-lookup"><span data-stu-id="824c2-117">2</span></span>     |
| <span data-ttu-id="824c2-118">**CAPICOM \_ 雜湊 \_ 演算法 \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="824c2-118">**CAPICOM\_HASH\_ALGORITHM\_MD5**</span></span>      | <span data-ttu-id="824c2-119">MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="824c2-119">MD5 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="824c2-120">3</span><span class="sxs-lookup"><span data-stu-id="824c2-120">3</span></span>     |
| <span data-ttu-id="824c2-121">**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 256**</span><span class="sxs-lookup"><span data-stu-id="824c2-121">**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</span></span> | <span data-ttu-id="824c2-122">256 SHA-1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="824c2-122">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="824c2-123">**CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="824c2-123">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="824c2-124">4</span><span class="sxs-lookup"><span data-stu-id="824c2-124">4</span></span>     |
| <span data-ttu-id="824c2-125">**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 384**</span><span class="sxs-lookup"><span data-stu-id="824c2-125">**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</span></span> | <span data-ttu-id="824c2-126">384 SHA-1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="824c2-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="824c2-127">**CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="824c2-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="824c2-128">5</span><span class="sxs-lookup"><span data-stu-id="824c2-128">5</span></span>     |
| <span data-ttu-id="824c2-129">**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 512**</span><span class="sxs-lookup"><span data-stu-id="824c2-129">**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</span></span> | <span data-ttu-id="824c2-130">512 SHA-1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="824c2-130">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="824c2-131">**CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="824c2-131">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="824c2-132">6</span><span class="sxs-lookup"><span data-stu-id="824c2-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="824c2-133">備註</span><span class="sxs-lookup"><span data-stu-id="824c2-133">Remarks</span></span>

<span data-ttu-id="824c2-134">[**HashedData 演算法**](hasheddata-algorithm.md)屬性會使用 **CAPICOM \_ 雜湊 \_ 演算法** 列舉。</span><span class="sxs-lookup"><span data-stu-id="824c2-134">The **CAPICOM\_HASH\_ALGORITHM** enumeration is used by the [**HashedData.Algorithm**](hasheddata-algorithm.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="824c2-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="824c2-135">Requirements</span></span>



| <span data-ttu-id="824c2-136">需求</span><span class="sxs-lookup"><span data-stu-id="824c2-136">Requirement</span></span> | <span data-ttu-id="824c2-137">值</span><span class="sxs-lookup"><span data-stu-id="824c2-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="824c2-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="824c2-138">Redistributable</span></span><br/> | <span data-ttu-id="824c2-139">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="824c2-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="824c2-140">標頭</span><span class="sxs-lookup"><span data-stu-id="824c2-140">Header</span></span><br/>          | <dl> <span data-ttu-id="824c2-141"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="824c2-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 
