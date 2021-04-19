---
description: IsTemporalCompressed 方法會判斷資料流程是否使用時態性壓縮。
ms.assetid: 06a57655-a304-429d-a150-819072b91016
title: 'CMediaType. IsTemporalCompressed 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsTemporalCompressed
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 09c9770c23e0cd7f1f5140a5f9b9f18299ddaa23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993448"
---
# <a name="cmediatypeistemporalcompressed-method"></a><span data-ttu-id="85502-103">CMediaType. IsTemporalCompressed 方法</span><span class="sxs-lookup"><span data-stu-id="85502-103">CMediaType.IsTemporalCompressed method</span></span>

<span data-ttu-id="85502-104">`IsTemporalCompressed`方法會判斷資料流程是否使用時態性壓縮。</span><span class="sxs-lookup"><span data-stu-id="85502-104">The `IsTemporalCompressed` method determines if the stream uses temporal compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="85502-105">語法</span><span class="sxs-lookup"><span data-stu-id="85502-105">Syntax</span></span>


```C++
BOOL IsTemporalCompressed() const;
```



## <a name="parameters"></a><span data-ttu-id="85502-106">參數</span><span class="sxs-lookup"><span data-stu-id="85502-106">Parameters</span></span>

<span data-ttu-id="85502-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="85502-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85502-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="85502-108">Return value</span></span>

<span data-ttu-id="85502-109">傳回 **bTemporalCompression** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="85502-109">Returns the value of the **bTemporalCompression** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="85502-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="85502-110">Requirements</span></span>



| <span data-ttu-id="85502-111">需求</span><span class="sxs-lookup"><span data-stu-id="85502-111">Requirement</span></span> | <span data-ttu-id="85502-112">值</span><span class="sxs-lookup"><span data-stu-id="85502-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85502-113">標頭</span><span class="sxs-lookup"><span data-stu-id="85502-113">Header</span></span><br/>  | <dl> <span data-ttu-id="85502-114"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="85502-114"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="85502-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="85502-115">Library</span></span><br/> | <dl> <span data-ttu-id="85502-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="85502-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85502-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85502-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85502-118">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="85502-118">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




