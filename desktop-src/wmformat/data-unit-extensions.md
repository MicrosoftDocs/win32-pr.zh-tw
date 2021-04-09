---
title: 資料單位延伸模組
description: 資料單位延伸模組
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media Format SDK，資料單位延伸模組
- Advanced Systems Format (ASF) 、資料單位延伸模組
- ASF (Advanced Systems Format) 、資料單位延伸模組
- Windows Media Format SDK，承載延伸系統
- Advanced Systems Format (ASF) 、承載延伸系統
- ASF (Advanced Systems Format) ，承載延伸系統
- 資料單位延伸，關於
- 承載單位延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681408"
---
# <a name="data-unit-extensions"></a><span data-ttu-id="0c4bc-111">資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="0c4bc-111">Data Unit Extensions</span></span>

<span data-ttu-id="0c4bc-112">Windows Media Format SDK 可讓您使用 *資料單位延伸* 模組（也稱為承載延伸系統）來補充範例中的資料。</span><span class="sxs-lookup"><span data-stu-id="0c4bc-112">The Windows Media Format SDK enables you to supplement data in samples with *data unit extensions*, also called payload extension systems.</span></span> <span data-ttu-id="0c4bc-113">本檔使用「資料單位延伸模組」一詞，以便與 [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)等方法名稱保持一致。</span><span class="sxs-lookup"><span data-stu-id="0c4bc-113">This documentation uses the term "data unit extensions" in order to remain consistent with method names such as [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span> <span data-ttu-id="0c4bc-114">資料單位延伸是在檔案的資料區段中附加至範例的名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="0c4bc-114">A data unit extension is a name/value pair that is attached to the sample in the data section of the file.</span></span> <span data-ttu-id="0c4bc-115">當讀取器抓取範例時，您可以使用緩衝區物件的方法來存取擴充的資料。</span><span class="sxs-lookup"><span data-stu-id="0c4bc-115">You can access the extended data using methods of the buffer object when the sample is retrieved by the reader.</span></span>

<span data-ttu-id="0c4bc-116">您可以根據自己的規格建立資料單位延伸模組，但此 SDK 的物件會預先定義並支援數種類型。</span><span class="sxs-lookup"><span data-stu-id="0c4bc-116">You can create data unit extensions to your own specifications, but several types are predefined and supported by the objects of this SDK.</span></span> <span data-ttu-id="0c4bc-117">這些標準延伸模組是用來為腳本和 Web 資料流程中的檔案名提供額外的資料 () 、SMPTE 時間代碼資料、非正方形圖元外觀比例、持續時間和交錯類型。</span><span class="sxs-lookup"><span data-stu-id="0c4bc-117">These standard extensions are used to provide additional data for file names (in script and Web streams), SMPTE time code data, non-square pixel aspect ratio, duration, and type of interlacing.</span></span>

<span data-ttu-id="0c4bc-118">若要使用資料單位延伸模組，您必須將資料流程設定為接受它們，然後將延伸加入至該資料流程的每個範例。</span><span class="sxs-lookup"><span data-stu-id="0c4bc-118">To use data unit extensions, you must configure the stream to accept them, and then add extensions to each sample for that stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c4bc-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c4bc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c4bc-120">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="0c4bc-120">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="0c4bc-121">**設定資料單位延伸模組**</span><span class="sxs-lookup"><span data-stu-id="0c4bc-121">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="0c4bc-122">**設定資料單位延伸模組**</span><span class="sxs-lookup"><span data-stu-id="0c4bc-122">**Setting Data Unit Extensions**</span></span>](setting-data-unit-extensions.md)
</dt> </dl>

 

 




