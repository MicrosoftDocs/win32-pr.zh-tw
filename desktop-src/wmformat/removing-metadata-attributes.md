---
title: 移除中繼資料屬性
description: 移除中繼資料屬性
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media Format SDK，移除中繼資料屬性
- Advanced Systems Format (ASF) ，移除中繼資料屬性
- ASF (Advanced Systems Format) ，移除中繼資料屬性
- 中繼資料，移除屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374789"
---
# <a name="removing-metadata-attributes"></a><span data-ttu-id="933d3-107">移除中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="933d3-107">Removing Metadata Attributes</span></span>

<span data-ttu-id="933d3-108">您可以藉由將索引和資料流程號碼傳遞至 [**IWMHeaderInfo3：:D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) 方法，來移除中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="933d3-108">You can remove a metadata attribute by passing its index and stream number to the [**IWMHeaderInfo3::DeleteAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) method.</span></span> <span data-ttu-id="933d3-109">移除屬性之後索引剩餘屬性的順序不會變更;原先索引值大於已移除的所有剩餘屬性，其索引值會減少一。</span><span class="sxs-lookup"><span data-stu-id="933d3-109">The order in which the remaining attributes are indexed after removing an attribute does not change; all remaining attributes that originally had an index value greater than the one removed have their index values reduced by one.</span></span> <span data-ttu-id="933d3-110">移除多個屬性時，請依索引的遞減順序來進行，以避免在編制索引時計算調整。</span><span class="sxs-lookup"><span data-stu-id="933d3-110">When removing multiple attributes, do so in descending order by index to avoid having to calculate the adjustment in indexing.</span></span>

<span data-ttu-id="933d3-111">為了方便移除值， [**IWMHeaderInfo3：： GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) 方法會以遞減順序傳回索引值。</span><span class="sxs-lookup"><span data-stu-id="933d3-111">For convenience in removing values, the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method returns the index values in descending order.</span></span>

> [!Note]  
> <span data-ttu-id="933d3-112">使用 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 方法取得的索引值與使用 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)方法取得的索引值不相容。</span><span class="sxs-lookup"><span data-stu-id="933d3-112">Index values obtained by using the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) are not compatible with index values obtained by using the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span> <span data-ttu-id="933d3-113">如果您使用某個介面的方法來變更檔案中的屬性，您應該假設先前從其他介面取出的任何索引值都不再有效，而且必須再次取得。</span><span class="sxs-lookup"><span data-stu-id="933d3-113">If you use the methods of one interface to change attributes in a file, you should assume that any index values previously retrieved from the other interface are no longer valid and must be obtained again.</span></span> <span data-ttu-id="933d3-114">如果可能的話，您應該避免使用 **IWMHeaderInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="933d3-114">You should avoid using the methods of **IWMHeaderInfo** if possible.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="933d3-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="933d3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="933d3-116">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="933d3-116">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




