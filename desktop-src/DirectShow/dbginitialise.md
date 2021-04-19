---
description: DbgInitialise 函式會初始化 debug 程式庫。 在零售組建中略過。
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: 'DbgInitialise 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995717"
---
# <a name="dbginitialise-function"></a><span data-ttu-id="b4a2b-104">DbgInitialise 函式</span><span class="sxs-lookup"><span data-stu-id="b4a2b-104">DbgInitialise function</span></span>

<span data-ttu-id="b4a2b-105">**DbgInitialise** 函式會初始化 debug 程式庫。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-105">The **DbgInitialise** function initializes the debug library.</span></span> <span data-ttu-id="b4a2b-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a2b-107">語法</span><span class="sxs-lookup"><span data-stu-id="b4a2b-107">Syntax</span></span>


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a><span data-ttu-id="b4a2b-108">參數</span><span class="sxs-lookup"><span data-stu-id="b4a2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a2b-109">*hInst*</span><span class="sxs-lookup"><span data-stu-id="b4a2b-109">*hInst*</span></span> 
</dt> <dd>

<span data-ttu-id="b4a2b-110">模組實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-110">Handle to the module instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a2b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4a2b-111">Return value</span></span>

<span data-ttu-id="b4a2b-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a2b-113">備註</span><span class="sxs-lookup"><span data-stu-id="b4a2b-113">Remarks</span></span>

<span data-ttu-id="b4a2b-114">在可執行檔中，請先呼叫這個方法，再使用 DirectShow debug 功能。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-114">In an executable, call this method before using the DirectShow debug facilities.</span></span> <span data-ttu-id="b4a2b-115">在可執行檔結束之前，呼叫 [**DbgTerminate**](dbgterminate.md) 函式來清除偵錯工具程式庫。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-115">Before the executable quits, call the [**DbgTerminate**](dbgterminate.md) function to clean up the debug library.</span></span>

<span data-ttu-id="b4a2b-116">在連結至基類程式庫 (Strmbase .lib) 的 DLL 中，不需要呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-116">In a DLL that links to the base-class library (Strmbase.lib), it is not necessary to call this function.</span></span> <span data-ttu-id="b4a2b-117">載入 DLL 時，會自動呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="b4a2b-117">The function is called automatically when the DLL is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a2b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4a2b-118">Requirements</span></span>



| <span data-ttu-id="b4a2b-119">需求</span><span class="sxs-lookup"><span data-stu-id="b4a2b-119">Requirement</span></span> | <span data-ttu-id="b4a2b-120">值</span><span class="sxs-lookup"><span data-stu-id="b4a2b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a2b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b4a2b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b4a2b-122"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b4a2b-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b4a2b-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b4a2b-123">Library</span></span><br/> | <dl> <span data-ttu-id="b4a2b-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b4a2b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a2b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4a2b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a2b-126">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="b4a2b-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




