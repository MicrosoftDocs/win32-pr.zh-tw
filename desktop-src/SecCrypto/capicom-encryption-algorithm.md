---
description: 定義要用於加密和解密的演算法。
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: 'CAPICOM_ENCRYPTION_ALGORITHM 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977520"
---
# <a name="capicom_encryption_algorithm-enumeration"></a><span data-ttu-id="75b57-103">CAPICOM \_ 加密 \_ 演算法列舉</span><span class="sxs-lookup"><span data-stu-id="75b57-103">CAPICOM\_ENCRYPTION\_ALGORITHM enumeration</span></span>

<span data-ttu-id="75b57-104">**CAPICOM \_ 加密 \_ 演算法** 列舉型別會定義要用於加密和解密的演算法。</span><span class="sxs-lookup"><span data-stu-id="75b57-104">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type defines the algorithms to be used in encryption and decryption.</span></span>

## <a name="members"></a><span data-ttu-id="75b57-105">成員</span><span class="sxs-lookup"><span data-stu-id="75b57-105">Members</span></span>



| <span data-ttu-id="75b57-106">member</span><span class="sxs-lookup"><span data-stu-id="75b57-106">Member</span></span>                                   | <span data-ttu-id="75b57-107">描述</span><span class="sxs-lookup"><span data-stu-id="75b57-107">Description</span></span>                                                                                                                                                                                              | <span data-ttu-id="75b57-108">值</span><span class="sxs-lookup"><span data-stu-id="75b57-108">Value</span></span>     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="75b57-109">**CAPICOM \_ 加密 \_ 演算法 \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="75b57-109">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</span></span>  | <span data-ttu-id="75b57-110">使用 RSA RC2 加密。</span><span class="sxs-lookup"><span data-stu-id="75b57-110">Use RSA RC2 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="75b57-111">0</span><span class="sxs-lookup"><span data-stu-id="75b57-111">0</span></span>         |
| <span data-ttu-id="75b57-112">**CAPICOM \_ 加密 \_ 演算法 \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="75b57-112">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</span></span>  | <span data-ttu-id="75b57-113">使用 RSA RC4 加密。</span><span class="sxs-lookup"><span data-stu-id="75b57-113">Use RSA RC4 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="75b57-114">1</span><span class="sxs-lookup"><span data-stu-id="75b57-114">1</span></span>         |
| <span data-ttu-id="75b57-115">**CAPICOM \_ 加密 \_ 演算法 \_ DES**</span><span class="sxs-lookup"><span data-stu-id="75b57-115">**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</span></span>  | <span data-ttu-id="75b57-116">使用 DES 加密。</span><span class="sxs-lookup"><span data-stu-id="75b57-116">Use DES encryption.</span></span><br/>                                                                                                                                                                           | <span data-ttu-id="75b57-117">2</span><span class="sxs-lookup"><span data-stu-id="75b57-117">2</span></span>         |
| <span data-ttu-id="75b57-118">**CAPICOM \_ 加密 \_ 演算法 \_ 3des**</span><span class="sxs-lookup"><span data-stu-id="75b57-118">**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</span></span> | <span data-ttu-id="75b57-119">使用三重 DES 加密。</span><span class="sxs-lookup"><span data-stu-id="75b57-119">Use triple DES encryption.</span></span><br/>                                                                                                                                                                    | <span data-ttu-id="75b57-120">3</span><span class="sxs-lookup"><span data-stu-id="75b57-120">3</span></span>         |
| <span data-ttu-id="75b57-121">**CAPICOM \_ 加密 \_ 演算法 \_ AES**</span><span class="sxs-lookup"><span data-stu-id="75b57-121">**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</span></span>  | <span data-ttu-id="75b57-122">使用 [*進階加密標準*](../secgloss/a-gly.md) (AES) 演算法。</span><span class="sxs-lookup"><span data-stu-id="75b57-122">Use the [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) algorithm.</span></span> <span data-ttu-id="75b57-123">此值只對 [**a**](encrypteddata.md) 物件有效。</span><span class="sxs-lookup"><span data-stu-id="75b57-123">This value is valid for the [**EncryptedData**](encrypteddata.md) object only.</span></span><br/> | <span data-ttu-id="75b57-124">4//v 2。0</span><span class="sxs-lookup"><span data-stu-id="75b57-124">4 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="75b57-125">備註</span><span class="sxs-lookup"><span data-stu-id="75b57-125">Remarks</span></span>

<span data-ttu-id="75b57-126">[**Algorithm.Name**](algorithm-name.md)屬性使用了 **CAPICOM \_ 加密 \_ 演算法** 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="75b57-126">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type is used by the [**Algorithm.Name**](algorithm-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b57-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="75b57-127">Requirements</span></span>



| <span data-ttu-id="75b57-128">需求</span><span class="sxs-lookup"><span data-stu-id="75b57-128">Requirement</span></span> | <span data-ttu-id="75b57-129">值</span><span class="sxs-lookup"><span data-stu-id="75b57-129">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75b57-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="75b57-130">Redistributable</span></span><br/> | <span data-ttu-id="75b57-131">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="75b57-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="75b57-132">標頭</span><span class="sxs-lookup"><span data-stu-id="75b57-132">Header</span></span><br/>          | <dl> <span data-ttu-id="75b57-133"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="75b57-133"><dt>Capicom.h</dt></span></span> </dl> |



 

 
