---
description: 確認呼叫進程具有記憶體區塊的寫入權限。 如果沒有，宏就會呼叫 DbgBreak 宏。
ms.assetid: efbb5ca6-0289-487d-b55a-f85b38d0515a
title: 'ValidateWritePtr 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: e7c955f31cf9e0bf1050c52b680dfc9b32741bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995506"
---
# <a name="validatewriteptr-macro"></a><span data-ttu-id="06f2a-104">ValidateWritePtr 宏</span><span class="sxs-lookup"><span data-stu-id="06f2a-104">ValidateWritePtr macro</span></span>

<span data-ttu-id="06f2a-105">確認呼叫進程具有記憶體區塊的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="06f2a-105">Verifies that the calling process has write access to a memory block.</span></span> <span data-ttu-id="06f2a-106">如果沒有，宏就會呼叫 [**DbgBreak**](dbgbreak.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="06f2a-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="06f2a-107">這個宏已被取代。</span><span class="sxs-lookup"><span data-stu-id="06f2a-107">This macro is deprecated.</span></span> <span data-ttu-id="06f2a-108">在 Windows Vista (和更新版本的 Windows SDK 中) 此宏不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="06f2a-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="06f2a-109">語法</span><span class="sxs-lookup"><span data-stu-id="06f2a-109">Syntax</span></span>


```C++
void ValidateWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="06f2a-110">參數</span><span class="sxs-lookup"><span data-stu-id="06f2a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f2a-111">*P*</span><span class="sxs-lookup"><span data-stu-id="06f2a-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="06f2a-112">記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="06f2a-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="06f2a-113">*Cb*</span><span class="sxs-lookup"><span data-stu-id="06f2a-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="06f2a-114">記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="06f2a-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06f2a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="06f2a-115">Return value</span></span>

<span data-ttu-id="06f2a-116">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="06f2a-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06f2a-117">備註</span><span class="sxs-lookup"><span data-stu-id="06f2a-117">Remarks</span></span>

<span data-ttu-id="06f2a-118">除非包含了 DirectShow 基類標頭檔，否則會忽略這個宏，除非已定義 DEBUG、 \_ debug 或 VFWROBUST。</span><span class="sxs-lookup"><span data-stu-id="06f2a-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="06f2a-119">此宏可能會有顯著的效能成本。</span><span class="sxs-lookup"><span data-stu-id="06f2a-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f2a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="06f2a-120">Requirements</span></span>



| <span data-ttu-id="06f2a-121">需求</span><span class="sxs-lookup"><span data-stu-id="06f2a-121">Requirement</span></span> | <span data-ttu-id="06f2a-122">值</span><span class="sxs-lookup"><span data-stu-id="06f2a-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06f2a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="06f2a-123">Header</span></span><br/> | <dl> <span data-ttu-id="06f2a-124"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="06f2a-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f2a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06f2a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f2a-126">指標驗證宏</span><span class="sxs-lookup"><span data-stu-id="06f2a-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




