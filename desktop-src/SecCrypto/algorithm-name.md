---
description: 設定或抓取用於簽署、封套和加密作業的演算法。 這是預設屬性。
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Algorithm.Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994573"
---
# <a name="algorithmname-property"></a><span data-ttu-id="6b04d-104">Algorithm.Name 屬性</span><span class="sxs-lookup"><span data-stu-id="6b04d-104">Algorithm.Name property</span></span>

<span data-ttu-id="6b04d-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6b04d-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="6b04d-106">相反地，請使用 [**AlgorithmIdentifier 類別**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="6b04d-106">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6b04d-107">**Name** 屬性會設定或抓取用於簽署、封套和加密作業的演算法。</span><span class="sxs-lookup"><span data-stu-id="6b04d-107">The **Name** property sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="6b04d-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="6b04d-108">This is the default property.</span></span>

<span data-ttu-id="6b04d-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6b04d-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b04d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b04d-110">Syntax</span></span>


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="6b04d-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="6b04d-111">Property value</span></span>

<span data-ttu-id="6b04d-112">[**CAPICOM \_ 加密 \_ 演算法**](capicom-encryption-algorithm.md)列舉的值，可指定要使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="6b04d-112">A value of the [**CAPICOM\_ENCRYPTION\_ALGORITHM**](capicom-encryption-algorithm.md) enumeration that specifies which algorithm to use.</span></span> <span data-ttu-id="6b04d-113">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="6b04d-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="6b04d-114">值</span><span class="sxs-lookup"><span data-stu-id="6b04d-114">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="6b04d-115">意義</span><span class="sxs-lookup"><span data-stu-id="6b04d-115">Meaning</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <span data-ttu-id="6b04d-116"><dt>**CAPICOM \_ 加密 \_ 演算法 \_ RC2**</dt></span><span class="sxs-lookup"><span data-stu-id="6b04d-116"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</dt></span></span> </dl>    | <span data-ttu-id="6b04d-117">使用 RC2 加密。</span><span class="sxs-lookup"><span data-stu-id="6b04d-117">Use RC2 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <span data-ttu-id="6b04d-118"><dt>**CAPICOM \_ 加密 \_ 演算法 \_ RC4**</dt></span><span class="sxs-lookup"><span data-stu-id="6b04d-118"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</dt></span></span> </dl>    | <span data-ttu-id="6b04d-119">使用 RC4 加密。</span><span class="sxs-lookup"><span data-stu-id="6b04d-119">Use RC4 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <span data-ttu-id="6b04d-120"><dt>**CAPICOM \_ 加密 \_ 演算法 \_ DES**</dt></span><span class="sxs-lookup"><span data-stu-id="6b04d-120"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</dt></span></span> </dl>    | <span data-ttu-id="6b04d-121">使用 DES 加密。</span><span class="sxs-lookup"><span data-stu-id="6b04d-121">Use DES encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <span data-ttu-id="6b04d-122"><dt>**CAPICOM \_ 加密 \_ 演算法 \_ 3des**</dt></span><span class="sxs-lookup"><span data-stu-id="6b04d-122"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</dt></span></span> </dl> | <span data-ttu-id="6b04d-123">使用三重 DES 加密。</span><span class="sxs-lookup"><span data-stu-id="6b04d-123">Use triple DES encryption.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <span data-ttu-id="6b04d-124"><dt>**CAPICOM \_ 加密 \_ 演算法 \_ AES**</dt></span><span class="sxs-lookup"><span data-stu-id="6b04d-124"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</dt></span></span> </dl>    | <span data-ttu-id="6b04d-125">使用 AES 演算法。</span><span class="sxs-lookup"><span data-stu-id="6b04d-125">Use the AES algorithm.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6b04d-126">備註</span><span class="sxs-lookup"><span data-stu-id="6b04d-126">Remarks</span></span>

<span data-ttu-id="6b04d-127">當這個屬性的值是直接或間接重設時，會重設物件的整個狀態。</span><span class="sxs-lookup"><span data-stu-id="6b04d-127">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b04d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b04d-128">Requirements</span></span>



| <span data-ttu-id="6b04d-129">需求</span><span class="sxs-lookup"><span data-stu-id="6b04d-129">Requirement</span></span> | <span data-ttu-id="6b04d-130">值</span><span class="sxs-lookup"><span data-stu-id="6b04d-130">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b04d-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6b04d-131">End of client support</span></span><br/> | <span data-ttu-id="6b04d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b04d-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6b04d-133">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6b04d-133">End of server support</span></span><br/> | <span data-ttu-id="6b04d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b04d-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6b04d-135">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6b04d-135">Redistributable</span></span><br/>       | <span data-ttu-id="6b04d-136">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6b04d-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6b04d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6b04d-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6b04d-138"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b04d-138"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
