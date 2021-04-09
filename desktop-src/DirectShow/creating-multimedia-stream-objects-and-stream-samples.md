---
description: 建立多媒體資料流程物件和資料流程範例
ms.assetid: 1aecdd39-f1b3-490b-b092-86d51439be02
title: 建立多媒體資料流程物件和資料流程範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cdc30129591bf1c67609ad6d15e8fd8286ae23
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945662"
---
# <a name="creating-multimedia-stream-objects-and-stream-samples"></a><span data-ttu-id="cad37-103">建立多媒體資料流程物件和資料流程範例</span><span class="sxs-lookup"><span data-stu-id="cad37-103">Creating Multimedia Stream Objects and Stream Samples</span></span>

> [!Note]  
> <span data-ttu-id="cad37-104">這些 Api 已被取代。</span><span class="sxs-lookup"><span data-stu-id="cad37-104">These APIs are deprecated.</span></span> <span data-ttu-id="cad37-105">應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。</span><span class="sxs-lookup"><span data-stu-id="cad37-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="cad37-106">支援 [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) 介面的物件是多媒體資料流程的基本容器。</span><span class="sxs-lookup"><span data-stu-id="cad37-106">Objects that support the [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) interface are the basic containers for multimedia data streams.</span></span> <span data-ttu-id="cad37-107">**IMultiMediaStream** 介面包含列舉物件之資料流程的方法;這些資料流程通常是影片和音訊資料，但可包含任何格式的資料，例如隱藏式字幕、純文字或 SMPTE 時間碼。</span><span class="sxs-lookup"><span data-stu-id="cad37-107">The **IMultiMediaStream** interface includes methods that enumerate the object's data streams; these streams are typically video and audio data, but can include data of any format, such as closed-captioning, plain text, or SMPTE timecode.</span></span> <span data-ttu-id="cad37-108">但是， **IMultiMediaStream** 介面是泛型容器，開發人員可以建立其他版本的介面，以支援特定的資料格式。</span><span class="sxs-lookup"><span data-stu-id="cad37-108">The **IMultiMediaStream** interface is a generic container, however; developers can create other versions of the interface that support specific data formats.</span></span> <span data-ttu-id="cad37-109">例如，執行 [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) 介面的物件可以列舉及控制任何 DirectShow 資料格式的資料流程。</span><span class="sxs-lookup"><span data-stu-id="cad37-109">Objects that implement the [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) interface, for example, can enumerate and control streams of any DirectShow data format.</span></span> <span data-ttu-id="cad37-110">由於個別資料流程的格式是特定的，因此，它們至少支援兩個不同的介面：一個泛型和一個資料特有的。</span><span class="sxs-lookup"><span data-stu-id="cad37-110">Because individual data streams are format specific, they support at least two different interfaces: one generic and one data-specific.</span></span> <span data-ttu-id="cad37-111">每個資料流程都支援 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) 介面，這會提供方法來取出其格式以及資料流程本身的指標。</span><span class="sxs-lookup"><span data-stu-id="cad37-111">Every stream supports the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface, which provides methods to retrieve its format and a pointer to the stream itself.</span></span> <span data-ttu-id="cad37-112">相反地， [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) 介面具有處理轉譯影片資料的方法。</span><span class="sxs-lookup"><span data-stu-id="cad37-112">The [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) interface, on the other hand, has methods that deal specifically with rendering video data.</span></span> <span data-ttu-id="cad37-113">任何衍生自 **IMultiMediaStream** 的介面也支援建立資料流程範例，也就是串流資料的基本單位。</span><span class="sxs-lookup"><span data-stu-id="cad37-113">Any interface derived from **IMultiMediaStream** also supports the creation of stream samples, the basic units of streaming data.</span></span>

<span data-ttu-id="cad37-114">多媒體範例是包含媒體資料之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="cad37-114">A multimedia sample is a reference to an object containing the media data.</span></span> <span data-ttu-id="cad37-115">若為影片影像，這是 DirectDraw 表面。</span><span class="sxs-lookup"><span data-stu-id="cad37-115">For a video image, this is a DirectDraw surface.</span></span> <span data-ttu-id="cad37-116">根據媒體類型 (音效、文字等等) ，範例的確切內容會有所不同。</span><span class="sxs-lookup"><span data-stu-id="cad37-116">The sample's exact content varies, depending on the type of media (sound, text, and so on).</span></span> <span data-ttu-id="cad37-117">因為範例只是資料物件的參考，所以任何數目的資料流程範例都可以參考相同的物件。</span><span class="sxs-lookup"><span data-stu-id="cad37-117">Because a sample is only a reference to the data object, any number of stream samples can refer to the same object.</span></span> <span data-ttu-id="cad37-118">[**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)介面會提供方法來取得和設定範例的特性，例如其開始和停止時間、狀態和資料流程關聯。</span><span class="sxs-lookup"><span data-stu-id="cad37-118">The [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) interface provides methods that get and set a sample's characteristics, such as its start and stop time, status, and stream association.</span></span> <span data-ttu-id="cad37-119">[**IStreamSample：： Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update)方法會在可讀取資料流程的情況下重新整理範例的資料。</span><span class="sxs-lookup"><span data-stu-id="cad37-119">The [**IStreamSample::Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) method refreshes the sample's data in the case of readable streams.</span></span> <span data-ttu-id="cad37-120">針對可寫入資料流程，它會將範例的資料寫入至資料流程。</span><span class="sxs-lookup"><span data-stu-id="cad37-120">For writable streams, it will write the sample's data to the stream.</span></span> <span data-ttu-id="cad37-121">一般而言，您會在呈現、傳輸或儲存串流資料的迴圈中使用 **Update** 方法。</span><span class="sxs-lookup"><span data-stu-id="cad37-121">Typically, you use the **Update** method in a loop that renders, transfers, or stores streaming data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cad37-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="cad37-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cad37-123">關於多媒體串流架構</span><span class="sxs-lookup"><span data-stu-id="cad37-123">About the Multimedia Streaming Architecture</span></span>](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



