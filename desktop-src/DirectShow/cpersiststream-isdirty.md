---
description: 指出物件自從上次儲存至其目前資料流程之後是否已變更。
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: 'CPersistStream. IsDirty 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990246"
---
# <a name="cpersiststreamisdirty-method"></a><span data-ttu-id="0f537-103">CPersistStream. IsDirty 方法</span><span class="sxs-lookup"><span data-stu-id="0f537-103">CPersistStream.IsDirty method</span></span>

<span data-ttu-id="0f537-104">指出物件自從上次儲存至其目前資料流程之後是否已變更。</span><span class="sxs-lookup"><span data-stu-id="0f537-104">Indicates whether the object has changed since it was last saved to its current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f537-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f537-105">Syntax</span></span>


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a><span data-ttu-id="0f537-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f537-106">Parameters</span></span>

<span data-ttu-id="0f537-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0f537-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f537-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f537-108">Return value</span></span>

<span data-ttu-id="0f537-109">\_如果篩選準則需要儲存，則傳回 [確定]， \_ 如果不需要儲存則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="0f537-109">Returns S\_OK if the filter needs saving and S\_FALSE if it does not need saving.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f537-110">備註</span><span class="sxs-lookup"><span data-stu-id="0f537-110">Remarks</span></span>

<span data-ttu-id="0f537-111">此成員函式會實作為 **IPersistStream：： IsDirty** 方法。</span><span class="sxs-lookup"><span data-stu-id="0f537-111">This member function implements the **IPersistStream::IsDirty** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f537-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f537-112">Requirements</span></span>



| <span data-ttu-id="0f537-113">需求</span><span class="sxs-lookup"><span data-stu-id="0f537-113">Requirement</span></span> | <span data-ttu-id="0f537-114">值</span><span class="sxs-lookup"><span data-stu-id="0f537-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f537-115">標頭</span><span class="sxs-lookup"><span data-stu-id="0f537-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0f537-116"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0f537-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f537-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f537-117">Library</span></span><br/> | <dl> <span data-ttu-id="0f537-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0f537-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f537-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f537-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f537-120">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="0f537-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




