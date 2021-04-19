---
description: GuidNames 是 DirectShow 基類庫中的全域陣列，其中包含代表 Uuid 中定義之 Guid 的字串。 這個陣列適用于產生 debug 輸出。
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: 'GuidNames (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978713"
---
# <a name="guidnames"></a><span data-ttu-id="50bea-104">GuidNames</span><span class="sxs-lookup"><span data-stu-id="50bea-104">GuidNames</span></span>

<span data-ttu-id="50bea-105">`GuidNames` 是 DirectShow 基類庫中的全域陣列，其中包含代表 Uuid 中定義之 Guid 的字串。</span><span class="sxs-lookup"><span data-stu-id="50bea-105">`GuidNames` is a global array in the DirectShow base class library that contains strings representing the GUIDs defined in Uuids.h.</span></span> <span data-ttu-id="50bea-106">這個陣列適用于產生 debug 輸出。</span><span class="sxs-lookup"><span data-stu-id="50bea-106">This array is useful for generating debug output.</span></span>

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a><span data-ttu-id="50bea-107">參數</span><span class="sxs-lookup"><span data-stu-id="50bea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50bea-108"><span id="guid"></span><span id="GUID"></span>*Guid*</span><span class="sxs-lookup"><span data-stu-id="50bea-108"><span id="guid"></span><span id="GUID"></span>*guid*</span></span>
</dt> <dd>

<span data-ttu-id="50bea-109">指定標頭檔 Uuid 中定義的任何 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="50bea-109">Specifies any GUID value defined in the header file Uuids.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50bea-110">備註</span><span class="sxs-lookup"><span data-stu-id="50bea-110">Remarks</span></span>

<span data-ttu-id="50bea-111">使用這個全域陣列，將 GUID 常數輸出為字串。</span><span class="sxs-lookup"><span data-stu-id="50bea-111">Use this global array to output GUID constants as strings.</span></span> <span data-ttu-id="50bea-112">例如，下列程式碼會將「媒體型影片」字串列印 \_ 到主控台：</span><span class="sxs-lookup"><span data-stu-id="50bea-112">For example, the following code prints the string "MEDIATYPE\_Video" to the console:</span></span>


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



<span data-ttu-id="50bea-113">如果 GUID 不相符，則會傳回「未知的 GUID 名稱」字串。</span><span class="sxs-lookup"><span data-stu-id="50bea-113">If the GUID is not matched, the string "Unknown GUID Name" is returned.</span></span> <span data-ttu-id="50bea-114">並非所有的 DirectShow Guid 都定義于 uuid. h 中。</span><span class="sxs-lookup"><span data-stu-id="50bea-114">Not all DirectShow GUIDs are defined in uuids.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="50bea-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="50bea-115">Requirements</span></span>



| <span data-ttu-id="50bea-116">需求</span><span class="sxs-lookup"><span data-stu-id="50bea-116">Requirement</span></span> | <span data-ttu-id="50bea-117">值</span><span class="sxs-lookup"><span data-stu-id="50bea-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50bea-118">標頭</span><span class="sxs-lookup"><span data-stu-id="50bea-118">Header</span></span><br/>  | <dl> <span data-ttu-id="50bea-119"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="50bea-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50bea-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="50bea-120">Library</span></span><br/> | <dl> <span data-ttu-id="50bea-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="50bea-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50bea-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50bea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50bea-123">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="50bea-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




