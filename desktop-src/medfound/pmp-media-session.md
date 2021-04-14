---
description: .
ms.assetid: CF3A427D-31D2-45FF-BE87-F192B758204E
title: PMP 媒體會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0e14d9e403620d273bb4aeb3347cba523f304b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321447"
---
# <a name="pmp-media-session"></a><span data-ttu-id="06887-103">PMP 媒體會話</span><span class="sxs-lookup"><span data-stu-id="06887-103">PMP Media Session</span></span>

<span data-ttu-id="06887-104">應用程式可以在稱為[受保護媒體路徑](protected-media-path.md) (PMP) 進程的個別進程中建立[媒體會話](media-session.md)。</span><span class="sxs-lookup"><span data-stu-id="06887-104">An application can create the [Media Session](media-session.md) in a separate process called the [Protected Media Path](protected-media-path.md) (PMP) process.</span></span> <span data-ttu-id="06887-105">PMP 程式的主要目的是要使用數位版權管理 (DRM) 來啟用受保護內容的播放。</span><span class="sxs-lookup"><span data-stu-id="06887-105">The main purpose of the PMP process is to enable playback of protected content using digital rights management (DRM).</span></span> <span data-ttu-id="06887-106">根據預設，PMP 程式會在受保護的環境內建立 (PE) 。</span><span class="sxs-lookup"><span data-stu-id="06887-106">By default, the PMP process is created inside a Protected Environment (PE).</span></span> <span data-ttu-id="06887-107">只有受信任的、簽署的元件可以載入 PE 內。</span><span class="sxs-lookup"><span data-stu-id="06887-107">Only trusted, signed components can be loaded inside a PE.</span></span> <span data-ttu-id="06887-108">PMP 程式的第二個優點是它會將應用程式進程與媒體管線隔離。</span><span class="sxs-lookup"><span data-stu-id="06887-108">A secondary benefit of the PMP process is that it isolates the application process from the media pipeline.</span></span> <span data-ttu-id="06887-109">如需 PMP 程式的詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。</span><span class="sxs-lookup"><span data-stu-id="06887-109">For more information about the PMP process, see [Protected Media Path](protected-media-path.md).</span></span>

<span data-ttu-id="06887-110">若要在 PMP 進程內建立媒體會話，請呼叫 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) 函式。</span><span class="sxs-lookup"><span data-stu-id="06887-110">To create the Media Session inside the PMP process, call the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span> <span data-ttu-id="06887-111">（選擇性）您可以傳入 **MFPMPSESSION 未 \_ 受保護的 \_ 進程** 旗標。</span><span class="sxs-lookup"><span data-stu-id="06887-111">Optionally, you can pass in the **MFPMPSESSION\_UNPROTECTED\_PROCESS** flag.</span></span> <span data-ttu-id="06887-112">如果設定此旗標，則會在未受保護的進程內建立 PMP 進程，而不是在 PE 進程中建立。</span><span class="sxs-lookup"><span data-stu-id="06887-112">If this flag is set, the PMP process is created inside an unprotected process, and not a PE process.</span></span> <span data-ttu-id="06887-113">未受保護的進程無法用於 DRM 播放，但可提供程式隔離的優點。</span><span class="sxs-lookup"><span data-stu-id="06887-113">The unprotected process cannot be used for DRM playback, but does give you the benefits of process isolation.</span></span>

