---
description: 通訊通常牽涉到可能有大量資料或未知長度的資料。
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: 使用 SecBufferDesc 和之 secbuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca7d8155a610263838d2baf2a7d1c8fc96ec874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851120"
---
# <a name="using-secbufferdesc-and-secbuffer"></a><span data-ttu-id="10032-103">使用 SecBufferDesc 和之 secbuffer</span><span class="sxs-lookup"><span data-stu-id="10032-103">Using SecBufferDesc and SecBuffer</span></span>

<span data-ttu-id="10032-104">通訊通常牽涉到可能有大量資料或未知長度的資料。</span><span class="sxs-lookup"><span data-stu-id="10032-104">Communication often involves potentially large amounts of data or data of unknown length.</span></span> <span data-ttu-id="10032-105">在這兩種情況下，傳送和接收資料是以類似或相同的方式來完成。</span><span class="sxs-lookup"><span data-stu-id="10032-105">Sending and receiving data is done in similar or identical fashion in both of these cases.</span></span> <span data-ttu-id="10032-106">為了處理未知長度和可能的大量資料，SSPI 通訊會使用兩個結構 [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) 和 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)來完成。</span><span class="sxs-lookup"><span data-stu-id="10032-106">To deal with unknown length and potentially large amounts of data, SSPI communication is done using two structures, [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) and [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).</span></span>

