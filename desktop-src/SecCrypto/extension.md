---
description: 代表單一憑證延伸。
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: '擴充物件 (Mmcobj .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990579"
---
# <a name="extension-object"></a><span data-ttu-id="4c8ac-103">Extension 物件</span><span class="sxs-lookup"><span data-stu-id="4c8ac-103">Extension object</span></span>

<span data-ttu-id="4c8ac-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4c8ac-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="4c8ac-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4c8ac-106">**擴充** 物件代表單一憑證延伸。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-106">The **Extension** object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4c8ac-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="4c8ac-107">When to use</span></span>

<span data-ttu-id="4c8ac-108">**擴充** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="4c8ac-108">The **Extension** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4c8ac-109">取出憑證延伸的 OID。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-109">Retrieve the OID of the certificate extension.</span></span>
-   <span data-ttu-id="4c8ac-110">取出 [**EncodedData**](encodeddata.md) 物件所代表的憑證擴充資料。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-110">Retrieve the certificate extension data represented by an [**EncodedData**](encodeddata.md) object.</span></span>
-   <span data-ttu-id="4c8ac-111">判斷憑證延伸是否標記為「重大」。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-111">Determine whether the certificate extension is marked as critical.</span></span>

## <a name="members"></a><span data-ttu-id="4c8ac-112">成員</span><span class="sxs-lookup"><span data-stu-id="4c8ac-112">Members</span></span>

<span data-ttu-id="4c8ac-113">**擴充** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4c8ac-113">The **Extension** object has these types of members:</span></span>

-   [<span data-ttu-id="4c8ac-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4c8ac-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c8ac-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4c8ac-115">Properties</span></span>

<span data-ttu-id="4c8ac-116">**擴充** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-116">The **Extension** object has these properties.</span></span>



| <span data-ttu-id="4c8ac-117">屬性</span><span class="sxs-lookup"><span data-stu-id="4c8ac-117">Property</span></span>                                                | <span data-ttu-id="4c8ac-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="4c8ac-118">Access type</span></span>          | <span data-ttu-id="4c8ac-119">Description</span><span class="sxs-lookup"><span data-stu-id="4c8ac-119">Description</span></span>                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c8ac-120">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="4c8ac-120">**EncodedData**</span></span>](extension-encodeddata.md)<br/> | <span data-ttu-id="4c8ac-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="4c8ac-121">Read-only</span></span><br/> | <span data-ttu-id="4c8ac-122">抓取延伸模組的編碼資料。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-122">Retrieves the encoded data for the extension.</span></span><br/>                                      |
| [<span data-ttu-id="4c8ac-123">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="4c8ac-123">**IsCritical**</span></span>](extension-iscritical.md)<br/>   | <span data-ttu-id="4c8ac-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="4c8ac-124">Read-only</span></span><br/> | <span data-ttu-id="4c8ac-125">抓取布林值，指出是否將延伸標記為重大。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-125">Retrieves a Boolean value that indicates whether the extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="4c8ac-126">**老**</span><span class="sxs-lookup"><span data-stu-id="4c8ac-126">**OID**</span></span>](extension-oid.md)<br/>                 | <span data-ttu-id="4c8ac-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="4c8ac-127">Read-only</span></span><br/> | <span data-ttu-id="4c8ac-128">抓取延伸模組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-128">Retrieves the object identifier for the extension.</span></span> <span data-ttu-id="4c8ac-129">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-129">This is the default property.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="4c8ac-130">備註</span><span class="sxs-lookup"><span data-stu-id="4c8ac-130">Remarks</span></span>

<span data-ttu-id="4c8ac-131">無法建立 **擴充** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-131">The **Extension** object cannot be created.</span></span>

<span data-ttu-id="4c8ac-132">[**擴充**](extensions.md)功能集合物件會使用 **擴充** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-132">The **Extension** object is used by the [**Extensions**](extensions.md) collection object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c8ac-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c8ac-133">Requirements</span></span>



| <span data-ttu-id="4c8ac-134">需求</span><span class="sxs-lookup"><span data-stu-id="4c8ac-134">Requirement</span></span> | <span data-ttu-id="4c8ac-135">值</span><span class="sxs-lookup"><span data-stu-id="4c8ac-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8ac-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4c8ac-136">End of client support</span></span><br/> | <span data-ttu-id="4c8ac-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c8ac-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4c8ac-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4c8ac-138">End of server support</span></span><br/> | <span data-ttu-id="4c8ac-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c8ac-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4c8ac-140">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4c8ac-140">Redistributable</span></span><br/>       | <span data-ttu-id="4c8ac-141">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4c8ac-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4c8ac-142">標頭</span><span class="sxs-lookup"><span data-stu-id="4c8ac-142">Header</span></span><br/>                | <dl> <span data-ttu-id="4c8ac-143"><dt>Mmcobj。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ac-143"><dt>Mmcobj.h</dt></span></span> </dl>    |
| <span data-ttu-id="4c8ac-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4c8ac-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4c8ac-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c8ac-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
