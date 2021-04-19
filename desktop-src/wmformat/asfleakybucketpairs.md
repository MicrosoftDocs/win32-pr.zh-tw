---
title: ASFLeakyBucketPairs
description: ASFLeakyBucketPairs 屬性是選擇性屬性，可描述變數位元速率檔案的緩衝需求。
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- ASFLeakyBucketPairs windows Media 格式
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965825"
---
# <a name="asfleakybucketpairs"></a><span data-ttu-id="c52fe-104">ASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="c52fe-104">ASFLeakyBucketPairs</span></span>

<span data-ttu-id="c52fe-105">**ASFLeakyBucketPairs** 屬性是選擇性屬性，可描述變數位元速率檔案的緩衝需求。</span><span class="sxs-lookup"><span data-stu-id="c52fe-105">The **ASFLeakyBucketPairs** attribute is an optional attribute that describes the buffering requirements for a variable bit rate file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c52fe-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="c52fe-106">Global Constant</span></span>

<span data-ttu-id="c52fe-107">g \_ wszASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="c52fe-107">g\_wszASFLeakyBucketPairs</span></span>

## <a name="data-type"></a><span data-ttu-id="c52fe-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="c52fe-108">Data Type</span></span>

<span data-ttu-id="c52fe-109">**WMT \_ 類型 \_ 二進位**</span><span class="sxs-lookup"><span data-stu-id="c52fe-109">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="c52fe-110">備註</span><span class="sxs-lookup"><span data-stu-id="c52fe-110">Remarks</span></span>

<span data-ttu-id="c52fe-111">這個屬性的格式如下：</span><span class="sxs-lookup"><span data-stu-id="c52fe-111">This attribute has the following format:</span></span>

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="c52fe-112">其中 *wReserved* 必須等於零，而 *bucket* 是 [**WM \_ 有漏洞 \_ bucket \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) 組結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="c52fe-112">Where *wReserved* must equal zero, and *bucket* is an array of [**WM\_LEAKY\_BUCKET\_PAIR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) structures.</span></span> <span data-ttu-id="c52fe-113">陣列必須包含至少兩個專案，但可以較大。</span><span class="sxs-lookup"><span data-stu-id="c52fe-113">The array must contain at least two entries, but can be larger.</span></span> <span data-ttu-id="c52fe-114">讀取器物件會使用此屬性來判斷播放前要緩衝的內容數量。</span><span class="sxs-lookup"><span data-stu-id="c52fe-114">The reader object uses this attribute to determine the amount of content to buffer before playback.</span></span>

## <a name="see-also"></a><span data-ttu-id="c52fe-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c52fe-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c52fe-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="c52fe-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