<span data-ttu-id="10032-107">[**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc)結構是 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構陣列的容器。</span><span class="sxs-lookup"><span data-stu-id="10032-107">A [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) structure is a container for an array of [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="10032-108">**SecBufferDesc** 結構具有下列成員：</span><span class="sxs-lookup"><span data-stu-id="10032-108">A **SecBufferDesc** structure has the following members:</span></span>

-   <span data-ttu-id="10032-109">版本號碼</span><span class="sxs-lookup"><span data-stu-id="10032-109">Version number</span></span>
-   <span data-ttu-id="10032-110">[**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)元素的數目</span><span class="sxs-lookup"><span data-stu-id="10032-110">Number of [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) elements</span></span>
-   <span data-ttu-id="10032-111">[**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構陣列的位址</span><span class="sxs-lookup"><span data-stu-id="10032-111">Address of the array of [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures</span></span>

<span data-ttu-id="10032-112">[**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)結構包含下列三個成員：</span><span class="sxs-lookup"><span data-stu-id="10032-112">A [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structure contains the following three members:</span></span>

-   <span data-ttu-id="10032-113">緩衝區中的位元組數目</span><span class="sxs-lookup"><span data-stu-id="10032-113">Number of bytes in the buffer</span></span>
-   <span data-ttu-id="10032-114">資料項目中包含的資訊類型</span><span class="sxs-lookup"><span data-stu-id="10032-114">Type of information contained in the data item</span></span>
-   <span data-ttu-id="10032-115">位元組本身</span><span class="sxs-lookup"><span data-stu-id="10032-115">The bytes themselves</span></span>

<span data-ttu-id="10032-116">整個 SSPI 訊息通常是由 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) 結構的陣列所組成。</span><span class="sxs-lookup"><span data-stu-id="10032-116">A whole SSPI message often consists of an array of [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures.</span></span>

<span data-ttu-id="10032-117">下列緩衝區資料類型的定義如下。</span><span class="sxs-lookup"><span data-stu-id="10032-117">The following buffer data types are defined as follows.</span></span>



| <span data-ttu-id="10032-118">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="10032-118">Buffer type</span></span>                | <span data-ttu-id="10032-119">意義</span><span class="sxs-lookup"><span data-stu-id="10032-119">Meaning</span></span>                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10032-120">之 SECBUFFER \_ 空白</span><span class="sxs-lookup"><span data-stu-id="10032-120">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="10032-121">未定義，由 [*安全性封裝*](../secgloss/s-gly.md) 函式取代</span><span class="sxs-lookup"><span data-stu-id="10032-121">Undefined, replaced by the [*security package*](../secgloss/s-gly.md) function</span></span> |
| <span data-ttu-id="10032-122">之 SECBUFFER \_ 資料</span><span class="sxs-lookup"><span data-stu-id="10032-122">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="10032-123">封包資料</span><span class="sxs-lookup"><span data-stu-id="10032-123">Packet data</span></span>                                                                                                                            |
| <span data-ttu-id="10032-124">之 SECBUFFER \_ TOKEN</span><span class="sxs-lookup"><span data-stu-id="10032-124">SECBUFFER\_TOKEN</span></span>           | <span data-ttu-id="10032-125">安全性權杖</span><span class="sxs-lookup"><span data-stu-id="10032-125">Security token</span></span>                                                                                                                         |
| <span data-ttu-id="10032-126">之 SECBUFFER \_ PKG \_ PARAMS</span><span class="sxs-lookup"><span data-stu-id="10032-126">SECBUFFER\_PKG\_PARAMS</span></span>     | <span data-ttu-id="10032-127">封裝特定參數</span><span class="sxs-lookup"><span data-stu-id="10032-127">Package-specific parameters</span></span>                                                                                                            |
| <span data-ttu-id="10032-128">\_遺漏之 SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="10032-128">SECBUFFER\_MISSING</span></span>         | <span data-ttu-id="10032-129">遺漏資料指標</span><span class="sxs-lookup"><span data-stu-id="10032-129">Missing data indicator</span></span>                                                                                                                 |
| <span data-ttu-id="10032-130">之 SECBUFFER \_ 額外</span><span class="sxs-lookup"><span data-stu-id="10032-130">SECBUFFER\_EXTRA</span></span>           | <span data-ttu-id="10032-131">額外的資料</span><span class="sxs-lookup"><span data-stu-id="10032-131">Extra data</span></span>                                                                                                                             |
| <span data-ttu-id="10032-132">之 SECBUFFER \_ 資料流程</span><span class="sxs-lookup"><span data-stu-id="10032-132">SECBUFFER\_STREAM</span></span>          | <span data-ttu-id="10032-133">安全性資料流程資料</span><span class="sxs-lookup"><span data-stu-id="10032-133">Security stream data</span></span>                                                                                                                   |
| <span data-ttu-id="10032-134">之 SECBUFFER \_ 資料流程 \_ 結尾</span><span class="sxs-lookup"><span data-stu-id="10032-134">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="10032-135">安全性資料流程尾端</span><span class="sxs-lookup"><span data-stu-id="10032-135">Security stream trailer</span></span>                                                                                                                |
| <span data-ttu-id="10032-136">之 SECBUFFER \_ 資料流程 \_ 標頭</span><span class="sxs-lookup"><span data-stu-id="10032-136">SECBUFFER\_STREAM\_HEADER</span></span>  | <span data-ttu-id="10032-137">安全性資料流程標頭</span><span class="sxs-lookup"><span data-stu-id="10032-137">Security stream header</span></span>                                                                                                                 |



 

<span data-ttu-id="10032-138">您可以使用位 **or** 運算搭配下列其中一個緩衝區類型來結合上述緩衝區類型。</span><span class="sxs-lookup"><span data-stu-id="10032-138">The buffer types above can be combined using a bitwise-**OR** operation with either of the following buffer types.</span></span>



| <span data-ttu-id="10032-139">緩衝區類型</span><span class="sxs-lookup"><span data-stu-id="10032-139">Buffer type</span></span>         | <span data-ttu-id="10032-140">意義</span><span class="sxs-lookup"><span data-stu-id="10032-140">Meaning</span></span>                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="10032-141">之 SECBUFFER \_ ATTRMASK</span><span class="sxs-lookup"><span data-stu-id="10032-141">SECBUFFER\_ATTRMASK</span></span> | <span data-ttu-id="10032-142">藉由分隔屬性旗標與緩衝區類型來遮罩安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="10032-142">Mask security attributes by separating the attribute flags from the buffer type.</span></span> |
| <span data-ttu-id="10032-143">之 SECBUFFER \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="10032-143">SECBUFFER\_READONLY</span></span> | <span data-ttu-id="10032-144">緩衝區是唯讀的</span><span class="sxs-lookup"><span data-stu-id="10032-144">Buffer is read-only</span></span>                                                              |



 

<span data-ttu-id="10032-145">在每次呼叫需要 [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) 參數的 SSPI API 之前，會宣告並初始化一或多個 [**之 secbuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) 陣列元素。</span><span class="sxs-lookup"><span data-stu-id="10032-145">Before each call to an SSPI API that requires a [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) parameter, one or more [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) array elements are declared and initialized.</span></span> <span data-ttu-id="10032-146">例如，可以有兩個安全性緩衝區：一個包含輸入訊息資料，另一個則用於安全性封裝所傳回的輸出不透明安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="10032-146">For example, there can be two security buffers: one that contains input message data and the other for the output opaque security token returned by the security package.</span></span> <span data-ttu-id="10032-147">安全性緩衝區描述項中的安全性緩衝區順序並不重要，但每個緩衝區都必須以其適當的類型標記。</span><span class="sxs-lookup"><span data-stu-id="10032-147">The order of security buffers in the security buffer descriptor is not important, but each buffer must be tagged with its appropriate type.</span></span> <span data-ttu-id="10032-148">唯讀標記可搭配 [*安全性封裝*](../secgloss/s-gly.md)不可修改的任何輸入緩衝區使用。</span><span class="sxs-lookup"><span data-stu-id="10032-148">A read-only tag can be used with any input buffer that must not be modified by the [*security package*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="10032-149">預期包含安全性權杖的輸出緩衝區大小是很重要的。</span><span class="sxs-lookup"><span data-stu-id="10032-149">The size of the output buffer that is expected to contain the security token is important.</span></span> <span data-ttu-id="10032-150">在初始設定期間，應用程式可以找到安全性封裝的權杖大小上限。</span><span class="sxs-lookup"><span data-stu-id="10032-150">An application can find the maximum token size for a security package during initial setup.</span></span> <span data-ttu-id="10032-151">對 [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) 的呼叫會傳回安全性封裝資訊的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="10032-151">The call to [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) returns an array of pointers to security package information.</span></span> <span data-ttu-id="10032-152">安全性套件資訊結構包含每個封裝的權杖大小上限。</span><span class="sxs-lookup"><span data-stu-id="10032-152">The security package information structure contains the maximum token size for each package.</span></span> <span data-ttu-id="10032-153">在此範例中，資訊位於 [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)結構的 **cbMaxToken** 成員中。</span><span class="sxs-lookup"><span data-stu-id="10032-153">In the example, the information is in the **cbMaxToken** member of the [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure.</span></span> <span data-ttu-id="10032-154">您可以稍後使用 [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa)取得相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="10032-154">The same information can be obtained later using [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa).</span></span>

<span data-ttu-id="10032-155">應用程式會初始化緩衝區描述中的緩衝區指標和大小，以指出可以找到訊息資料和其他資訊的位置。</span><span class="sxs-lookup"><span data-stu-id="10032-155">The application initializes the buffer pointers and sizes in the buffer description to indicate where message data and other information can be found.</span></span>

<span data-ttu-id="10032-156">如需詳細資訊，請參閱 [之 secbuffer 和 SecBufferDesc 範例程式碼](secbuffer-and-secbufferdesc-example-code.md)。</span><span class="sxs-lookup"><span data-stu-id="10032-156">For details, see [SecBuffer and SecBufferDesc Example Code](secbuffer-and-secbufferdesc-example-code.md).</span></span>

 

 
