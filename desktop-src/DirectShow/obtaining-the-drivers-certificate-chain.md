---
description: 取得驅動程式憑證鏈
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: 取得驅動程式憑證鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3f46e395550ca4bcb02396fe09126c1232f2c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845747"
---
# <a name="obtaining-the-drivers-certificate-chain"></a><span data-ttu-id="d72a5-103">取得驅動程式憑證鏈</span><span class="sxs-lookup"><span data-stu-id="d72a5-103">Obtaining the Drivers Certificate Chain</span></span>

<span data-ttu-id="d72a5-104">若要 (COPP) 使用經認證的輸出保護通訊協定，應用程式必須先建立一個 DirectShow 圖形，其中包含視頻混合轉譯篩選 (VMR-7 或 VMR-9) 。</span><span class="sxs-lookup"><span data-stu-id="d72a5-104">To use Certified Output Protection Protocol (COPP), the application first must build a DirectShow graph that includes the Video Mixing Render filter (VMR-7 or VMR-9).</span></span> <span data-ttu-id="d72a5-105">較舊的影片轉譯器篩選器不支援 COPP。</span><span class="sxs-lookup"><span data-stu-id="d72a5-105">The older Video Renderer filter does not support COPP.</span></span> <span data-ttu-id="d72a5-106">在呼叫任何 COPP 方法之前，應用程式必須建立影片播放圖形，並將該解碼器連接至 VMR 濾波器的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="d72a5-106">Before calling any COPP methods, the application must build a video playback graph and connect the decoder to the VMR filter's input pin.</span></span> <span data-ttu-id="d72a5-107">不需要播放影片檔案。</span><span class="sxs-lookup"><span data-stu-id="d72a5-107">It is not necessary to play the video file.</span></span>

<span data-ttu-id="d72a5-108">建立圖形之後，請查詢 [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) 介面的 VMR，然後呼叫 [**IAMCertifiedOutputProtection：： KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange)。</span><span class="sxs-lookup"><span data-stu-id="d72a5-108">After building the graph, query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface, and then call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="d72a5-109">這個方法會傳回類型為 GUID 的128位亂數字，以及位元組陣列的指標，其中包含以 UTF-8 格式表示的驅動程式 XML 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="d72a5-109">This method returns a 128-bit random number typed as a GUID, along with a pointer to a byte array that contains the driver's XML certificate chain in UTF-8 format.</span></span> <span data-ttu-id="d72a5-110">下列程式碼說明如何取得憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="d72a5-110">The following code shows how to get the certificate chain.</span></span>


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a><span data-ttu-id="d72a5-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="d72a5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d72a5-112">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="d72a5-112">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



