---
description: 指定用於簽署、封套和加密作業的演算法。
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: '演算法物件 (Capicom. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994572"
---
# <a name="algorithm-object"></a><span data-ttu-id="7ae57-103">演算法物件</span><span class="sxs-lookup"><span data-stu-id="7ae57-103">Algorithm object</span></span>

<span data-ttu-id="7ae57-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7ae57-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="7ae57-105">相反地，請使用 [**AlgorithmIdentifier 類別**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="7ae57-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7ae57-106">**演算法** 物件指定用於簽署、封套和加密作業的演算法。</span><span class="sxs-lookup"><span data-stu-id="7ae57-106">The **Algorithm** object specifies the algorithm used for signing, enveloping, and encrypting operations.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7ae57-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="7ae57-107">When to use</span></span>

<span data-ttu-id="7ae57-108">**演算法** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="7ae57-108">The **Algorithm** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="7ae57-109">設定或取出要使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="7ae57-109">Set or retrieve the algorithm to be used.</span></span>
-   <span data-ttu-id="7ae57-110">設定或取出金鑰長度。</span><span class="sxs-lookup"><span data-stu-id="7ae57-110">Set or retrieve the key length.</span></span>

> [!Note]  
> <span data-ttu-id="7ae57-111">CAPICOM 嘗試使用系統預設密碼編譯服務提供者 (CSP) 。</span><span class="sxs-lookup"><span data-stu-id="7ae57-111">CAPICOM attempts to use the system default cryptographic service provider (CSP).</span></span> <span data-ttu-id="7ae57-112">如果該 CSP 無法提供所要求的演算法或金鑰長度，則 CAPICOM 會搜尋可用的 Microsoft 提供的 CSP，以處理要求的演算法和金鑰長度（依此可用性順序）： Microsoft 增強型密碼編譯提供者、Microsoft 強式密碼編譯提供者、Microsoft 基礎密碼編譯提供者。</span><span class="sxs-lookup"><span data-stu-id="7ae57-112">If that CSP cannot provide the requested algorithm or key length, CAPICOM searches for an available Microsoft-provided CSP that can handle the requested algorithm and key length, in this order of availability: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span></span>

 

## <a name="members"></a><span data-ttu-id="7ae57-113">成員</span><span class="sxs-lookup"><span data-stu-id="7ae57-113">Members</span></span>

<span data-ttu-id="7ae57-114">**演算法** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7ae57-114">The **Algorithm** object has these types of members:</span></span>

-   [<span data-ttu-id="7ae57-115">屬性</span><span class="sxs-lookup"><span data-stu-id="7ae57-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ae57-116">屬性</span><span class="sxs-lookup"><span data-stu-id="7ae57-116">Properties</span></span>

<span data-ttu-id="7ae57-117">**演算法** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7ae57-117">The **Algorithm** object has these properties.</span></span>



| <span data-ttu-id="7ae57-118">屬性</span><span class="sxs-lookup"><span data-stu-id="7ae57-118">Property</span></span>                                            | <span data-ttu-id="7ae57-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="7ae57-119">Access type</span></span>           | <span data-ttu-id="7ae57-120">Description</span><span class="sxs-lookup"><span data-stu-id="7ae57-120">Description</span></span>                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae57-121">**KeyLength**</span><span class="sxs-lookup"><span data-stu-id="7ae57-121">**KeyLength**</span></span>](algorithm-keylength.md)<br/> | <span data-ttu-id="7ae57-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7ae57-122">Read/write</span></span><br/> | <span data-ttu-id="7ae57-123">設定或抓取索引鍵的長度。</span><span class="sxs-lookup"><span data-stu-id="7ae57-123">Sets or retrieves the length of the key.</span></span><br/>                                                                               |
| [<span data-ttu-id="7ae57-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="7ae57-124">**Name**</span></span>](algorithm-name.md)<br/>           | <span data-ttu-id="7ae57-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7ae57-125">Read/write</span></span><br/> | <span data-ttu-id="7ae57-126">設定或抓取用於簽署、封套和加密作業的演算法。</span><span class="sxs-lookup"><span data-stu-id="7ae57-126">Sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="7ae57-127">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="7ae57-127">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ae57-128">備註</span><span class="sxs-lookup"><span data-stu-id="7ae57-128">Remarks</span></span>

<span data-ttu-id="7ae57-129">無法建立 **演算法** 物件。</span><span class="sxs-lookup"><span data-stu-id="7ae57-129">The **Algorithm** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae57-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ae57-130">Requirements</span></span>



| <span data-ttu-id="7ae57-131">需求</span><span class="sxs-lookup"><span data-stu-id="7ae57-131">Requirement</span></span> | <span data-ttu-id="7ae57-132">值</span><span class="sxs-lookup"><span data-stu-id="7ae57-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae57-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7ae57-133">End of client support</span></span><br/> | <span data-ttu-id="7ae57-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ae57-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7ae57-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7ae57-135">End of server support</span></span><br/> | <span data-ttu-id="7ae57-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ae57-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7ae57-137">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7ae57-137">Redistributable</span></span><br/>       | <span data-ttu-id="7ae57-138">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7ae57-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7ae57-139">標頭</span><span class="sxs-lookup"><span data-stu-id="7ae57-139">Header</span></span><br/>                | <dl> <span data-ttu-id="7ae57-140"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="7ae57-140"><dt>Capicom.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ae57-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7ae57-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7ae57-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ae57-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae57-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ae57-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae57-144">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="7ae57-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
