---
title: 間隔語法
description: 表示時間間隔值。
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- 間隔語法 AD 架構
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385318"
---
# <a name="interval-syntax"></a><span data-ttu-id="543d6-104">間隔語法</span><span class="sxs-lookup"><span data-stu-id="543d6-104">Interval syntax</span></span>

<span data-ttu-id="543d6-105">表示時間間隔值。</span><span class="sxs-lookup"><span data-stu-id="543d6-105">Represents a time interval value.</span></span> <span data-ttu-id="543d6-106">實際的時間單位取決於使用此語法的屬性。</span><span class="sxs-lookup"><span data-stu-id="543d6-106">The actual time units depend on which attribute is using this syntax.</span></span> <span data-ttu-id="543d6-107">這個語法與 [**LargeInteger**](s-largeinteger.md) 語法完全相同，但最高值和最低值都是不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="543d6-107">This syntax is identical to the [**LargeInteger**](s-largeinteger.md) syntax, except the high and low values are unsigned integers.</span></span>



| <span data-ttu-id="543d6-108">進入</span><span class="sxs-lookup"><span data-stu-id="543d6-108">Entry</span></span> | <span data-ttu-id="543d6-109">值</span><span class="sxs-lookup"><span data-stu-id="543d6-109">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="543d6-110">名稱</span><span class="sxs-lookup"><span data-stu-id="543d6-110">Name</span></span>         | <span data-ttu-id="543d6-111">間隔</span><span class="sxs-lookup"><span data-stu-id="543d6-111">Interval</span></span>                                                                           |
| <span data-ttu-id="543d6-112">語法識別碼</span><span class="sxs-lookup"><span data-stu-id="543d6-112">Syntax ID</span></span>    | <span data-ttu-id="543d6-113">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="543d6-113">2.5.5.16</span></span>                                                                           |
| <span data-ttu-id="543d6-114">OM 識別碼</span><span class="sxs-lookup"><span data-stu-id="543d6-114">OM ID</span></span>        | <span data-ttu-id="543d6-115">65</span><span class="sxs-lookup"><span data-stu-id="543d6-115">65</span></span>                                                                                 |
| <span data-ttu-id="543d6-116">MAPI 類型</span><span class="sxs-lookup"><span data-stu-id="543d6-116">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="543d6-117">ADS 類型</span><span class="sxs-lookup"><span data-stu-id="543d6-117">ADS Type</span></span>     | <span data-ttu-id="543d6-118">ADSTYPE \_ 大型 \_ 整數</span><span class="sxs-lookup"><span data-stu-id="543d6-118">ADSTYPE\_LARGE\_INTEGER</span></span>                                                            |
| <span data-ttu-id="543d6-119">Variant 類型</span><span class="sxs-lookup"><span data-stu-id="543d6-119">Variant Type</span></span> | <span data-ttu-id="543d6-120">VT \_ 分派</span><span class="sxs-lookup"><span data-stu-id="543d6-120">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="543d6-121">SDS 類型</span><span class="sxs-lookup"><span data-stu-id="543d6-121">SDS Type</span></span>     | <span data-ttu-id="543d6-122">可以轉換成 [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="543d6-122">A COM object that can be cast to an [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span></span> |



## <a name="see-also"></a><span data-ttu-id="543d6-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="543d6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="543d6-124">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="543d6-124">**IADsLargeInteger**</span></span>](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[<span data-ttu-id="543d6-125">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="543d6-125">**LargeInteger**</span></span>](s-largeinteger.md)
</dt> </dl>

 

 
