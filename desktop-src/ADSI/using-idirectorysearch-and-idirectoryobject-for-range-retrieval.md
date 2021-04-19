---
title: 使用 >idirectorysearch 和 IDirectoryObject 進行範圍抓取
description: IDirectoryObject 或 >idirectorysearch 介面可以用來取得屬性值的範圍。 若要這樣做，請為查詢中要求的其中一個屬性指定屬性和範圍。
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- '>idirectorysearch ADSI，用來取得群組成員的範圍'
- IDirectoryObject ADSI，用來取得群組成員的範圍
- 使用 >idirectorysearch 和 IDirectoryObject 的範圍抓取 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966777"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a><span data-ttu-id="bddd3-107">使用 >idirectorysearch 和 IDirectoryObject 進行範圍抓取</span><span class="sxs-lookup"><span data-stu-id="bddd3-107">Using IDirectorySearch and IDirectoryObject for Range Retrieval</span></span>

<span data-ttu-id="bddd3-108">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)或 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面可以用來取得屬性值的範圍。</span><span class="sxs-lookup"><span data-stu-id="bddd3-108">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) or [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="bddd3-109">若要這樣做，請為查詢中要求的其中一個屬性指定屬性和範圍。</span><span class="sxs-lookup"><span data-stu-id="bddd3-109">To do this, specify the attribute and range for one of the attributes requested in the query.</span></span>

## <a name="range-retrieval-with-idirectoryobject"></a><span data-ttu-id="bddd3-110">使用 IDirectoryObject 的範圍抓取</span><span class="sxs-lookup"><span data-stu-id="bddd3-110">Range Retrieval with IDirectoryObject</span></span>

<span data-ttu-id="bddd3-111">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)介面可用於範圍抓取，方法是在呼叫 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes)方法時，指定屬性和 *pAttributesName* 陣列中其中一個屬性的範圍。</span><span class="sxs-lookup"><span data-stu-id="bddd3-111">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface can be used for range retrieval by specifying the attribute and range for one of the attributes in the *pAttributesName* array when calling the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



<span data-ttu-id="bddd3-112">如需詳細資訊和示範如何使用 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面進行範圍抓取的程式碼範例，請參閱 [使用 IDirectoryObject 範圍的範例程式碼](example-code-for-ranging-with-idirectoryobject.md)。</span><span class="sxs-lookup"><span data-stu-id="bddd3-112">For more information and a code example that shows how to use the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for range retrieval, see [Example Code for Ranging with IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).</span></span>

## <a name="range-retrieval-with-idirectorysearch"></a><span data-ttu-id="bddd3-113">使用 >idirectorysearch 的範圍抓取</span><span class="sxs-lookup"><span data-stu-id="bddd3-113">Range Retrieval with IDirectorySearch</span></span>

<span data-ttu-id="bddd3-114">[**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面可用於範圍抓取，方法是在呼叫 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)方法時，指定屬性和 *pAttributesName* 陣列中其中一個已抓取屬性的範圍。</span><span class="sxs-lookup"><span data-stu-id="bddd3-114">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface can be used for range retrieval by specifying the attribute and range for one of the retrieved attributes in the *pAttributesName* array when calling the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method.</span></span>


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



<span data-ttu-id="bddd3-115">使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面進行範圍抓取時，有一個問題必須特別解決。</span><span class="sxs-lookup"><span data-stu-id="bddd3-115">When using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="bddd3-116">當要求的範圍超過剩余值的數目時， [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 會傳回 **\_ \_ \_ 未 \_ 設定的 E ADS 資料行**。</span><span class="sxs-lookup"><span data-stu-id="bddd3-116">When the range requested exceeds the number of remaining values, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="bddd3-117">若要取得剩餘的值，必須使用範圍萬用字元 ' \* '。</span><span class="sxs-lookup"><span data-stu-id="bddd3-117">To retrieve the remaining values, it is necessary to use the range wildcard '\*'.</span></span> <span data-ttu-id="bddd3-118">例如，如果群組包含150成員，則可以使用範圍抓取來正常地取出成員值0-100。</span><span class="sxs-lookup"><span data-stu-id="bddd3-118">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="bddd3-119">如果接著要求範圍101-200， **>idirectorysearch：： GetColumn** 會傳回 **\_ \_ \_ 未 \_ 設定的 E ADS 資料行**。</span><span class="sxs-lookup"><span data-stu-id="bddd3-119">If range 101-200 is then requested, **IDirectorySearch::GetColumn** will return **E\_ADS\_COLUMN\_NOT\_SET**.</span></span> <span data-ttu-id="bddd3-120">使用 [**>idirectorysearch：： GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) 方法可以避免這個問題。</span><span class="sxs-lookup"><span data-stu-id="bddd3-120">This problem can be avoided by using the [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) method.</span></span> <span data-ttu-id="bddd3-121">一般來說， **GetNextColumnName** 會傳回原始查詢字串。</span><span class="sxs-lookup"><span data-stu-id="bddd3-121">Normally, **GetNextColumnName** will return the original query string.</span></span> <span data-ttu-id="bddd3-122">不過，當要求的範圍超過剩余值的數目時， **GetNextColumnName** 會以範圍萬用字元 ' ' 取代高範圍的值，以傳回已修改的查詢字串版本 \* 。</span><span class="sxs-lookup"><span data-stu-id="bddd3-122">However, when the range requested exceeds the number of remaining values, **GetNextColumnName** will return a modified version of the query string by replacing the high range value with the range wildcard '\*'.</span></span> <span data-ttu-id="bddd3-123">在上述範例中，第一個查詢會使用 "member; range = 0-100" 的屬性字串來執行，且 **GetNextColumnName** 會傳回 "member; range = 0-100"。</span><span class="sxs-lookup"><span data-stu-id="bddd3-123">In the example above, the first query would be performed with an attribute string of "member;range=0-100" and **GetNextColumnName** will return "member;range=0-100".</span></span> <span data-ttu-id="bddd3-124">在第二個查詢中，屬性字串會是 "member; range = 101-200"，但 **GetNextColumnName** 會傳回 "member; range = 101- \* "。</span><span class="sxs-lookup"><span data-stu-id="bddd3-124">In the second query, the attribute string would be "member;range=101-200", but **GetNextColumnName** will return "member;range=101-\*".</span></span> <span data-ttu-id="bddd3-125">您可以藉由比較原始屬性字串與 **GetNextColumnName** 的結果來判斷這種情況。</span><span class="sxs-lookup"><span data-stu-id="bddd3-125">This case can be determined by comparing the original attribute string to the result of **GetNextColumnName**.</span></span> <span data-ttu-id="bddd3-126">如果字串不同，則應該使用範圍萬用字元再次要求最後一個值區塊。</span><span class="sxs-lookup"><span data-stu-id="bddd3-126">If the strings are different, the last block of values should be requested again with the range wildcard.</span></span>

<span data-ttu-id="bddd3-127">如需詳細資訊和示範如何使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面進行範圍抓取的程式碼範例，請參閱 [使用 >idirectorysearch 範圍的範例程式碼](example-code-for-ranging-with-idirectorysearch.md)。</span><span class="sxs-lookup"><span data-stu-id="bddd3-127">For more information and a code example that shows how to use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for range retrieval, see [Example Code for Ranging with IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).</span></span>

 

 




