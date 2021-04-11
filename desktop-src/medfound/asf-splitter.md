---
description: ASF 分隔器
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: ASF 分隔器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111888"
---
# <a name="asf-splitter"></a><span data-ttu-id="1ec66-103">ASF 分隔器</span><span class="sxs-lookup"><span data-stu-id="1ec66-103">ASF Splitter</span></span>

<span data-ttu-id="1ec66-104">ASF *分隔器* 物件是 WMContainer 層元件，可剖析 Advanced Systems 格式的 Asf 資料物件 (asf) 檔。</span><span class="sxs-lookup"><span data-stu-id="1ec66-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="1ec66-105">您可以使用分隔器來讀取資料物件中的資料封包，並產生資料流程範例。</span><span class="sxs-lookup"><span data-stu-id="1ec66-105">You can use the splitter to read the data packets in the Data Object and generate stream samples.</span></span> <span data-ttu-id="1ec66-106">如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="1ec66-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="1ec66-107">分隔器會公開 [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) 介面。</span><span class="sxs-lookup"><span data-stu-id="1ec66-107">The splitter exposes the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span> <span data-ttu-id="1ec66-108">分割器會針對選取的資料流程剖析 ASF 資料封包，並將其重新封裝為公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的個別範例物件。</span><span class="sxs-lookup"><span data-stu-id="1ec66-108">The splitter parses ASF data packets for the selected streams and repackages them into individual sample objects that expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="1ec66-109">分隔器是媒體基礎的平台層級元件之一。</span><span class="sxs-lookup"><span data-stu-id="1ec66-109">The splitter is one of the platform-level components of Media Foundation.</span></span> <span data-ttu-id="1ec66-110">ASF 媒體來源會在內部使用分隔器來剖析 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="1ec66-110">The ASF media source uses the splitter internally to parse ASF files.</span></span>

<span data-ttu-id="1ec66-111">下圖說明如何透過分隔器產生 ASF 檔案的範例。</span><span class="sxs-lookup"><span data-stu-id="1ec66-111">The following diagram illustrates sample generation for an ASF file through the splitter.</span></span>

![顯示 asf 檔案產生範例的圖表](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

<span data-ttu-id="1ec66-113">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="1ec66-113">This section contains the following topics:</span></span>



| <span data-ttu-id="1ec66-114">主題</span><span class="sxs-lookup"><span data-stu-id="1ec66-114">Topic</span></span>                                                                                                                        | <span data-ttu-id="1ec66-115">描述</span><span class="sxs-lookup"><span data-stu-id="1ec66-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="1ec66-116">建立 ASF 分隔器物件</span><span class="sxs-lookup"><span data-stu-id="1ec66-116">Creating the ASF Splitter Object</span></span>](creating-the-asf-splitter-object.md)                                                     | <span data-ttu-id="1ec66-117">如何建立及初始化分隔器。</span><span class="sxs-lookup"><span data-stu-id="1ec66-117">How to create and initialize the splitter.</span></span>                              |
| [<span data-ttu-id="1ec66-118">設定 ASF 分隔器物件</span><span class="sxs-lookup"><span data-stu-id="1ec66-118">Configuring the ASF Splitter Object</span></span>](configuring-the-asf-splitter-object.md)                                               | <span data-ttu-id="1ec66-119">分隔器的設定。</span><span class="sxs-lookup"><span data-stu-id="1ec66-119">Configuration settings for the splitter.</span></span>                                |
| [<span data-ttu-id="1ec66-120">從現有的 ASF 資料物件產生資料流程範例</span><span class="sxs-lookup"><span data-stu-id="1ec66-120">Generating Stream Samples from an Existing ASF Data Object</span></span>](generating-stream-samples-from-an-existing-asf-data-object.md) | <span data-ttu-id="1ec66-121">如何剖析 ASF 資料物件並產生 packetized 流範例。</span><span class="sxs-lookup"><span data-stu-id="1ec66-121">How to parse the ASF Data Object and generate packetized steam samples.</span></span> |



 

<span data-ttu-id="1ec66-122">下表顯示相關的資料物件屬性。</span><span class="sxs-lookup"><span data-stu-id="1ec66-122">The following table shows the relevant Data Object attributes.</span></span>



| <span data-ttu-id="1ec66-123">屬性</span><span class="sxs-lookup"><span data-stu-id="1ec66-123">Attribute</span></span>                                                                                                    | <span data-ttu-id="1ec66-124">描述</span><span class="sxs-lookup"><span data-stu-id="1ec66-124">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ec66-125">**MF \_ PD \_ ASF \_ FILEPROPERTIES 封 \_ 包**</span><span class="sxs-lookup"><span data-stu-id="1ec66-125">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)                   | <span data-ttu-id="1ec66-126">ASF 資料物件中的資料封包數目。</span><span class="sxs-lookup"><span data-stu-id="1ec66-126">Number of data packets in the ASF Data Object.</span></span>                                                       |
| [<span data-ttu-id="1ec66-127">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最小封 \_ 包 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="1ec66-127">**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | <span data-ttu-id="1ec66-128">檔案中的資料封包大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1ec66-128">Minimum size of the data packets in the file, in bytes.</span></span>                                              |
| [<span data-ttu-id="1ec66-129">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 封 \_ 包 \_ 大小上限**</span><span class="sxs-lookup"><span data-stu-id="1ec66-129">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | <span data-ttu-id="1ec66-130">檔案中資料封包的大小上限（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="1ec66-130">Maximum size of the data packets in the file, in bytes</span></span>                                               |
| [<span data-ttu-id="1ec66-131">**MF \_ PD \_ ASF \_ 資料 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="1ec66-131">**MF\_PD\_ASF\_DATA\_LENGTH**</span></span>](mf-pd-asf-data-length-attribute.md)                                         | <span data-ttu-id="1ec66-132">ASF 資料物件的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1ec66-132">Size of the ASF Data Object, in bytes.</span></span>                                                               |
| [<span data-ttu-id="1ec66-133">**MF \_ PD \_ ASF \_ 資料 \_ 起始 \_ 位移**</span><span class="sxs-lookup"><span data-stu-id="1ec66-133">**MF\_PD\_ASF\_DATA\_START\_OFFSET**</span></span>](mf-pd-asf-data-start-offset-attribute.md)                            | <span data-ttu-id="1ec66-134">相對於檔案開頭之 ASF 資料物件中第一個資料封包的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1ec66-134">Offset, in bytes, to the first data packet in the ASF Data Object relative to the start of the file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1ec66-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ec66-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ec66-136">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="1ec66-136">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="1ec66-137">教學課程：讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="1ec66-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="1ec66-138">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="1ec66-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



