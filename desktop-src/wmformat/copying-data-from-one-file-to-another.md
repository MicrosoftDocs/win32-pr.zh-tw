---
title: 將資料從一個檔案複製到另一個檔案
description: 將資料從一個檔案複製到另一個檔案
ms.assetid: 1403c396-46ea-48b1-a535-922ffca31bc2
keywords:
- Windows Media Format SDK，複製資料
- Advanced Systems Format (ASF) ，複製資料
- ASF (Advanced Systems Format) ，複製資料
- 資料流程，複製資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b38a1675ac79630371fe4d3fda66d44b4b2990
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932507"
---
# <a name="copying-data-from-one-file-to-another"></a><span data-ttu-id="17862-107">將資料從一個檔案複製到另一個檔案</span><span class="sxs-lookup"><span data-stu-id="17862-107">Copying Data from One File to Another</span></span>

<span data-ttu-id="17862-108">在最基本的層級上，將資料流程從一個 ASF 檔案複製到另一個 ASF 檔案相當簡單。</span><span class="sxs-lookup"><span data-stu-id="17862-108">At the most basic level, copying a stream from one ASF file to another is fairly straightforward.</span></span> <span data-ttu-id="17862-109">不過，在處理來自多個輸入檔的資料流程或複製您先解壓縮並重新編碼的資料流程時，需要考慮一些問題。</span><span class="sxs-lookup"><span data-stu-id="17862-109">However, there are issues to consider when working with streams from multiple input files or when copying streams that you first decompress and re-encode.</span></span>

<span data-ttu-id="17862-110">下列各節說明複製資料流程。</span><span class="sxs-lookup"><span data-stu-id="17862-110">The following sections describe copying streams.</span></span>



| <span data-ttu-id="17862-111">區段</span><span class="sxs-lookup"><span data-stu-id="17862-111">Section</span></span>                                                                                              | <span data-ttu-id="17862-112">Descripiton</span><span class="sxs-lookup"><span data-stu-id="17862-112">Descripiton</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17862-113">複製資料流程而不解壓縮資料</span><span class="sxs-lookup"><span data-stu-id="17862-113">Copying Streams Without Decompressing the Data</span></span>](copying-streams-without-decompressing-the-data.md) | <span data-ttu-id="17862-114">描述如何使用壓縮的範例複製資料流程，以保留內容的品質。</span><span class="sxs-lookup"><span data-stu-id="17862-114">Describes how to copy streams using compressed samples to preserve the quality of the content.</span></span> |
| [<span data-ttu-id="17862-115">使用解壓縮的範例複製資料流程</span><span class="sxs-lookup"><span data-stu-id="17862-115">Copying Streams Using Decompressed Samples</span></span>](copying-streams-using-decompressed-samples.md)         | <span data-ttu-id="17862-116">描述使用解壓縮的範例複製資料流程時的困難之處。</span><span class="sxs-lookup"><span data-stu-id="17862-116">Describes the difficulties in copying streams using decompressed samples.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="17862-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="17862-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17862-118">**設定檔管理員物件**</span><span class="sxs-lookup"><span data-stu-id="17862-118">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="17862-119">**串流設定物件**</span><span class="sxs-lookup"><span data-stu-id="17862-119">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="17862-120">**同步讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="17862-120">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="17862-121">**寫入器物件**</span><span class="sxs-lookup"><span data-stu-id="17862-121">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




