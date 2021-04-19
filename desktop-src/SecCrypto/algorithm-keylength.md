---
description: 設定或抓取索引鍵的長度。
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: KeyLength 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999320"
---
# <a name="algorithmkeylength-property"></a><span data-ttu-id="2ffe9-103">KeyLength 屬性</span><span class="sxs-lookup"><span data-stu-id="2ffe9-103">Algorithm.KeyLength property</span></span>

<span data-ttu-id="2ffe9-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="2ffe9-105">相反地，請使用 [**AlgorithmIdentifier 類別**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="2ffe9-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2ffe9-106">**KeyLength** 屬性會設定或抓取索引鍵的長度。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-106">The **KeyLength** property sets or retrieves the length of the key.</span></span>

<span data-ttu-id="2ffe9-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ffe9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ffe9-108">Syntax</span></span>


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a><span data-ttu-id="2ffe9-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="2ffe9-109">Property value</span></span>

<span data-ttu-id="2ffe9-110">指定金鑰長度之 [**CAPICOM \_ 加密 \_ 金鑰 \_ 長度**](capicom-encryption-key-length.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-110">A value of the [**CAPICOM\_ENCRYPTION\_KEY\_LENGTH**](capicom-encryption-key-length.md) enumeration that specifies the key length.</span></span> <span data-ttu-id="2ffe9-111">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="2ffe9-112">值</span><span class="sxs-lookup"><span data-stu-id="2ffe9-112">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="2ffe9-113">意義</span><span class="sxs-lookup"><span data-stu-id="2ffe9-113">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <span data-ttu-id="2ffe9-114"><dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 上限**</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe9-114"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</dt></span></span> </dl>     | <span data-ttu-id="2ffe9-115">使用指定的加密演算法所提供的最大金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-115">Use the maximum key length available with the indicated encryption algorithm.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <span data-ttu-id="2ffe9-116"><dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 40 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe9-116"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="2ffe9-117">使用40位的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-117">Use 40-bit keys.</span></span><br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <span data-ttu-id="2ffe9-118"><dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 56 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe9-118"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="2ffe9-119">使用56位金鑰（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-119">Use 56-bit keys if available.</span></span><br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <span data-ttu-id="2ffe9-120"><dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 128 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe9-120"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</dt></span></span> </dl> | <span data-ttu-id="2ffe9-121">使用128位金鑰（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-121">Use 128-bit keys if available.</span></span><br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <span data-ttu-id="2ffe9-122"><dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 192 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe9-122"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</dt></span></span> </dl> | <span data-ttu-id="2ffe9-123">使用192位的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-123">Use 192-bit keys.</span></span> <span data-ttu-id="2ffe9-124">此金鑰長度僅適用于 AES。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-124">This key length is available only for AES.</span></span><br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <span data-ttu-id="2ffe9-125"><dt>**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 256 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe9-125"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</dt></span></span> </dl> | <span data-ttu-id="2ffe9-126">使用256位的金鑰。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-126">Use 256-bit keys.</span></span> <span data-ttu-id="2ffe9-127">此金鑰長度僅適用于 AES。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-127">This key length is available only for AES.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2ffe9-128">備註</span><span class="sxs-lookup"><span data-stu-id="2ffe9-128">Remarks</span></span>

<span data-ttu-id="2ffe9-129">使用 DES 和3DES 加密演算法時，金鑰長度是標準的，而且會忽略 **KeyLength** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2ffe9-129">When DES and 3DES encryption algorithms are used, the key lengths are standard and the **KeyLength** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ffe9-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ffe9-130">Requirements</span></span>



| <span data-ttu-id="2ffe9-131">需求</span><span class="sxs-lookup"><span data-stu-id="2ffe9-131">Requirement</span></span> | <span data-ttu-id="2ffe9-132">值</span><span class="sxs-lookup"><span data-stu-id="2ffe9-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ffe9-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2ffe9-133">End of client support</span></span><br/> | <span data-ttu-id="2ffe9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ffe9-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2ffe9-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2ffe9-135">End of server support</span></span><br/> | <span data-ttu-id="2ffe9-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ffe9-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2ffe9-137">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2ffe9-137">Redistributable</span></span><br/>       | <span data-ttu-id="2ffe9-138">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2ffe9-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2ffe9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2ffe9-139">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2ffe9-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ffe9-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ffe9-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ffe9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ffe9-142">**演算法**</span><span class="sxs-lookup"><span data-stu-id="2ffe9-142">**Algorithm**</span></span>](algorithm.md)
</dt> </dl>

 

 
