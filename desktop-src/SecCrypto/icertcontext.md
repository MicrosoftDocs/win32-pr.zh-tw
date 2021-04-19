---
description: 提供 CAPICOM x.509v3 憑證物件內容的存取權。 此內容可讓 CAPICOM 憑證用於其他的 CryptoAPI 衍生。
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: ICertCoNtext 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996280"
---
# <a name="icertcontext-interface"></a><span data-ttu-id="7c000-104">ICertCoNtext 介面</span><span class="sxs-lookup"><span data-stu-id="7c000-104">ICertContext interface</span></span>

<span data-ttu-id="7c000-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="7c000-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="7c000-106">**ICertCoNtext** 介面可讓您存取 CAPICOM x.509v3 [**憑證**](certificate.md)物件的內容。</span><span class="sxs-lookup"><span data-stu-id="7c000-106">The **ICertContext** interface provides access to the context of a CAPICOM X.509v3 [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="7c000-107">此內容可讓 CAPICOM 憑證用於其他的 CryptoAPI 衍生。</span><span class="sxs-lookup"><span data-stu-id="7c000-107">This context allows the CAPICOM certificate to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7c000-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="7c000-108">When to use</span></span>

<span data-ttu-id="7c000-109">當您需要在 CryptoAPI 的另一個衍生中使用 CAPICOM [**憑證**](certificate.md) 物件時，請使用此介面。</span><span class="sxs-lookup"><span data-stu-id="7c000-109">Use this interface when you need to use a CAPICOM [**Certificate**](certificate.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="7c000-110">成員</span><span class="sxs-lookup"><span data-stu-id="7c000-110">Members</span></span>

<span data-ttu-id="7c000-111">**ICertCoNtext** 介面具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7c000-111">The **ICertContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="7c000-112">方法</span><span class="sxs-lookup"><span data-stu-id="7c000-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7c000-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7c000-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7c000-114">方法</span><span class="sxs-lookup"><span data-stu-id="7c000-114">Methods</span></span>

<span data-ttu-id="7c000-115">**ICertCoNtext** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7c000-115">The **ICertContext** interface has these methods.</span></span>



| <span data-ttu-id="7c000-116">方法</span><span class="sxs-lookup"><span data-stu-id="7c000-116">Method</span></span>                                          | <span data-ttu-id="7c000-117">描述</span><span class="sxs-lookup"><span data-stu-id="7c000-117">Description</span></span>                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c000-118">**FreeCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7c000-118">**FreeContext**</span></span>](icertcontext-freecontext.md) | <span data-ttu-id="7c000-119">釋放 \_ 透過 [**CertCoNtext**](icertcontext-certcontext.md) 屬性取得的 PCCERT 內容。</span><span class="sxs-lookup"><span data-stu-id="7c000-119">Releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7c000-120">屬性</span><span class="sxs-lookup"><span data-stu-id="7c000-120">Properties</span></span>

<span data-ttu-id="7c000-121">**ICertCoNtext** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7c000-121">The **ICertContext** interface has these properties.</span></span>



| <span data-ttu-id="7c000-122">屬性</span><span class="sxs-lookup"><span data-stu-id="7c000-122">Property</span></span>                                                   | <span data-ttu-id="7c000-123">存取類型</span><span class="sxs-lookup"><span data-stu-id="7c000-123">Access type</span></span>           | <span data-ttu-id="7c000-124">Description</span><span class="sxs-lookup"><span data-stu-id="7c000-124">Description</span></span>                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="7c000-125">**CertCoNtext**</span><span class="sxs-lookup"><span data-stu-id="7c000-125">**CertContext**</span></span>](icertcontext-certcontext.md)<br/> | <span data-ttu-id="7c000-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7c000-126">Read/write</span></span><br/> | <span data-ttu-id="7c000-127">設定或抓取憑證的 PCCERT \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="7c000-127">Sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c000-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c000-128">Requirements</span></span>



| <span data-ttu-id="7c000-129">需求</span><span class="sxs-lookup"><span data-stu-id="7c000-129">Requirement</span></span> | <span data-ttu-id="7c000-130">值</span><span class="sxs-lookup"><span data-stu-id="7c000-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c000-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7c000-131">Redistributable</span></span><br/> | <span data-ttu-id="7c000-132">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7c000-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7c000-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7c000-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="7c000-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c000-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