<span data-ttu-id="06887-114">[**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函式會將指標傳回給媒體會話的 proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="06887-114">The [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function returns a pointer to a proxy object for the Media Session.</span></span> <span data-ttu-id="06887-115">應用程式會透過 proxy 與媒體會話進行通訊。</span><span class="sxs-lookup"><span data-stu-id="06887-115">The application communicates with the Media Session through the proxy.</span></span>

![pmp 流程內媒體會話的圖例](images/pmp01.png)

<span data-ttu-id="06887-117">根據預設，當應用程式建立拓撲時，會在應用程式進程內建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="06887-117">By default, when the application creates a topology, the media source is created inside the application process.</span></span> <span data-ttu-id="06887-118">媒體來源的 proxy 是在 PMP 進程內建立的。</span><span class="sxs-lookup"><span data-stu-id="06887-118">A proxy to the media source is created inside the PMP process.</span></span> <span data-ttu-id="06887-119">媒體來源可以使用 [**IMFPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) 介面，在 PMP 進程內建立物件。</span><span class="sxs-lookup"><span data-stu-id="06887-119">The media source can create objects inside the PMP process by using the [**IMFPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) interface.</span></span> <span data-ttu-id="06887-120">例如，為了支援 DRM，媒體來源會建立名為「 *輸入信任授權* 單位」的物件 (ITA) 。</span><span class="sxs-lookup"><span data-stu-id="06887-120">For example, to support DRM, a media source creates an object called an *input trust authority* (ITA).</span></span> <span data-ttu-id="06887-121">您必須在 PMP 程式內建立 ITA。</span><span class="sxs-lookup"><span data-stu-id="06887-121">The ITA must be created inside the PMP process.</span></span> <span data-ttu-id="06887-122"> (需 ITAs 的詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。 ) 若要使用 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 介面，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="06887-122">(For more information about ITAs, see [Protected Media Path](protected-media-path.md).) To use the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface, do the following:</span></span>

1.  <span data-ttu-id="06887-123">媒體來源必須執行 [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) 介面。</span><span class="sxs-lookup"><span data-stu-id="06887-123">The media source must implement the [**IMFPMPClient**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient) interface.</span></span>
2.  <span data-ttu-id="06887-124">在拓撲解析期間，媒體會話 proxy 會呼叫媒體來源上的 [**IMFPMPClient：： SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) 方法。</span><span class="sxs-lookup"><span data-stu-id="06887-124">During topology resolution, the Media Session proxy calls the [**IMFPMPClient::SetPMPHost**](/windows/desktop/api/mfidl/nf-mfidl-imfpmpclient-setpmphost) method on the media source.</span></span>
3.  <span data-ttu-id="06887-125">媒體來源會呼叫 [**IMFPMPHost：： CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) ，以在 PMP 進程內建立物件。</span><span class="sxs-lookup"><span data-stu-id="06887-125">The media source calls [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) to create the object inside the PMP process.</span></span> <span data-ttu-id="06887-126">物件必須有已註冊的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="06887-126">The object must have a registered CLSID.</span></span> <span data-ttu-id="06887-127">此外，若要在 PE 中載入，物件必須是受信任且經過數位簽署。</span><span class="sxs-lookup"><span data-stu-id="06887-127">Also, to load inside the PE, the object must be trusted and digitally signed.</span></span> <span data-ttu-id="06887-128">如需程式碼簽署受保護媒體元件的相關資訊，請參閱 [Windows Vista 中受保護媒體元件的白皮書程式碼簽署](/windows-hardware/test/hlk/)</span><span class="sxs-lookup"><span data-stu-id="06887-128">For information about code signing protected media components, see the white paper [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/)</span></span>

<span data-ttu-id="06887-129">下圖顯示在應用程式進程中建立的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="06887-129">The following illustration shows the media source created in the application process.</span></span>

![應用程式進程中媒體來源的圖例。](images/pmp02.png)

<span data-ttu-id="06887-131">另一個替代方式是在 PMP 會話內建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="06887-131">Another alternative is to create the media source inside the PMP session.</span></span>

1.  <span data-ttu-id="06887-132">當您建立媒體會話時，請設定 [ [**MF \_ 會話 \_ 遠端 \_ 來源 \_ 模式]**](mf-session-remote-source-mode-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="06887-132">Set the [**MF\_SESSION\_REMOTE\_SOURCE\_MODE**](mf-session-remote-source-mode-attribute.md) attribute when you create the Media Session.</span></span> <span data-ttu-id="06887-133">設定屬性是在 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數中指定。</span><span class="sxs-lookup"><span data-stu-id="06887-133">Configuration attributes are specified in the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>
2.  <span data-ttu-id="06887-134">在媒體會話上呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ，以取得 [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="06887-134">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the Media Session to get a pointer to the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface.</span></span> <span data-ttu-id="06887-135">服務識別碼為 **MF \_ PMP \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="06887-135">The service identifier is **MF\_PMP\_SERVICE**.</span></span>
3.  <span data-ttu-id="06887-136">使用類別識別碼 **CLSID \_ MFSourceResolver** 來呼叫 [**IMFPMPHost：： CREATEOBJECTBYCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) ，以在 PMP 流程內建立來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="06887-136">Call [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) with the class identifier **CLSID\_MFSourceResolver** to create the source resolver inside the PMP process.</span></span> <span data-ttu-id="06887-137">方法會將指標傳回給來源解析程式的 proxy。</span><span class="sxs-lookup"><span data-stu-id="06887-137">The method returns a pointer to a proxy for the source resolver.</span></span>
4.  <span data-ttu-id="06887-138">呼叫 [**IMFSourceResolver：： BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) 或 [**IMFSourceResolver：： BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) 來建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="06887-138">Call [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) or [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) to create the media source.</span></span>
    > [!Note]  
    > <span data-ttu-id="06887-139">在此情況下，您必須使用這些方法的非同步版本，因為同步版本無法遠端處理。</span><span class="sxs-lookup"><span data-stu-id="06887-139">In this case, you must use the asynchronous versions of these methods, because the synchronous versions are not remotable.</span></span>

     

<span data-ttu-id="06887-140">下圖顯示在 PMP 流程中建立的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="06887-140">The following illustration shows the media source created in the PMP process.</span></span>

![pmp 流程中媒體來源的圖例。](images/pmp03.png)

## <a name="related-topics"></a><span data-ttu-id="06887-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="06887-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06887-143">如何播放受保護的媒體檔案</span><span class="sxs-lookup"><span data-stu-id="06887-143">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> <dt>

[<span data-ttu-id="06887-144">媒體會話</span><span class="sxs-lookup"><span data-stu-id="06887-144">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="06887-145">受保護的媒體路徑</span><span class="sxs-lookup"><span data-stu-id="06887-145">Protected Media Path</span></span>](protected-media-path.md)
</dt> </dl>

 

 
