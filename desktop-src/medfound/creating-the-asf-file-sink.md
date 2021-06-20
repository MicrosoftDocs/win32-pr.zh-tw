---
description: 瞭解如何建立可讓應用程式用來將 ASF 媒體資料封存至檔案的 ASF file 接收器。
ms.assetid: 991f3345-a6b4-45c2-a89d-3c13c70b6bbc
title: 建立 ASF 檔接收器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fcd9ea19f0200dfd330f421fd5dac2cd100b702
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409921"
---
# <a name="creating-the-asf-file-sink"></a><span data-ttu-id="b1498-103">建立 ASF 檔接收器</span><span class="sxs-lookup"><span data-stu-id="b1498-103">Creating the ASF File Sink</span></span>

<span data-ttu-id="b1498-104">ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。</span><span class="sxs-lookup"><span data-stu-id="b1498-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="b1498-105">如需 ASF 媒體接收器的物件模型和一般使用方式的相關資訊，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。</span><span class="sxs-lookup"><span data-stu-id="b1498-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="b1498-106">有兩種方式可以建立 ASF 檔案接收的實例。</span><span class="sxs-lookup"><span data-stu-id="b1498-106">There are two ways of creating an instance of the ASF file sink.</span></span> <span data-ttu-id="b1498-107">您可以呼叫 [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) 或 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)。</span><span class="sxs-lookup"><span data-stu-id="b1498-107">You can call [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) or [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate).</span></span>

<span data-ttu-id="b1498-108">如果您呼叫 [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)，就必須指定輸出檔案的位元組資料流程，接收會在編碼會話期間寫入 ASF 內容。</span><span class="sxs-lookup"><span data-stu-id="b1498-108">If you call [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), you must specify a byte stream, for the output file, into which the sink will write the ASF content during an encoding session.</span></span> <span data-ttu-id="b1498-109">指定的位元組資料流程必須具有可搜尋和可寫入的功能，否則 **MFCreateASFMediaSink** 呼叫會失敗，並出現 E \_ 失敗的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b1498-109">The specified byte stream must have seekable and writable capabilities otherwise the **MFCreateASFMediaSink** call fails with the E\_FAIL error code.</span></span> <span data-ttu-id="b1498-110">此呼叫會建立同進程的檔案接收物件，並將指標傳回至 file 接收器的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) 介面。</span><span class="sxs-lookup"><span data-stu-id="b1498-110">This call creates an in-process file sink object and returns a pointer to the [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface of the file sink.</span></span>

<span data-ttu-id="b1498-111">如果您呼叫 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)，就必須指定檔案接收寫入媒體資料的輸出檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="b1498-111">If you call [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), you must specify the URL of the output file into which the file sink will write media data.</span></span> <span data-ttu-id="b1498-112">在此情況下，檔案接收會在內部建立位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="b1498-112">In this case, the file sink internally creates the byte stream.</span></span> <span data-ttu-id="b1498-113">函數會傳回檔案接收之 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b1498-113">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface of the file sink.</span></span> <span data-ttu-id="b1498-114">收件者</span><span class="sxs-lookup"><span data-stu-id="b1498-114">To</span></span>

<span data-ttu-id="b1498-115">當您的編碼拓撲設計如下時，請考慮 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) 而不是 [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)：</span><span class="sxs-lookup"><span data-stu-id="b1498-115">Consider [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) instead of [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink), when your encoding topology is designed as follows:</span></span>

-   <span data-ttu-id="b1498-116">編碼拓撲適用于受保護的媒體路徑 (PMP) ，而 file 接收器則是跨進程使用。</span><span class="sxs-lookup"><span data-stu-id="b1498-116">The encoding topology is for the protected media path (PMP) and the file sink is used out-of-process.</span></span>
-   <span data-ttu-id="b1498-117">拓撲的輸出節點會使用傳回到檔案接收之啟始物件的指標來建立，而您的應用程式會依資料流程號碼追蹤檔案接收中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="b1498-117">The output node of the topology is created by using the returned pointer to the activate object of the file sink and your application is keeping track of the streams in the file sink by stream numbers.</span></span>
    > [!Note]  
    > <span data-ttu-id="b1498-118">您可以藉由呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)來啟動 file 接收器。</span><span class="sxs-lookup"><span data-stu-id="b1498-118">You can activate the file sink by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="b1498-119">不過，您不需要啟用物件明確。</span><span class="sxs-lookup"><span data-stu-id="b1498-119">However you do not need to activate the object explictly.</span></span> <span data-ttu-id="b1498-120">媒體會話會追蹤啟用物件，並在編碼會話期間自動啟動檔案接收。</span><span class="sxs-lookup"><span data-stu-id="b1498-120">The Media Session keeps track of the activation object and activates the file sink automatically during the encoding session.</span></span>

     

