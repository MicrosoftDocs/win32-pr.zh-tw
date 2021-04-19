---
description: 表示 Microsoft 擴充的屬性。
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: ExtendedProperty 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998861"
---
# <a name="extendedproperty-object"></a><span data-ttu-id="2cd2e-103">ExtendedProperty 物件</span><span class="sxs-lookup"><span data-stu-id="2cd2e-103">ExtendedProperty object</span></span>

<span data-ttu-id="2cd2e-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2cd2e-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="2cd2e-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="2cd2e-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="2cd2e-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="2cd2e-108">**ExtendedProperty** 物件代表 Microsoft 擴充的屬性。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-108">The **ExtendedProperty** object represents a Microsoft-extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2cd2e-109">使用時機</span><span class="sxs-lookup"><span data-stu-id="2cd2e-109">When to use</span></span>

<span data-ttu-id="2cd2e-110">**ExtendedProperty** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="2cd2e-110">The **ExtendedProperty** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="2cd2e-111">設定或取出擴充屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-111">Set or retrieve the type of the extended property.</span></span>
-   <span data-ttu-id="2cd2e-112">設定或取出用來編碼擴充屬性的編碼類型。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-112">Set or retrieve the type of encoding used to encode the extended property.</span></span>

## <a name="members"></a><span data-ttu-id="2cd2e-113">成員</span><span class="sxs-lookup"><span data-stu-id="2cd2e-113">Members</span></span>

<span data-ttu-id="2cd2e-114">**ExtendedProperty** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2cd2e-114">The **ExtendedProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="2cd2e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="2cd2e-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2cd2e-116">屬性</span><span class="sxs-lookup"><span data-stu-id="2cd2e-116">Properties</span></span>

<span data-ttu-id="2cd2e-117">**ExtendedProperty** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-117">The **ExtendedProperty** object has these properties.</span></span>



| <span data-ttu-id="2cd2e-118">屬性</span><span class="sxs-lookup"><span data-stu-id="2cd2e-118">Property</span></span>                                             | <span data-ttu-id="2cd2e-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="2cd2e-119">Access type</span></span>           | <span data-ttu-id="2cd2e-120">Description</span><span class="sxs-lookup"><span data-stu-id="2cd2e-120">Description</span></span>                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cd2e-121">**PropID**</span><span class="sxs-lookup"><span data-stu-id="2cd2e-121">**PropID**</span></span>](extendedproperty-propid.md)<br/> | <span data-ttu-id="2cd2e-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2cd2e-122">Read/write</span></span><br/> | <span data-ttu-id="2cd2e-123">可設定或抓取擴充屬性之類型的 [**CAPICOM \_ PROPID**](capicom-propid.md) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-123">A value of the [**CAPICOM\_PROPID**](capicom-propid.md) enumeration that sets or retrieves the type of extended property.</span></span><br/> <span data-ttu-id="2cd2e-124">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-124">This is the default property.</span></span><br/> |
| [<span data-ttu-id="2cd2e-125">**值**</span><span class="sxs-lookup"><span data-stu-id="2cd2e-125">**Value**</span></span>](extendedproperty-value.md)<br/>   | <span data-ttu-id="2cd2e-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2cd2e-126">Read/write</span></span><br/> | <span data-ttu-id="2cd2e-127">可設定或抓取擴充屬性資料之 [**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-127">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that sets or retrieves the extended property data.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="2cd2e-128">備註</span><span class="sxs-lookup"><span data-stu-id="2cd2e-128">Remarks</span></span>

<span data-ttu-id="2cd2e-129">**ExtendedProperty** 物件是由 [**ExtendedProperties**](extendedproperties.md)集合所使用。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-129">The **ExtendedProperty** object is used by the [**ExtendedProperties**](extendedproperties.md) collection.</span></span>

<span data-ttu-id="2cd2e-130">您可以建立 **ExtendedProperty** 物件，而且不安全地編寫腳本。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-130">The **ExtendedProperty** object can be created, and it is not safe for scripting.</span></span> <span data-ttu-id="2cd2e-131">**ExtendedProperty** 物件的 PROGID 是 CAPICOM。ExtendedProperty。1。</span><span class="sxs-lookup"><span data-stu-id="2cd2e-131">The ProgID for the **ExtendedProperty** object is CAPICOM.ExtendedProperty.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd2e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cd2e-132">Requirements</span></span>



| <span data-ttu-id="2cd2e-133">需求</span><span class="sxs-lookup"><span data-stu-id="2cd2e-133">Requirement</span></span> | <span data-ttu-id="2cd2e-134">值</span><span class="sxs-lookup"><span data-stu-id="2cd2e-134">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd2e-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2cd2e-135">End of client support</span></span><br/> | <span data-ttu-id="2cd2e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cd2e-136">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2cd2e-137">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2cd2e-137">End of server support</span></span><br/> | <span data-ttu-id="2cd2e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cd2e-138">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2cd2e-139">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2cd2e-139">Redistributable</span></span><br/>       | <span data-ttu-id="2cd2e-140">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2cd2e-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2cd2e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd2e-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2cd2e-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2e-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
