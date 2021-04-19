---
description: 提供 CAPICOM 存放區物件內容的存取權。 此內容允許將 CAPICOM 憑證存放區用於其他的 CryptoAPI 衍生。
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: ICertStore 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989833"
---
# <a name="icertstore-interface"></a><span data-ttu-id="b10a5-104">ICertStore 介面</span><span class="sxs-lookup"><span data-stu-id="b10a5-104">ICertStore interface</span></span>

<span data-ttu-id="b10a5-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="b10a5-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="b10a5-106">**ICertStore** 介面可讓您存取 CAPICOM [**存放區**](store.md)物件的內容。</span><span class="sxs-lookup"><span data-stu-id="b10a5-106">The **ICertStore** interface provides access to the context of a CAPICOM [**Store**](store.md) object.</span></span> <span data-ttu-id="b10a5-107">此內容允許將 CAPICOM 憑證存放區用於其他的 CryptoAPI 衍生。</span><span class="sxs-lookup"><span data-stu-id="b10a5-107">This context allows the CAPICOM certificate store to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b10a5-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="b10a5-108">When to use</span></span>

<span data-ttu-id="b10a5-109">當您需要在 CryptoAPI 的另一個衍生中使用 CAPICOM [**存放區**](store.md) 物件時，請使用此介面。</span><span class="sxs-lookup"><span data-stu-id="b10a5-109">Use this interface when you need to use a CAPICOM [**Store**](store.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="b10a5-110">成員</span><span class="sxs-lookup"><span data-stu-id="b10a5-110">Members</span></span>

<span data-ttu-id="b10a5-111">**ICertStore** 介面具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b10a5-111">The **ICertStore** interface has these types of members:</span></span>

-   [<span data-ttu-id="b10a5-112">方法</span><span class="sxs-lookup"><span data-stu-id="b10a5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b10a5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b10a5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b10a5-114">方法</span><span class="sxs-lookup"><span data-stu-id="b10a5-114">Methods</span></span>

<span data-ttu-id="b10a5-115">**ICertStore** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b10a5-115">The **ICertStore** interface has these methods.</span></span>



| <span data-ttu-id="b10a5-116">方法</span><span class="sxs-lookup"><span data-stu-id="b10a5-116">Method</span></span>                                        | <span data-ttu-id="b10a5-117">描述</span><span class="sxs-lookup"><span data-stu-id="b10a5-117">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b10a5-118">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="b10a5-118">**CloseHandle**</span></span>](icertstore-closehandle.md) | <span data-ttu-id="b10a5-119">關閉透過 [**StoreHandle**](icertstore-storehandle.md) 屬性取得的 HCERTSTORE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="b10a5-119">Closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b10a5-120">屬性</span><span class="sxs-lookup"><span data-stu-id="b10a5-120">Properties</span></span>

<span data-ttu-id="b10a5-121">**ICertStore** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b10a5-121">The **ICertStore** interface has these properties.</span></span>



| <span data-ttu-id="b10a5-122">屬性</span><span class="sxs-lookup"><span data-stu-id="b10a5-122">Property</span></span>                                                     | <span data-ttu-id="b10a5-123">存取類型</span><span class="sxs-lookup"><span data-stu-id="b10a5-123">Access type</span></span>           | <span data-ttu-id="b10a5-124">Description</span><span class="sxs-lookup"><span data-stu-id="b10a5-124">Description</span></span>                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b10a5-125">**StoreHandle**</span><span class="sxs-lookup"><span data-stu-id="b10a5-125">**StoreHandle**</span></span>](icertstore-storehandle.md)<br/>     | <span data-ttu-id="b10a5-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b10a5-126">Read/write</span></span><br/> | <span data-ttu-id="b10a5-127">設定或抓取證書存儲的 HCERTSTORE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="b10a5-127">Sets or retrieves the HCERTSTORE handle of a certificate store.</span></span><br/>                                          |
| [<span data-ttu-id="b10a5-128">**StoreLocation**</span><span class="sxs-lookup"><span data-stu-id="b10a5-128">**StoreLocation**</span></span>](icertstore-storelocation.md)<br/> | <span data-ttu-id="b10a5-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b10a5-129">Read/write</span></span><br/> | <span data-ttu-id="b10a5-130">設定或抓取證書存儲的 [**CAPICOM \_ 存放區 \_ 位置**](capicom-store-location.md) 。</span><span class="sxs-lookup"><span data-stu-id="b10a5-130">Sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b10a5-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b10a5-131">Requirements</span></span>



| <span data-ttu-id="b10a5-132">需求</span><span class="sxs-lookup"><span data-stu-id="b10a5-132">Requirement</span></span> | <span data-ttu-id="b10a5-133">值</span><span class="sxs-lookup"><span data-stu-id="b10a5-133">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b10a5-134">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b10a5-134">Redistributable</span></span><br/> | <span data-ttu-id="b10a5-135">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b10a5-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b10a5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b10a5-136">DLL</span></span><br/>             | <dl> <span data-ttu-id="b10a5-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b10a5-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




