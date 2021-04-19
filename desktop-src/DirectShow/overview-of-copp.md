---
description: COPP 總覽
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: COPP 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970500"
---
# <a name="overview-of-copp"></a><span data-ttu-id="77ce9-103">COPP 總覽</span><span class="sxs-lookup"><span data-stu-id="77ce9-103">Overview of COPP</span></span>

<span data-ttu-id="77ce9-104">以下是應用程式必須執行的基本步驟，才能使用認證輸出保護通訊協定 (COPP) 。</span><span class="sxs-lookup"><span data-stu-id="77ce9-104">Here are the basic steps that an application must perform to use Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="77ce9-105">**取得驅動程式的憑證鏈**</span><span class="sxs-lookup"><span data-stu-id="77ce9-105">**Get the driver's certificate chain**</span></span>

1.  <span data-ttu-id="77ce9-106">使用影片混合轉譯器 (VMR-7 或 VMR-9) 或 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器篩選器 (EVR) ，建立可轉譯影片的 DirectShow 播放圖形。</span><span class="sxs-lookup"><span data-stu-id="77ce9-106">Build a DirectShow playback graph that renders video using the Video Mixing Renderer (VMR-7 or VMR-9) or the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) filter (EVR).</span></span>
2.  <span data-ttu-id="77ce9-107">查詢 [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) 介面的 VMR。</span><span class="sxs-lookup"><span data-stu-id="77ce9-107">Query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface.</span></span>
3.  <span data-ttu-id="77ce9-108">呼叫 [**IAMCertifiedOutputProtection：： KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange)。</span><span class="sxs-lookup"><span data-stu-id="77ce9-108">Call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="77ce9-109">這個方法會從驅動程式傳回128位的亂數字，以及包含驅動程式2048位 RSA 公開金鑰的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="77ce9-109">This method returns a 128-bit random number from the driver, along with a certificate chain that contains the driver's 2048-bit RSA public key.</span></span>

<span data-ttu-id="77ce9-110">**驗證憑證鏈**</span><span class="sxs-lookup"><span data-stu-id="77ce9-110">**Validate the certificate chain**</span></span>

1.  <span data-ttu-id="77ce9-111">驗證憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="77ce9-111">Validate the certificate chain.</span></span> <span data-ttu-id="77ce9-112">如果憑證鏈無效，請停止。</span><span class="sxs-lookup"><span data-stu-id="77ce9-112">If the certificate chain is not valid, stop.</span></span>
2.  <span data-ttu-id="77ce9-113">檢查憑證撤銷清單 (CRL) 。</span><span class="sxs-lookup"><span data-stu-id="77ce9-113">Check the certificate revocation list (CRL).</span></span> <span data-ttu-id="77ce9-114">如果憑證鏈中有任何憑證出現在撤銷清單中，請停止。</span><span class="sxs-lookup"><span data-stu-id="77ce9-114">If any of the certificates in the certificate chain appears in the revocation list, stop.</span></span>
3.  <span data-ttu-id="77ce9-115">從憑證鏈取得 RSA 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="77ce9-115">Get the RSA public key from the certificate chain.</span></span>

<span data-ttu-id="77ce9-116">**將 COPP 會話初始化**</span><span class="sxs-lookup"><span data-stu-id="77ce9-116">**Initialize the COPP Session**</span></span>

1.  <span data-ttu-id="77ce9-117">產生128位 AES 工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="77ce9-117">Generate a 128-bit AES session key.</span></span> <span data-ttu-id="77ce9-118">此金鑰是用來簽署資料，並確認已簽署的資料尚未遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="77ce9-118">This key is used to sign data and to verify that signed data has not been tampered with.</span></span>
2.  <span data-ttu-id="77ce9-119">產生兩個密碼編譯安全32位亂數字。</span><span class="sxs-lookup"><span data-stu-id="77ce9-119">Generate two cryptographically secure 32-bit random numbers.</span></span> <span data-ttu-id="77ce9-120">第一個是狀態序號，而第二個是命令序號。</span><span class="sxs-lookup"><span data-stu-id="77ce9-120">The first is a status sequence number, and the second is a command sequence number.</span></span> <span data-ttu-id="77ce9-121">每次應用程式傳送命令或狀態要求時，它會遞增對應的序號，並在 COPP 命令中包含此號碼或要求資料。</span><span class="sxs-lookup"><span data-stu-id="77ce9-121">Each time the application sends a command or status request, it increments the corresponding sequence number, and includes this number in the COPP command or request data.</span></span>
3.  <span data-ttu-id="77ce9-122">從圖形驅動程式、AES 工作階段金鑰、狀態序號和命令序號串連128位的亂數字。</span><span class="sxs-lookup"><span data-stu-id="77ce9-122">Concatenate the 128-bit random number from the graphics driver, the AES session key, the status sequence number, and the command sequence number.</span></span> <span data-ttu-id="77ce9-123">使用驅動程式的公開金鑰來加密此位元組陣列，並將結果傳遞給 [**IAMCertifiedOutputProtection：： SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart)。</span><span class="sxs-lookup"><span data-stu-id="77ce9-123">Encrypt this byte array using the driver's public key and pass the result to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span></span>

<span data-ttu-id="77ce9-124">**傳送 COPP 命令和狀態要求**</span><span class="sxs-lookup"><span data-stu-id="77ce9-124">**Send COPP Commands and Status Requests**</span></span>

1.  <span data-ttu-id="77ce9-125">藉由呼叫 [**IAMCertifiedOutputProtection：:P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus)，查詢可用的保護類型和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="77ce9-125">Query for the available protection types and other information by calling [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span></span>
2.  <span data-ttu-id="77ce9-126">藉由呼叫 [**IAMCertifiedOutputProtection：:P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand)來設定所需的保護層級。</span><span class="sxs-lookup"><span data-stu-id="77ce9-126">Set the desired protection levels by calling [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span></span>
3.  <span data-ttu-id="77ce9-127">定期查詢目前的本機保護層級。</span><span class="sxs-lookup"><span data-stu-id="77ce9-127">Periodically query for the current local protection level.</span></span> <span data-ttu-id="77ce9-128">如果本機保護等級未預期地變更，或如果偵測到問題，則停止播放。</span><span class="sxs-lookup"><span data-stu-id="77ce9-128">Stop playback if the local protection level changes unexpectedly or if a problem is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77ce9-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="77ce9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ce9-130">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="77ce9-130">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



