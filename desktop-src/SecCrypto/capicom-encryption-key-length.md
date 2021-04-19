---
description: 定義要用於加密的金鑰長度。
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: 'CAPICOM_ENCRYPTION_KEY_LENGTH 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995512"
---
# <a name="capicom_encryption_key_length-enumeration"></a><span data-ttu-id="d5453-103">CAPICOM \_ 加密 \_ 金鑰 \_ 長度列舉</span><span class="sxs-lookup"><span data-stu-id="d5453-103">CAPICOM\_ENCRYPTION\_KEY\_LENGTH enumeration</span></span>

<span data-ttu-id="d5453-104">**CAPICOM \_ 加密 \_ 金鑰 \_ 長度** 列舉類型會定義要在加密中使用的 [*金鑰長度*](../secgloss/k-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="d5453-104">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type defines the [*key length*](../secgloss/k-gly.md) to be used in encryption.</span></span>

## <a name="members"></a><span data-ttu-id="d5453-105">成員</span><span class="sxs-lookup"><span data-stu-id="d5453-105">Members</span></span>



| <span data-ttu-id="d5453-106">member</span><span class="sxs-lookup"><span data-stu-id="d5453-106">Member</span></span>                                          | <span data-ttu-id="d5453-107">描述</span><span class="sxs-lookup"><span data-stu-id="d5453-107">Description</span></span>                                                                               | <span data-ttu-id="d5453-108">值</span><span class="sxs-lookup"><span data-stu-id="d5453-108">Value</span></span>     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d5453-109">**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 上限**</span><span class="sxs-lookup"><span data-stu-id="d5453-109">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</span></span>   | <span data-ttu-id="d5453-110">使用指定的加密演算法所提供的最大金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="d5453-110">Uses the maximum key length available with the indicated encryption algorithm.</span></span><br/> | <span data-ttu-id="d5453-111">0</span><span class="sxs-lookup"><span data-stu-id="d5453-111">0</span></span>         |
| <span data-ttu-id="d5453-112">**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 40 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="d5453-112">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</span></span>  | <span data-ttu-id="d5453-113">使用40位的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d5453-113">Uses 40-bit keys.</span></span><br/>                                                              | <span data-ttu-id="d5453-114">1</span><span class="sxs-lookup"><span data-stu-id="d5453-114">1</span></span>         |
| <span data-ttu-id="d5453-115">**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 56 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="d5453-115">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</span></span>  | <span data-ttu-id="d5453-116">使用56位金鑰（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d5453-116">Uses 56-bit keys if available.</span></span><br/>                                                 | <span data-ttu-id="d5453-117">2</span><span class="sxs-lookup"><span data-stu-id="d5453-117">2</span></span>         |
| <span data-ttu-id="d5453-118">**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 128 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="d5453-118">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</span></span> | <span data-ttu-id="d5453-119">使用128位金鑰（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d5453-119">Uses 128-bit keys if available.</span></span><br/>                                                | <span data-ttu-id="d5453-120">3</span><span class="sxs-lookup"><span data-stu-id="d5453-120">3</span></span>         |
| <span data-ttu-id="d5453-121">**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 192 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="d5453-121">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</span></span> | <span data-ttu-id="d5453-122">使用192位的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d5453-122">Uses 192-bit keys.</span></span> <span data-ttu-id="d5453-123">此金鑰長度僅適用于 AES。</span><span class="sxs-lookup"><span data-stu-id="d5453-123">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="d5453-124">4//v 2。0</span><span class="sxs-lookup"><span data-stu-id="d5453-124">4 // v2.0</span></span> |
| <span data-ttu-id="d5453-125">**CAPICOM \_ 加密 \_ 金鑰 \_ 長度 \_ 256 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="d5453-125">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</span></span> | <span data-ttu-id="d5453-126">使用256位的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d5453-126">Uses 256-bit keys.</span></span> <span data-ttu-id="d5453-127">此金鑰長度僅適用于 AES。</span><span class="sxs-lookup"><span data-stu-id="d5453-127">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="d5453-128">5//v 2。0</span><span class="sxs-lookup"><span data-stu-id="d5453-128">5 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="d5453-129">備註</span><span class="sxs-lookup"><span data-stu-id="d5453-129">Remarks</span></span>

<span data-ttu-id="d5453-130">[**KeyLength**](algorithm-keylength.md)屬性使用了 **CAPICOM \_ 加密 \_ 金鑰 \_ 長度** 列舉類型。</span><span class="sxs-lookup"><span data-stu-id="d5453-130">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type is used by the [**Algorithm.KeyLength**](algorithm-keylength.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5453-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5453-131">Requirements</span></span>



| <span data-ttu-id="d5453-132">需求</span><span class="sxs-lookup"><span data-stu-id="d5453-132">Requirement</span></span> | <span data-ttu-id="d5453-133">值</span><span class="sxs-lookup"><span data-stu-id="d5453-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5453-134">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d5453-134">Redistributable</span></span><br/> | <span data-ttu-id="d5453-135">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d5453-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="d5453-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d5453-136">Header</span></span><br/>          | <dl> <span data-ttu-id="d5453-137"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="d5453-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 
