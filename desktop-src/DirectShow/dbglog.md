---
description: 如果已針對指定的類型和層級啟用記錄，DbgLog 宏會將字串傳送至偵錯工具輸出位置。 零售組建中會忽略此宏。
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: 'DbgLog 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981351"
---
# <a name="dbglog-macro"></a><span data-ttu-id="673cb-104">DbgLog 宏</span><span class="sxs-lookup"><span data-stu-id="673cb-104">DbgLog macro</span></span>

<span data-ttu-id="673cb-105">如果已針對指定的類型和層級啟用記錄， **DbgLog** 宏會將字串傳送至偵錯工具輸出位置。</span><span class="sxs-lookup"><span data-stu-id="673cb-105">The **DbgLog** macro sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> <span data-ttu-id="673cb-106">零售組建中會忽略此宏。</span><span class="sxs-lookup"><span data-stu-id="673cb-106">This macro is ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="673cb-107">語法</span><span class="sxs-lookup"><span data-stu-id="673cb-107">Syntax</span></span>


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a><span data-ttu-id="673cb-108">參數</span><span class="sxs-lookup"><span data-stu-id="673cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673cb-109">*類型*</span><span class="sxs-lookup"><span data-stu-id="673cb-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="673cb-110">一或多個訊息類型的位元組合。</span><span class="sxs-lookup"><span data-stu-id="673cb-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="673cb-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="673cb-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="673cb-112">此訊息的記錄層級。</span><span class="sxs-lookup"><span data-stu-id="673cb-112">Logging level for this message.</span></span>

</dd> <dt>

<span data-ttu-id="673cb-113">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="673cb-113">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="673cb-114">**Printf** 樣式的格式字串。</span><span class="sxs-lookup"><span data-stu-id="673cb-114">A **printf** -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="673cb-115">*...*</span><span class="sxs-lookup"><span data-stu-id="673cb-115">*...*</span></span> 
</dt> <dd>

<span data-ttu-id="673cb-116">格式字串的其他引數。</span><span class="sxs-lookup"><span data-stu-id="673cb-116">Additional arguments for the format string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673cb-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="673cb-117">Return value</span></span>

<span data-ttu-id="673cb-118">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="673cb-118">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="673cb-119">備註</span><span class="sxs-lookup"><span data-stu-id="673cb-119">Remarks</span></span>

<span data-ttu-id="673cb-120">如果任何訊息類型的 debug 記錄設定為指定的層級或更高的層級，此宏就會將格式化的字串傳送至偵錯工具的輸出位置。</span><span class="sxs-lookup"><span data-stu-id="673cb-120">If debug logging for any of the message types is set to the specified level or higher, this macro sends the formatted string to the debug output location.</span></span>

<span data-ttu-id="673cb-121">宏會自動將換行字元加入至輸出字串。</span><span class="sxs-lookup"><span data-stu-id="673cb-121">The macro automatically adds a newline character to the output string.</span></span>

> [!Note]  
> <span data-ttu-id="673cb-122">另外一組括弧必須用來括住巨集引數：</span><span class="sxs-lookup"><span data-stu-id="673cb-122">An additional set of parentheses must enclose the macro parameters:</span></span>

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a><span data-ttu-id="673cb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="673cb-123">Requirements</span></span>



| <span data-ttu-id="673cb-124">需求</span><span class="sxs-lookup"><span data-stu-id="673cb-124">Requirement</span></span> | <span data-ttu-id="673cb-125">值</span><span class="sxs-lookup"><span data-stu-id="673cb-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="673cb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="673cb-126">Header</span></span><br/> | <dl> <span data-ttu-id="673cb-127"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="673cb-127"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673cb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="673cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673cb-129">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="673cb-129">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




