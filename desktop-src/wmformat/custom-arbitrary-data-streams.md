---
title: 自訂任意資料流程
description: 自訂任意資料流程
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media Format SDK，自訂任意資料流程
- Advanced Systems Format (ASF) 、自訂任意資料流程
- ASF (Advanced Systems Format) ，自訂任意資料流程
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 自訂任意資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968258"
---
# <a name="custom-arbitrary-data-streams"></a><span data-ttu-id="06c5c-110">自訂任意資料流程</span><span class="sxs-lookup"><span data-stu-id="06c5c-110">Custom Arbitrary Data Streams</span></span>

<span data-ttu-id="06c5c-111">您可以在 ASF 檔案中建立資料流程，以包含任何資料類型。</span><span class="sxs-lookup"><span data-stu-id="06c5c-111">You can create a stream in an ASF file to contain any sort of data.</span></span> <span data-ttu-id="06c5c-112">如果任何支援的資料流程類型都不符合您的需求，您必須使用任意資料流程。</span><span class="sxs-lookup"><span data-stu-id="06c5c-112">If none of the supported stream types suits your needs, you must use an arbitrary data stream.</span></span> <span data-ttu-id="06c5c-113">寫入器物件會處理任意資料流程，就像處理任何未壓縮的資料流程一樣;這些範例會從檔案的資料區段中的其他資料流程 packetized 和結合範例。</span><span class="sxs-lookup"><span data-stu-id="06c5c-113">The writer object handles an arbitrary data stream just as it does any uncompressed stream; the samples are packetized and combined with the samples from other streams in the data section of the file.</span></span> <span data-ttu-id="06c5c-114">當然，只有經過特別設計來處理任意類型的讀取應用程式，才能在讀取物件傳遞之後處理資料。</span><span class="sxs-lookup"><span data-stu-id="06c5c-114">Of course, only a reading application that has been specifically programmed to deal with your arbitrary type will be able to handle the data after it is delivered by the reading object.</span></span>

<span data-ttu-id="06c5c-115">任意資料流程的常見用法之一，是針對使用協力廠商編解碼器編碼的媒體資料。</span><span class="sxs-lookup"><span data-stu-id="06c5c-115">One common use of arbitrary data streams is for media data encoded by using a third-party codec.</span></span> <span data-ttu-id="06c5c-116">因為此 SDK 的物件不會直接與協力廠商編解碼器互動，所以您的撰寫應用程式必須使用編解碼器的編碼部分來處理範例，並將壓縮的範例傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="06c5c-116">Because the objects of this SDK do not interact directly with third-party codecs, your writing application must process the samples with the encoding portion of the codec and pass the compressed samples to the writer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06c5c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="06c5c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06c5c-118">**任意資料流程**</span><span class="sxs-lookup"><span data-stu-id="06c5c-118">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="06c5c-119">**設定自訂任意資料流程**</span><span class="sxs-lookup"><span data-stu-id="06c5c-119">**Configuring Custom Arbitrary Streams**</span></span>](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




