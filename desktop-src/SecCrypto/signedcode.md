---
description: 提供使用 Authenticode 數位簽章來簽署可執行檔的功能。
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: SignedCode 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984861"
---
# <a name="signedcode-object"></a><span data-ttu-id="871bd-103">SignedCode 物件</span><span class="sxs-lookup"><span data-stu-id="871bd-103">SignedCode object</span></span>

<span data-ttu-id="871bd-104">\[**SignedCode** 物件可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="871bd-104">\[The **SignedCode** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="871bd-105">相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。</span><span class="sxs-lookup"><span data-stu-id="871bd-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="871bd-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="871bd-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="871bd-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="871bd-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="871bd-108">**SignedCode** 物件提供使用 Authenticode 數位簽章來簽署可執行檔的功能。</span><span class="sxs-lookup"><span data-stu-id="871bd-108">The **SignedCode** object provides functionality for signing executable files with an Authenticode digital signature.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="871bd-109">使用時機</span><span class="sxs-lookup"><span data-stu-id="871bd-109">When to use</span></span>

<span data-ttu-id="871bd-110">**SignedCode** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="871bd-110">The **SignedCode** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="871bd-111">簽署可執行檔。</span><span class="sxs-lookup"><span data-stu-id="871bd-111">Sign executable files.</span></span>
-   <span data-ttu-id="871bd-112">時間戳記可執行檔。</span><span class="sxs-lookup"><span data-stu-id="871bd-112">Time stamp executable files.</span></span>
-   <span data-ttu-id="871bd-113">判斷可執行檔的簽章是否有效。</span><span class="sxs-lookup"><span data-stu-id="871bd-113">Determine whether the signature of the executable file is valid.</span></span>
-   <span data-ttu-id="871bd-114">設定或取得可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="871bd-114">Set or retrieve the path to the executable file.</span></span>
-   <span data-ttu-id="871bd-115">取得可執行檔的簽署者和時間戳記程式。</span><span class="sxs-lookup"><span data-stu-id="871bd-115">Retrieve the signer and time stamper of the executable file.</span></span>
-   <span data-ttu-id="871bd-116">取得可執行檔的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="871bd-116">Retrieve a collection of the certificates for the executable file.</span></span>
-   <span data-ttu-id="871bd-117">取得可執行檔描述的描述或 URL。</span><span class="sxs-lookup"><span data-stu-id="871bd-117">Retrieve a description or the URL to the description of the executable file.</span></span>

## <a name="members"></a><span data-ttu-id="871bd-118">成員</span><span class="sxs-lookup"><span data-stu-id="871bd-118">Members</span></span>

<span data-ttu-id="871bd-119">**SignedCode** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="871bd-119">The **SignedCode** object has these types of members:</span></span>

-   [<span data-ttu-id="871bd-120">方法</span><span class="sxs-lookup"><span data-stu-id="871bd-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="871bd-121">屬性</span><span class="sxs-lookup"><span data-stu-id="871bd-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="871bd-122">方法</span><span class="sxs-lookup"><span data-stu-id="871bd-122">Methods</span></span>

<span data-ttu-id="871bd-123">**SignedCode** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="871bd-123">The **SignedCode** object has these methods.</span></span>



| <span data-ttu-id="871bd-124">方法</span><span class="sxs-lookup"><span data-stu-id="871bd-124">Method</span></span>                                    | <span data-ttu-id="871bd-125">描述</span><span class="sxs-lookup"><span data-stu-id="871bd-125">Description</span></span>                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="871bd-126">**標誌**</span><span class="sxs-lookup"><span data-stu-id="871bd-126">**Sign**</span></span>](signedcode-sign.md)           | <span data-ttu-id="871bd-127">建立 Authenticode 數位簽章，並簽署 [**SignedCode**](signedcode-filename.md) 中指定的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="871bd-127">Creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>    |
| [<span data-ttu-id="871bd-128">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="871bd-128">**Timestamp**</span></span>](signedcode-timestamp.md) | <span data-ttu-id="871bd-129">在 [**SignedCode**](signedcode-filename.md) 中指定的已簽署可執行檔上建立 Authenticode 時間戳記簽章。</span><span class="sxs-lookup"><span data-stu-id="871bd-129">Creates an Authenticode time stamp signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/> |
| [<span data-ttu-id="871bd-130">**驗證**</span><span class="sxs-lookup"><span data-stu-id="871bd-130">**Verify**</span></span>](signedcode-verify.md)       | <span data-ttu-id="871bd-131">驗證 [**SignedCode**](signedcode-filename.md) 中指定之已簽署可執行檔的 Authenticode 簽章。</span><span class="sxs-lookup"><span data-stu-id="871bd-131">Verifies the Authenticode signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="871bd-132">屬性</span><span class="sxs-lookup"><span data-stu-id="871bd-132">Properties</span></span>

<span data-ttu-id="871bd-133">**SignedCode** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="871bd-133">The **SignedCode** object has these properties.</span></span>



| <span data-ttu-id="871bd-134">屬性</span><span class="sxs-lookup"><span data-stu-id="871bd-134">Property</span></span>                                                       | <span data-ttu-id="871bd-135">存取類型</span><span class="sxs-lookup"><span data-stu-id="871bd-135">Access type</span></span>           | <span data-ttu-id="871bd-136">Description</span><span class="sxs-lookup"><span data-stu-id="871bd-136">Description</span></span>                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="871bd-137">**憑證**</span><span class="sxs-lookup"><span data-stu-id="871bd-137">**Certificates**</span></span>](signedcode-certificates.md)<br/>     | <span data-ttu-id="871bd-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="871bd-138">Read-only</span></span><br/>  | <span data-ttu-id="871bd-139">[**憑證**](certificates.md)集合，其中包含已簽署之可執行檔中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="871bd-139">A [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span><br/>             |
| [<span data-ttu-id="871bd-140">**描述**</span><span class="sxs-lookup"><span data-stu-id="871bd-140">**Description**</span></span>](signedcode-description.md)<br/>       | <span data-ttu-id="871bd-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="871bd-141">Read/write</span></span><br/> | <span data-ttu-id="871bd-142">字串，其中包含已簽署之可執行檔的描述。</span><span class="sxs-lookup"><span data-stu-id="871bd-142">A string that contains a description of the signed executable file.</span></span><br/>                                                             |
| [<span data-ttu-id="871bd-143">**DescriptionURL**</span><span class="sxs-lookup"><span data-stu-id="871bd-143">**DescriptionURL**</span></span>](signedcode-descriptionurl.md)<br/> | <span data-ttu-id="871bd-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="871bd-144">Read/write</span></span><br/> | <span data-ttu-id="871bd-145">字串，其中包含已簽署可執行檔之描述的 HTTP 位址。</span><span class="sxs-lookup"><span data-stu-id="871bd-145">A string that contains the HTTP address to a description of the signed executable file.</span></span><br/>                                         |
| [<span data-ttu-id="871bd-146">**檔案名**</span><span class="sxs-lookup"><span data-stu-id="871bd-146">**FileName**</span></span>](signedcode-filename.md)<br/>             | <span data-ttu-id="871bd-147">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="871bd-147">Read/write</span></span><br/> | <span data-ttu-id="871bd-148">字串，包含包含可執行檔之內容檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="871bd-148">A string that contains the path to the content file that contains the executable file.</span></span><br/> <span data-ttu-id="871bd-149">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="871bd-149">This is the default property.</span></span><br/> |
| [<span data-ttu-id="871bd-150">**簽署者**</span><span class="sxs-lookup"><span data-stu-id="871bd-150">**Signer**</span></span>](signedcode-signer.md)<br/>                 | <span data-ttu-id="871bd-151">唯讀</span><span class="sxs-lookup"><span data-stu-id="871bd-151">Read-only</span></span><br/>  | <span data-ttu-id="871bd-152">[**簽署者**](signer.md)物件，可存取可執行檔的簽署者。</span><span class="sxs-lookup"><span data-stu-id="871bd-152">A [**Signer**](signer.md) object that provides access to the signer of the executable file.</span></span><br/>                                    |
| [<span data-ttu-id="871bd-153">**Timestamper**</span><span class="sxs-lookup"><span data-stu-id="871bd-153">**Timestamper**</span></span>](signedcode-timestamper.md)<br/>       | <span data-ttu-id="871bd-154">唯讀</span><span class="sxs-lookup"><span data-stu-id="871bd-154">Read-only</span></span><br/>  | <span data-ttu-id="871bd-155">[**簽署者**](signer.md)物件，可存取可執行檔的時間戳記程式。</span><span class="sxs-lookup"><span data-stu-id="871bd-155">A [**Signer**](signer.md) object that provides access to the time stamper of the executable file.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="871bd-156">備註</span><span class="sxs-lookup"><span data-stu-id="871bd-156">Remarks</span></span>

<span data-ttu-id="871bd-157">您可以建立 **SignedCode** 物件，而且對腳本而言並不安全。</span><span class="sxs-lookup"><span data-stu-id="871bd-157">The **SignedCode** object can be created, and is not safe for scripting.</span></span> <span data-ttu-id="871bd-158">**SignedCode** 物件的 PROGID 是 CAPICOM。SignedCode。1。</span><span class="sxs-lookup"><span data-stu-id="871bd-158">The ProgID for the **SignedCode** object is CAPICOM.SignedCode.1.</span></span>

<span data-ttu-id="871bd-159">可執行檔的類型應為可使用 Authenticode 技術簽署的型別，例如副檔名為 .cab、.cat、.exe、.dll、.vbs 或 .ocx 的檔案。</span><span class="sxs-lookup"><span data-stu-id="871bd-159">The executable file should be of a type that can be signed with Authenticode technology, for example, files that have a file name extension of .cab, .cat, .exe, .dll, .vbs, or .ocx.</span></span>

## <a name="requirements"></a><span data-ttu-id="871bd-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="871bd-160">Requirements</span></span>



| <span data-ttu-id="871bd-161">需求</span><span class="sxs-lookup"><span data-stu-id="871bd-161">Requirement</span></span> | <span data-ttu-id="871bd-162">值</span><span class="sxs-lookup"><span data-stu-id="871bd-162">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="871bd-163">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="871bd-163">Redistributable</span></span><br/> | <span data-ttu-id="871bd-164">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="871bd-164">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="871bd-165">DLL</span><span class="sxs-lookup"><span data-stu-id="871bd-165">DLL</span></span><br/>             | <dl> <span data-ttu-id="871bd-166"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="871bd-166"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
