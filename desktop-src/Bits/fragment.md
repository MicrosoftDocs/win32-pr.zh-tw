---
title: 片段
description: 使用片段封包將上傳檔案的片段傳送至伺服器。
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- 片段位
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092552"
---
# <a name="fragment"></a><span data-ttu-id="26615-104">片段</span><span class="sxs-lookup"><span data-stu-id="26615-104">Fragment</span></span>

<span data-ttu-id="26615-105">使用 **片段** 封包將上傳檔案的片段傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="26615-105">Use the **Fragment** packet to send a fragment of the upload file to the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a><span data-ttu-id="26615-106">標題</span><span class="sxs-lookup"><span data-stu-id="26615-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="26615-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST</span><span class="sxs-lookup"><span data-stu-id="26615-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="26615-108">識別此封包到 BITS 伺服器的位特定動詞。</span><span class="sxs-lookup"><span data-stu-id="26615-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="26615-109">將遠端 URL 取代為絕對或相對 URI。</span><span class="sxs-lookup"><span data-stu-id="26615-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="26615-110">通常，將遠端 URL 取代為作業的遠端檔案名。</span><span class="sxs-lookup"><span data-stu-id="26615-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="26615-111">如需網路負載平衡的考慮，請參閱 [**建立會話**](create-session.md) 封包中的 BITS 主機識別碼標頭。</span><span class="sxs-lookup"><span data-stu-id="26615-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="26615-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型</span><span class="sxs-lookup"><span data-stu-id="26615-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="26615-113">將此要求封包識別為片段封包。</span><span class="sxs-lookup"><span data-stu-id="26615-113">Identifies this request packet as a Fragment packet.</span></span>

</dd> <dt>

<span data-ttu-id="26615-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼</span><span class="sxs-lookup"><span data-stu-id="26615-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="26615-115">識別伺服器會話的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="26615-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="26615-116">將 {guid} 取代為伺服器在 [**建立會話**](ack-for-create-session.md) 回應封包的 Ack 中傳回的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="26615-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> <dt>

<span data-ttu-id="26615-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>內容名稱</span><span class="sxs-lookup"><span data-stu-id="26615-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span></span>
</dt> <dd>

<span data-ttu-id="26615-118">請僅使用初始片段來指定此標頭。</span><span class="sxs-lookup"><span data-stu-id="26615-118">Specify this header only with the initial fragment.</span></span> <span data-ttu-id="26615-119">使用作業中的本機檔案名取代檔案名。</span><span class="sxs-lookup"><span data-stu-id="26615-119">Replace filename with the name of the local file name from the job.</span></span> <span data-ttu-id="26615-120">名稱不包含路徑。</span><span class="sxs-lookup"><span data-stu-id="26615-120">The name does not include the path.</span></span>

</dd> <dt>

<span data-ttu-id="26615-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>內容長度</span><span class="sxs-lookup"><span data-stu-id="26615-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="26615-122">以片段主體中傳送的位元組數取代長度。</span><span class="sxs-lookup"><span data-stu-id="26615-122">Replace length with the number of bytes sent in the fragment body.</span></span>

</dd> <dt>

<span data-ttu-id="26615-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>內容約制</span><span class="sxs-lookup"><span data-stu-id="26615-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="26615-124">告訴伺服器要將範圍套用到目的地檔案中。</span><span class="sxs-lookup"><span data-stu-id="26615-124">Tells the server where to apply the range in the destination file.</span></span> <span data-ttu-id="26615-125">將範圍取代為目的地檔案中範圍的起始和結束位移。</span><span class="sxs-lookup"><span data-stu-id="26615-125">Replace range with the start and end offsets of the range in the destination file.</span></span> <span data-ttu-id="26615-126">位移以零為基底。</span><span class="sxs-lookup"><span data-stu-id="26615-126">The offsets are zero-based.</span></span> <span data-ttu-id="26615-127">如果指定的範圍與現有的範圍重迭，則位只會寫入範圍中非重迭的部分;BITS 不會覆寫現有的內容。</span><span class="sxs-lookup"><span data-stu-id="26615-127">If the given range overlaps an existing range, BITS writes only the non-overlapping portion of the range; BITS does not overwrite existing content.</span></span> <span data-ttu-id="26615-128">例如，如果第一個封包的範圍是0到100，而第二個封包的範圍是50到150，則 BITS 只寫入第二個封包的位元組101至150。</span><span class="sxs-lookup"><span data-stu-id="26615-128">For example, if the first packet contained the range 0 through 100 and the second packet contained the range 50 through 150, BITS writes only bytes 101 through 150 from the second packet.</span></span> <span data-ttu-id="26615-129">將總長度取代為檔案中的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="26615-129">Replace total-length with the total number of bytes in the file.</span></span>

