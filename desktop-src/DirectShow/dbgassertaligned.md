---
description: 測試指標是否對齊指定的界限。 如果沒有，此宏會叫用 ASSERT 宏。 在零售組建中略過。
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: 'DbgAssertAligned 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979571"
---
# <a name="dbgassertaligned-macro"></a><span data-ttu-id="bd19a-105">DbgAssertAligned 宏</span><span class="sxs-lookup"><span data-stu-id="bd19a-105">DbgAssertAligned macro</span></span>

<span data-ttu-id="bd19a-106">測試指標是否對齊指定的界限。</span><span class="sxs-lookup"><span data-stu-id="bd19a-106">Tests whether a pointer is aligned to a specified boundary.</span></span> <span data-ttu-id="bd19a-107">如果沒有，此宏會叫用 [**ASSERT**](assert.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="bd19a-107">If not, this macro invokes the [**ASSERT**](assert.md) macro.</span></span> <span data-ttu-id="bd19a-108">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="bd19a-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd19a-109">語法</span><span class="sxs-lookup"><span data-stu-id="bd19a-109">Syntax</span></span>


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a><span data-ttu-id="bd19a-110">參數</span><span class="sxs-lookup"><span data-stu-id="bd19a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd19a-111">*ptr*</span><span class="sxs-lookup"><span data-stu-id="bd19a-111">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="bd19a-112">指標變數。</span><span class="sxs-lookup"><span data-stu-id="bd19a-112">Pointer variable.</span></span>

</dd> <dt>

<span data-ttu-id="bd19a-113">*對準*</span><span class="sxs-lookup"><span data-stu-id="bd19a-113">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="bd19a-114">需要的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="bd19a-114">Required alignment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd19a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd19a-115">Return value</span></span>

<span data-ttu-id="bd19a-116">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bd19a-116">This macro does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd19a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd19a-117">Requirements</span></span>



| <span data-ttu-id="bd19a-118">需求</span><span class="sxs-lookup"><span data-stu-id="bd19a-118">Requirement</span></span> | <span data-ttu-id="bd19a-119">值</span><span class="sxs-lookup"><span data-stu-id="bd19a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd19a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="bd19a-120">Header</span></span><br/> | <dl> <span data-ttu-id="bd19a-121"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bd19a-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd19a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd19a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd19a-123">Assert 和中斷點宏</span><span class="sxs-lookup"><span data-stu-id="bd19a-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




