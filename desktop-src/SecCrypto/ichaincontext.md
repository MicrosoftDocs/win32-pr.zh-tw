---
description: 提供 CAPICOM 鏈物件內容的存取權。 此內容允許將 CAPICOM 憑證信任鏈用於其他的 CryptoAPI 衍生。
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: IChainCoNtext 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001489"
---
# <a name="ichaincontext-interface"></a><span data-ttu-id="ef92c-104">IChainCoNtext 介面</span><span class="sxs-lookup"><span data-stu-id="ef92c-104">IChainContext interface</span></span>

<span data-ttu-id="ef92c-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="ef92c-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="ef92c-106">**IChainCoNtext** 介面可讓您存取 CAPICOM [**鏈**](chain.md)物件的內容。</span><span class="sxs-lookup"><span data-stu-id="ef92c-106">The **IChainContext** interface provides access to the context of a CAPICOM [**Chain**](chain.md) object.</span></span> <span data-ttu-id="ef92c-107">此內容允許將 CAPICOM 憑證信任鏈用於其他的 CryptoAPI 衍生。</span><span class="sxs-lookup"><span data-stu-id="ef92c-107">This context allows the CAPICOM certificate trust chain to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ef92c-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="ef92c-108">When to use</span></span>

<span data-ttu-id="ef92c-109">當您需要在 CryptoAPI 的另一個衍生中使用 CAPICOM [**鏈**](chain.md) 物件時，請使用此介面。</span><span class="sxs-lookup"><span data-stu-id="ef92c-109">Use this interface when you need to use a CAPICOM [**Chain**](chain.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="ef92c-110">成員</span><span class="sxs-lookup"><span data-stu-id="ef92c-110">Members</span></span>

<span data-ttu-id="ef92c-111">**IChainCoNtext** 介面具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ef92c-111">The **IChainContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="ef92c-112">方法</span><span class="sxs-lookup"><span data-stu-id="ef92c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ef92c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ef92c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ef92c-114">方法</span><span class="sxs-lookup"><span data-stu-id="ef92c-114">Methods</span></span>

<span data-ttu-id="ef92c-115">**IChainCoNtext** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ef92c-115">The **IChainContext** interface has these methods.</span></span>



| <span data-ttu-id="ef92c-116">方法</span><span class="sxs-lookup"><span data-stu-id="ef92c-116">Method</span></span>                                           | <span data-ttu-id="ef92c-117">描述</span><span class="sxs-lookup"><span data-stu-id="ef92c-117">Description</span></span>                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef92c-118">**FreeCoNtext**</span><span class="sxs-lookup"><span data-stu-id="ef92c-118">**FreeContext**</span></span>](ichaincontext-freecontext.md) | <span data-ttu-id="ef92c-119">釋放 \_ \_ 透過 [**ChainCoNtext**](ichaincontext-chaincontext.md) 屬性取得的 PCCERT 鏈內容。</span><span class="sxs-lookup"><span data-stu-id="ef92c-119">Releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ef92c-120">屬性</span><span class="sxs-lookup"><span data-stu-id="ef92c-120">Properties</span></span>

<span data-ttu-id="ef92c-121">**IChainCoNtext** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ef92c-121">The **IChainContext** interface has these properties.</span></span>



| <span data-ttu-id="ef92c-122">屬性</span><span class="sxs-lookup"><span data-stu-id="ef92c-122">Property</span></span>                                                      | <span data-ttu-id="ef92c-123">存取類型</span><span class="sxs-lookup"><span data-stu-id="ef92c-123">Access type</span></span>           | <span data-ttu-id="ef92c-124">Description</span><span class="sxs-lookup"><span data-stu-id="ef92c-124">Description</span></span>                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="ef92c-125">**ChainCoNtext**</span><span class="sxs-lookup"><span data-stu-id="ef92c-125">**ChainContext**</span></span>](ichaincontext-chaincontext.md)<br/> | <span data-ttu-id="ef92c-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ef92c-126">Read/write</span></span><br/> | <span data-ttu-id="ef92c-127">設定或抓取憑證的 PCCERT \_ 鏈 \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="ef92c-127">Sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef92c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef92c-128">Requirements</span></span>



| <span data-ttu-id="ef92c-129">需求</span><span class="sxs-lookup"><span data-stu-id="ef92c-129">Requirement</span></span> | <span data-ttu-id="ef92c-130">值</span><span class="sxs-lookup"><span data-stu-id="ef92c-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef92c-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ef92c-131">Redistributable</span></span><br/> | <span data-ttu-id="ef92c-132">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ef92c-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ef92c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ef92c-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="ef92c-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef92c-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




