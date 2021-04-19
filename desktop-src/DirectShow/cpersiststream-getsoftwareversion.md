---
description: 抓取此資料流程的軟體版本。
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: 'CPersistStream. GetSoftwareVersion 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994737"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a><span data-ttu-id="c4cf5-103">CPersistStream. GetSoftwareVersion 方法</span><span class="sxs-lookup"><span data-stu-id="c4cf5-103">CPersistStream.GetSoftwareVersion method</span></span>

<span data-ttu-id="c4cf5-104">抓取此資料流程的軟體版本。</span><span class="sxs-lookup"><span data-stu-id="c4cf5-104">Retrieves the software version for this stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4cf5-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4cf5-105">Syntax</span></span>


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a><span data-ttu-id="c4cf5-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4cf5-106">Parameters</span></span>

<span data-ttu-id="c4cf5-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c4cf5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4cf5-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4cf5-108">Return value</span></span>

<span data-ttu-id="c4cf5-109">傳回包含版本號碼的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="c4cf5-109">Returns a **DWORD** containing the version number.</span></span> <span data-ttu-id="c4cf5-110">每次變更資料流程的格式時，應該改變此函式，以傳回比之前更大的數位。</span><span class="sxs-lookup"><span data-stu-id="c4cf5-110">Each time the format of the stream is changed, this function should be altered to return a larger number than before.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4cf5-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4cf5-111">Requirements</span></span>



| <span data-ttu-id="c4cf5-112">需求</span><span class="sxs-lookup"><span data-stu-id="c4cf5-112">Requirement</span></span> | <span data-ttu-id="c4cf5-113">值</span><span class="sxs-lookup"><span data-stu-id="c4cf5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4cf5-114">標頭</span><span class="sxs-lookup"><span data-stu-id="c4cf5-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c4cf5-115"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c4cf5-115"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c4cf5-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="c4cf5-116">Library</span></span><br/> | <dl> <span data-ttu-id="c4cf5-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c4cf5-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4cf5-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4cf5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4cf5-119">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="c4cf5-119">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




