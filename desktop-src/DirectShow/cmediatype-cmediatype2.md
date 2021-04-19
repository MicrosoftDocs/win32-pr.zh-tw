---
description: 深入瞭解 CMediaType. CMediaType (Mtype 的) 方法。 這個方法會使用 ' majortype ' 參數。
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: CMediaType. CMediaType 函式 (Mtype .h) -majortype 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106991506"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a><span data-ttu-id="ae236-104">CMediaType. CMediaType 函式 (Mtype .h) -majortype 參數</span><span class="sxs-lookup"><span data-stu-id="ae236-104">CMediaType.CMediaType constructor (Mtype.h) - majortype parameter</span></span>

<span data-ttu-id="ae236-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="ae236-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae236-106">語法</span><span class="sxs-lookup"><span data-stu-id="ae236-106">Syntax</span></span>


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a><span data-ttu-id="ae236-107">參數</span><span class="sxs-lookup"><span data-stu-id="ae236-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae236-108">*majortype*</span><span class="sxs-lookup"><span data-stu-id="ae236-108">*majortype*</span></span> 
</dt> <dd>

<span data-ttu-id="ae236-109">主要類型 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="ae236-109">Pointer to a major type **GUID**.</span></span> <span data-ttu-id="ae236-110">此函式會將主要類型 GUID 初始化為此值。</span><span class="sxs-lookup"><span data-stu-id="ae236-110">The constructor initializes the major type GUID to this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae236-111">備註</span><span class="sxs-lookup"><span data-stu-id="ae236-111">Remarks</span></span>

<span data-ttu-id="ae236-112">此函式會呼叫 [**CMediaType：： InitMediaType**](cmediatype-initmediatype.md) 方法來初始化媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ae236-112">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae236-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae236-113">Requirements</span></span>

| <span data-ttu-id="ae236-114">需求</span><span class="sxs-lookup"><span data-stu-id="ae236-114">Requirement</span></span>                   | <span data-ttu-id="ae236-115">值</span><span class="sxs-lookup"><span data-stu-id="ae236-115">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae236-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ae236-116">Header</span></span>  | <span data-ttu-id="ae236-117">Mtype (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="ae236-117">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="ae236-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="ae236-118">Library</span></span> | <span data-ttu-id="ae236-119"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="ae236-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ae236-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae236-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae236-121">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="ae236-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




