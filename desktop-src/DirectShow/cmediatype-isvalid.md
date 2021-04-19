---
description: IsValid 方法會判斷是否已將主要類型指派給這個物件。
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: 'CMediaType 的 IsValid 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000894"
---
# <a name="cmediatypeisvalid-method"></a><span data-ttu-id="d5635-103">CMediaType. IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="d5635-103">CMediaType.IsValid method</span></span>

<span data-ttu-id="d5635-104">`IsValid`方法會判斷是否已將主要類型指派給這個物件。</span><span class="sxs-lookup"><span data-stu-id="d5635-104">The `IsValid` method determines whether a major type has been assigned to this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5635-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5635-105">Syntax</span></span>


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a><span data-ttu-id="d5635-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5635-106">Parameters</span></span>

<span data-ttu-id="d5635-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d5635-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5635-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5635-108">Return value</span></span>

<span data-ttu-id="d5635-109">如果已將主要類型指派給此物件，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d5635-109">Returns **TRUE** if a major type has been assigned to this object.</span></span> <span data-ttu-id="d5635-110">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d5635-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5635-111">備註</span><span class="sxs-lookup"><span data-stu-id="d5635-111">Remarks</span></span>

<span data-ttu-id="d5635-112">根據預設， [**CMediaType**](cmediatype.md) 物件會使用 GUID Null 的主要類型進行初始化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5635-112">By default, [**CMediaType**](cmediatype.md) objects are initialized with a major type of GUID\_NULL.</span></span> <span data-ttu-id="d5635-113">呼叫這個方法，以判斷物件是否已正確初始化。</span><span class="sxs-lookup"><span data-stu-id="d5635-113">Call this method to determine whether the object has been correctly initialized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5635-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5635-114">Requirements</span></span>



| <span data-ttu-id="d5635-115">需求</span><span class="sxs-lookup"><span data-stu-id="d5635-115">Requirement</span></span> | <span data-ttu-id="d5635-116">值</span><span class="sxs-lookup"><span data-stu-id="d5635-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5635-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d5635-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d5635-118"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d5635-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d5635-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5635-119">Library</span></span><br/> | <dl> <span data-ttu-id="d5635-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d5635-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5635-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5635-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5635-122">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="d5635-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




