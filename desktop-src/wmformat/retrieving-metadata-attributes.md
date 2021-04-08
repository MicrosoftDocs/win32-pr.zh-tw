---
title: 正在抓取中繼資料屬性
description: 正在抓取中繼資料屬性
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media Format SDK，正在抓取中繼資料屬性
- Advanced Systems Format (ASF) ，正在抓取中繼資料屬性
- ASF (Advanced Systems Format) ，正在抓取中繼資料屬性
- 中繼資料，正在抓取屬性
- 資料流程，正在抓取中繼資料屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023006"
---
# <a name="retrieving-metadata-attributes"></a><span data-ttu-id="a9df5-108">正在抓取中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="a9df5-108">Retrieving Metadata Attributes</span></span>

<span data-ttu-id="a9df5-109">若要從檔案標頭取出屬性，您必須知道屬性的資料流程號碼和索引。</span><span class="sxs-lookup"><span data-stu-id="a9df5-109">To retrieve an attribute from a file header, you must know the stream number and index of the attribute.</span></span> <span data-ttu-id="a9df5-110">您可以使用 [**IWMHeaderInfo3：： GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) 方法，以相同的語言取得具有相同名稱或所有索引的所有屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="a9df5-110">You can use the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method to get the indexes for all attributes with the same name or all indexes in the same language.</span></span> <span data-ttu-id="a9df5-111">如同 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)的其他方法， **GetAttributeIndices** 會處理單一資料流程，或使用資料流程0來處理所有檔案層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9df5-111">Like the other methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** deals with a single stream, or with all file-level attributes using stream 0.</span></span> <span data-ttu-id="a9df5-112">您可以針對串流號碼使用0xFFFF，以取得符合整個檔案中的準則的全域索引（不論串流號碼為何）。</span><span class="sxs-lookup"><span data-stu-id="a9df5-112">You can use 0xFFFF for the stream number to get global indexes matching your criteria throughout the entire file, regardless of stream number.</span></span>

<span data-ttu-id="a9df5-113">當您知道您想要取得之屬性的索引時，請呼叫 [**IWMHeaderInfo3：： GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) 來取得屬性。</span><span class="sxs-lookup"><span data-stu-id="a9df5-113">When you know the index of the attribute you want to retrieve, call [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) to get the attribute.</span></span> <span data-ttu-id="a9df5-114">您必須對每個抓取的屬性進行兩個 **GetAttributeByIndexEx** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a9df5-114">You need to make two calls to **GetAttributeByIndexEx** for each attribute retrieved.</span></span> <span data-ttu-id="a9df5-115">在第一次呼叫時，傳遞 **Null** 作為名稱和資料緩衝區指標，以取得所需的大小。</span><span class="sxs-lookup"><span data-stu-id="a9df5-115">On the first call, pass **NULL** for the name and data buffer pointers to get the size needed.</span></span> <span data-ttu-id="a9df5-116">然後，配置所指定大小的緩衝區，並進行第二次呼叫以取得名稱和資料。</span><span class="sxs-lookup"><span data-stu-id="a9df5-116">Then allocate buffers of the size indicated and make the second call to retrieve the name and data.</span></span>

<span data-ttu-id="a9df5-117">如需示範如何取得中繼資料屬性的範例程式碼，請參閱 [取得檔案中的所有中繼資料](to-retrieve-all-metadata-in-a-file.md)。</span><span class="sxs-lookup"><span data-stu-id="a9df5-117">For example code showing how to retrieve metadata attributes, see [To Retrieve All Metadata in a File](to-retrieve-all-metadata-in-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9df5-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9df5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9df5-119">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="a9df5-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




