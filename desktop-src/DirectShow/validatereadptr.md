---
description: 確認呼叫進程具有記憶體區塊的讀取權限。 如果沒有，宏就會呼叫 DbgBreak 宏。
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: 'ValidateReadPtr 宏 (Wxdebug) '
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
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996091"
---
# <a name="validatereadptr-macro"></a><span data-ttu-id="e4e3e-104">ValidateReadPtr 宏</span><span class="sxs-lookup"><span data-stu-id="e4e3e-104">ValidateReadPtr macro</span></span>

<span data-ttu-id="e4e3e-105">確認呼叫進程具有記憶體區塊的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-105">Verifies that the calling process has read access to a memory block.</span></span> <span data-ttu-id="e4e3e-106">如果沒有，宏就會呼叫 [**DbgBreak**](dbgbreak.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="e4e3e-107">這個宏已被取代。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-107">This macro is deprecated.</span></span> <span data-ttu-id="e4e3e-108">在 Windows Vista (和更新版本的 Windows SDK 中) 此宏不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e4e3e-109">語法</span><span class="sxs-lookup"><span data-stu-id="e4e3e-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="e4e3e-110">參數</span><span class="sxs-lookup"><span data-stu-id="e4e3e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e3e-111">*P*</span><span class="sxs-lookup"><span data-stu-id="e4e3e-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="e4e3e-112">記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="e4e3e-113">*Cb*</span><span class="sxs-lookup"><span data-stu-id="e4e3e-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="e4e3e-114">記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e3e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4e3e-115">Return value</span></span>

<span data-ttu-id="e4e3e-116">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e3e-117">備註</span><span class="sxs-lookup"><span data-stu-id="e4e3e-117">Remarks</span></span>

<span data-ttu-id="e4e3e-118">除非包含了 DirectShow 基類標頭檔，否則會忽略這個宏，除非已定義 DEBUG、 \_ debug 或 VFWROBUST。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="e4e3e-119">此宏可能會有顯著的效能成本。</span><span class="sxs-lookup"><span data-stu-id="e4e3e-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e3e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4e3e-120">Requirements</span></span>



| <span data-ttu-id="e4e3e-121">需求</span><span class="sxs-lookup"><span data-stu-id="e4e3e-121">Requirement</span></span> | <span data-ttu-id="e4e3e-122">值</span><span class="sxs-lookup"><span data-stu-id="e4e3e-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e3e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e4e3e-123">Header</span></span><br/> | <dl> <span data-ttu-id="e4e3e-124"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e4e3e-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4e3e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4e3e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e3e-126">指標驗證宏</span><span class="sxs-lookup"><span data-stu-id="e4e3e-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




