---
description: 設定或抓取所使用的雜湊演算法類型。
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: HashedData 演算法屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993980"
---
# <a name="hasheddataalgorithm-property"></a><span data-ttu-id="7c516-103">HashedData 演算法屬性</span><span class="sxs-lookup"><span data-stu-id="7c516-103">HashedData.Algorithm property</span></span>

<span data-ttu-id="7c516-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7c516-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7c516-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**HashAlgorithm 類別**](/previous-versions/windows/)。\]</span><span class="sxs-lookup"><span data-stu-id="7c516-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7c516-106">**演算法** 屬性會設定或抓取所使用的雜湊演算法類型。</span><span class="sxs-lookup"><span data-stu-id="7c516-106">The **Algorithm** property sets or retrieves the type of hashing algorithm used.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c516-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c516-107">Syntax</span></span>


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="7c516-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="7c516-108">Property value</span></span>

<span data-ttu-id="7c516-109">定義雜湊演算法之 [**CAPICOM \_ 雜湊 \_ 演算法**](capicom-hash-algorithm.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="7c516-109">A value of the [**CAPICOM\_HASH\_ALGORITHM**](capicom-hash-algorithm.md) enumeration that defines a hash algorithm.</span></span> <span data-ttu-id="7c516-110">預設值為 [CAPICOM \_ 雜湊 \_ 演算法 \_ SHA1]。</span><span class="sxs-lookup"><span data-stu-id="7c516-110">The default value is CAPICOM\_HASH\_ALGORITHM\_SHA1.</span></span> <span data-ttu-id="7c516-111">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="7c516-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="7c516-112">值</span><span class="sxs-lookup"><span data-stu-id="7c516-112">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="7c516-113">意義</span><span class="sxs-lookup"><span data-stu-id="7c516-113">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <span data-ttu-id="7c516-114"><dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA1**</dt></span><span class="sxs-lookup"><span data-stu-id="7c516-114"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA1**</dt></span></span> </dl>           | <span data-ttu-id="7c516-115">SHA1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7c516-115">SHA1 hashing algorithm.</span></span><br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <span data-ttu-id="7c516-116"><dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ MD2**</dt></span><span class="sxs-lookup"><span data-stu-id="7c516-116"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD2**</dt></span></span> </dl>              | <span data-ttu-id="7c516-117">MD2 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7c516-117">MD2 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <span data-ttu-id="7c516-118"><dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ MD4**</dt></span><span class="sxs-lookup"><span data-stu-id="7c516-118"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD4**</dt></span></span> </dl>              | <span data-ttu-id="7c516-119">MD4 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7c516-119">MD4 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <span data-ttu-id="7c516-120"><dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ MD5**</dt></span><span class="sxs-lookup"><span data-stu-id="7c516-120"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD5**</dt></span></span> </dl>              | <span data-ttu-id="7c516-121">MD5 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7c516-121">MD5 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <span data-ttu-id="7c516-122"><dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 256**</dt></span><span class="sxs-lookup"><span data-stu-id="7c516-122"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</dt></span></span> </dl> | <span data-ttu-id="7c516-123">256 SHA-1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7c516-123">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="7c516-124">**CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="7c516-124">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <span data-ttu-id="7c516-125"><dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 384**</dt></span><span class="sxs-lookup"><span data-stu-id="7c516-125"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</dt></span></span> </dl> | <span data-ttu-id="7c516-126">384 SHA-1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7c516-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="7c516-127">**CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="7c516-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <span data-ttu-id="7c516-128"><dt>**CAPICOM \_ 雜湊 \_ 演算法 \_ SHA \_ 512**</dt></span><span class="sxs-lookup"><span data-stu-id="7c516-128"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</dt></span></span> </dl> | <span data-ttu-id="7c516-129">512 SHA-1 雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7c516-129">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="7c516-130">**CAPICOM 2.0.0.3 和更早版本：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="7c516-130">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c516-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c516-131">Requirements</span></span>



| <span data-ttu-id="7c516-132">需求</span><span class="sxs-lookup"><span data-stu-id="7c516-132">Requirement</span></span> | <span data-ttu-id="7c516-133">值</span><span class="sxs-lookup"><span data-stu-id="7c516-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c516-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7c516-134">End of client support</span></span><br/> | <span data-ttu-id="7c516-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c516-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7c516-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7c516-136">End of server support</span></span><br/> | <span data-ttu-id="7c516-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c516-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7c516-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7c516-138">Redistributable</span></span><br/>       | <span data-ttu-id="7c516-139">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7c516-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7c516-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7c516-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7c516-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c516-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c516-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c516-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c516-143">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="7c516-143">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
