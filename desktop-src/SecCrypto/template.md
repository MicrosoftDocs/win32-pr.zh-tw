---
description: 代表憑證的憑證延伸範本。
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: 範本物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fedd64979ad74ceac3f6d54af58c57d8d8b2b134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996410"
---
# <a name="template-object"></a><span data-ttu-id="53596-103">範本物件</span><span class="sxs-lookup"><span data-stu-id="53596-103">Template object</span></span>

<span data-ttu-id="53596-104">\[**範本** 物件可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="53596-104">\[The **Template** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="53596-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]</span><span class="sxs-lookup"><span data-stu-id="53596-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="53596-106">**範本** 物件代表憑證的憑證延伸範本。</span><span class="sxs-lookup"><span data-stu-id="53596-106">The **Template** object represents the certificate extension template of the certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="53596-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="53596-107">When to use</span></span>

<span data-ttu-id="53596-108">**範本** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="53596-108">The **Template** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="53596-109">判斷範本是否標記為重大或存在。</span><span class="sxs-lookup"><span data-stu-id="53596-109">Determine whether the template is marked critical or present.</span></span>
-   <span data-ttu-id="53596-110">取得 (OID) 或範本名稱的 [*物件識別碼*](../secgloss/o-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="53596-110">Retrieve the [*object identifier*](../secgloss/o-gly.md) (OID) or name of the template.</span></span>
-   <span data-ttu-id="53596-111">取出範本的次要或主要版本。</span><span class="sxs-lookup"><span data-stu-id="53596-111">Retrieve the minor or major version of the template.</span></span>

## <a name="members"></a><span data-ttu-id="53596-112">成員</span><span class="sxs-lookup"><span data-stu-id="53596-112">Members</span></span>

<span data-ttu-id="53596-113">**範本** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="53596-113">The **Template** object has these types of members:</span></span>

-   [<span data-ttu-id="53596-114">屬性</span><span class="sxs-lookup"><span data-stu-id="53596-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53596-115">屬性</span><span class="sxs-lookup"><span data-stu-id="53596-115">Properties</span></span>

<span data-ttu-id="53596-116">**範本** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="53596-116">The **Template** object has these properties.</span></span>



| <span data-ttu-id="53596-117">屬性</span><span class="sxs-lookup"><span data-stu-id="53596-117">Property</span></span>                                                 | <span data-ttu-id="53596-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="53596-118">Access type</span></span>          | <span data-ttu-id="53596-119">Description</span><span class="sxs-lookup"><span data-stu-id="53596-119">Description</span></span>                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53596-120">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="53596-120">**IsCritical**</span></span>](template-iscritical.md)<br/>     | <span data-ttu-id="53596-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="53596-121">Read-only</span></span><br/> | <span data-ttu-id="53596-122">抓取布林值，指出範本延伸是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="53596-122">Retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="53596-123">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="53596-123">**IsPresent**</span></span>](template-ispresent.md)<br/>       | <span data-ttu-id="53596-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="53596-124">Read-only</span></span><br/> | <span data-ttu-id="53596-125">抓取布林值，指出範本延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="53596-125">Retrieves a Boolean value that indicates whether the template extension is present.</span></span><br/>         |
| [<span data-ttu-id="53596-126">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="53596-126">**MajorVersion**</span></span>](template-majorversion.md)<br/> | <span data-ttu-id="53596-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="53596-127">Read-only</span></span><br/> | <span data-ttu-id="53596-128">捕獲範本的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="53596-128">Retrieves the major version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="53596-129">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="53596-129">**MinorVersion**</span></span>](template-minorversion.md)<br/> | <span data-ttu-id="53596-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="53596-130">Read-only</span></span><br/> | <span data-ttu-id="53596-131">捕獲範本的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="53596-131">Retrieves the minor version number of the template.</span></span><br/>                                         |
| [<span data-ttu-id="53596-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="53596-132">**Name**</span></span>](template-name.md)<br/>                 | <span data-ttu-id="53596-133">唯讀</span><span class="sxs-lookup"><span data-stu-id="53596-133">Read-only</span></span><br/> | <span data-ttu-id="53596-134">抓取包含範本名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="53596-134">Retrieves a string that contains the name of the template.</span></span><br/>                                  |
| [<span data-ttu-id="53596-135">**老**</span><span class="sxs-lookup"><span data-stu-id="53596-135">**OID**</span></span>](template-oid.md)<br/>                   | <span data-ttu-id="53596-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="53596-136">Read-only</span></span><br/> | <span data-ttu-id="53596-137">抓取識別 **範本** 物件的 [**OID**](oid.md)物件。</span><span class="sxs-lookup"><span data-stu-id="53596-137">Retrieves an [**OID**](oid.md) object that identifies the **Template** object.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="53596-138">備註</span><span class="sxs-lookup"><span data-stu-id="53596-138">Remarks</span></span>

<span data-ttu-id="53596-139">無法建立 **範本** 物件。</span><span class="sxs-lookup"><span data-stu-id="53596-139">The **Template** object cannot be created.</span></span>

<span data-ttu-id="53596-140">[**Certificate. template**](certificate-template.md)方法會傳回 **範本** 物件。</span><span class="sxs-lookup"><span data-stu-id="53596-140">A **Template** object is returned by the [**Certificate.Template**](certificate-template.md) method.</span></span>

<span data-ttu-id="53596-141">CAPICOM 會使用兩種不同版本的憑證範本。</span><span class="sxs-lookup"><span data-stu-id="53596-141">CAPICOM uses two different versions of certificate templates.</span></span> <span data-ttu-id="53596-142">下表顯示每個憑證範本版本的名稱和 OID。</span><span class="sxs-lookup"><span data-stu-id="53596-142">The following table shows the name and OID for each certificate template version.</span></span>



| <span data-ttu-id="53596-143">版本</span><span class="sxs-lookup"><span data-stu-id="53596-143">Version</span></span> | <span data-ttu-id="53596-144">Name</span><span class="sxs-lookup"><span data-stu-id="53596-144">Name</span></span>                               | <span data-ttu-id="53596-145">OID</span><span class="sxs-lookup"><span data-stu-id="53596-145">OID</span></span>                    |
|---------|------------------------------------|------------------------|
| <span data-ttu-id="53596-146">V1</span><span class="sxs-lookup"><span data-stu-id="53596-146">V1</span></span>      | <span data-ttu-id="53596-147">szOID \_ 註冊 \_ CERTTYPE \_ 延伸模組</span><span class="sxs-lookup"><span data-stu-id="53596-147">szOID\_ENROLL\_CERTTYPE\_EXTENSION</span></span> | <span data-ttu-id="53596-148">元1.3.6.1.4.1.311.20.2 參考</span><span class="sxs-lookup"><span data-stu-id="53596-148">"1.3.6.1.4.1.311.20.2"</span></span> |
| <span data-ttu-id="53596-149">V2</span><span class="sxs-lookup"><span data-stu-id="53596-149">V2</span></span>      | <span data-ttu-id="53596-150">szOID \_ 證書 \_ 範本</span><span class="sxs-lookup"><span data-stu-id="53596-150">szOID\_CERTIFICATE\_TEMPLATE</span></span>       | <span data-ttu-id="53596-151">"1.3.6.1.4.1.311.21.7"</span><span class="sxs-lookup"><span data-stu-id="53596-151">"1.3.6.1.4.1.311.21.7"</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="53596-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="53596-152">Requirements</span></span>



| <span data-ttu-id="53596-153">需求</span><span class="sxs-lookup"><span data-stu-id="53596-153">Requirement</span></span> | <span data-ttu-id="53596-154">值</span><span class="sxs-lookup"><span data-stu-id="53596-154">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53596-155">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="53596-155">Redistributable</span></span><br/> | <span data-ttu-id="53596-156">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="53596-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="53596-157">DLL</span><span class="sxs-lookup"><span data-stu-id="53596-157">DLL</span></span><br/>             | <dl> <span data-ttu-id="53596-158"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53596-158"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