-   <span data-ttu-id="b1498-121">資料流程資訊是在 ContentInfo 物件中設定。</span><span class="sxs-lookup"><span data-stu-id="b1498-121">The stream information is configured in the ContentInfo object.</span></span> <span data-ttu-id="b1498-122">Disucssed 下一個子區段。</span><span class="sxs-lookup"><span data-stu-id="b1498-122">Disucssed in the next sub-section.</span></span>

<span data-ttu-id="b1498-123">建立 ASF 檔案接收之後，必須先設定它，才能建立拓撲。</span><span class="sxs-lookup"><span data-stu-id="b1498-123">After creating the ASF file sink it must be configured before building the topology.</span></span> <span data-ttu-id="b1498-124">檔案接收必須知道下列資訊，才能產生輸出檔。</span><span class="sxs-lookup"><span data-stu-id="b1498-124">The file sink needs to know the following information in order to generate the output file.</span></span>

-   <span data-ttu-id="b1498-125">基本資料流程資訊</span><span class="sxs-lookup"><span data-stu-id="b1498-125">Basic stream information</span></span>
-   <span data-ttu-id="b1498-126">編碼模式資訊</span><span class="sxs-lookup"><span data-stu-id="b1498-126">Encoding mode information</span></span>
-   <span data-ttu-id="b1498-127">中繼資料</span><span class="sxs-lookup"><span data-stu-id="b1498-127">Metadata</span></span>

<span data-ttu-id="b1498-128">檔案接收會執行 [ASF ContentInfo 物件](asf-contentinfo-object.md) 並公開 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面，讓應用程式可以使用它來設定與資料流程及編碼相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="b1498-128">The file sink implements the [ASF ContentInfo Object](asf-contentinfo-object.md) and exposes the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface so that an application can use it to set information related to the streams and encoding.</span></span> <span data-ttu-id="b1498-129">根據您呼叫來建立檔案接收的函式而定，有兩種方式可以取得 **IMFASFContentInfo** 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="b1498-129">Depending on the function you called to create the file sink, there are two ways of getting a reference to the **IMFASFContentInfo** interface.</span></span>

-   <span data-ttu-id="b1498-130">如果您呼叫 [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)函數，應用程式必須在傳回的檔案接收上呼叫 **IMFMediaSink：： QueryInterface** ，以查詢 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)介面。</span><span class="sxs-lookup"><span data-stu-id="b1498-130">If you call the [**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink) function, the application must query for [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface by calling **IMFMediaSink::QueryInterface** on the returned file sink.</span></span>
-   <span data-ttu-id="b1498-131">如果您選擇呼叫 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)，此函式會預期您在呼叫之前已有完整設定的 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="b1498-131">If you choose to call [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate), this function expects that you have a fully-configured ContentInfo object prior to the call.</span></span> <span data-ttu-id="b1498-132">若要這樣做，您必須藉由呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 來建立空的 ContentInfo 物件，然後使用所有必要的資訊進行設定。</span><span class="sxs-lookup"><span data-stu-id="b1498-132">To do this, you need to create an empty ContentInfo object by calling [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) and then configure it with all the required information.</span></span> <span data-ttu-id="b1498-133">將設定的 ContentInfo 物件傳遞至 **MFCreateASFMediaSinkActivate** ，以接收接收啟始物件的指標。</span><span class="sxs-lookup"><span data-stu-id="b1498-133">Pass the configured ContentInfo object to the **MFCreateASFMediaSinkActivate** to receive a pointer to the sink activate object.</span></span> <span data-ttu-id="b1498-134">您無法使用傳回的啟用物件來啟動檔案接收，然後變更任何資料流程或編碼資訊。</span><span class="sxs-lookup"><span data-stu-id="b1498-134">You cannot activate the file sink by using the returned activation object and then change any stream or encoding information.</span></span>

<span data-ttu-id="b1498-135">如需有關設定接收資料流程和特定屬性的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="b1498-135">For information about configuring sink streams and specific properties, see the following topics:</span></span>

-   [<span data-ttu-id="b1498-136">將資料流程資訊新增至 ASF 檔案接收</span><span class="sxs-lookup"><span data-stu-id="b1498-136">Adding Stream Information to the ASF File Sink</span></span>](adding-stream-information-to-the-asf-file-sink.md)
-   [<span data-ttu-id="b1498-137">設定 File 接收中的屬性</span><span class="sxs-lookup"><span data-stu-id="b1498-137">Setting Properties in the File Sink</span></span>](setting-properties-in-the-file-sink.md)
-   [<span data-ttu-id="b1498-138">將中繼資料新增至 File 接收器</span><span class="sxs-lookup"><span data-stu-id="b1498-138">Adding Metadata to the File Sink</span></span>](adding-metadata-to-the-file-sink.md)

## <a name="related-topics"></a><span data-ttu-id="b1498-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="b1498-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1498-140">ASF 媒體接收</span><span class="sxs-lookup"><span data-stu-id="b1498-140">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="b1498-141">管線層 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="b1498-141">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="b1498-142">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="b1498-142">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



