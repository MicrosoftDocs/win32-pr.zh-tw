---
description: StringFromResource 函式會從資源檔載入具有指定資源識別碼的字串。
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: 'StringFromResource 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983179"
---
# <a name="stringfromresource-function"></a><span data-ttu-id="48a1a-103">StringFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="48a1a-103">StringFromResource function</span></span>

<span data-ttu-id="48a1a-104">`StringFromResource`函數會從資源檔載入具有指定資源識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="48a1a-104">The `StringFromResource` function loads a string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a1a-105">語法</span><span class="sxs-lookup"><span data-stu-id="48a1a-105">Syntax</span></span>


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="48a1a-106">參數</span><span class="sxs-lookup"><span data-stu-id="48a1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a1a-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="48a1a-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="48a1a-108">對應至 *iResourceID* 之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="48a1a-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="48a1a-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="48a1a-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="48a1a-110">要取出之字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="48a1a-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a1a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="48a1a-111">Return value</span></span>

<span data-ttu-id="48a1a-112">傳回與 *pBuffer* 相同的字串。</span><span class="sxs-lookup"><span data-stu-id="48a1a-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="48a1a-113">如果函式不成功，則會傳回 null 字串。</span><span class="sxs-lookup"><span data-stu-id="48a1a-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="48a1a-114">備註</span><span class="sxs-lookup"><span data-stu-id="48a1a-114">Remarks</span></span>

<span data-ttu-id="48a1a-115">*PBuffer* 緩衝區必須至少為 STR 的 \_ 最大 \_ 長度位元組。</span><span class="sxs-lookup"><span data-stu-id="48a1a-115">The *pBuffer* buffer must be at least STR\_MAX\_LENGTH bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="48a1a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="48a1a-116">Requirements</span></span>



| <span data-ttu-id="48a1a-117">需求</span><span class="sxs-lookup"><span data-stu-id="48a1a-117">Requirement</span></span> | <span data-ttu-id="48a1a-118">值</span><span class="sxs-lookup"><span data-stu-id="48a1a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a1a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="48a1a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="48a1a-120"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="48a1a-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="48a1a-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="48a1a-121">Library</span></span><br/> | <dl> <span data-ttu-id="48a1a-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="48a1a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a1a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48a1a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a1a-124">屬性頁 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="48a1a-124">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




