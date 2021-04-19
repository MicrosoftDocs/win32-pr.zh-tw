---
description: 函式方法。
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: CSourceStream. ~ CSourceStream (Source. h) 的函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa27d50a9c1acbc9c8a27407cb97673d60158e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976112"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="510ba-103">CSourceStream. ~ CSourceStream 的函式</span><span class="sxs-lookup"><span data-stu-id="510ba-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="510ba-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="510ba-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="510ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="510ba-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="510ba-106">備註</span><span class="sxs-lookup"><span data-stu-id="510ba-106">Remarks</span></span>

<span data-ttu-id="510ba-107">此函式會藉由呼叫 [**CSource：： RemovePin**](csource-removepin.md)，自動移除擁有篩選的釘選。</span><span class="sxs-lookup"><span data-stu-id="510ba-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="510ba-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="510ba-108">Requirements</span></span>



| <span data-ttu-id="510ba-109">需求</span><span class="sxs-lookup"><span data-stu-id="510ba-109">Requirement</span></span> | <span data-ttu-id="510ba-110">值</span><span class="sxs-lookup"><span data-stu-id="510ba-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="510ba-111">標頭</span><span class="sxs-lookup"><span data-stu-id="510ba-111">Header</span></span><br/>  | <dl> <span data-ttu-id="510ba-112"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="510ba-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="510ba-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="510ba-113">Library</span></span><br/> | <dl> <span data-ttu-id="510ba-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="510ba-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="510ba-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="510ba-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="510ba-116">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="510ba-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




