---
description: 確認呼叫進程具有字串的讀取存取權。 如果沒有，宏就會呼叫 DbgBreak 宏。
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: 'ValidateStringPtr 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997801"
---
# <a name="validatestringptr-macro"></a><span data-ttu-id="3a7f0-104">ValidateStringPtr 宏</span><span class="sxs-lookup"><span data-stu-id="3a7f0-104">ValidateStringPtr macro</span></span>

<span data-ttu-id="3a7f0-105">確認呼叫進程具有字串的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="3a7f0-105">Verifies that the calling process has read access to a string.</span></span> <span data-ttu-id="3a7f0-106">如果沒有，宏就會呼叫 [**DbgBreak**](dbgbreak.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="3a7f0-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="3a7f0-107">這個宏已被取代。</span><span class="sxs-lookup"><span data-stu-id="3a7f0-107">This macro is deprecated.</span></span> <span data-ttu-id="3a7f0-108">在 Windows Vista (和更新版本的 Windows SDK 中) 此宏不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="3a7f0-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3a7f0-109">語法</span><span class="sxs-lookup"><span data-stu-id="3a7f0-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="3a7f0-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a7f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a7f0-111">*P*</span><span class="sxs-lookup"><span data-stu-id="3a7f0-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="3a7f0-112">以 Null 終止的 **TCHAR** 字串指標。</span><span class="sxs-lookup"><span data-stu-id="3a7f0-112">Pointer to a NULL-terminated **TCHAR** string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a7f0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a7f0-113">Return value</span></span>

<span data-ttu-id="3a7f0-114">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3a7f0-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a7f0-115">備註</span><span class="sxs-lookup"><span data-stu-id="3a7f0-115">Remarks</span></span>

<span data-ttu-id="3a7f0-116">除非包含了 DirectShow 基類標頭檔，否則會忽略這個宏，除非已定義 DEBUG、 \_ debug 或 VFWROBUST。</span><span class="sxs-lookup"><span data-stu-id="3a7f0-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="3a7f0-117">此宏可能會有顯著的效能成本。</span><span class="sxs-lookup"><span data-stu-id="3a7f0-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a7f0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a7f0-118">Requirements</span></span>



| <span data-ttu-id="3a7f0-119">需求</span><span class="sxs-lookup"><span data-stu-id="3a7f0-119">Requirement</span></span> | <span data-ttu-id="3a7f0-120">值</span><span class="sxs-lookup"><span data-stu-id="3a7f0-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a7f0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3a7f0-121">Header</span></span><br/> | <dl> <span data-ttu-id="3a7f0-122"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3a7f0-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a7f0-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a7f0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a7f0-124">指標驗證宏</span><span class="sxs-lookup"><span data-stu-id="3a7f0-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




