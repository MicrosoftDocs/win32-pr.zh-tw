---
description: DbgCheckModuleLevel 函式會檢查是否已針對指定的訊息類型和層級啟用記錄功能。 在零售組建中略過。
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: 'DbgCheckModuleLevel 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976238"
---
# <a name="dbgcheckmodulelevel-function"></a><span data-ttu-id="7f167-104">DbgCheckModuleLevel 函式</span><span class="sxs-lookup"><span data-stu-id="7f167-104">DbgCheckModuleLevel function</span></span>

<span data-ttu-id="7f167-105">`DbgCheckModuleLevel`函數會檢查是否已針對指定的訊息類型和層級啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="7f167-105">The `DbgCheckModuleLevel` function checks whether logging is enabled for the given message types and level.</span></span> <span data-ttu-id="7f167-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="7f167-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f167-107">語法</span><span class="sxs-lookup"><span data-stu-id="7f167-107">Syntax</span></span>


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="7f167-108">參數</span><span class="sxs-lookup"><span data-stu-id="7f167-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f167-109">*類型*</span><span class="sxs-lookup"><span data-stu-id="7f167-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="7f167-110">一或多個訊息類型的位元組合。</span><span class="sxs-lookup"><span data-stu-id="7f167-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="7f167-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="7f167-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="7f167-112">記錄層級</span><span class="sxs-lookup"><span data-stu-id="7f167-112">Logging level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f167-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f167-113">Return value</span></span>

<span data-ttu-id="7f167-114">如果指定之任何訊息類型的記錄設定為指定的層級或更高的層級，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="7f167-114">Returns **TRUE** if logging for any of the specified message types is set to the specified level or higher.</span></span> <span data-ttu-id="7f167-115">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7f167-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f167-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f167-116">Requirements</span></span>



| <span data-ttu-id="7f167-117">需求</span><span class="sxs-lookup"><span data-stu-id="7f167-117">Requirement</span></span> | <span data-ttu-id="7f167-118">值</span><span class="sxs-lookup"><span data-stu-id="7f167-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f167-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7f167-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7f167-120"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7f167-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f167-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f167-121">Library</span></span><br/> | <dl> <span data-ttu-id="7f167-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7f167-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f167-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f167-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f167-124">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="7f167-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




