---
description: DbgSetModuleLevel 函數會設定一或多個訊息類型的記錄層級。 在零售組建中略過。
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: 'DbgSetModuleLevel 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983018"
---
# <a name="dbgsetmodulelevel-function"></a><span data-ttu-id="4fb89-104">DbgSetModuleLevel 函式</span><span class="sxs-lookup"><span data-stu-id="4fb89-104">DbgSetModuleLevel function</span></span>

<span data-ttu-id="4fb89-105">**DbgSetModuleLevel** 函數會設定一或多個訊息類型的記錄層級。</span><span class="sxs-lookup"><span data-stu-id="4fb89-105">The **DbgSetModuleLevel** function sets the logging level for one or more message types.</span></span> <span data-ttu-id="4fb89-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="4fb89-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb89-107">語法</span><span class="sxs-lookup"><span data-stu-id="4fb89-107">Syntax</span></span>


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="4fb89-108">參數</span><span class="sxs-lookup"><span data-stu-id="4fb89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb89-109">*類型*</span><span class="sxs-lookup"><span data-stu-id="4fb89-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="4fb89-110">一或多個訊息類型的位元組合。</span><span class="sxs-lookup"><span data-stu-id="4fb89-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="4fb89-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="4fb89-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="4fb89-112">指定訊息類型的記錄層級。</span><span class="sxs-lookup"><span data-stu-id="4fb89-112">Logging level for the specified message types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fb89-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fb89-113">Return value</span></span>

<span data-ttu-id="4fb89-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4fb89-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb89-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fb89-115">Requirements</span></span>



| <span data-ttu-id="4fb89-116">需求</span><span class="sxs-lookup"><span data-stu-id="4fb89-116">Requirement</span></span> | <span data-ttu-id="4fb89-117">值</span><span class="sxs-lookup"><span data-stu-id="4fb89-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb89-118">標頭</span><span class="sxs-lookup"><span data-stu-id="4fb89-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4fb89-119"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4fb89-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4fb89-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="4fb89-120">Library</span></span><br/> | <dl> <span data-ttu-id="4fb89-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4fb89-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb89-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fb89-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb89-123">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="4fb89-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




