---
description: SetSubtype 方法會指定子類型。
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: 'CMediaType. SetSubtype 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989783"
---
# <a name="cmediatypesetsubtype-method"></a><span data-ttu-id="06393-103">CMediaType. SetSubtype 方法</span><span class="sxs-lookup"><span data-stu-id="06393-103">CMediaType.SetSubtype method</span></span>

<span data-ttu-id="06393-104">`SetSubtype`方法會指定子類型。</span><span class="sxs-lookup"><span data-stu-id="06393-104">The `SetSubtype` method specifies the subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="06393-105">語法</span><span class="sxs-lookup"><span data-stu-id="06393-105">Syntax</span></span>


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a><span data-ttu-id="06393-106">參數</span><span class="sxs-lookup"><span data-stu-id="06393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06393-107">*psubtype*</span><span class="sxs-lookup"><span data-stu-id="06393-107">*psubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="06393-108">指定子類型之 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="06393-108">Pointer to a **GUID** that specifies the subtype.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06393-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="06393-109">Return value</span></span>

<span data-ttu-id="06393-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="06393-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="06393-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="06393-111">Requirements</span></span>



| <span data-ttu-id="06393-112">需求</span><span class="sxs-lookup"><span data-stu-id="06393-112">Requirement</span></span> | <span data-ttu-id="06393-113">值</span><span class="sxs-lookup"><span data-stu-id="06393-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06393-114">標頭</span><span class="sxs-lookup"><span data-stu-id="06393-114">Header</span></span><br/>  | <dl> <span data-ttu-id="06393-115"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="06393-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="06393-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="06393-116">Library</span></span><br/> | <dl> <span data-ttu-id="06393-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="06393-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06393-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06393-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06393-119">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="06393-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




