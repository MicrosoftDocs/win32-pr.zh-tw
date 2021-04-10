---
description: ASF 多工器
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: ASF 多工器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026059"
---
# <a name="asf-multiplexer"></a><span data-ttu-id="f2e6d-103">ASF 多工器</span><span class="sxs-lookup"><span data-stu-id="f2e6d-103">ASF Multiplexer</span></span>

<span data-ttu-id="f2e6d-104">ASF 多工器是 *一種 WMContainer* 層物件，可與 [asf 資料物件](asf-file-structure.md) 搭配使用，並讓應用程式能夠產生 asf 容器的資料封包。</span><span class="sxs-lookup"><span data-stu-id="f2e6d-104">The ASF *multiplexer* is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate data packets for an ASF container.</span></span> <span data-ttu-id="f2e6d-105">多工器接受媒體 [範例](media-samples.md) 形式的媒體資料，並根據 [Asf 標頭物件](asf-file-structure.md)中所定義的串流和 asf 封包參數輸出媒體範例。</span><span class="sxs-lookup"><span data-stu-id="f2e6d-105">The multiplexer accepts media data in the form of [Media Samples](media-samples.md) and outputs media samples based on streaming and ASF packet parameters defined in the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="f2e6d-106">輸出媒體範例會保存包含 packetized 數位媒體資料的一或多個媒體緩衝區的參考。您可以在檔案編碼案例中使用這個物件，它會從編碼器接收編碼的資料流程範例，或使用 ASF ASF 轉碼 (remuxing) 。</span><span class="sxs-lookup"><span data-stu-id="f2e6d-106">The output media samples hold references to one or more media buffers that contain packetized digital media data.You can use this object in a file encoding scenario where it receives encoded stream samples from the encoder or for ASF-ASF transcoding (remuxing).</span></span>

<span data-ttu-id="f2e6d-107">下圖說明使用多工器的 asf 檔案產生的 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="f2e6d-107">The following diagram illustrates ASF data packet generation for an ASF file using the multiplexer.</span></span>

![顯示 asf 資料封包產生的圖表](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

<span data-ttu-id="f2e6d-109">如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="f2e6d-109">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="f2e6d-110">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="f2e6d-110">This section contains the following topics:</span></span>



| <span data-ttu-id="f2e6d-111">主題</span><span class="sxs-lookup"><span data-stu-id="f2e6d-111">Topic</span></span>                                                                  | <span data-ttu-id="f2e6d-112">描述</span><span class="sxs-lookup"><span data-stu-id="f2e6d-112">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="f2e6d-113">建立多工器物件</span><span class="sxs-lookup"><span data-stu-id="f2e6d-113">Creating the Multiplexer Object</span></span>](creating-the-multiplexer-object.md) | <span data-ttu-id="f2e6d-114">如何建立及初始化多工器。</span><span class="sxs-lookup"><span data-stu-id="f2e6d-114">How to create and initialize the multiplexer.</span></span>                     |
| [<span data-ttu-id="f2e6d-115">產生新的 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="f2e6d-115">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md) | <span data-ttu-id="f2e6d-116">如何產生資料封包，以構成新的 ASF 資料物件。</span><span class="sxs-lookup"><span data-stu-id="f2e6d-116">How to generate data packets to constitute a new ASF Data Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f2e6d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2e6d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2e6d-118">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="f2e6d-118">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="f2e6d-119">教學課程：將 ASF 資料流程從一個檔案複製到另一個檔案</span><span class="sxs-lookup"><span data-stu-id="f2e6d-119">Tutorial: Copying ASF Streams from One File to Another</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="f2e6d-120">教學課程：使用 CBR 編碼方式撰寫 WMA 檔案</span><span class="sxs-lookup"><span data-stu-id="f2e6d-120">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



