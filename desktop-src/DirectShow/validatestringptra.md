---
description: 確認呼叫進程具有 ANSI 字串的讀取權限。 如果沒有，宏就會呼叫 DbgBreak 宏。
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: 'ValidateStringPtrA 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978508"
---
# <a name="validatestringptra-macro"></a><span data-ttu-id="3bc60-104">ValidateStringPtrA 宏</span><span class="sxs-lookup"><span data-stu-id="3bc60-104">ValidateStringPtrA macro</span></span>

<span data-ttu-id="3bc60-105">確認呼叫進程具有 ANSI 字串的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="3bc60-105">Verifies that the calling process has read access to an ANSI string.</span></span> <span data-ttu-id="3bc60-106">如果沒有，宏就會呼叫 [**DbgBreak**](dbgbreak.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="3bc60-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="3bc60-107">這個宏已被取代。</span><span class="sxs-lookup"><span data-stu-id="3bc60-107">This macro is deprecated.</span></span> <span data-ttu-id="3bc60-108">在 Windows Vista (和更新版本的 Windows SDK 中) 此宏不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="3bc60-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3bc60-109">語法</span><span class="sxs-lookup"><span data-stu-id="3bc60-109">Syntax</span></span>


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="3bc60-110">參數</span><span class="sxs-lookup"><span data-stu-id="3bc60-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc60-111">*P*</span><span class="sxs-lookup"><span data-stu-id="3bc60-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc60-112">以 Null 結束的 ANSI 字串指標。</span><span class="sxs-lookup"><span data-stu-id="3bc60-112">Pointer to a NULL-terminated ANSI string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bc60-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bc60-113">Return value</span></span>

<span data-ttu-id="3bc60-114">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3bc60-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bc60-115">備註</span><span class="sxs-lookup"><span data-stu-id="3bc60-115">Remarks</span></span>

<span data-ttu-id="3bc60-116">除非包含了 DirectShow 基類標頭檔，否則會忽略這個宏，除非已定義 DEBUG、 \_ debug 或 VFWROBUST。</span><span class="sxs-lookup"><span data-stu-id="3bc60-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc60-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bc60-117">Requirements</span></span>



| <span data-ttu-id="3bc60-118">需求</span><span class="sxs-lookup"><span data-stu-id="3bc60-118">Requirement</span></span> | <span data-ttu-id="3bc60-119">值</span><span class="sxs-lookup"><span data-stu-id="3bc60-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc60-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3bc60-120">Header</span></span><br/> | <dl> <span data-ttu-id="3bc60-121"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3bc60-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc60-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bc60-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc60-123">指標驗證宏</span><span class="sxs-lookup"><span data-stu-id="3bc60-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




