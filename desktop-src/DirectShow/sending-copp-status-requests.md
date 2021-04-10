---
description: 傳送 COPP 狀態要求
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: 傳送 COPP 狀態要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687384"
---
# <a name="sending-copp-status-requests"></a><span data-ttu-id="dc574-103">傳送 COPP 狀態要求</span><span class="sxs-lookup"><span data-stu-id="dc574-103">Sending COPP Status Requests</span></span>

<span data-ttu-id="dc574-104">若要傳送經認證的輸出保護通訊協定 (COPP) 狀態要求，請在 [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) 結構中填入要求資料。</span><span class="sxs-lookup"><span data-stu-id="dc574-104">To send a Certified Output Protection Protocol (COPP) status request, fill in an [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure with the request data.</span></span> <span data-ttu-id="dc574-105">結構成員如下：</span><span class="sxs-lookup"><span data-stu-id="dc574-105">The structure members are:</span></span>

-   <span data-ttu-id="dc574-106">**rApp**。</span><span class="sxs-lookup"><span data-stu-id="dc574-106">**rApp**.</span></span> <span data-ttu-id="dc574-107">128位的亂數字，以 GUID 類型。</span><span class="sxs-lookup"><span data-stu-id="dc574-107">A 128-bit random number, typed as a GUID.</span></span> <span data-ttu-id="dc574-108">驅動程式回應中會傳回相同的數位。</span><span class="sxs-lookup"><span data-stu-id="dc574-108">The same number is returned in the driver's response.</span></span> <span data-ttu-id="dc574-109">您應該在堆積上配置亂數字，然後將它複製到結構中。</span><span class="sxs-lookup"><span data-stu-id="dc574-109">You should allocate the random number on the heap and then copy it into structure.</span></span> <span data-ttu-id="dc574-110">這可防止攻擊者修改 [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) 結構的內容。</span><span class="sxs-lookup"><span data-stu-id="dc574-110">This guards against attacks where the attacker modifies the contents of the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure.</span></span>
-   <span data-ttu-id="dc574-111">**guidStatusRequestID**。</span><span class="sxs-lookup"><span data-stu-id="dc574-111">**guidStatusRequestID**.</span></span> <span data-ttu-id="dc574-112">識別要求的 GUID。</span><span class="sxs-lookup"><span data-stu-id="dc574-112">A GUID that identifies the request.</span></span> <span data-ttu-id="dc574-113">請參閱 [COPP 查詢參考](copp-query-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="dc574-113">See [COPP Query Reference](copp-query-reference.md).</span></span>
-   <span data-ttu-id="dc574-114">**dwSequence**。</span><span class="sxs-lookup"><span data-stu-id="dc574-114">**dwSequence**.</span></span> <span data-ttu-id="dc574-115">狀態序號。</span><span class="sxs-lookup"><span data-stu-id="dc574-115">The status sequence number.</span></span> <span data-ttu-id="dc574-116">在每個狀態要求之後遞增此值。</span><span class="sxs-lookup"><span data-stu-id="dc574-116">Increment this value after each status request.</span></span> <span data-ttu-id="dc574-117"> (在 [起始 COPP 會話](initiating-a-copp-session.md)的區段中，此值在程式碼範例中會顯示為 *uStatusSeq* ) 。</span><span class="sxs-lookup"><span data-stu-id="dc574-117">(In the section [Initiating a COPP Session](initiating-a-copp-session.md), this value is shown as *uStatusSeq* in the code examples.)</span></span>
-   <span data-ttu-id="dc574-118">**cbSizeData**。</span><span class="sxs-lookup"><span data-stu-id="dc574-118">**cbSizeData**.</span></span> <span data-ttu-id="dc574-119">要求所需的任何其他資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dc574-119">The size, in bytes, of any additional data needed for the request.</span></span>
-   <span data-ttu-id="dc574-120">**>statusdata**。</span><span class="sxs-lookup"><span data-stu-id="dc574-120">**StatusData**.</span></span> <span data-ttu-id="dc574-121">狀態要求的資料。</span><span class="sxs-lookup"><span data-stu-id="dc574-121">Data for the status request.</span></span>

<span data-ttu-id="dc574-122">將 [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) 結構傳遞至 [**IAMCertifiedOutputProtection：:P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) 方法。</span><span class="sxs-lookup"><span data-stu-id="dc574-122">Pass the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure to the [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) method.</span></span> <span data-ttu-id="dc574-123">例如，下列程式碼會傳送狀態要求，以查詢可用的保護機制：</span><span class="sxs-lookup"><span data-stu-id="dc574-123">For example, the following code sends a status request that queries which protection mechanisms are available:</span></span>


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



<span data-ttu-id="dc574-124">回應會寫入 [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput)結構的 **COPPStatus** 成員中。</span><span class="sxs-lookup"><span data-stu-id="dc574-124">The response is written into the **COPPStatus** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure.</span></span> <span data-ttu-id="dc574-125">**CbSizeData** 成員會提供回應中有效資料的大小。</span><span class="sxs-lookup"><span data-stu-id="dc574-125">The size of the valid data in the response is given in the **cbSizeData** member.</span></span> <span data-ttu-id="dc574-126">為確保訊息的完整性，驅動程式會使用 OMAC 1 演算法來計算 (MAC) 的訊息驗證碼，並在結構的 **macKDI** 成員中傳回此值。</span><span class="sxs-lookup"><span data-stu-id="dc574-126">To ensure the integrity of the message, the driver computes a message authentication code (MAC) using the OMAC 1 algorithm, and returns this value in the structure's **macKDI** member.</span></span> <span data-ttu-id="dc574-127">應用程式應驗證此值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="dc574-127">The application should verify this value as follows:</span></span>

1.  <span data-ttu-id="dc574-128">針對在 [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) (結構的 **macKDI** 成員後面出現的資料區塊，計算 OMAC 標記，也就是 **cbSizeData** plus **COPPStatus**) 。</span><span class="sxs-lookup"><span data-stu-id="dc574-128">Calculate the OMAC tag for the block of data that appears after the **macKDI** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure (in other words, **cbSizeData** plus **COPPStatus**).</span></span>
2.  <span data-ttu-id="dc574-129">使用直接 **memcmp**，將此標記與 **macKDI** 中的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="dc574-129">Compare this tag with the value in **macKDI**, using a straight **memcmp**.</span></span>

<span data-ttu-id="dc574-130">OMAC 1 演算法的詳細說明，請參閱 [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) 。</span><span class="sxs-lookup"><span data-stu-id="dc574-130">The OMAC 1 algorithm is described in detail at [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html).</span></span> <span data-ttu-id="dc574-131">COPP 會使用下列 OMAC-1 參數：</span><span class="sxs-lookup"><span data-stu-id="dc574-131">COPP uses the following OMAC-1 parameters:</span></span>

-   <span data-ttu-id="dc574-132">E = AES</span><span class="sxs-lookup"><span data-stu-id="dc574-132">E = AES</span></span>
-   <span data-ttu-id="dc574-133">t = 128 位</span><span class="sxs-lookup"><span data-stu-id="dc574-133">t = 128 bits</span></span>

<span data-ttu-id="dc574-134">從狀態要求傳回的資料一律會從兩個專案開始：</span><span class="sxs-lookup"><span data-stu-id="dc574-134">The data returned from the status request always starts with two items:</span></span>

-   <span data-ttu-id="dc574-135">應用程式所傳遞的相同 **rApp** 值。</span><span class="sxs-lookup"><span data-stu-id="dc574-135">The same value of **rApp** that was passed by the application.</span></span> <span data-ttu-id="dc574-136">您應確認這個值符合堆積上儲存的原始值。</span><span class="sxs-lookup"><span data-stu-id="dc574-136">You should verify that this value matches the original value stored on the heap.</span></span>
-   <span data-ttu-id="dc574-137">[**COPP \_ StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags)值，指出輸出保護狀態是否已變更。</span><span class="sxs-lookup"><span data-stu-id="dc574-137">A [**COPP\_StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) value that indicates whether the output protection status has changed.</span></span>

<span data-ttu-id="dc574-138">由於連接可能會遺失或重新設定，因此應用程式應該定期輪詢驅動程式是否有目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="dc574-138">Because the connection can be lost or reconfigured, the application should periodically poll the driver for the current status.</span></span> <span data-ttu-id="dc574-139">如果 \_ 已設定 COPP RenegotiationRequired 旗標，則應用程式應該嘗試重設保護層級。</span><span class="sxs-lookup"><span data-stu-id="dc574-139">If the COPP\_RenegotiationRequired flag is set, the application should attempt to reset the protection level.</span></span> <span data-ttu-id="dc574-140">如果 \_ 已設定 COPP LinkLost 旗標，應用程式應該停止播放內容。</span><span class="sxs-lookup"><span data-stu-id="dc574-140">If the COPP\_LinkLost flag is set, the application should stop playing the content.</span></span> <span data-ttu-id="dc574-141">例如， \_ 可能會傳回 COPP LinkLost 旗標，因為使用者已中斷輸出連接器的連線。</span><span class="sxs-lookup"><span data-stu-id="dc574-141">For example, the COPP\_LinkLost flag can be returned because the user disconnected the output connector.</span></span> <span data-ttu-id="dc574-142">應用程式應該釋放目前的 VMR 實例、建立新的 VMR 實例，然後建立新的 COPP 會話， (包括金鑰交換和憑證驗證) 。</span><span class="sxs-lookup"><span data-stu-id="dc574-142">The application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc574-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc574-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc574-144">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="dc574-144">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