</dd> <dt>

<span data-ttu-id="26615-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>內容編碼</span><span class="sxs-lookup"><span data-stu-id="26615-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="26615-131">以用戶端在片段上使用的編碼類型取代編碼。</span><span class="sxs-lookup"><span data-stu-id="26615-131">Replace encoding with the type of encoding the client uses on the fragment.</span></span> <span data-ttu-id="26615-132">用戶端必須使用伺服器在 [**建立會話**](ack-for-create-session.md) 回應封包的 Ack Accept-Encoding 標頭中所識別的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="26615-132">The client must use the encoding that the server identifies in the Accept-Encoding header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="26615-133">伺服器使用編碼類型來解碼片段。</span><span class="sxs-lookup"><span data-stu-id="26615-133">The server uses the encoding type to decode the fragment.</span></span> <span data-ttu-id="26615-134">所有片段都必須指定相同的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="26615-134">All fragments must specify the same encoding.</span></span>

<span data-ttu-id="26615-135">如果編碼類型為 Identity，請勿傳送此標頭。</span><span class="sxs-lookup"><span data-stu-id="26615-135">Do not send this header if the encoding type is Identity.</span></span> <span data-ttu-id="26615-136">BITS 伺服器僅支援身分識別編碼。</span><span class="sxs-lookup"><span data-stu-id="26615-136">The BITS server supports only Identity encoding.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26615-137">備註</span><span class="sxs-lookup"><span data-stu-id="26615-137">Remarks</span></span>

<span data-ttu-id="26615-138">片段是在封包主體中傳送的位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="26615-138">The fragment is a range of bytes sent in the body of the packet.</span></span> <span data-ttu-id="26615-139">用戶端會依順序從位移零開始傳送片段;伺服器不會追蹤非連續的範圍。</span><span class="sxs-lookup"><span data-stu-id="26615-139">The client sends the fragments in sequential order starting with offset zero; the server does not keep track of non-contiguous ranges.</span></span> <span data-ttu-id="26615-140">如果用戶端傳送非連續的範圍，伺服器會傳回 HTTP 416 (範圍-未] 正確的) 傳回程序代碼，在 [**片段**](ack-for-fragment.md) 回應的 Ack 中。</span><span class="sxs-lookup"><span data-stu-id="26615-140">If the client sends non-contiguous ranges, the server returns an HTTP 416 (range-not-satisfiable) return code in the [**Ack for Fragment**](ack-for-fragment.md) response.</span></span>

<span data-ttu-id="26615-141">Content-type *標頭是標準的 HTTP* 1.1 標頭。</span><span class="sxs-lookup"><span data-stu-id="26615-141">The Content-*xxxx* headers are standard HTTP 1.1 headers.</span></span> <span data-ttu-id="26615-142">如需 *content-type 標頭* 的詳細資訊，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) 規格。</span><span class="sxs-lookup"><span data-stu-id="26615-142">For more details on the Content-*xxxx* headers, see the [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) specification.</span></span>

## <a name="see-also"></a><span data-ttu-id="26615-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26615-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26615-144">**適用于片段的 Ack**</span><span class="sxs-lookup"><span data-stu-id="26615-144">**Ack for Fragment**</span></span>](ack-for-fragment.md)
</dt> <dt>

[<span data-ttu-id="26615-145">**關閉會話**</span><span class="sxs-lookup"><span data-stu-id="26615-145">**Close-Session**</span></span>](close-session.md)
</dt> <dt>

[<span data-ttu-id="26615-146">**建立-會話**</span><span class="sxs-lookup"><span data-stu-id="26615-146">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




