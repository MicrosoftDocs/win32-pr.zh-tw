---
description: 設定 FOURCCMap 物件的 FOURCC 部分。
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'FOURCCMap：： SetFOURCC 方法 (Fourcc .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976144"
---
# <a name="fourccmapsetfourcc-method"></a><span data-ttu-id="937e7-103">FOURCCMap：： SetFOURCC 方法</span><span class="sxs-lookup"><span data-stu-id="937e7-103">FOURCCMap::SetFOURCC method</span></span>

<span data-ttu-id="937e7-104">設定 [**FOURCCMap**](fourccmap.md)物件的 **FOURCC** 部分。</span><span class="sxs-lookup"><span data-stu-id="937e7-104">Sets the **FOURCC** portion of the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="937e7-105">語法</span><span class="sxs-lookup"><span data-stu-id="937e7-105">Syntax</span></span>


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="937e7-106">參數</span><span class="sxs-lookup"><span data-stu-id="937e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="937e7-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="937e7-107">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="937e7-108">傳回的全域唯一識別碼的指標， (**GUID**) **FOURCCMap** 物件的一部分。</span><span class="sxs-lookup"><span data-stu-id="937e7-108">Pointer to the returned globally unique identifier (**GUID**) part of the **FOURCCMap** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="937e7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="937e7-109">Return value</span></span>

<span data-ttu-id="937e7-110">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="937e7-110">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="937e7-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="937e7-111">Requirements</span></span>



| <span data-ttu-id="937e7-112">需求</span><span class="sxs-lookup"><span data-stu-id="937e7-112">Requirement</span></span> | <span data-ttu-id="937e7-113">值</span><span class="sxs-lookup"><span data-stu-id="937e7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="937e7-114">標頭</span><span class="sxs-lookup"><span data-stu-id="937e7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="937e7-115"><dt>Fourcc (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="937e7-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="937e7-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="937e7-116">Library</span></span><br/> | <dl> <span data-ttu-id="937e7-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="937e7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="937e7-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="937e7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="937e7-119">**FOURCCMap 類別**</span><span class="sxs-lookup"><span data-stu-id="937e7-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




