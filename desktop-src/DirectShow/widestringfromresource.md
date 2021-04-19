---
description: WideStringFromResource 函式會從資源檔載入具有指定資源識別碼的寬字元字串。
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: 'WideStringFromResource 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994128"
---
# <a name="widestringfromresource-function"></a><span data-ttu-id="5df0c-103">WideStringFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="5df0c-103">WideStringFromResource function</span></span>

<span data-ttu-id="5df0c-104">`WideStringFromResource`函數會從資源檔載入具有指定資源識別碼的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="5df0c-104">The `WideStringFromResource` function loads a wide-character string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df0c-105">語法</span><span class="sxs-lookup"><span data-stu-id="5df0c-105">Syntax</span></span>


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="5df0c-106">參數</span><span class="sxs-lookup"><span data-stu-id="5df0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df0c-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="5df0c-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="5df0c-108">對應至 *iResourceID* 之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="5df0c-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="5df0c-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="5df0c-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="5df0c-110">要取出之字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5df0c-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df0c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5df0c-111">Return value</span></span>

<span data-ttu-id="5df0c-112">傳回與 *pBuffer* 相同的字串。</span><span class="sxs-lookup"><span data-stu-id="5df0c-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="5df0c-113">如果函式不成功，則會傳回 null 字串。</span><span class="sxs-lookup"><span data-stu-id="5df0c-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df0c-114">備註</span><span class="sxs-lookup"><span data-stu-id="5df0c-114">Remarks</span></span>

<span data-ttu-id="5df0c-115">屬性頁通常會透過其 COM 介面呼叫，而不論二進位檔的建立方式為何，都使用寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="5df0c-115">Property pages are typically called through their COM interfaces, which use wide-character strings regardless of how the binary is built.</span></span> <span data-ttu-id="5df0c-116">此函數可讓您將資源字串轉換成寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="5df0c-116">This function allows you to convert a resource string to a wide-character string.</span></span> <span data-ttu-id="5df0c-117">此函式會將資源轉換為寬字元字串 (如果它在載入後尚未) 的話。</span><span class="sxs-lookup"><span data-stu-id="5df0c-117">The function converts the resource to a wide-character string (if it is not already one) after loading it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df0c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5df0c-118">Requirements</span></span>



| <span data-ttu-id="5df0c-119">需求</span><span class="sxs-lookup"><span data-stu-id="5df0c-119">Requirement</span></span> | <span data-ttu-id="5df0c-120">值</span><span class="sxs-lookup"><span data-stu-id="5df0c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5df0c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5df0c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5df0c-122"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5df0c-122"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5df0c-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="5df0c-123">Library</span></span><br/> | <dl> <span data-ttu-id="5df0c-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5df0c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5df0c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5df0c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df0c-126">屬性頁 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="5df0c-126">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




