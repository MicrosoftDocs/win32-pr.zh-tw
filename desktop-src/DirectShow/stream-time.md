---
description: 請注意，這個 API 已被取代。 新的應用程式不應使用它。 資料流程 \_ 時間資料類型是用來表示 Microsoft DirectShow 多媒體串流中的參考時間。 單位為100毫微秒。
ms.assetid: eff79c58-09d8-4665-9138-752ffaf02e26
title: 'STREAM_TIME (Mmstream) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4603aafeb8901eaa0465ab43030c78b76e1ac5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000015"
---
# <a name="stream_time"></a><span data-ttu-id="219a5-106">資料流程 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="219a5-106">STREAM\_TIME</span></span>

> [!Note]  
> <span data-ttu-id="219a5-107">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="219a5-107">This API is deprecated.</span></span> <span data-ttu-id="219a5-108">新的應用程式不應使用它。</span><span class="sxs-lookup"><span data-stu-id="219a5-108">New applications should not use it.</span></span>

 

<span data-ttu-id="219a5-109">資料流程 \_ 時間資料類型是用來表示 Microsoft DirectShow 多媒體串流中的參考時間。</span><span class="sxs-lookup"><span data-stu-id="219a5-109">The STREAM\_TIME data type is used to express reference times in Microsoft DirectShow multimedia streaming.</span></span> <span data-ttu-id="219a5-110">單位為100毫微秒。</span><span class="sxs-lookup"><span data-stu-id="219a5-110">Units are 100 nanoseconds.</span></span>


```C++
typedef LONGLONG STREAM_TIME;
```



## <a name="remarks"></a><span data-ttu-id="219a5-111">備註</span><span class="sxs-lookup"><span data-stu-id="219a5-111">Remarks</span></span>

<span data-ttu-id="219a5-112">這種資料類型相當於 [DirectShow [**參考 \_ 時間**](reference-time.md) ] 資料類型。</span><span class="sxs-lookup"><span data-stu-id="219a5-112">This data type is equivalent to the DirectShow [**REFERENCE\_TIME**](reference-time.md) data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="219a5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="219a5-113">Requirements</span></span>



| <span data-ttu-id="219a5-114">需求</span><span class="sxs-lookup"><span data-stu-id="219a5-114">Requirement</span></span> | <span data-ttu-id="219a5-115">值</span><span class="sxs-lookup"><span data-stu-id="219a5-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="219a5-116">標頭</span><span class="sxs-lookup"><span data-stu-id="219a5-116">Header</span></span><br/> | <dl> <span data-ttu-id="219a5-117"><dt>Mmstream。h</dt></span><span class="sxs-lookup"><span data-stu-id="219a5-117"><dt>Mmstream.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="219a5-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="219a5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219a5-119">多媒體串流資料類型</span><span class="sxs-lookup"><span data-stu-id="219a5-119">Multimedia Streaming Data Types</span></span>](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




