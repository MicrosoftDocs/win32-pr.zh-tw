---
description: CAPICOM \_ 金鑰 \_ 使用方法列舉會定義金鑰的使用方式。 在 CAPICOM 2.0 中引進。
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: 'CAPICOM_KEY_USAGE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000013"
---
# <a name="capicom_key_usage-enumeration"></a><span data-ttu-id="72ecd-104">CAPICOM \_ 金鑰 \_ 使用方法列舉</span><span class="sxs-lookup"><span data-stu-id="72ecd-104">CAPICOM\_KEY\_USAGE enumeration</span></span>

<span data-ttu-id="72ecd-105">**CAPICOM \_ 金鑰 \_ 使用** 方法列舉會定義金鑰的使用方式。</span><span class="sxs-lookup"><span data-stu-id="72ecd-105">The **CAPICOM\_KEY\_USAGE** enumeration defines the ways in which a key can be used.</span></span> <span data-ttu-id="72ecd-106">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="72ecd-106">Introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="72ecd-107">成員</span><span class="sxs-lookup"><span data-stu-id="72ecd-107">Members</span></span>



| <span data-ttu-id="72ecd-108">member</span><span class="sxs-lookup"><span data-stu-id="72ecd-108">Member</span></span>                                      | <span data-ttu-id="72ecd-109">描述</span><span class="sxs-lookup"><span data-stu-id="72ecd-109">Description</span></span>                                                                                                                      | <span data-ttu-id="72ecd-110">值</span><span class="sxs-lookup"><span data-stu-id="72ecd-110">Value</span></span>      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="72ecd-111">**CAPICOM \_ 數位 \_ 簽名 \_ 金鑰 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="72ecd-111">**CAPICOM\_DIGITAL\_SIGNATURE\_KEY\_USAGE**</span></span> | <span data-ttu-id="72ecd-112">金鑰可以用來建立數位簽章。</span><span class="sxs-lookup"><span data-stu-id="72ecd-112">The key can be used to create a digital signature.</span></span><br/>                                                                    | <span data-ttu-id="72ecd-113">0x00000080</span><span class="sxs-lookup"><span data-stu-id="72ecd-113">0x00000080</span></span> |
| <span data-ttu-id="72ecd-114">**CAPICOM \_ 不可 \_ 否認性 \_ 金鑰 \_ 使用方法**</span><span class="sxs-lookup"><span data-stu-id="72ecd-114">**CAPICOM\_NON\_REPUDIATION\_KEY\_USAGE**</span></span>   | <span data-ttu-id="72ecd-115">金鑰可用於不可 [*否認*](../secgloss/n-gly.md)性。</span><span class="sxs-lookup"><span data-stu-id="72ecd-115">The key can be used for [*nonrepudiation*](../secgloss/n-gly.md).</span></span><br/> | <span data-ttu-id="72ecd-116">0x00000040</span><span class="sxs-lookup"><span data-stu-id="72ecd-116">0x00000040</span></span> |
| <span data-ttu-id="72ecd-117">**CAPICOM \_ 金鑰 \_ 加密 \_ 金鑰 \_ 使用方法**</span><span class="sxs-lookup"><span data-stu-id="72ecd-117">**CAPICOM\_KEY\_ENCIPHERMENT\_KEY\_USAGE**</span></span>  | <span data-ttu-id="72ecd-118">金鑰可以用來加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="72ecd-118">The key can be used to encrypt a key.</span></span><br/>                                                                                 | <span data-ttu-id="72ecd-119">0x00000020</span><span class="sxs-lookup"><span data-stu-id="72ecd-119">0x00000020</span></span> |
| <span data-ttu-id="72ecd-120">**CAPICOM \_ 資料 \_ 加密 \_ 金鑰 \_ 使用方法**</span><span class="sxs-lookup"><span data-stu-id="72ecd-120">**CAPICOM\_DATA\_ENCIPHERMENT\_KEY\_USAGE**</span></span> | <span data-ttu-id="72ecd-121">金鑰可以用來加密資料。</span><span class="sxs-lookup"><span data-stu-id="72ecd-121">The key can be used to encrypt data.</span></span><br/>                                                                                  | <span data-ttu-id="72ecd-122">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72ecd-122">0x00000010</span></span> |
| <span data-ttu-id="72ecd-123">**CAPICOM \_ 金鑰 \_ 合約 \_ 金鑰 \_ 使用方法**</span><span class="sxs-lookup"><span data-stu-id="72ecd-123">**CAPICOM\_KEY\_AGREEMENT\_KEY\_USAGE**</span></span>     | <span data-ttu-id="72ecd-124">金鑰可用於金鑰協定。</span><span class="sxs-lookup"><span data-stu-id="72ecd-124">The key can be used for key agreement.</span></span><br/>                                                                                | <span data-ttu-id="72ecd-125">0x00000008</span><span class="sxs-lookup"><span data-stu-id="72ecd-125">0x00000008</span></span> |
| <span data-ttu-id="72ecd-126">**CAPICOM \_ 金鑰 \_ 憑證 \_ 簽署 \_ 金鑰 \_ 使用方法**</span><span class="sxs-lookup"><span data-stu-id="72ecd-126">**CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE**</span></span>    | <span data-ttu-id="72ecd-127">金鑰可用於金鑰憑證簽署。</span><span class="sxs-lookup"><span data-stu-id="72ecd-127">The key can be used for key certificate signing.</span></span> <span data-ttu-id="72ecd-128">此值相當於 CAPICOM \_ 離線 \_ CRL \_ 簽署 \_ 金鑰使用方式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="72ecd-128">This value is equivalent to CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE.</span></span><br/> | <span data-ttu-id="72ecd-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="72ecd-129">0x00000004</span></span> |
| <span data-ttu-id="72ecd-130">**CAPICOM \_ 離線 \_ CRL \_ 簽署 \_ 金鑰 \_ 使用方法**</span><span class="sxs-lookup"><span data-stu-id="72ecd-130">**CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE**</span></span> | <span data-ttu-id="72ecd-131">金鑰可用於金鑰憑證簽署。</span><span class="sxs-lookup"><span data-stu-id="72ecd-131">The key can be used for key certificate signing.</span></span> <span data-ttu-id="72ecd-132">此值相當於 CAPICOM \_ 金鑰憑證 \_ \_ 簽署 \_ 金鑰使用方式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="72ecd-132">This value is equivalent to CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE.</span></span><br/>    | <span data-ttu-id="72ecd-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72ecd-133">0x00000002</span></span> |
| <span data-ttu-id="72ecd-134">**CAPICOM \_ CRL \_ 簽署 \_ 金鑰 \_ 使用方法**</span><span class="sxs-lookup"><span data-stu-id="72ecd-134">**CAPICOM\_CRL\_SIGN\_KEY\_USAGE**</span></span>          | <span data-ttu-id="72ecd-135">金鑰可以用來簽署。</span><span class="sxs-lookup"><span data-stu-id="72ecd-135">The key can be used for signing.</span></span><br/>                                                                                      | <span data-ttu-id="72ecd-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="72ecd-136">0x00000002</span></span> |
| <span data-ttu-id="72ecd-137">**CAPICOM \_ \_ 只加密 \_ 金鑰 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="72ecd-137">**CAPICOM\_ENCIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="72ecd-138">金鑰只能用來加密。</span><span class="sxs-lookup"><span data-stu-id="72ecd-138">The key can only be used to encrypt.</span></span><br/>                                                                                  | <span data-ttu-id="72ecd-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72ecd-139">0x00000001</span></span> |
| <span data-ttu-id="72ecd-140">**CAPICOM \_ \_ 只解密 \_ 金鑰 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="72ecd-140">**CAPICOM\_DECIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="72ecd-141">金鑰只能用來解密。</span><span class="sxs-lookup"><span data-stu-id="72ecd-141">The key can only be used to decrypt.</span></span><br/>                                                                                  | <span data-ttu-id="72ecd-142">0x00008000</span><span class="sxs-lookup"><span data-stu-id="72ecd-142">0x00008000</span></span> |



## <a name="requirements"></a><span data-ttu-id="72ecd-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="72ecd-143">Requirements</span></span>



| <span data-ttu-id="72ecd-144">需求</span><span class="sxs-lookup"><span data-stu-id="72ecd-144">Requirement</span></span> | <span data-ttu-id="72ecd-145">值</span><span class="sxs-lookup"><span data-stu-id="72ecd-145">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72ecd-146">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="72ecd-146">Redistributable</span></span><br/> | <span data-ttu-id="72ecd-147">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="72ecd-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="72ecd-148">標頭</span><span class="sxs-lookup"><span data-stu-id="72ecd-148">Header</span></span><br/>          | <dl> <span data-ttu-id="72ecd-149"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="72ecd-149"><dt>Capicom.h</dt></span></span> </dl> |



 

 
