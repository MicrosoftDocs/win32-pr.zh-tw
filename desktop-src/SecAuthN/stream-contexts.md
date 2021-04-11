---
description: 串流內容會處理安全的資料流程導向通訊協定，例如 SSL 或 PCT。
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: 資料流程內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53103dc1269c05e5a2c162133d21e167d8035c2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943844"
---
# <a name="stream-contexts"></a><span data-ttu-id="85ffa-103">資料流程內容</span><span class="sxs-lookup"><span data-stu-id="85ffa-103">Stream Contexts</span></span>

<span data-ttu-id="85ffa-104">串流內容會處理安全的資料流程導向通訊協定，例如 SSL 或 PCT。</span><span class="sxs-lookup"><span data-stu-id="85ffa-104">Stream contexts handle the secure stream-oriented protocols such as SSL or PCT.</span></span> <span data-ttu-id="85ffa-105">為了共用相同的介面和類似的認證管理，SSPI 提供資料流程內容支援。</span><span class="sxs-lookup"><span data-stu-id="85ffa-105">In the interest of sharing the same interface and similar credential management, SSPI provides support for stream contexts.</span></span> <span data-ttu-id="85ffa-106">[*安全性通訊協定*](../secgloss/s-gly.md)結合了串流驗證配置和記錄格式。</span><span class="sxs-lookup"><span data-stu-id="85ffa-106">The [*security protocol*](../secgloss/s-gly.md) incorporates both the stream authentication scheme and record formats.</span></span>

<span data-ttu-id="85ffa-107">為了提供資料流程導向的通訊協定，支援串流內容的 [*安全性套件*](../secgloss/s-gly.md) 具有下列處理常式特性：</span><span class="sxs-lookup"><span data-stu-id="85ffa-107">To provide stream-oriented protocols, [*security packages*](../secgloss/s-gly.md) that support stream contexts have the following process characteristics:</span></span>

