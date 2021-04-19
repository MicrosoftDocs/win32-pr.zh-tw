---
description: NAME 宏會產生僅限 debug 的字串。
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: '名稱 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994697"
---
# <a name="name"></a><span data-ttu-id="373af-103">名稱</span><span class="sxs-lookup"><span data-stu-id="373af-103">NAME</span></span>

<span data-ttu-id="373af-104">**NAME** 宏會產生僅限 debug 的字串。</span><span class="sxs-lookup"><span data-stu-id="373af-104">The **NAME** macro generates a debug-only string.</span></span>

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="373af-105">參數</span><span class="sxs-lookup"><span data-stu-id="373af-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="373af-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="373af-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="373af-107">文字字串。</span><span class="sxs-lookup"><span data-stu-id="373af-107">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="373af-108">備註</span><span class="sxs-lookup"><span data-stu-id="373af-108">Remarks</span></span>

<span data-ttu-id="373af-109">在 debug 組建中，此宏相當於 **文字** 宏。</span><span class="sxs-lookup"><span data-stu-id="373af-109">In debug builds, this macro is equivalent to the **TEXT** macro.</span></span> <span data-ttu-id="373af-110">在零售組建中，它會解析為 (TCHAR \*) **Null**。</span><span class="sxs-lookup"><span data-stu-id="373af-110">In retail builds, it resolves to (TCHAR\*) **NULL**.</span></span> <span data-ttu-id="373af-111">宣告衍生自 [**CBaseObject**](cbaseobject.md) 類別的物件名稱時，這個宏很有用。</span><span class="sxs-lookup"><span data-stu-id="373af-111">This macro is useful when declaring the name of an object that derives from the [**CBaseObject**](cbaseobject.md) class.</span></span>


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a><span data-ttu-id="373af-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="373af-112">Requirements</span></span>



| <span data-ttu-id="373af-113">需求</span><span class="sxs-lookup"><span data-stu-id="373af-113">Requirement</span></span> | <span data-ttu-id="373af-114">值</span><span class="sxs-lookup"><span data-stu-id="373af-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="373af-115">標頭</span><span class="sxs-lookup"><span data-stu-id="373af-115">Header</span></span><br/>  | <dl> <span data-ttu-id="373af-116"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="373af-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="373af-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="373af-117">Library</span></span><br/> | <dl> <span data-ttu-id="373af-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="373af-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="373af-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="373af-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="373af-120">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="373af-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




