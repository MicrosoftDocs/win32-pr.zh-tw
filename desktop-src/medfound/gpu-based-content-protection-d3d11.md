---
description: 本主題說明&8211 的影片內容 \# 、圖形驅動程式可提供的保護功能。
ms.assetid: 3FDB4908-C75D-4AE0-B32E-93F840E4F30A
title: 使用 D3D11 影片 GPU-Based 內容保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78097492d375d50688f2472f5d2de99cc21f8594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026034"
---
# <a name="gpu-based-content-protection-with-d3d11-video"></a><span data-ttu-id="074bd-103">使用 D3D11 影片 GPU-Based 內容保護</span><span class="sxs-lookup"><span data-stu-id="074bd-103">GPU-Based Content Protection with D3D11 Video</span></span>

<span data-ttu-id="074bd-104">本主題說明圖形驅動程式可提供的影片內容-保護功能。</span><span class="sxs-lookup"><span data-stu-id="074bd-104">This topic describes video content–protection capabilities that a graphics driver can provide.</span></span>

-   [<span data-ttu-id="074bd-105">簡介</span><span class="sxs-lookup"><span data-stu-id="074bd-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="074bd-106">解碼流程的總覽</span><span class="sxs-lookup"><span data-stu-id="074bd-106">Overview of the Decoding Process</span></span>](#overview-of-the-decoding-process)
-   [<span data-ttu-id="074bd-107">加密解碼的壓縮影片緩衝區</span><span class="sxs-lookup"><span data-stu-id="074bd-107">Encrypting Compressed Video Buffers for the Decoder</span></span>](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [<span data-ttu-id="074bd-108">1. 查詢驅動程式的內容保護功能</span><span class="sxs-lookup"><span data-stu-id="074bd-108">1. Query the Content Protection Capabilities of the Driver</span></span>](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [<span data-ttu-id="074bd-109">2. 設定已驗證的通道</span><span class="sxs-lookup"><span data-stu-id="074bd-109">2. Configure the Authenticated Channel</span></span>](#2-configure-the-authenticated-channel)
    -   [<span data-ttu-id="074bd-110">3. 設定密碼編譯會話</span><span class="sxs-lookup"><span data-stu-id="074bd-110">3. Configure the Cryptographic Session</span></span>](#3-configure-the-cryptographic-session)
    -   [<span data-ttu-id="074bd-111">4. 建立解碼器與密碼編譯會話的關聯</span><span class="sxs-lookup"><span data-stu-id="074bd-111">4. Associate the decoder with the Cryptographic Session</span></span>](#4-associate-the-decoder-with-the-cryptographic-session)
-   [<span data-ttu-id="074bd-112">傳送已驗證的通道命令</span><span class="sxs-lookup"><span data-stu-id="074bd-112">Sending Authenticated Channel Commands</span></span>](#sending-authenticated-channel-commands)
-   [<span data-ttu-id="074bd-113">傳送已驗證的通道查詢</span><span class="sxs-lookup"><span data-stu-id="074bd-113">Sending Authenticated Channel Queries</span></span>](#sending-authenticated-channel-queries)
-   [<span data-ttu-id="074bd-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="074bd-114">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="074bd-115">簡介</span><span class="sxs-lookup"><span data-stu-id="074bd-115">Introduction</span></span>

<span data-ttu-id="074bd-116">下圖顯示受保護的影片內容如何流經要轉譯之管線的簡化觀點。</span><span class="sxs-lookup"><span data-stu-id="074bd-116">The following diagram shows a simplified view of how protected video content travels through the pipeline to be rendered.</span></span>

![顯示受保護的影片內容的圖表。](images/d3d9video01.png)

> [!Note]
>
> <span data-ttu-id="074bd-118">此圖表不會描述 (PMP) 的 [受保護媒體路徑](protected-media-path.md) 。</span><span class="sxs-lookup"><span data-stu-id="074bd-118">The [Protected Media Path](protected-media-path.md) (PMP) is not depicted in this diagram.</span></span> <span data-ttu-id="074bd-119">此處所顯示的資料流程可能發生在 PMP 程式中，或在應用程式進程內。</span><span class="sxs-lookup"><span data-stu-id="074bd-119">The data flow that is shown here might occur within a PMP process, or within an application process.</span></span>

 

<span data-ttu-id="074bd-120">此解碼器會從外部來源接收加密的壓縮影片資料。</span><span class="sxs-lookup"><span data-stu-id="074bd-120">The decoder receives encrypted, compressed video data from an external source.</span></span> <span data-ttu-id="074bd-121">此外，也會假設解碼器也會收到密碼編譯金鑰，以將此資料解密。</span><span class="sxs-lookup"><span data-stu-id="074bd-121">It is assumed also the decoder also receives a cryptographic key to decrypt this data.</span></span> <span data-ttu-id="074bd-122">本主題不會說明影片來源與解碼器之間的金鑰交換，但 PMP 會定義一個可能的機制。</span><span class="sxs-lookup"><span data-stu-id="074bd-122">This topic does not describe the key exchange between the video source and decoder, but the PMP defines one possible mechanism.</span></span> <span data-ttu-id="074bd-123">GPU 不包含在這個階段。</span><span class="sxs-lookup"><span data-stu-id="074bd-123">The GPU is not involved at this stage.</span></span>

<span data-ttu-id="074bd-124">針對硬體加速解碼，軟體解碼器會將壓縮的影片內容傳遞給 GPU。</span><span class="sxs-lookup"><span data-stu-id="074bd-124">For hardware-accelerated decoding, the software decoder passes compressed video content to the GPU.</span></span> <span data-ttu-id="074bd-125">為了保護此內容，此解碼器會重新加密資料（通常是使用 AES CTR），再將它傳遞給硬體加速器。</span><span class="sxs-lookup"><span data-stu-id="074bd-125">To protect this content, the decoder re-encrypts the data, typically using AES-CTR, before passing it to the hardware accelerator.</span></span> <span data-ttu-id="074bd-126">金鑰交換器制是在解碼器和圖形驅動程式之間定義。</span><span class="sxs-lookup"><span data-stu-id="074bd-126">A key-exchange mechanism is defined between the decoder and the graphics driver.</span></span>

<span data-ttu-id="074bd-127">解碼的影片畫面會儲存在視訊記憶體中，通常是以純文字顯示。</span><span class="sxs-lookup"><span data-stu-id="074bd-127">Decoded video frames are stored in video memory, generally in the clear.</span></span> <span data-ttu-id="074bd-128">此時，系統會處理框架並呈現出來。</span><span class="sxs-lookup"><span data-stu-id="074bd-128">At this point, the frames are processed and then presented.</span></span> <span data-ttu-id="074bd-129">簡報有兩個主要選項。</span><span class="sxs-lookup"><span data-stu-id="074bd-129">There are two main options for presentation.</span></span>

-   <span data-ttu-id="074bd-130">使用 D3D9 API 時，可以使用硬體重迭來呈現畫面格。</span><span class="sxs-lookup"><span data-stu-id="074bd-130">When using the D3D9 API, frames can be presented using a hardware overlay.</span></span> <span data-ttu-id="074bd-131">D3D11 中不支援硬體過度。</span><span class="sxs-lookup"><span data-stu-id="074bd-131">Hardware overly is not supported in D3D11.</span></span> <span data-ttu-id="074bd-132">如需詳細資訊，請參閱 [硬體覆蓋支援](hardware-overlay-support.md)。</span><span class="sxs-lookup"><span data-stu-id="074bd-132">For more information, see [Hardware Overlay Support](hardware-overlay-support.md).</span></span>
-   <span data-ttu-id="074bd-133">桌面視窗可以顯示畫面格，以使用共用的表面來管理 (DWM) 。</span><span class="sxs-lookup"><span data-stu-id="074bd-133">Frames can be presented by the Desktop Window Manage (DWM) using a shared surface.</span></span>

<span data-ttu-id="074bd-134">最後一個步驟是在監視器上顯示畫面格，這可能需要在圖形配接器與顯示裝置之間進行連結保護。</span><span class="sxs-lookup"><span data-stu-id="074bd-134">The last step is to display the frame on the monitor, which may require link protection between the graphics card and the display device.</span></span> <span data-ttu-id="074bd-135">High-Bandwidth 數位內容保護 (HDCP) ，就是連結保護的範例。</span><span class="sxs-lookup"><span data-stu-id="074bd-135">An example of link protection is High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="074bd-136">連結保護是使用 [輸出保護管理員](output-protection-manager.md) (OPM) 來設定。</span><span class="sxs-lookup"><span data-stu-id="074bd-136">Link protection is configured using [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="074bd-137">本主題不會說明 OPM;如需詳細資訊，請參閱 [使用輸出保護管理員](using-output-protection-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="074bd-137">This topic does not describe OPM; for more information, see [Using Output Protection Manager](using-output-protection-manager.md).</span></span>

## <a name="overview-of-the-decoding-process"></a><span data-ttu-id="074bd-138">解碼流程的總覽</span><span class="sxs-lookup"><span data-stu-id="074bd-138">Overview of the Decoding Process</span></span>

<span data-ttu-id="074bd-139">在硬體加速解碼期間，軟體解碼器必須將壓縮的影片資料傳遞到圖形配接器。</span><span class="sxs-lookup"><span data-stu-id="074bd-139">During hardware-accelerated decoding, the software decoder must pass compressed video data to the graphics card.</span></span> <span data-ttu-id="074bd-140">針對 premium 內容，此資料通常必須先使用對稱金鑰加密加密，才會傳送至 GPU。</span><span class="sxs-lookup"><span data-stu-id="074bd-140">For premium content, this data typically must be encrypted, using symmetric-key encryption, before it is sent to the GPU.</span></span>

<span data-ttu-id="074bd-141">若要加密影片進行解碼，軟體解碼器會使用下列介面：</span><span class="sxs-lookup"><span data-stu-id="074bd-141">To encrypt the video for decoding, the software decoder uses the following interfaces:</span></span>

-   <span data-ttu-id="074bd-142">[**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)。</span><span class="sxs-lookup"><span data-stu-id="074bd-142">[**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder).</span></span> <span data-ttu-id="074bd-143">表示解碼器裝置，也稱為快速鍵。</span><span class="sxs-lookup"><span data-stu-id="074bd-143">Represents the decoder device, also called the accelerator.</span></span>
-   <span data-ttu-id="074bd-144">[**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)。</span><span class="sxs-lookup"><span data-stu-id="074bd-144">[**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession).</span></span> <span data-ttu-id="074bd-145">代表提供加密金鑰的密碼編譯會話。</span><span class="sxs-lookup"><span data-stu-id="074bd-145">Represents a cryptographic session, which provides the encryption key.</span></span>
-   <span data-ttu-id="074bd-146">[**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel)。</span><span class="sxs-lookup"><span data-stu-id="074bd-146">[**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel).</span></span> <span data-ttu-id="074bd-147">代表已驗證的通道，可讓軟體解碼器將密碼編譯會話與解碼器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="074bd-147">Represents an authenticated channel, which enables the software decoder to associate the cryptographic session with the decoder.</span></span>

![顯示 direct3d9 解碼介面的圖表。](images/d3d9video02.png)

<span data-ttu-id="074bd-149">所有這些介面都是從 Direct3D11 裝置取得，如下所示：</span><span class="sxs-lookup"><span data-stu-id="074bd-149">All of these interfaces are obtained from the Direct3D11 device, as follows:</span></span>



| <span data-ttu-id="074bd-150">介面</span><span class="sxs-lookup"><span data-stu-id="074bd-150">Interface</span></span>                                                        | <span data-ttu-id="074bd-151">建立</span><span class="sxs-lookup"><span data-stu-id="074bd-151">Creation</span></span>                                                                                                                                                |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="074bd-152">**ID3D11VideoDecoder**</span><span class="sxs-lookup"><span data-stu-id="074bd-152">**ID3D11VideoDecoder**</span></span>](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)                 | <span data-ttu-id="074bd-153">呼叫 [**ID3D11VideoDevice：： CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview)。</span><span class="sxs-lookup"><span data-stu-id="074bd-153">Call [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview).</span></span> <span data-ttu-id="074bd-154">此解碼器類型是由設定檔 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="074bd-154">The decoder type is identified by a profile GUID.</span></span> |
| [<span data-ttu-id="074bd-155">**ID3D11CryptoSession**</span><span class="sxs-lookup"><span data-stu-id="074bd-155">**ID3D11CryptoSession**</span></span>](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)               | <span data-ttu-id="074bd-156">呼叫 [**ID3D11VideoDevice：： CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession)。</span><span class="sxs-lookup"><span data-stu-id="074bd-156">Call [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession).</span></span>                                                           |
| [<span data-ttu-id="074bd-157">**ID3D11AuthenticatedChannel**</span><span class="sxs-lookup"><span data-stu-id="074bd-157">**ID3D11AuthenticatedChannel**</span></span>](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) | <span data-ttu-id="074bd-158">呼叫 [**ID3D11VideoDevice：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel)。</span><span class="sxs-lookup"><span data-stu-id="074bd-158">Call [**ID3D11VideoDevice::CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel).</span></span>                                             |



 

> [!Note]  
> <span data-ttu-id="074bd-159">若要取得 [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice)介面的指標，請在 [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device)介面上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="074bd-159">To get a pointer to the [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) interface.</span></span>

 

<span data-ttu-id="074bd-160">經過驗證的通道會提供軟體解碼器與驅動程式之間的信任通道。</span><span class="sxs-lookup"><span data-stu-id="074bd-160">The authenticated channel provides a trusted communication channel between the software decoder and the driver.</span></span> <span data-ttu-id="074bd-161">通道的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="074bd-161">The communication channel works as follows:</span></span>

-   <span data-ttu-id="074bd-162">驅動程式會提供其根憑證由 Microsoft 簽署的 x.509 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="074bd-162">The driver provides an X.509 certificate chain whose root certificate is signed by Microsoft.</span></span>
-   <span data-ttu-id="074bd-163">憑證包含驅動程式的 RSA 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-163">The certificate contains an RSA public key for the driver.</span></span>
-   <span data-ttu-id="074bd-164">軟體解碼器會使用公開金鑰來傳送128位 AES 工作階段金鑰給驅動程式。</span><span class="sxs-lookup"><span data-stu-id="074bd-164">The software decoder uses the public key to send the driver a 128-bit AES session key.</span></span>
-   <span data-ttu-id="074bd-165">軟體解碼器會將查詢和命令傳送給已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="074bd-165">The software decoder sends queries and commands to the authenticated channel.</span></span>
-   <span data-ttu-id="074bd-166">工作階段金鑰是用來計算查詢和命令 (Mac) 的訊息驗證碼。</span><span class="sxs-lookup"><span data-stu-id="074bd-166">The session key is used to compute message authentication codes (MACs) for the queries and commands.</span></span> <span data-ttu-id="074bd-167">驅動程式會使用 Mac 來確認查詢/命令資料的完整性，而軟體解碼器會使用它們來確認驅動程式回應資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="074bd-167">The driver uses the MACs to verify the integrity of the query/command data, and the software decoder uses them to verify the integrity of the response data from the driver.</span></span>

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a><span data-ttu-id="074bd-168">加密解碼的壓縮影片緩衝區</span><span class="sxs-lookup"><span data-stu-id="074bd-168">Encrypting Compressed Video Buffers for the Decoder</span></span>

<span data-ttu-id="074bd-169">以下是加密和解碼流程的高階總覽：</span><span class="sxs-lookup"><span data-stu-id="074bd-169">Here is a high-level overview of the encryption and decoding process:</span></span>

1.  <span data-ttu-id="074bd-170">軟體解碼器會接收來自影片來源的加密資料串流。</span><span class="sxs-lookup"><span data-stu-id="074bd-170">The software decoder receives a stream of encrypted data from the video source.</span></span> <span data-ttu-id="074bd-171">此解碼會解密此資料流程。</span><span class="sxs-lookup"><span data-stu-id="074bd-171">The decoder decrypts this stream.</span></span>
2.  <span data-ttu-id="074bd-172">軟體解碼會使用密碼編譯會話來協商工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-172">The software decoder negotiates a session key with the cryptographic session.</span></span>
3.  <span data-ttu-id="074bd-173">軟體解碼器會使用已驗證的通道，將密碼編譯會話與解碼器裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="074bd-173">The software decoder uses the authenticated channel to associate the cryptographic session with the decoder device.</span></span>
4.  <span data-ttu-id="074bd-174">軟體解碼器會將壓縮的資料放在從 (加速器) 的解碼器裝置取得的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="074bd-174">The software decoder puts compressed data in buffers that it gets from the decoder device (accelerator).</span></span> <span data-ttu-id="074bd-175">針對受保護的內容，軟體編碼器會使用工作階段金鑰進行加密，以將放置在緩衝區中的資料加密。</span><span class="sxs-lookup"><span data-stu-id="074bd-175">For protected content, the software encoder encrypts the data that is puts into the buffers, using the session key for the encryption.</span></span>
    > [!Note]  
    > <span data-ttu-id="074bd-176">有些驅動程式會使用內容金鑰，而不是使用工作階段金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="074bd-176">Some drivers use a content key, instead of the session key, for encryption.</span></span> <span data-ttu-id="074bd-177">內容金鑰可從一個畫面格變更為下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="074bd-177">The content key could change from one frame to the next.</span></span>

     

5.  <span data-ttu-id="074bd-178">此解碼器會將加密的壓縮緩衝區提交到加速器。</span><span class="sxs-lookup"><span data-stu-id="074bd-178">The decoder submits the encrypted compressed buffers to the accelerator.</span></span> <span data-ttu-id="074bd-179">針對 AES CTR，此解碼器也會傳遞初始化向量。</span><span class="sxs-lookup"><span data-stu-id="074bd-179">For AES-CTR, the decoder also passes the initialization vector.</span></span> <span data-ttu-id="074bd-180">如果使用內容金鑰，則此解碼器會傳遞使用工作階段金鑰加密的內容金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-180">If a content key is used, the decoder passes the content key, encrypted using the session key.</span></span>

<span data-ttu-id="074bd-181">Direct3D11 具有128位 AES CTR 的標準支援，但其設計目的是要延伸至其他加密類型。</span><span class="sxs-lookup"><span data-stu-id="074bd-181">Direct3D11 has standard support for 128-bit AES-CTR, but is designed to extend to additional encryption types.</span></span>

<span data-ttu-id="074bd-182">接下來的五個章節會提供更詳細的步驟。</span><span class="sxs-lookup"><span data-stu-id="074bd-182">The next five sections give more detailed steps.</span></span>

-   [<span data-ttu-id="074bd-183">1. 查詢驅動程式的內容保護功能</span><span class="sxs-lookup"><span data-stu-id="074bd-183">1. Query the Content Protection Capabilities of the Driver</span></span>](#1-query-the-content-protection-capabilities-of-the-driver)
-   [<span data-ttu-id="074bd-184">2. 設定已驗證的通道</span><span class="sxs-lookup"><span data-stu-id="074bd-184">2. Configure the Authenticated Channel</span></span>](#2-configure-the-authenticated-channel)
-   [<span data-ttu-id="074bd-185">3. 設定密碼編譯會話</span><span class="sxs-lookup"><span data-stu-id="074bd-185">3. Configure the Cryptographic Session</span></span>](#3-configure-the-cryptographic-session)
-   [<span data-ttu-id="074bd-186">4. 建立解碼器與密碼編譯會話的關聯</span><span class="sxs-lookup"><span data-stu-id="074bd-186">4. Associate the decoder with the Cryptographic Session</span></span>](#4-associate-the-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a><span data-ttu-id="074bd-187">1. 查詢驅動程式的內容保護功能</span><span class="sxs-lookup"><span data-stu-id="074bd-187">1. Query the Content Protection Capabilities of the Driver</span></span>

<span data-ttu-id="074bd-188">嘗試套用加密之前，請先取得驅動程式的內容保護功能。</span><span class="sxs-lookup"><span data-stu-id="074bd-188">Before attempting to apply encryption, get the content protection capabilities of the driver.</span></span>

1.  <span data-ttu-id="074bd-189">取得 ID3D11Device 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="074bd-189">Get a pointer to the ID3D11Device interface.</span></span>
2.  <span data-ttu-id="074bd-190">呼叫 [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice)介面的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="074bd-190">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) interface.</span></span>
3.  <span data-ttu-id="074bd-191">呼叫 [**ID3D11VideoDevice：： GetContentProtectionCaps**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps)。</span><span class="sxs-lookup"><span data-stu-id="074bd-191">Call [**ID3D11VideoDevice::GetContentProtectionCaps**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps).</span></span> <span data-ttu-id="074bd-192">這個方法會使用驅動程式的內容保護功能來填滿 [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) 結構。</span><span class="sxs-lookup"><span data-stu-id="074bd-192">This method fills in a [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) structure with the driver’s content protection capabilities.</span></span>

<span data-ttu-id="074bd-193">請特別注意下列功能：</span><span class="sxs-lookup"><span data-stu-id="074bd-193">In particular, look for the following capabilities:</span></span>

-   <span data-ttu-id="074bd-194">如果 **Caps** 成員包含 **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE** 或 **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE** 旗標，驅動程式就可以執行加密。</span><span class="sxs-lookup"><span data-stu-id="074bd-194">If the **Caps** member contains the **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE** or **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE** flag, the driver can perform encryption.</span></span>
-   <span data-ttu-id="074bd-195">如果 **Caps** 成員包含 **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** 旗標，驅動程式會使用不同的內容金鑰進行解密。</span><span class="sxs-lookup"><span data-stu-id="074bd-195">If the **Caps** member contains the **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** flag, the driver uses a separate content key for decryption.</span></span>
-   <span data-ttu-id="074bd-196">呼叫 [**ID3D11VideoDevice：： CheckCryptoKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) ，以判斷驅動程式支援哪些類型的金鑰交換來產生工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-196">Call [**ID3D11VideoDevice::CheckCryptoKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) to determine which types of key exchanges the driver supports for generating the session key.</span></span>

<span data-ttu-id="074bd-197">**Caps** 成員中會指出額外的功能。</span><span class="sxs-lookup"><span data-stu-id="074bd-197">Additional capabilities are indicated in the **Caps** member.</span></span>

### <a name="2-configure-the-authenticated-channel"></a><span data-ttu-id="074bd-198">2. 設定已驗證的通道</span><span class="sxs-lookup"><span data-stu-id="074bd-198">2. Configure the Authenticated Channel</span></span>

<span data-ttu-id="074bd-199">下一步是設定已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="074bd-199">The next step is to configure the authenticated channel.</span></span>

1.  <span data-ttu-id="074bd-200">呼叫 [**ID3D11VideoDevice：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) 來建立已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="074bd-200">Call [**ID3D11VideoDevice::CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) to create the authenticated channel.</span></span> <span data-ttu-id="074bd-201">針對 *ChannelType* 參數，指定符合驅動程式功能的通道類型。</span><span class="sxs-lookup"><span data-stu-id="074bd-201">For the *ChannelType* parameter, specify a channel type that matches the capabilities of the driver.</span></span>
    -   <span data-ttu-id="074bd-202">**D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** 通道類型對應到 **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**。</span><span class="sxs-lookup"><span data-stu-id="074bd-202">The **D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** channel type corresponds to **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**.</span></span>
    -   <span data-ttu-id="074bd-203">**D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** 通道類型對應到 **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**。</span><span class="sxs-lookup"><span data-stu-id="074bd-203">The **D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** channel type corresponds to **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**.</span></span>

    <span data-ttu-id="074bd-204">**CreateAuthenticatedChannel** 方法會傳回 [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="074bd-204">The **CreateAuthenticatedChannel** method returns a pointer to the [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) interface.</span></span>
2.  <span data-ttu-id="074bd-205">呼叫 [**ID3D11AuthenticatedChannel：： GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) ，以取得驅動程式的 x.509 憑證的大小。</span><span class="sxs-lookup"><span data-stu-id="074bd-205">Call [**ID3D11AuthenticatedChannel::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) to get the size of the driver's X.509 certificate.</span></span> <span data-ttu-id="074bd-206">配置所需大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="074bd-206">Allocate a buffer of the required size.</span></span>
3.  <span data-ttu-id="074bd-207">呼叫 [**ID3D11AuthenticatedChannel：： GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) 以取得憑證。</span><span class="sxs-lookup"><span data-stu-id="074bd-207">Call [**ID3D11AuthenticatedChannel::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) to get the certificate.</span></span> <span data-ttu-id="074bd-208">方法會將憑證複製到在上一個步驟中配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="074bd-208">The method copies the certificate into the buffer that was allocated in the previous step.</span></span>
4.  <span data-ttu-id="074bd-209">確認驅動程式的憑證已由 Microsoft 簽署，但尚未撤銷。</span><span class="sxs-lookup"><span data-stu-id="074bd-209">Verify that the driver’s certificate was signed by Microsoft and has not been revoked.</span></span>
5.  <span data-ttu-id="074bd-210">從憑證取得公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-210">Get the public key from the certificate.</span></span>
6.  <span data-ttu-id="074bd-211">產生隨機的 RSA 工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-211">Generate a random RSA session key.</span></span> <span data-ttu-id="074bd-212">此工作階段金鑰是用來簽署傳送至已驗證通道的資料。</span><span class="sxs-lookup"><span data-stu-id="074bd-212">This session key is used to sign data that is sent to the authenticated channel.</span></span> <span data-ttu-id="074bd-213">使用驅動程式的公開金鑰來加密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-213">Encrypt the session key using the driver's public key.</span></span>
7.  <span data-ttu-id="074bd-214">呼叫 [**ID3D11VideoCoNtext：： NegotiateAuthenticatedChannelKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) ，將加密的工作階段金鑰傳送至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="074bd-214">Call [**ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) to send the encrypted session key to the driver.</span></span>
8.  <span data-ttu-id="074bd-215">將安全通道初始化，如下所示：</span><span class="sxs-lookup"><span data-stu-id="074bd-215">Initialize the secure channel as follows:</span></span>
    1.  <span data-ttu-id="074bd-216">填入檔中所述的 [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) 結構。</span><span class="sxs-lookup"><span data-stu-id="074bd-216">Fill in a [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) structure as described in the documentation.</span></span>
    2.  <span data-ttu-id="074bd-217">藉由呼叫 [**ID3D11VideoCoNtext：： ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel)來傳送 [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input)命令，如傳送 [已驗證的通道命令](#sending-authenticated-channel-commands)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="074bd-217">Send the [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) command by calling [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) as described in the section [Sending Authenticated Channel Commands](#sending-authenticated-channel-commands).</span></span> <span data-ttu-id="074bd-218">此命令包含傳送至已驗證通道之命令和查詢的起始序號。</span><span class="sxs-lookup"><span data-stu-id="074bd-218">This command contains the starting sequence numbers for the commands and queries that are sent to the authenticated channel.</span></span>
9.  <span data-ttu-id="074bd-219">將 [**D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) 查詢傳送給已驗證的通道，以驗證通道類型，如傳送 [已驗證的通道查詢](#sending-authenticated-channel-queries)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="074bd-219">Verify the channel type by sending a [**D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) query to the authenticated channel, as described in the section [Sending Authenticated Channel Queries](#sending-authenticated-channel-queries).</span></span> <span data-ttu-id="074bd-220">檢查通道類型是否符合您在 [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) 方法中指定的專案。</span><span class="sxs-lookup"><span data-stu-id="074bd-220">Check that the channel type matches what you specified in the [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) method.</span></span>

### <a name="3-configure-the-cryptographic-session"></a><span data-ttu-id="074bd-221">3. 設定密碼編譯會話</span><span class="sxs-lookup"><span data-stu-id="074bd-221">3. Configure the Cryptographic Session</span></span>

<span data-ttu-id="074bd-222">接下來，設定密碼編譯會話，並建立工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-222">Next, configure the cryptographic session and establish the session key.</span></span>

1.  <span data-ttu-id="074bd-223">呼叫 [**ID3D11VideoDevice：： CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) 來建立密碼編譯會話。</span><span class="sxs-lookup"><span data-stu-id="074bd-223">Call [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) to create the cryptographic session.</span></span> <span data-ttu-id="074bd-224">這個方法會傳回 [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="074bd-224">This method returns a pointer to the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface.</span></span>
2.  <span data-ttu-id="074bd-225">呼叫 [**ID3D11CryptoSession：： GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) ，以取得驅動程式的 x.509 憑證的大小。</span><span class="sxs-lookup"><span data-stu-id="074bd-225">Call [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) to get the size of the driver's X.509 certificate.</span></span> <span data-ttu-id="074bd-226">配置所需大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="074bd-226">Allocate a buffer of the required size.</span></span>
3.  <span data-ttu-id="074bd-227">呼叫 [**ID3D11CryptoSession：： GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) 以取得憑證。</span><span class="sxs-lookup"><span data-stu-id="074bd-227">Call [**ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) to get the certificate.</span></span> <span data-ttu-id="074bd-228">方法會將憑證複製到在上一個步驟中配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="074bd-228">The method copies the certificate into the buffer that was allocated in the previous step.</span></span>
4.  <span data-ttu-id="074bd-229">確認驅動程式的憑證已由 Microsoft 簽署，但尚未撤銷。</span><span class="sxs-lookup"><span data-stu-id="074bd-229">Verify that the driver’s certificate was signed by Microsoft and has not been revoked.</span></span>
5.  <span data-ttu-id="074bd-230">從憑證取得公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-230">Get the public key from the certificate.</span></span>
6.  <span data-ttu-id="074bd-231">產生隨機的 RSA 工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-231">Generate a random RSA session key.</span></span> <span data-ttu-id="074bd-232">這是來自已驗證通道工作階段金鑰的個別工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-232">This is a separate session key from the authenticated channel session key.</span></span> <span data-ttu-id="074bd-233">使用驅動程式的公開金鑰來加密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-233">Encrypt the session key using the driver's public key.</span></span>
7.  <span data-ttu-id="074bd-234">呼叫 [**ID3D11VideoCoNtext：： NegotiateCryptoSessionKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) ，將加密的工作階段金鑰傳送至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="074bd-234">Call [**ID3D11VideoContext::NegotiateCryptoSessionKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) to send the encrypted session key to the driver.</span></span>
8.  <span data-ttu-id="074bd-235">如果內容保護功能包含 **3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY**，請建立隨機的 RSA 內容金鑰。</span><span class="sxs-lookup"><span data-stu-id="074bd-235">If the content protection capabilities include **3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY**, create a random RSA content key.</span></span> <span data-ttu-id="074bd-236">稍後會在解碼程式中使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="074bd-236">This will be used later in the decoding process.</span></span>

### <a name="4-associate-the-decoder-with-the-cryptographic-session"></a><span data-ttu-id="074bd-237">4. 建立解碼器與密碼編譯會話的關聯</span><span class="sxs-lookup"><span data-stu-id="074bd-237">4. Associate the decoder with the Cryptographic Session</span></span>

<span data-ttu-id="074bd-238">接下來，將解碼器裝置與 Direct3D11 裝置和密碼編譯會話產生關聯，如下所示：</span><span class="sxs-lookup"><span data-stu-id="074bd-238">Next, associate the decoder device with the Direct3D11 device and the cryptographic session, as follows:</span></span>

1.  <span data-ttu-id="074bd-239">將 [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) 查詢傳送至已驗證的通道，以取得 Direct3D11 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="074bd-239">Get a handle to the Direct3D11 device, by sending a [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) query to the authenticated channel.</span></span>
2.  <span data-ttu-id="074bd-240">在 [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) 結構中填入下列資訊：</span><span class="sxs-lookup"><span data-stu-id="074bd-240">Fill in a [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) structure with the following information:</span></span>
    -   <span data-ttu-id="074bd-241">將 **DecodeHandle** 成員設定為從 [**ID3D11VideoDecoder：： GetDriverHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle)傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="074bd-241">Set the **DecodeHandle** member to the handle returned from [**ID3D11VideoDecoder::GetDriverHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle).</span></span>
    -   <span data-ttu-id="074bd-242">將 **CryptoSessionHandle** 成員設定為從 [**ID3D11CryptoSession：： GetCryptoSessionHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle)傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="074bd-242">Set the **CryptoSessionHandle** member to the handle returned from [**ID3D11CryptoSession::GetCryptoSessionHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle).</span></span>
    -   <span data-ttu-id="074bd-243">將 **DeviceHandle** 成員設定為 Direct3D11 裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="074bd-243">Set the **DeviceHandle** member to the Direct3D11 device handle.</span></span>
3.  <span data-ttu-id="074bd-244">呼叫 [**ID3D11VideoCoNtext：： ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) ，將 [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) 命令傳送到已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="074bd-244">Call [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) to send a [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) command to the authenticated channel.</span></span>

<span data-ttu-id="074bd-245">下圖說明控制碼的交換：</span><span class="sxs-lookup"><span data-stu-id="074bd-245">The following diagram illustrates the exchange of handles:</span></span>

![此圖顯示 dxva 解碼器如何與密碼編譯會話相關聯。](images/d3d9video03.png)

<span data-ttu-id="074bd-247">軟體解碼器現在可以使用密碼編譯工作階段金鑰來加密壓縮的影片緩衝區。</span><span class="sxs-lookup"><span data-stu-id="074bd-247">The software decoder can now use the cryptographic session key to encrypt the compressed video buffers.</span></span> <span data-ttu-id="074bd-248">每個壓縮的緩衝區都會有自己的初始化向量 (IV) 在 [**D3D11_VIDEO_DECODER_BUFFER_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc)結構的 **pIV** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="074bd-248">Each compressed buffer will have its own initialization vector (IV) specified in the **pIV** member of the [**D3D11_VIDEO_DECODER_BUFFER_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc) structure.</span></span>

## <a name="sending-authenticated-channel-commands"></a><span data-ttu-id="074bd-249">傳送已驗證的通道命令</span><span class="sxs-lookup"><span data-stu-id="074bd-249">Sending Authenticated Channel Commands</span></span>

<span data-ttu-id="074bd-250">定義了一組命令來設定已驗證的通道和設定各種內容保護。</span><span class="sxs-lookup"><span data-stu-id="074bd-250">A set of commands are defined for configuring the authenticated channel and setting various content protections.</span></span> <span data-ttu-id="074bd-251">如需命令清單，請參閱 [內容保護命令](content-protection-commands.md)。</span><span class="sxs-lookup"><span data-stu-id="074bd-251">For a list of commands, see [Content Protection Commands](content-protection-commands.md).</span></span>

<span data-ttu-id="074bd-252">若要將命令傳送至已驗證的通道，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="074bd-252">To send a command to the authenticated channel, perform the following steps.</span></span>

1.  <span data-ttu-id="074bd-253">填寫輸入資料結構。</span><span class="sxs-lookup"><span data-stu-id="074bd-253">Fill in the input data structure.</span></span> <span data-ttu-id="074bd-254">此資料結構一律是 [**D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) 結構，後面接著其他欄位。</span><span class="sxs-lookup"><span data-stu-id="074bd-254">This data structure is always a [**D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) structure followed by additional fields.</span></span> <span data-ttu-id="074bd-255">填寫 **D3D11_AUTHENTICATED_CONFIGURE_INPUT** 結構，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="074bd-255">Fill in the **D3D11_AUTHENTICATED_CONFIGURE_INPUT** structure as shown in the following table.</span></span>

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="074bd-256">member</span><span class="sxs-lookup"><span data-stu-id="074bd-256">Member</span></span></th>
    <th><span data-ttu-id="074bd-257">描述</span><span class="sxs-lookup"><span data-stu-id="074bd-257">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="074bd-258"><strong>omac</strong></span><span class="sxs-lookup"><span data-stu-id="074bd-258"><strong>omac</strong></span></span></td>
    <td><span data-ttu-id="074bd-259">請立即略過此欄位。</span><span class="sxs-lookup"><span data-stu-id="074bd-259">Skip this field for now.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="074bd-260"><strong>ConfigureType</strong></span><span class="sxs-lookup"><span data-stu-id="074bd-260"><strong>ConfigureType</strong></span></span></td>
    <td><span data-ttu-id="074bd-261">識別命令的 GUID。</span><span class="sxs-lookup"><span data-stu-id="074bd-261">GUID that identifies the command.</span></span> <span data-ttu-id="074bd-262">如需命令清單，請參閱 <a href="content-protection-commands.md">內容保護命令</a>。</span><span class="sxs-lookup"><span data-stu-id="074bd-262">For a list of commands, see <a href="content-protection-commands.md">Content Protection Commands</a>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="074bd-263"><strong>hChannel</strong></span><span class="sxs-lookup"><span data-stu-id="074bd-263"><strong>hChannel</strong></span></span></td>
    <td><span data-ttu-id="074bd-264">已驗證通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="074bd-264">The handle to the authenticated channel.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="074bd-265"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="074bd-265"><strong>SequenceNumber</strong></span></span></td>
    <td><span data-ttu-id="074bd-266">序號。</span><span class="sxs-lookup"><span data-stu-id="074bd-266">The sequence number.</span></span> <span data-ttu-id="074bd-267">第一個序號是藉由傳送 <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="074bd-267">The first sequence number is specified by sending a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> command.</span></span> <span data-ttu-id="074bd-268">每次您傳送另一個命令時，就會將此數位遞增1。</span><span class="sxs-lookup"><span data-stu-id="074bd-268">Each time you send another command, increment this number by 1.</span></span> <span data-ttu-id="074bd-269">此序號會防止重新執行攻擊。</span><span class="sxs-lookup"><span data-stu-id="074bd-269">The sequence number guards against replay attacks.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="074bd-270">使用兩個不同的序號，一個用於命令，一個用於查詢。</span><span class="sxs-lookup"><span data-stu-id="074bd-270">Two separate sequence numbers are used, one for commands and one for queries.</span></span>
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="074bd-271">針對出現在輸入結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。</span><span class="sxs-lookup"><span data-stu-id="074bd-271">Calculate the OMAC tag for the block of data that appears after the **omac** member of the input structure.</span></span> <span data-ttu-id="074bd-272">然後將此標記值複製到 **omac** 成員中。</span><span class="sxs-lookup"><span data-stu-id="074bd-272">Then copy this tag value into the **omac** member.</span></span>
3.  <span data-ttu-id="074bd-273">呼叫 [**ID3D11VideoCoNtext：： ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel)。</span><span class="sxs-lookup"><span data-stu-id="074bd-273">Call [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel).</span></span>
4.  <span data-ttu-id="074bd-274">驅動程式會將命令的輸出放在 [**D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) 結構中。</span><span class="sxs-lookup"><span data-stu-id="074bd-274">The driver places the output from the command in the [**D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) structure.</span></span>
5.  <span data-ttu-id="074bd-275">針對出現在輸出結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。</span><span class="sxs-lookup"><span data-stu-id="074bd-275">Calculate the OMAC tag for the block of data that appears after the **omac** member of the output structure.</span></span> <span data-ttu-id="074bd-276">將此值與 **omac** 成員的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="074bd-276">Compare this with the value of the **omac** member.</span></span> <span data-ttu-id="074bd-277">如果不相符，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="074bd-277">Fail if they do not match.</span></span>
6.  <span data-ttu-id="074bd-278">比較輸出結構中 **ConfigureType**、 **hChannel** 和 **SequenceNumber** 成員的值與這些成員的值。</span><span class="sxs-lookup"><span data-stu-id="074bd-278">Compare the values of the **ConfigureType**, **hChannel**, and **SequenceNumber** members in the output structure against your values for those members.</span></span> <span data-ttu-id="074bd-279">如果不相符，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="074bd-279">Fail if they do not match.</span></span>
7.  <span data-ttu-id="074bd-280">遞增下一個命令的序號。</span><span class="sxs-lookup"><span data-stu-id="074bd-280">Increment the sequence number for the next command.</span></span>

## <a name="sending-authenticated-channel-queries"></a><span data-ttu-id="074bd-281">傳送已驗證的通道查詢</span><span class="sxs-lookup"><span data-stu-id="074bd-281">Sending Authenticated Channel Queries</span></span>

<span data-ttu-id="074bd-282">系統會定義一組查詢來取得已驗證通道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="074bd-282">A set of queries are defined for retrieving information about the authenticated channel.</span></span> <span data-ttu-id="074bd-283">如需查詢清單，請參閱 [內容保護查詢](content-protection-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="074bd-283">For a list of queries, see [Content Protection Queries](content-protection-queries.md).</span></span>

<span data-ttu-id="074bd-284">若要將命令傳送至已驗證的通道，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="074bd-284">To send a command to the authenticated channel, perform the following steps.</span></span>

1.  <span data-ttu-id="074bd-285">填寫輸入資料結構。</span><span class="sxs-lookup"><span data-stu-id="074bd-285">Fill in the input data structure.</span></span> <span data-ttu-id="074bd-286">此資料結構一律是 [**D3D11_AUTHENTICATED_QUERY_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) 結構，後面可能接著其他欄位。</span><span class="sxs-lookup"><span data-stu-id="074bd-286">This data structure is always a [**D3D11_AUTHENTICATED_QUERY_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) structure, possibly followed by additional fields.</span></span> <span data-ttu-id="074bd-287">填寫 **D3D11_AUTHENTICATED_QUERY_INPUT** 結構，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="074bd-287">Fill in the **D3D11_AUTHENTICATED_QUERY_INPUT** structure as shown in the following table.</span></span>

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="074bd-288">member</span><span class="sxs-lookup"><span data-stu-id="074bd-288">Member</span></span></th>
    <th><span data-ttu-id="074bd-289">描述</span><span class="sxs-lookup"><span data-stu-id="074bd-289">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="074bd-290"><strong>QueryType</strong></span><span class="sxs-lookup"><span data-stu-id="074bd-290"><strong>QueryType</strong></span></span></td>
    <td><span data-ttu-id="074bd-291">識別查詢的 GUID。</span><span class="sxs-lookup"><span data-stu-id="074bd-291">GUID that identifies the query.</span></span> <span data-ttu-id="074bd-292">如需查詢清單，請參閱 <a href="content-protection-queries.md">內容保護查詢</a>。</span><span class="sxs-lookup"><span data-stu-id="074bd-292">For a list of queries, see <a href="content-protection-queries.md">Content Protection Queries</a>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="074bd-293"><strong>hChannel</strong></span><span class="sxs-lookup"><span data-stu-id="074bd-293"><strong>hChannel</strong></span></span></td>
    <td><span data-ttu-id="074bd-294">已驗證通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="074bd-294">The handle to the authenticated channel.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="074bd-295"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="074bd-295"><strong>SequenceNumber</strong></span></span></td>
    <td><span data-ttu-id="074bd-296">序號。</span><span class="sxs-lookup"><span data-stu-id="074bd-296">The sequence number.</span></span> <span data-ttu-id="074bd-297">第一個序號是藉由傳送 <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="074bd-297">The first sequence number is specified by sending a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> command.</span></span> <span data-ttu-id="074bd-298">每次您傳送另一個查詢時，會將此數位遞增1。</span><span class="sxs-lookup"><span data-stu-id="074bd-298">Each time you send another query, increment this number by 1.</span></span> <span data-ttu-id="074bd-299">此序號會防止重新執行攻擊。</span><span class="sxs-lookup"><span data-stu-id="074bd-299">The sequence number guards against replay attacks.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="074bd-300">使用兩個不同的序號，一個用於命令，一個用於查詢。</span><span class="sxs-lookup"><span data-stu-id="074bd-300">Two separate sequence numbers are used, one for commands and one for queries.</span></span>
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="074bd-301">呼叫 [**ID3D11VideoCoNtext：： QueryAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel)。</span><span class="sxs-lookup"><span data-stu-id="074bd-301">Call [**ID3D11VideoContext::QueryAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel).</span></span>
3.  <span data-ttu-id="074bd-302">驅動程式會將查詢的輸出放在 [**D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) 結構中。</span><span class="sxs-lookup"><span data-stu-id="074bd-302">The driver places the output from the query in a [**D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) structure.</span></span> <span data-ttu-id="074bd-303">根據查詢類型而定，這個結構後面會接著其他欄位。</span><span class="sxs-lookup"><span data-stu-id="074bd-303">This structure is followed by additional fields, depending on the query type.</span></span>
4.  <span data-ttu-id="074bd-304">針對出現在輸出結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。</span><span class="sxs-lookup"><span data-stu-id="074bd-304">Calculate the OMAC tag for the block of data that appears after the **omac** member of the output structure.</span></span> <span data-ttu-id="074bd-305">將此值與 **omac** 成員的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="074bd-305">Compare this with the value of the **omac** member.</span></span> <span data-ttu-id="074bd-306">如果不相符，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="074bd-306">Fail if they do not match.</span></span>
5.  <span data-ttu-id="074bd-307">比較輸出結構中 **ConfigureType**、 **hChannel** 和 **SequenceNumber** 成員的值與這些成員的值。</span><span class="sxs-lookup"><span data-stu-id="074bd-307">Compare the values of the **ConfigureType**, **hChannel**, and **SequenceNumber** members in the output structure against your values for those members.</span></span> <span data-ttu-id="074bd-308">如果不相符，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="074bd-308">Fail if they do not match.</span></span>
6.  <span data-ttu-id="074bd-309">遞增下一個查詢的序號。</span><span class="sxs-lookup"><span data-stu-id="074bd-309">Increment the sequence number for the next query.</span></span>

## <a name="related-topics"></a><span data-ttu-id="074bd-310">相關主題</span><span class="sxs-lookup"><span data-stu-id="074bd-310">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="074bd-311">Direct3D 11 影片 Api</span><span class="sxs-lookup"><span data-stu-id="074bd-311">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 
