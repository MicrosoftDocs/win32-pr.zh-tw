---
description: 描述影片內容&\# 8211; 圖形驅動程式可提供的保護功能。
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based 內容保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc1a0f88cae199b9aab38e5ec429ea5427f44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556185"
---
# <a name="gpu-based-content-protection"></a><span data-ttu-id="d40b7-103">GPU-Based 內容保護</span><span class="sxs-lookup"><span data-stu-id="d40b7-103">GPU-Based Content Protection</span></span>

<span data-ttu-id="d40b7-104">本主題說明圖形驅動程式可提供的影片內容-保護功能。</span><span class="sxs-lookup"><span data-stu-id="d40b7-104">This topic describes video content–protection capabilities that a graphics driver can provide.</span></span>

-   [<span data-ttu-id="d40b7-105">簡介</span><span class="sxs-lookup"><span data-stu-id="d40b7-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d40b7-106">解碼流程的總覽</span><span class="sxs-lookup"><span data-stu-id="d40b7-106">Overview of the Decoding Process</span></span>](#overview-of-the-decoding-process)
-   [<span data-ttu-id="d40b7-107">加密解碼的壓縮影片緩衝區</span><span class="sxs-lookup"><span data-stu-id="d40b7-107">Encrypting Compressed Video Buffers for the Decoder</span></span>](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [<span data-ttu-id="d40b7-108">1. 查詢驅動程式的內容保護功能</span><span class="sxs-lookup"><span data-stu-id="d40b7-108">1. Query the Content Protection Capabilities of the Driver</span></span>](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [<span data-ttu-id="d40b7-109">2. 設定已驗證的通道</span><span class="sxs-lookup"><span data-stu-id="d40b7-109">2. Configure the Authenticated Channel</span></span>](#2-configure-the-authenticated-channel)
    -   [<span data-ttu-id="d40b7-110">3. 設定密碼編譯會話</span><span class="sxs-lookup"><span data-stu-id="d40b7-110">3. Configure the Cryptographic Session</span></span>](#3-configure-the-cryptographic-session)
    -   [<span data-ttu-id="d40b7-111">4. 取得 DXVA 解碼器裝置的控制碼</span><span class="sxs-lookup"><span data-stu-id="d40b7-111">4. Get a Handle to the DXVA Decoder Device</span></span>](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [<span data-ttu-id="d40b7-112">5. 將 DXVA 解碼器與密碼編譯會話產生關聯</span><span class="sxs-lookup"><span data-stu-id="d40b7-112">5. Associate the DXVA Decoder with the Cryptographic Session</span></span>](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [<span data-ttu-id="d40b7-113">傳送已驗證的通道命令</span><span class="sxs-lookup"><span data-stu-id="d40b7-113">Sending Authenticated Channel Commands</span></span>](#sending-authenticated-channel-commands)
-   [<span data-ttu-id="d40b7-114">傳送已驗證的通道查詢</span><span class="sxs-lookup"><span data-stu-id="d40b7-114">Sending Authenticated Channel Queries</span></span>](#sending-authenticated-channel-queries)
-   [<span data-ttu-id="d40b7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="d40b7-115">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d40b7-116">簡介</span><span class="sxs-lookup"><span data-stu-id="d40b7-116">Introduction</span></span>

<span data-ttu-id="d40b7-117">下圖顯示受保護的影片內容如何流經要轉譯之管線的簡化觀點。</span><span class="sxs-lookup"><span data-stu-id="d40b7-117">The following diagram shows a simplified view of how protected video content travels through the pipeline to be rendered.</span></span>

![顯示受保護的影片內容的圖表。](images/d3d9video01.png)

> [!Note]  
> <span data-ttu-id="d40b7-119">此圖表不會描述 (PMP) 的 [受保護媒體路徑](protected-media-path.md) 。</span><span class="sxs-lookup"><span data-stu-id="d40b7-119">The [Protected Media Path](protected-media-path.md) (PMP) is not depicted in this diagram.</span></span> <span data-ttu-id="d40b7-120">此處所顯示的資料流程可能發生在 PMP 程式中，或在應用程式進程內。</span><span class="sxs-lookup"><span data-stu-id="d40b7-120">The data flow that is shown here might occur within a PMP process, or within an application process.</span></span>

 

<span data-ttu-id="d40b7-121">此解碼器會從外部來源接收加密的壓縮影片資料。</span><span class="sxs-lookup"><span data-stu-id="d40b7-121">The decoder receives encrypted, compressed video data from an external source.</span></span> <span data-ttu-id="d40b7-122">此外，也會假設解碼器也會收到密碼編譯金鑰，以將此資料解密。</span><span class="sxs-lookup"><span data-stu-id="d40b7-122">It is assumed also the decoder also receives a cryptographic key to decrypt this data.</span></span> <span data-ttu-id="d40b7-123">本主題不會說明影片來源與解碼器之間的金鑰交換，但 PMP 會定義一個可能的機制。</span><span class="sxs-lookup"><span data-stu-id="d40b7-123">This topic does not describe the key exchange between the video source and decoder, but the PMP defines one possible mechanism.</span></span> <span data-ttu-id="d40b7-124">GPU 不包含在這個階段。</span><span class="sxs-lookup"><span data-stu-id="d40b7-124">The GPU is not involved at this stage.</span></span>

<span data-ttu-id="d40b7-125">針對硬體加速解碼，軟體解碼器會將壓縮的影片內容傳遞給 GPU。</span><span class="sxs-lookup"><span data-stu-id="d40b7-125">For hardware-accelerated decoding, the software decoder passes compressed video content to the GPU.</span></span> <span data-ttu-id="d40b7-126">為了保護此內容，此解碼器會重新加密資料（通常是使用 AES CTR），再將它傳遞給硬體加速器。</span><span class="sxs-lookup"><span data-stu-id="d40b7-126">To protect this content, the decoder re-encrypts the data, typically using AES-CTR, before passing it to the hardware accelerator.</span></span> <span data-ttu-id="d40b7-127">金鑰交換器制是在解碼器和圖形驅動程式之間定義。</span><span class="sxs-lookup"><span data-stu-id="d40b7-127">A key-exchange mechanism is defined between the decoder and the graphics driver.</span></span>

<span data-ttu-id="d40b7-128">解碼的影片畫面會儲存在視訊記憶體中，通常是以純文字顯示。</span><span class="sxs-lookup"><span data-stu-id="d40b7-128">Decoded video frames are stored in video memory, generally in the clear.</span></span> <span data-ttu-id="d40b7-129">此時，系統會處理框架並呈現出來。</span><span class="sxs-lookup"><span data-stu-id="d40b7-129">At this point, the frames are processed and then presented.</span></span> <span data-ttu-id="d40b7-130">簡報有兩個主要選項。</span><span class="sxs-lookup"><span data-stu-id="d40b7-130">There are two main options for presentation.</span></span>

-   <span data-ttu-id="d40b7-131">畫面格可以使用硬體重迭顯示。</span><span class="sxs-lookup"><span data-stu-id="d40b7-131">Frames can be presented using a hardware overlay.</span></span> <span data-ttu-id="d40b7-132">如需詳細資訊，請參閱 [硬體覆蓋支援](hardware-overlay-support.md)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-132">For more information, see [Hardware Overlay Support](hardware-overlay-support.md).</span></span>
-   <span data-ttu-id="d40b7-133">桌面視窗可以顯示畫面格，以使用共用的表面來管理 (DWM) 。</span><span class="sxs-lookup"><span data-stu-id="d40b7-133">Frames can be presented by the Desktop Window Manage (DWM) using a shared surface.</span></span>

<span data-ttu-id="d40b7-134">最後一個步驟是在監視器上顯示畫面格，這可能需要在圖形配接器與顯示裝置之間進行連結保護。</span><span class="sxs-lookup"><span data-stu-id="d40b7-134">The last step is to display the frame on the monitor, which may require link protection between the graphics card and the display device.</span></span> <span data-ttu-id="d40b7-135">High-Bandwidth 數位內容保護 (HDCP) ，就是連結保護的範例。</span><span class="sxs-lookup"><span data-stu-id="d40b7-135">An example of link protection is High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="d40b7-136">連結保護是使用 [輸出保護管理員](output-protection-manager.md) (OPM) 來設定。</span><span class="sxs-lookup"><span data-stu-id="d40b7-136">Link protection is configured using [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="d40b7-137">本主題不會說明 OPM;如需詳細資訊，請參閱 [使用輸出保護管理員](using-output-protection-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-137">This topic does not describe OPM; for more information, see [Using Output Protection Manager](using-output-protection-manager.md).</span></span>

## <a name="overview-of-the-decoding-process"></a><span data-ttu-id="d40b7-138">解碼流程的總覽</span><span class="sxs-lookup"><span data-stu-id="d40b7-138">Overview of the Decoding Process</span></span>

<span data-ttu-id="d40b7-139">在硬體加速解碼期間，軟體解碼器必須將壓縮的影片資料傳遞到圖形配接器。</span><span class="sxs-lookup"><span data-stu-id="d40b7-139">During hardware-accelerated decoding, the software decoder must pass compressed video data to the graphics card.</span></span> <span data-ttu-id="d40b7-140">針對 premium 內容，此資料通常必須先使用對稱金鑰加密加密，才會傳送至 GPU。</span><span class="sxs-lookup"><span data-stu-id="d40b7-140">For premium content, this data typically must be encrypted, using symmetric-key encryption, before it is sent to the GPU.</span></span>

<span data-ttu-id="d40b7-141">若要加密影片進行解碼，軟體解碼器會使用下列介面：</span><span class="sxs-lookup"><span data-stu-id="d40b7-141">To encrypt the video for decoding, the software decoder uses the following interfaces:</span></span>

-   <span data-ttu-id="d40b7-142">[**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-142">[**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder).</span></span> <span data-ttu-id="d40b7-143">代表 DXVA 解碼器裝置，也稱為快速鍵。</span><span class="sxs-lookup"><span data-stu-id="d40b7-143">Represents the DXVA decoder device, also called the accelerator.</span></span>
-   <span data-ttu-id="d40b7-144">[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-144">[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9).</span></span> <span data-ttu-id="d40b7-145">代表提供加密金鑰的密碼編譯會話。</span><span class="sxs-lookup"><span data-stu-id="d40b7-145">Represents a cryptographic session, which provides the encryption key.</span></span>
-   <span data-ttu-id="d40b7-146">[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-146">[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9).</span></span> <span data-ttu-id="d40b7-147">代表已驗證的通道，可讓軟體解碼器將密碼編譯會話與 DXVA 解碼器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d40b7-147">Represents an authenticated channel, which enables the software decoder to associate the cryptographic session with the DXVA decoder.</span></span>

![顯示 direct3d9 解碼介面的圖表。](images/d3d9video02.png)

<span data-ttu-id="d40b7-149">所有這些介面都是從 Direct3D 裝置取得，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d40b7-149">All of these interfaces are obtained from the Direct3D device, as follows:</span></span>



| <span data-ttu-id="d40b7-150">介面</span><span class="sxs-lookup"><span data-stu-id="d40b7-150">Interface</span></span>                                                                | <span data-ttu-id="d40b7-151">建立</span><span class="sxs-lookup"><span data-stu-id="d40b7-151">Creation</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d40b7-152">**IDirectXVideoDecoder**</span><span class="sxs-lookup"><span data-stu-id="d40b7-152">**IDirectXVideoDecoder**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | <span data-ttu-id="d40b7-153">呼叫 [**IDirectXVideoDecoderService：： CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-153">Call [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span></span> <span data-ttu-id="d40b7-154">DXVA 解碼器裝置是由 DXVA 設定檔 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="d40b7-154">The DXVA decoder device is identified by a DXVA profile GUID.</span></span> |
| [<span data-ttu-id="d40b7-155">**IDirect3DCryptoSession9**</span><span class="sxs-lookup"><span data-stu-id="d40b7-155">**IDirect3DCryptoSession9**</span></span>](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | <span data-ttu-id="d40b7-156">呼叫 [**IDirect3DDevice9Video：： CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-156">Call [**IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession).</span></span>                                                                         |
| [<span data-ttu-id="d40b7-157">**IDirect3DAuthenticatedChannel9**</span><span class="sxs-lookup"><span data-stu-id="d40b7-157">**IDirect3DAuthenticatedChannel9**</span></span>](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | <span data-ttu-id="d40b7-158">呼叫 [**IDirect3DDevice9Video：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-158">Call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="d40b7-159">若要取得 [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) 介面的指標，請在 D3D9Ex 裝置上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="d40b7-159">To get a pointer to the [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a D3D9Ex device.</span></span>

 

<span data-ttu-id="d40b7-160">經過驗證的通道會提供軟體解碼器與驅動程式之間的信任通道。</span><span class="sxs-lookup"><span data-stu-id="d40b7-160">The authenticated channel provides a trusted communication channel between the software decoder and the driver.</span></span> <span data-ttu-id="d40b7-161">通道的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="d40b7-161">The communication channel works as follows:</span></span>

-   <span data-ttu-id="d40b7-162">驅動程式會提供其根憑證由 Microsoft 簽署的 x.509 憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="d40b7-162">The driver provides an X.509 certificate chain whose root certificate is signed by Microsoft.</span></span>
-   <span data-ttu-id="d40b7-163">憑證包含驅動程式的 RSA 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-163">The certificate contains an RSA public key for the driver.</span></span>
-   <span data-ttu-id="d40b7-164">軟體解碼器會使用公開金鑰來傳送128位 AES 工作階段金鑰給驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d40b7-164">The software decoder uses the public key to send the driver a 128-bit AES session key.</span></span>
-   <span data-ttu-id="d40b7-165">軟體解碼器會將查詢和命令傳送給已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="d40b7-165">The software decoder sends queries and commands to the authenticated channel.</span></span>
-   <span data-ttu-id="d40b7-166">工作階段金鑰是用來計算查詢和命令 (Mac) 的訊息驗證碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-166">The session key is used to compute message authentication codes (MACs) for the queries and commands.</span></span> <span data-ttu-id="d40b7-167">驅動程式會使用 Mac 來確認查詢/命令資料的完整性，而軟體解碼器會使用它們來確認驅動程式回應資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="d40b7-167">The driver uses the MACs to verify the integrity of the query/command data, and the software decoder uses them to verify the integrity of the response data from the driver.</span></span>

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a><span data-ttu-id="d40b7-168">加密解碼的壓縮影片緩衝區</span><span class="sxs-lookup"><span data-stu-id="d40b7-168">Encrypting Compressed Video Buffers for the Decoder</span></span>

<span data-ttu-id="d40b7-169">以下是加密和解碼流程的高階總覽：</span><span class="sxs-lookup"><span data-stu-id="d40b7-169">Here is a high-level overview of the encryption and decoding process:</span></span>

1.  <span data-ttu-id="d40b7-170">軟體解碼器會接收來自影片來源的加密資料串流。</span><span class="sxs-lookup"><span data-stu-id="d40b7-170">The software decoder receives a stream of encrypted data from the video source.</span></span> <span data-ttu-id="d40b7-171">此解碼會解密此資料流程。</span><span class="sxs-lookup"><span data-stu-id="d40b7-171">The decoder decrypts this stream.</span></span>
2.  <span data-ttu-id="d40b7-172">軟體解碼會使用密碼編譯會話來協商工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-172">The software decoder negotiates a session key with the cryptographic session.</span></span>
3.  <span data-ttu-id="d40b7-173">軟體解碼器會使用已驗證的通道，將密碼編譯會話與 DXVA 解碼器裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d40b7-173">The software decoder uses the authenticated channel to associate the cryptographic session with the DXVA decoder device.</span></span>
4.  <span data-ttu-id="d40b7-174">軟體解碼器會將壓縮的資料放在從 DXVA 解碼器裝置 (加速器) 取得的 DXVA 緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="d40b7-174">The software decoder puts compressed data in DXVA buffers that it gets from the DXVA decoder device (accelerator).</span></span> <span data-ttu-id="d40b7-175">針對受保護的內容，軟體編碼器會使用工作階段金鑰進行加密，以將放置在 DXVA 緩衝區中的資料加密。</span><span class="sxs-lookup"><span data-stu-id="d40b7-175">For protected content, the software encoder encrypts the data that is puts into the DXVA buffers, using the session key for the encryption.</span></span>
    > [!Note]  
    > <span data-ttu-id="d40b7-176">有些驅動程式會使用內容金鑰，而不是使用工作階段金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="d40b7-176">Some drivers use a content key, instead of the session key, for encryption.</span></span> <span data-ttu-id="d40b7-177">內容金鑰可從一個畫面格變更為下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="d40b7-177">The content key could change from one frame to the next.</span></span>

     

5.  <span data-ttu-id="d40b7-178">此解碼器會將加密的壓縮緩衝區提交到加速器。</span><span class="sxs-lookup"><span data-stu-id="d40b7-178">The decoder submits the encrypted compressed buffers to the accelerator.</span></span> <span data-ttu-id="d40b7-179">針對 AES CTR，此解碼器也會傳遞初始化向量。</span><span class="sxs-lookup"><span data-stu-id="d40b7-179">For AES-CTR, the decoder also passes the initialization vector.</span></span> <span data-ttu-id="d40b7-180">如果使用內容金鑰，則此解碼會傳遞內容金鑰，並使用工作階段金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="d40b7-180">If a content key is used, the decoder passes content key, encrypted using the session key.</span></span>

<span data-ttu-id="d40b7-181">Direct3D 具有128位 AES CTR 的標準支援，但其設計目的是要延伸至其他加密類型。</span><span class="sxs-lookup"><span data-stu-id="d40b7-181">Direct3D has standard support for 128-bit AES-CTR, but is designed to extend to additional encryption types.</span></span>

<span data-ttu-id="d40b7-182">接下來的五個章節會提供更詳細的步驟。</span><span class="sxs-lookup"><span data-stu-id="d40b7-182">The next five sections give more detailed steps.</span></span>

-   [<span data-ttu-id="d40b7-183">1. 查詢驅動程式的內容保護功能</span><span class="sxs-lookup"><span data-stu-id="d40b7-183">1. Query the Content Protection Capabilities of the Driver</span></span>](#1-query-the-content-protection-capabilities-of-the-driver)
-   [<span data-ttu-id="d40b7-184">2. 設定已驗證的通道</span><span class="sxs-lookup"><span data-stu-id="d40b7-184">2. Configure the Authenticated Channel</span></span>](#2-configure-the-authenticated-channel)
-   [<span data-ttu-id="d40b7-185">3. 設定密碼編譯會話</span><span class="sxs-lookup"><span data-stu-id="d40b7-185">3. Configure the Cryptographic Session</span></span>](#3-configure-the-cryptographic-session)
-   [<span data-ttu-id="d40b7-186">4. 取得 DXVA 解碼器裝置的控制碼</span><span class="sxs-lookup"><span data-stu-id="d40b7-186">4. Get a Handle to the DXVA Decoder Device</span></span>](#4-get-a-handle-to-the-dxva-decoder-device)
-   [<span data-ttu-id="d40b7-187">5. 將 DXVA 解碼器與密碼編譯會話產生關聯</span><span class="sxs-lookup"><span data-stu-id="d40b7-187">5. Associate the DXVA Decoder with the Cryptographic Session</span></span>](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a><span data-ttu-id="d40b7-188">1. 查詢驅動程式的內容保護功能</span><span class="sxs-lookup"><span data-stu-id="d40b7-188">1. Query the Content Protection Capabilities of the Driver</span></span>

<span data-ttu-id="d40b7-189">嘗試套用加密之前，請先取得驅動程式的內容保護功能。</span><span class="sxs-lookup"><span data-stu-id="d40b7-189">Before attempting to apply encryption, get the content protection capabilities of the driver.</span></span>

1.  <span data-ttu-id="d40b7-190">取得 Direct3D 9 裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="d40b7-190">Get a pointer to the Direct3D 9 device.</span></span>
2.  <span data-ttu-id="d40b7-191">呼叫 [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)介面的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="d40b7-191">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) interface.</span></span>
3.  <span data-ttu-id="d40b7-192">呼叫 [**IDirect3DDevice9Video：： GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-192">Call [**IDirect3DDevice9Video::GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps).</span></span> <span data-ttu-id="d40b7-193">這個方法會在 [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) 結構中填入驅動程式的內容保護功能。</span><span class="sxs-lookup"><span data-stu-id="d40b7-193">This method fills in a [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) structure with the driver’s content protection capabilities.</span></span>

<span data-ttu-id="d40b7-194">請特別注意下列功能：</span><span class="sxs-lookup"><span data-stu-id="d40b7-194">In particular, look for the following capabilities:</span></span>

-   <span data-ttu-id="d40b7-195">如果 **Caps** 成員包含 **D3DCPCAPS_SOFTWARE** 或 **D3DCPCAPS_HARDWARE** 旗標，驅動程式就可以執行加密。</span><span class="sxs-lookup"><span data-stu-id="d40b7-195">If the **Caps** member contains the **D3DCPCAPS_SOFTWARE** or **D3DCPCAPS_HARDWARE** flag, the driver can perform encryption.</span></span>
-   <span data-ttu-id="d40b7-196">**KeyExchangeType** 成員會指定如何執行工作階段金鑰的金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="d40b7-196">The **KeyExchangeType** member specifies how to perform key exchange for the session key.</span></span>
-   <span data-ttu-id="d40b7-197">如果 **Caps** 成員包含 **D3DCPCAPS_CONTENTKEY** 旗標，驅動程式會使用不同的內容金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="d40b7-197">If the **Caps** member contains the **D3DCPCAPS_CONTENTKEY** flag, the driver uses a separate content key for encryption.</span></span> <span data-ttu-id="d40b7-198">當您產生工作階段金鑰時，這很重要。</span><span class="sxs-lookup"><span data-stu-id="d40b7-198">This is important when you generate the session key.</span></span>

<span data-ttu-id="d40b7-199">**Caps** 成員中會指出額外的功能。</span><span class="sxs-lookup"><span data-stu-id="d40b7-199">Additional capabilities are indicated in the **Caps** member.</span></span>

### <a name="2-configure-the-authenticated-channel"></a><span data-ttu-id="d40b7-200">2. 設定已驗證的通道</span><span class="sxs-lookup"><span data-stu-id="d40b7-200">2. Configure the Authenticated Channel</span></span>

<span data-ttu-id="d40b7-201">下一步是設定已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="d40b7-201">The next step is to configure the authenticated channel.</span></span>

1.  <span data-ttu-id="d40b7-202">呼叫 [**IDirect3DDevice9Video：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) 來建立已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="d40b7-202">Call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) to create the authenticated channel.</span></span> <span data-ttu-id="d40b7-203">針對 *ChannelType* 參數，指定符合驅動程式功能的通道類型。</span><span class="sxs-lookup"><span data-stu-id="d40b7-203">For the *ChannelType* parameter, specify a channel type that matches the capabilities of the driver.</span></span>
    -   <span data-ttu-id="d40b7-204">**D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** 通道類型對應到 **D3DCPCAPS_SOFTWARE**。</span><span class="sxs-lookup"><span data-stu-id="d40b7-204">The **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** channel type corresponds to **D3DCPCAPS_SOFTWARE**.</span></span>
    -   <span data-ttu-id="d40b7-205">**D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** 通道類型對應到 **D3DCPCAPS_HARDWARE**。</span><span class="sxs-lookup"><span data-stu-id="d40b7-205">The **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** channel type corresponds to **D3DCPCAPS_HARDWARE**.</span></span>

    <span data-ttu-id="d40b7-206">**CreateAuthenticatedChannel** 方法會傳回 [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)介面的指標，以及通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-206">The **CreateAuthenticatedChannel** method returns a pointer to the [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) interface along with a handle to the channel.</span></span> <span data-ttu-id="d40b7-207">稍後會使用此控制碼，將密碼編譯會話與已驗證的通道產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d40b7-207">The handle is used later to associate the cryptographic session with the authenticated channel.</span></span>
2.  <span data-ttu-id="d40b7-208">呼叫 [**IDirect3DAuthenticatedChannel9：： GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) ，以取得驅動程式的 x.509 憑證的大小。</span><span class="sxs-lookup"><span data-stu-id="d40b7-208">Call [**IDirect3DAuthenticatedChannel9::GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) to get the size of the driver's X.509 certificate.</span></span> <span data-ttu-id="d40b7-209">配置所需大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d40b7-209">Allocate a buffer of the required size.</span></span>
3.  <span data-ttu-id="d40b7-210">呼叫 [**IDirect3DAuthenticatedChannel9：： GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) 以取得憑證。</span><span class="sxs-lookup"><span data-stu-id="d40b7-210">Call [**IDirect3DAuthenticatedChannel9::GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) to get the certificate.</span></span> <span data-ttu-id="d40b7-211">方法會將憑證複製到在上一個步驟中配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d40b7-211">The method copies the certificate into the buffer that was allocated in the previous step.</span></span>
4.  <span data-ttu-id="d40b7-212">確認驅動程式的憑證已由 Microsoft 簽署，但尚未撤銷。</span><span class="sxs-lookup"><span data-stu-id="d40b7-212">Verify that the driver’s certificate was signed by Microsoft and has not been revoked.</span></span>
5.  <span data-ttu-id="d40b7-213">從憑證取得公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-213">Get the public key from the certificate.</span></span>
6.  <span data-ttu-id="d40b7-214">產生隨機的 RSA 工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-214">Generate a random RSA session key.</span></span> <span data-ttu-id="d40b7-215">此工作階段金鑰是用來簽署傳送至已驗證通道的資料。</span><span class="sxs-lookup"><span data-stu-id="d40b7-215">This session key is used to sign data that is sent to the authenticated channel.</span></span> <span data-ttu-id="d40b7-216">使用驅動程式的公開金鑰來加密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-216">Encrypt the session key using the driver's public key.</span></span>
7.  <span data-ttu-id="d40b7-217">呼叫 [**IDirect3DAuthenticatedChannel9：： NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) ，將加密的工作階段金鑰傳送至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d40b7-217">Call [**IDirect3DAuthenticatedChannel9::NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) to send the encrypted session key to the driver.</span></span>
8.  <span data-ttu-id="d40b7-218">將安全通道初始化，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d40b7-218">Initialize the secure channel as follows:</span></span>
    1.  <span data-ttu-id="d40b7-219">填入檔中所述的 [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d40b7-219">Fill in a [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) structure as described in the documentation.</span></span>
    2.  <span data-ttu-id="d40b7-220">藉由呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)來傳送 [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md)命令，如傳送 [已驗證的通道命令](#sending-authenticated-channel-commands)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="d40b7-220">Send the [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) command by calling [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) as described in the section [Sending Authenticated Channel Commands](#sending-authenticated-channel-commands).</span></span> <span data-ttu-id="d40b7-221">此命令包含傳送至已驗證通道之命令和查詢的起始序號。</span><span class="sxs-lookup"><span data-stu-id="d40b7-221">This command contains the starting sequence numbers for the commands and queries that are sent to the authenticated channel.</span></span>
9.  <span data-ttu-id="d40b7-222">將 [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) 查詢傳送給已驗證的通道，以驗證通道類型，如傳送 [已驗證的通道查詢](#sending-authenticated-channel-queries)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="d40b7-222">Verify the channel type by sending a [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) query to the authenticated channel, as described in the section [Sending Authenticated Channel Queries](#sending-authenticated-channel-queries).</span></span> <span data-ttu-id="d40b7-223">檢查通道類型是否符合您在 [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) 方法中指定的專案。</span><span class="sxs-lookup"><span data-stu-id="d40b7-223">Check that the channel type matches what you specified in the [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) method.</span></span>

### <a name="3-configure-the-cryptographic-session"></a><span data-ttu-id="d40b7-224">3. 設定密碼編譯會話</span><span class="sxs-lookup"><span data-stu-id="d40b7-224">3. Configure the Cryptographic Session</span></span>

<span data-ttu-id="d40b7-225">接下來，設定密碼編譯會話，並建立工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-225">Next, configure the cryptographic session and establish the session key.</span></span>

1.  <span data-ttu-id="d40b7-226">呼叫 [**IDirect3DDevice9Video：： CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) 來建立密碼編譯會話。</span><span class="sxs-lookup"><span data-stu-id="d40b7-226">Call [**IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) to create the cryptographic session.</span></span> <span data-ttu-id="d40b7-227">這個方法會傳回 [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) 介面的指標，以及密碼編譯會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-227">This method returns a pointer to the [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) interface and along with a handle to the cryptographic session.</span></span>
2.  <span data-ttu-id="d40b7-228">呼叫 [**IDirect3DCryptoSession9：： GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) ，以取得驅動程式的 x.509 憑證的大小。</span><span class="sxs-lookup"><span data-stu-id="d40b7-228">Call [**IDirect3DCryptoSession9::GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) to get the size of the driver's X.509 certificate.</span></span> <span data-ttu-id="d40b7-229">配置所需大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d40b7-229">Allocate a buffer of the required size.</span></span>
3.  <span data-ttu-id="d40b7-230">呼叫 [**IDirect3DCryptoSession9：： GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) 以取得憑證。</span><span class="sxs-lookup"><span data-stu-id="d40b7-230">Call [**IDirect3DCryptoSession9::GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) to get the certificate.</span></span> <span data-ttu-id="d40b7-231">方法會將憑證複製到在上一個步驟中配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d40b7-231">The method copies the certificate into the buffer that was allocated in the previous step.</span></span>
4.  <span data-ttu-id="d40b7-232">確認驅動程式的憑證已由 Microsoft 簽署，但尚未撤銷。</span><span class="sxs-lookup"><span data-stu-id="d40b7-232">Verify that the driver’s certificate was signed by Microsoft and has not been revoked.</span></span>
5.  <span data-ttu-id="d40b7-233">從憑證取得公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-233">Get the public key from the certificate.</span></span>
6.  <span data-ttu-id="d40b7-234">產生隨機的 RSA 工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-234">Generate a random RSA session key.</span></span> <span data-ttu-id="d40b7-235">這是來自已驗證通道工作階段金鑰的個別工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-235">This is a separate session key from the authenticated channel session key.</span></span> <span data-ttu-id="d40b7-236">使用驅動程式的公開金鑰來加密工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-236">Encrypt the session key using the driver's public key.</span></span>
7.  <span data-ttu-id="d40b7-237">呼叫 [**IDirect3DCryptoSession9：： NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) ，將加密的工作階段金鑰傳送至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d40b7-237">Call [**IDirect3DCryptoSession9::NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) to send the encrypted session key to the driver.</span></span>
8.  <span data-ttu-id="d40b7-238">如果內容保護功能包含 **D3DCPCAPS_CONTENTKEY**，請建立隨機的 RSA 內容金鑰。</span><span class="sxs-lookup"><span data-stu-id="d40b7-238">If the content protection capabilities include **D3DCPCAPS_CONTENTKEY**, create a random RSA content key.</span></span> <span data-ttu-id="d40b7-239">稍後會在解碼程式中使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="d40b7-239">This will be used later in the decoding process.</span></span>

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a><span data-ttu-id="d40b7-240">4. 取得 DXVA 解碼器裝置的控制碼</span><span class="sxs-lookup"><span data-stu-id="d40b7-240">4. Get a Handle to the DXVA Decoder Device</span></span>

<span data-ttu-id="d40b7-241">在下一個步驟中，您將需要 DXVA 解碼器裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-241">For the next step, you will need a handle to the DXVA decoder device.</span></span> <span data-ttu-id="d40b7-242">若要取得此控制碼，請填寫 DXVA2_DecodeExecuteParams 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d40b7-242">To get this handle, fill in a DXVA2_DecodeExecuteParams structure as follows:</span></span>


```C++
HANDLE hDecodeDeviceHandle;

DXVA2_DecodeExecuteParams execParams = {0};
DXVA2_DecodeExtensionData ExtensionExecute = {0};
    
execParams.NumCompBuffers = 0;
execParams.pCompressedBuffers = NULL;
execParams.pExtensionData = &ExtensionExecute;

ExtensionExecute.Function = DXVA2_DECODE_GET_DRIVER_HANDLE;
ExtensionExecute.pPrivateInputData = NULL;
ExtensionExecute.PrivateInputDataSize = 0;
ExtensionExecute.pPrivateOutputData = &hDecodeDeviceHandle;
ExtensionExecute.PrivateOutputDataSize = sizeof(HANDLE);
```



<span data-ttu-id="d40b7-243">將 [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams)結構的 **pExtensionData** 成員設定為 [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata)結構的位址。</span><span class="sxs-lookup"><span data-stu-id="d40b7-243">Set the **pExtensionData** member of the [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) structure to the address of a [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) structure.</span></span>

<span data-ttu-id="d40b7-244">在 [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) 結構中，將 **函數** 成員設定為 **DXVA2_DECODE_GET_DRIVER_HANDLE**。</span><span class="sxs-lookup"><span data-stu-id="d40b7-244">In the [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) structure, set the **Function** member to **DXVA2_DECODE_GET_DRIVER_HANDLE**.</span></span> <span data-ttu-id="d40b7-245">將 **pPrivateOutputData** 設定為足以儲存 **控制碼** 值的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="d40b7-245">Set **pPrivateOutputData** to the address of a buffer that is large enough to store a **HANDLE** value.</span></span> <span data-ttu-id="d40b7-246"> (在上述範例中，此緩衝區是 *hDecodeDeviceHandle* 變數。 ) </span><span class="sxs-lookup"><span data-stu-id="d40b7-246">(In the previous example, this buffer is the *hDecodeDeviceHandle* variable.)</span></span>

<span data-ttu-id="d40b7-247">然後呼叫 [**IDirectXVideoDecoder：： Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) 並傳入 [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="d40b7-247">Then call [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) and pass in the address of the [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) structure.</span></span> <span data-ttu-id="d40b7-248">DXVA 解碼器的控制碼會在 **pPrivateOutputData** 中傳回。</span><span class="sxs-lookup"><span data-stu-id="d40b7-248">The handle to the DXVA decoder is returned in **pPrivateOutputData**.</span></span>

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a><span data-ttu-id="d40b7-249">5. 將 DXVA 解碼器與密碼編譯會話產生關聯</span><span class="sxs-lookup"><span data-stu-id="d40b7-249">5. Associate the DXVA Decoder with the Cryptographic Session</span></span>

<span data-ttu-id="d40b7-250">接下來，將 DXVA 解碼器裝置與 Direct3D 裝置和密碼編譯會話產生關聯，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d40b7-250">Next, associate the DXVA decoder device with the Direct3D device and the cryptographic session, as follows:</span></span>

1.  <span data-ttu-id="d40b7-251">取得 DXVA 解碼器裝置的控制碼，如上一節中所述。</span><span class="sxs-lookup"><span data-stu-id="d40b7-251">Get a handle to the DXVA decoder device, as described in the previous section.</span></span>
2.  <span data-ttu-id="d40b7-252">將 [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) 查詢傳送至已驗證的通道，以取得 Direct3D 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-252">Get a handle to the Direct3D device, by sending a [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) query to the authenticated channel.</span></span>
3.  <span data-ttu-id="d40b7-253">在 [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) 結構中填入下列資訊：</span><span class="sxs-lookup"><span data-stu-id="d40b7-253">Fill in a [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) structure with the following information:</span></span>
    -   <span data-ttu-id="d40b7-254">將 **DXVA2DecodeHandle** 成員設定為 DXVA 解碼器裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-254">Set the **DXVA2DecodeHandle** member to the handle to the DXVA decoder device.</span></span>
    -   <span data-ttu-id="d40b7-255">將 **CryptoSessionHandle** 成員設定為密碼編譯會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-255">Set the **CryptoSessionHandle** member to the handle to the cryptographic session.</span></span> <span data-ttu-id="d40b7-256">[**IDirect3DDevice9Video：： CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession)方法會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-256">This handle is returned by the [**IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) method.</span></span>
    -   <span data-ttu-id="d40b7-257">將 **DeviceHandle** 成員設定為 Direct3D 裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-257">Set the **DeviceHandle** member to the Direct3D device handle.</span></span>
4.  <span data-ttu-id="d40b7-258">呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 以傳送 [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) 命令給已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="d40b7-258">Call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) to send a [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) command to the authenticated channel.</span></span>

<span data-ttu-id="d40b7-259">下圖說明控制碼的交換：</span><span class="sxs-lookup"><span data-stu-id="d40b7-259">The following diagram illustrates the exchange of handles:</span></span>

![此圖顯示 dxva 解碼器如何與密碼編譯會話相關聯。](images/d3d9video03.png)

<span data-ttu-id="d40b7-261">軟體解碼器現在可以使用密碼編譯工作階段金鑰來加密壓縮的影片緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d40b7-261">The software decoder can now use the cryptographic session key to encrypt the compressed video buffers.</span></span> <span data-ttu-id="d40b7-262">每個壓縮的緩衝區都會有自己的初始化向量 (IV) 在 [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc)結構的 **pvPVPState** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="d40b7-262">Each compressed buffer will have its own initialization vector (IV) specified in the **pvPVPState** member of the [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) structure.</span></span>

## <a name="sending-authenticated-channel-commands"></a><span data-ttu-id="d40b7-263">傳送已驗證的通道命令</span><span class="sxs-lookup"><span data-stu-id="d40b7-263">Sending Authenticated Channel Commands</span></span>

<span data-ttu-id="d40b7-264">定義了一組命令來設定已驗證的通道和設定各種內容保護。</span><span class="sxs-lookup"><span data-stu-id="d40b7-264">A set of commands are defined for configuring the authenticated channel and setting various content protections.</span></span> <span data-ttu-id="d40b7-265">如需命令清單，請參閱 [內容保護命令](content-protection-commands.md)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-265">For a list of commands, see [Content Protection Commands](content-protection-commands.md).</span></span>

<span data-ttu-id="d40b7-266">若要將命令傳送至已驗證的通道，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="d40b7-266">To send a command to the authenticated channel, perform the following steps.</span></span>

1.  <span data-ttu-id="d40b7-267">填寫輸入資料結構。</span><span class="sxs-lookup"><span data-stu-id="d40b7-267">Fill in the input data structure.</span></span> <span data-ttu-id="d40b7-268">此資料結構一律是 [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) 結構，後面接著其他欄位。</span><span class="sxs-lookup"><span data-stu-id="d40b7-268">This data structure is always a [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) structure followed by additional fields.</span></span> <span data-ttu-id="d40b7-269">填寫 **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** 結構，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="d40b7-269">Fill in the **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** structure as shown in the following table.</span></span>

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d40b7-270">member</span><span class="sxs-lookup"><span data-stu-id="d40b7-270">Member</span></span></th>
    <th><span data-ttu-id="d40b7-271">描述</span><span class="sxs-lookup"><span data-stu-id="d40b7-271">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="d40b7-272"><strong>omac</strong></span><span class="sxs-lookup"><span data-stu-id="d40b7-272"><strong>omac</strong></span></span></td>
    <td><span data-ttu-id="d40b7-273">請立即略過此欄位。</span><span class="sxs-lookup"><span data-stu-id="d40b7-273">Skip this field for now.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d40b7-274"><strong>ConfigureType</strong></span><span class="sxs-lookup"><span data-stu-id="d40b7-274"><strong>ConfigureType</strong></span></span></td>
    <td><span data-ttu-id="d40b7-275">識別命令的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d40b7-275">GUID that identifies the command.</span></span> <span data-ttu-id="d40b7-276">如需命令清單，請參閱 <a href="content-protection-commands.md">內容保護命令</a>。</span><span class="sxs-lookup"><span data-stu-id="d40b7-276">For a list of commands, see <a href="content-protection-commands.md">Content Protection Commands</a>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d40b7-277"><strong>hChannel</strong></span><span class="sxs-lookup"><span data-stu-id="d40b7-277"><strong>hChannel</strong></span></span></td>
    <td><span data-ttu-id="d40b7-278">已驗證通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-278">The handle to the authenticated channel.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d40b7-279"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="d40b7-279"><strong>SequenceNumber</strong></span></span></td>
    <td><span data-ttu-id="d40b7-280">序號。</span><span class="sxs-lookup"><span data-stu-id="d40b7-280">The sequence number.</span></span> <span data-ttu-id="d40b7-281">第一個序號是藉由傳送 <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="d40b7-281">The first sequence number is specified by sending a <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> command.</span></span> <span data-ttu-id="d40b7-282">每次您傳送另一個命令時，就會將此數位遞增1。</span><span class="sxs-lookup"><span data-stu-id="d40b7-282">Each time you send another command, increment this number by 1.</span></span> <span data-ttu-id="d40b7-283">此序號會防止重新執行攻擊。</span><span class="sxs-lookup"><span data-stu-id="d40b7-283">The sequence number guards against replay attacks.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="d40b7-284">使用兩個不同的序號，一個用於命令，一個用於查詢。</span><span class="sxs-lookup"><span data-stu-id="d40b7-284">Two separate sequence numbers are used, one for commands and one for queries.</span></span>
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="d40b7-285">針對出現在輸入結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。</span><span class="sxs-lookup"><span data-stu-id="d40b7-285">Calculate the OMAC tag for the block of data that appears after the **omac** member of the input structure.</span></span> <span data-ttu-id="d40b7-286">然後將此標記值複製到 **omac** 成員中。</span><span class="sxs-lookup"><span data-stu-id="d40b7-286">Then copy this tag value into the **omac** member.</span></span>
3.  <span data-ttu-id="d40b7-287">呼叫 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-287">Call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>
4.  <span data-ttu-id="d40b7-288">驅動程式會將命令的輸出放在 [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) 結構中。</span><span class="sxs-lookup"><span data-stu-id="d40b7-288">The driver places the output from the command in the [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) structure.</span></span>
5.  <span data-ttu-id="d40b7-289">針對出現在輸出結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。</span><span class="sxs-lookup"><span data-stu-id="d40b7-289">Calculate the OMAC tag for the block of data that appears after the **omac** member of the output structure.</span></span> <span data-ttu-id="d40b7-290">將此值與 **omac** 成員的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="d40b7-290">Compare this with the value of the **omac** member.</span></span> <span data-ttu-id="d40b7-291">如果不相符，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="d40b7-291">Fail if they do not match.</span></span>
6.  <span data-ttu-id="d40b7-292">比較輸出結構中 **ConfigureType**、 **hChannel** 和 **SequenceNumber** 成員的值與這些成員的值。</span><span class="sxs-lookup"><span data-stu-id="d40b7-292">Compare the values of the **ConfigureType**, **hChannel**, and **SequenceNumber** members in the output structure against your values for those members.</span></span> <span data-ttu-id="d40b7-293">如果不相符，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="d40b7-293">Fail if they do not match.</span></span>
7.  <span data-ttu-id="d40b7-294">遞增下一個命令的序號。</span><span class="sxs-lookup"><span data-stu-id="d40b7-294">Increment the sequence number for the next command.</span></span>

## <a name="sending-authenticated-channel-queries"></a><span data-ttu-id="d40b7-295">傳送已驗證的通道查詢</span><span class="sxs-lookup"><span data-stu-id="d40b7-295">Sending Authenticated Channel Queries</span></span>

<span data-ttu-id="d40b7-296">系統會定義一組查詢來取得已驗證通道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d40b7-296">A set of queries are defined for retrieving information about the authenticated channel.</span></span> <span data-ttu-id="d40b7-297">如需查詢清單，請參閱 [內容保護查詢](content-protection-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-297">For a list of queries, see [Content Protection Queries](content-protection-queries.md).</span></span>

<span data-ttu-id="d40b7-298">若要將命令傳送至已驗證的通道，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="d40b7-298">To send a command to the authenticated channel, perform the following steps.</span></span>

1.  <span data-ttu-id="d40b7-299">填寫輸入資料結構。</span><span class="sxs-lookup"><span data-stu-id="d40b7-299">Fill in the input data structure.</span></span> <span data-ttu-id="d40b7-300">此資料結構一律是 [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) 結構，後面可能接著其他欄位。</span><span class="sxs-lookup"><span data-stu-id="d40b7-300">This data structure is always a [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) structure, possibly followed by additional fields.</span></span> <span data-ttu-id="d40b7-301">填寫 **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** 結構，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="d40b7-301">Fill in the **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** structure as shown in the following table.</span></span>

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d40b7-302">member</span><span class="sxs-lookup"><span data-stu-id="d40b7-302">Member</span></span></th>
    <th><span data-ttu-id="d40b7-303">描述</span><span class="sxs-lookup"><span data-stu-id="d40b7-303">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="d40b7-304"><strong>QueryType</strong></span><span class="sxs-lookup"><span data-stu-id="d40b7-304"><strong>QueryType</strong></span></span></td>
    <td><span data-ttu-id="d40b7-305">識別查詢的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d40b7-305">GUID that identifies the query.</span></span> <span data-ttu-id="d40b7-306">如需查詢清單，請參閱 <a href="content-protection-queries.md">內容保護查詢</a>。</span><span class="sxs-lookup"><span data-stu-id="d40b7-306">For a list of queries, see <a href="content-protection-queries.md">Content Protection Queries</a>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d40b7-307"><strong>hChannel</strong></span><span class="sxs-lookup"><span data-stu-id="d40b7-307"><strong>hChannel</strong></span></span></td>
    <td><span data-ttu-id="d40b7-308">已驗證通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d40b7-308">The handle to the authenticated channel.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d40b7-309"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="d40b7-309"><strong>SequenceNumber</strong></span></span></td>
    <td><span data-ttu-id="d40b7-310">序號。</span><span class="sxs-lookup"><span data-stu-id="d40b7-310">The sequence number.</span></span> <span data-ttu-id="d40b7-311">第一個序號是藉由傳送 <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> 命令來指定。</span><span class="sxs-lookup"><span data-stu-id="d40b7-311">The first sequence number is specified by sending a <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> command.</span></span> <span data-ttu-id="d40b7-312">每次您傳送另一個查詢時，會將此數位遞增1。</span><span class="sxs-lookup"><span data-stu-id="d40b7-312">Each time you send another query, increment this number by 1.</span></span> <span data-ttu-id="d40b7-313">此序號會防止重新執行攻擊。</span><span class="sxs-lookup"><span data-stu-id="d40b7-313">The sequence number guards against replay attacks.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="d40b7-314">使用兩個不同的序號，一個用於命令，一個用於查詢。</span><span class="sxs-lookup"><span data-stu-id="d40b7-314">Two separate sequence numbers are used, one for commands and one for queries.</span></span>
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="d40b7-315">呼叫 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="d40b7-315">Call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>
3.  <span data-ttu-id="d40b7-316">驅動程式會將查詢的輸出放在 [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) 結構中。</span><span class="sxs-lookup"><span data-stu-id="d40b7-316">The driver places the output from the query in a [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure.</span></span> <span data-ttu-id="d40b7-317">根據查詢類型而定，這個結構後面會接著其他欄位。</span><span class="sxs-lookup"><span data-stu-id="d40b7-317">This structure is followed by additional fields, depending on the query type.</span></span>
4.  <span data-ttu-id="d40b7-318">針對出現在輸出結構之 **OMAC** 成員後面的資料區塊，計算 OMAC 標記。</span><span class="sxs-lookup"><span data-stu-id="d40b7-318">Calculate the OMAC tag for the block of data that appears after the **omac** member of the output structure.</span></span> <span data-ttu-id="d40b7-319">將此值與 **omac** 成員的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="d40b7-319">Compare this with the value of the **omac** member.</span></span> <span data-ttu-id="d40b7-320">如果不相符，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="d40b7-320">Fail if they do not match.</span></span>
5.  <span data-ttu-id="d40b7-321">比較輸出結構中 **ConfigureType**、 **hChannel** 和 **SequenceNumber** 成員的值與這些成員的值。</span><span class="sxs-lookup"><span data-stu-id="d40b7-321">Compare the values of the **ConfigureType**, **hChannel**, and **SequenceNumber** members in the output structure against your values for those members.</span></span> <span data-ttu-id="d40b7-322">如果不相符，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="d40b7-322">Fail if they do not match.</span></span>
6.  <span data-ttu-id="d40b7-323">遞增下一個查詢的序號。</span><span class="sxs-lookup"><span data-stu-id="d40b7-323">Increment the sequence number for the next query.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d40b7-324">相關主題</span><span class="sxs-lookup"><span data-stu-id="d40b7-324">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d40b7-325">Direct3D 9 影片 Api</span><span class="sxs-lookup"><span data-stu-id="d40b7-325">Direct3D 9 Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 