-   <span data-ttu-id="85ffa-108">封裝會設定 SECPKG \_ 旗 \_ 標資料流程旗標，表示它支援資料流程語義。</span><span class="sxs-lookup"><span data-stu-id="85ffa-108">The package sets the SECPKG\_FLAG\_STREAM flag to indicate that it supports stream semantics.</span></span>
-   <span data-ttu-id="85ffa-109">傳輸應用程式會要求資料流程語義，方法 \_ 是 \_ \_ \_ 在 InitializeSecurityCoNtext 的呼叫中設定 ISC 要求資料流程和 ASC 要求資料流程旗標 [**(一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 和 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數。</span><span class="sxs-lookup"><span data-stu-id="85ffa-109">Transport applications requests stream semantics by setting the ISC\_REQ\_STREAM and ASC\_REQ\_STREAM flags in the calls to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) and [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) functions.</span></span>
-   <span data-ttu-id="85ffa-110">應用程式會使用 [**SecPkgCoNtext \_ StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes)結構來呼叫 [**QueryCoNtextAttributes (一般)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa)函式，以查詢要提供的緩衝區數目以及要為標頭或結尾保留的大小的 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="85ffa-110">The application calls the [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) function with a [**SecPkgContext\_StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) structure to query the [*security context*](../secgloss/s-gly.md) for the number of buffers to provide and the sizes to reserve for headers or trailers.</span></span>
-   <span data-ttu-id="85ffa-111">應用程式會在實際處理資料時，提供緩衝區描述項給備用。</span><span class="sxs-lookup"><span data-stu-id="85ffa-111">The application provides buffer descriptors to spare during the actual processing of the data.</span></span> <span data-ttu-id="85ffa-112">藉由指定資料流程語義，呼叫端會指出要進行額外處理的意願，讓 [*安全性封裝*](../secgloss/s-gly.md) 可以處理訊息的封鎖。</span><span class="sxs-lookup"><span data-stu-id="85ffa-112">By specifying stream semantics, the caller indicates willingness to do extra processing so that the [*security package*](../secgloss/s-gly.md) can handle the blocking of the messages.</span></span> <span data-ttu-id="85ffa-113">基本上，在 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函式中，呼叫端會傳入緩衝區清單。</span><span class="sxs-lookup"><span data-stu-id="85ffa-113">In essence, for the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions, the caller passes in a list of buffers.</span></span> <span data-ttu-id="85ffa-114">從資料流程導向 (（例如 TCP 埠) ）接收訊息時，呼叫端會傳入緩衝區清單，如下所示。</span><span class="sxs-lookup"><span data-stu-id="85ffa-114">When a message is received from a channel that is stream-oriented (such as a TCP port), the caller passes in a buffer list as follows.</span></span>

    | <span data-ttu-id="85ffa-115">Buffer</span><span class="sxs-lookup"><span data-stu-id="85ffa-115">Buffer</span></span> | <span data-ttu-id="85ffa-116">長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-116">Length</span></span>         | <span data-ttu-id="85ffa-117">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="85ffa-117">Buffer type</span></span>      |
    |--------|----------------|------------------|
    | <span data-ttu-id="85ffa-118">1</span><span class="sxs-lookup"><span data-stu-id="85ffa-118">1</span></span>      | <span data-ttu-id="85ffa-119">訊息長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-119">Message Length</span></span> | <span data-ttu-id="85ffa-120">之 SECBUFFER \_ 資料</span><span class="sxs-lookup"><span data-stu-id="85ffa-120">SECBUFFER\_DATA</span></span>  |
    | <span data-ttu-id="85ffa-121">2</span><span class="sxs-lookup"><span data-stu-id="85ffa-121">2</span></span>      | <span data-ttu-id="85ffa-122">0</span><span class="sxs-lookup"><span data-stu-id="85ffa-122">0</span></span>              | <span data-ttu-id="85ffa-123">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="85ffa-123">SECBUFFER\_EMPTY</span></span> |
    | <span data-ttu-id="85ffa-124">3</span><span class="sxs-lookup"><span data-stu-id="85ffa-124">3</span></span>      | <span data-ttu-id="85ffa-125">0</span><span class="sxs-lookup"><span data-stu-id="85ffa-125">0</span></span>              | <span data-ttu-id="85ffa-126">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="85ffa-126">SECBUFFER\_EMPTY</span></span> |
    | <span data-ttu-id="85ffa-127">4</span><span class="sxs-lookup"><span data-stu-id="85ffa-127">4</span></span>      | <span data-ttu-id="85ffa-128">0</span><span class="sxs-lookup"><span data-stu-id="85ffa-128">0</span></span>              | <span data-ttu-id="85ffa-129">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="85ffa-129">SECBUFFER\_EMPTY</span></span> |
    | <span data-ttu-id="85ffa-130">5</span><span class="sxs-lookup"><span data-stu-id="85ffa-130">5</span></span>      | <span data-ttu-id="85ffa-131">0</span><span class="sxs-lookup"><span data-stu-id="85ffa-131">0</span></span>              | <span data-ttu-id="85ffa-132">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="85ffa-132">SECBUFFER\_EMPTY</span></span> |

    

     

    <span data-ttu-id="85ffa-133">然後，安全性封裝會在 [*BLOB*](../secgloss/b-gly.md)上運作。</span><span class="sxs-lookup"><span data-stu-id="85ffa-133">The security package then works on the [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="85ffa-134">如果函數傳回成功，緩衝區清單看起來會像下面這樣。</span><span class="sxs-lookup"><span data-stu-id="85ffa-134">If the function returns successfully, the buffer list looks like the following.</span></span>

    

    | <span data-ttu-id="85ffa-135">Buffer</span><span class="sxs-lookup"><span data-stu-id="85ffa-135">Buffer</span></span> | <span data-ttu-id="85ffa-136">長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-136">Length</span></span>         | <span data-ttu-id="85ffa-137">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="85ffa-137">Buffer type</span></span>                |
    |--------|----------------|----------------------------|
    | <span data-ttu-id="85ffa-138">1</span><span class="sxs-lookup"><span data-stu-id="85ffa-138">1</span></span>      | <span data-ttu-id="85ffa-139">標頭長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-139">Header Length</span></span>  | <span data-ttu-id="85ffa-140">之 SECBUFFER \_ 資料流程 \_ 標頭</span><span class="sxs-lookup"><span data-stu-id="85ffa-140">SECBUFFER\_STREAM\_HEADER</span></span>  |
    | <span data-ttu-id="85ffa-141">2</span><span class="sxs-lookup"><span data-stu-id="85ffa-141">2</span></span>      | <span data-ttu-id="85ffa-142">資料長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-142">Data Length</span></span>    | <span data-ttu-id="85ffa-143">之 SECBUFFER \_ 資料</span><span class="sxs-lookup"><span data-stu-id="85ffa-143">SECBUFFER\_DATA</span></span>            |
    | <span data-ttu-id="85ffa-144">3</span><span class="sxs-lookup"><span data-stu-id="85ffa-144">3</span></span>      | <span data-ttu-id="85ffa-145">尾端長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-145">Trailer Length</span></span> | <span data-ttu-id="85ffa-146">之 SECBUFFER \_ 資料流程 \_ 結尾</span><span class="sxs-lookup"><span data-stu-id="85ffa-146">SECBUFFER\_STREAM\_TRAILER</span></span> |
    | <span data-ttu-id="85ffa-147">4</span><span class="sxs-lookup"><span data-stu-id="85ffa-147">4</span></span>      | <span data-ttu-id="85ffa-148">0</span><span class="sxs-lookup"><span data-stu-id="85ffa-148">0</span></span>              | <span data-ttu-id="85ffa-149">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="85ffa-149">SECBUFFER\_EMPTY</span></span>           |
    | <span data-ttu-id="85ffa-150">5</span><span class="sxs-lookup"><span data-stu-id="85ffa-150">5</span></span>      | <span data-ttu-id="85ffa-151">0</span><span class="sxs-lookup"><span data-stu-id="85ffa-151">0</span></span>              | <span data-ttu-id="85ffa-152">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="85ffa-152">SECBUFFER\_EMPTY</span></span>           |

    

     

    <span data-ttu-id="85ffa-153">封裝也可能會傳回 \# 長度為 x 的緩衝區4和緩衝區類型之 secbuffer \_ 額外的，表示此緩衝區中的資料是下一筆記錄的一部分，而且尚未處理。</span><span class="sxs-lookup"><span data-stu-id="85ffa-153">The package could have also returned buffer \#4 with length x and buffer type SECBUFFER\_EXTRA indicating that the data in this buffer is part of the next record and has not yet been processed.</span></span> <span data-ttu-id="85ffa-154">相反地，如果訊息函式傳回 SEC \_ E \_ 未完成的 \_ 訊息錯誤碼，則傳回的緩衝區清單看起來會像下面這樣。</span><span class="sxs-lookup"><span data-stu-id="85ffa-154">Conversely, if the message function returns the SEC\_E\_INCOMPLETE\_MESSAGE error code, the returned buffer list would look like the following.</span></span>

    

    | <span data-ttu-id="85ffa-155">Buffer</span><span class="sxs-lookup"><span data-stu-id="85ffa-155">Buffer</span></span> | <span data-ttu-id="85ffa-156">長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-156">Length</span></span> | <span data-ttu-id="85ffa-157">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="85ffa-157">Buffer type</span></span>        |
    |--------|--------|--------------------|
    | <span data-ttu-id="85ffa-158">1</span><span class="sxs-lookup"><span data-stu-id="85ffa-158">1</span></span>      | <span data-ttu-id="85ffa-159">x</span><span class="sxs-lookup"><span data-stu-id="85ffa-159">x</span></span>      | <span data-ttu-id="85ffa-160">\_遺漏之 SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="85ffa-160">SECBUFFER\_MISSING</span></span> |

    

     

    <span data-ttu-id="85ffa-161">這表示需要更多資料來處理記錄。</span><span class="sxs-lookup"><span data-stu-id="85ffa-161">This indicates that more data was needed to process the record.</span></span> <span data-ttu-id="85ffa-162">不同于訊息函式傳回的大部分錯誤，此緩衝區類型並不表示內容已遭入侵。</span><span class="sxs-lookup"><span data-stu-id="85ffa-162">Unlike most errors returned from a message function, this buffer type does not indicate that the context has been compromised.</span></span> <span data-ttu-id="85ffa-163">相反地，它會指出需要更多資料。</span><span class="sxs-lookup"><span data-stu-id="85ffa-163">Instead, it indicates that more data is needed.</span></span> <span data-ttu-id="85ffa-164">[*安全性套件*](../secgloss/s-gly.md) 在這種情況下不能更新其 [*狀態*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="85ffa-164">[*security packages*](../secgloss/s-gly.md) must not update their [*state*](../secgloss/s-gly.md) in this condition.</span></span>

    <span data-ttu-id="85ffa-165">同樣地，在通訊的寄件者端，呼叫端可以呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式。</span><span class="sxs-lookup"><span data-stu-id="85ffa-165">Similarly, on the sender side of the communication, the caller can call the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function.</span></span> <span data-ttu-id="85ffa-166">安全性封裝可能需要重新配置緩衝區或複製內容。</span><span class="sxs-lookup"><span data-stu-id="85ffa-166">The security package may need to reallocate the buffer or copy things around.</span></span> <span data-ttu-id="85ffa-167">呼叫端可以更有效率地提供緩衝區清單，如下所示。</span><span class="sxs-lookup"><span data-stu-id="85ffa-167">The caller can be more efficient by providing a buffer list as follows.</span></span>

    

    | <span data-ttu-id="85ffa-168">Buffer</span><span class="sxs-lookup"><span data-stu-id="85ffa-168">Buffer</span></span> | <span data-ttu-id="85ffa-169">長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-169">Length</span></span>         | <span data-ttu-id="85ffa-170">類型</span><span class="sxs-lookup"><span data-stu-id="85ffa-170">Type</span></span>                       |
    |--------|----------------|----------------------------|
    | <span data-ttu-id="85ffa-171">1</span><span class="sxs-lookup"><span data-stu-id="85ffa-171">1</span></span>      | <span data-ttu-id="85ffa-172">標頭長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-172">Header Length</span></span>  | <span data-ttu-id="85ffa-173">之 SECBUFFER \_ 資料流程 \_ 標頭</span><span class="sxs-lookup"><span data-stu-id="85ffa-173">SECBUFFER\_STREAM\_HEADER</span></span>  |
    | <span data-ttu-id="85ffa-174">2</span><span class="sxs-lookup"><span data-stu-id="85ffa-174">2</span></span>      | <span data-ttu-id="85ffa-175">資料長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-175">Data Length</span></span>    | <span data-ttu-id="85ffa-176">之 SECBUFFER \_ 資料</span><span class="sxs-lookup"><span data-stu-id="85ffa-176">SECBUFFER\_DATA</span></span>            |
    | <span data-ttu-id="85ffa-177">3</span><span class="sxs-lookup"><span data-stu-id="85ffa-177">3</span></span>      | <span data-ttu-id="85ffa-178">尾端長度</span><span class="sxs-lookup"><span data-stu-id="85ffa-178">Trailer Length</span></span> | <span data-ttu-id="85ffa-179">之 SECBUFFER \_ 資料流程 \_ 結尾</span><span class="sxs-lookup"><span data-stu-id="85ffa-179">SECBUFFER\_STREAM\_TRAILER</span></span> |

    

     

    <span data-ttu-id="85ffa-180">這可讓呼叫端更有效率地使用緩衝區。</span><span class="sxs-lookup"><span data-stu-id="85ffa-180">This allows the caller to use the buffers more efficiently.</span></span> <span data-ttu-id="85ffa-181">藉由呼叫 [**QueryCoNtextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) 函式來判斷在呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)之前要保留的空間量，此作業對應用程式和安全性封裝而言會更有效率。</span><span class="sxs-lookup"><span data-stu-id="85ffa-181">By calling the [**QueryContextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) function to determine the amount of space to reserve before calling [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), the operation is more efficient for the application and the security package.</span></span>

 

 
