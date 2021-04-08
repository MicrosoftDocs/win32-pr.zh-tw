---
title: iid_is 屬性
description: '\ Iid \_ 是 \ 指標屬性，可指定介面指標所指向之 COM 介面的 iid。'
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is 屬性 MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022306"
---
# <a name="iid_is-attribute"></a><span data-ttu-id="0a15a-104">iid \_ 為屬性</span><span class="sxs-lookup"><span data-stu-id="0a15a-104">iid\_is attribute</span></span>

<span data-ttu-id="0a15a-105">**\[ Iid \_ 是 \]** 指標屬性，可指定介面指標所指向之 COM 介面的 iid。</span><span class="sxs-lookup"><span data-stu-id="0a15a-105">The **\[iid\_is\]** pointer attribute specifies the IID of the COM interface pointed to by an interface pointer.</span></span>

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a><span data-ttu-id="0a15a-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a15a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a15a-107">*有限運算式*</span><span class="sxs-lookup"><span data-stu-id="0a15a-107">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="0a15a-108">指定 C 語言運算式。</span><span class="sxs-lookup"><span data-stu-id="0a15a-108">Specifies a C-language expression.</span></span> <span data-ttu-id="0a15a-109">MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。</span><span class="sxs-lookup"><span data-stu-id="0a15a-109">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="0a15a-110">MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。</span><span class="sxs-lookup"><span data-stu-id="0a15a-110">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a15a-111">備註</span><span class="sxs-lookup"><span data-stu-id="0a15a-111">Remarks</span></span>

<span data-ttu-id="0a15a-112">您可以在函數參數和結構或等位成員的屬性清單中使用 **\[ iid \_ \]** 。</span><span class="sxs-lookup"><span data-stu-id="0a15a-112">You can use **\[iid\_is\]** in attribute lists for function parameters and for structure or union members.</span></span> <span data-ttu-id="0a15a-113">存根使用 IID 來判斷如何封送處理介面指標。</span><span class="sxs-lookup"><span data-stu-id="0a15a-113">The stubs use the IID to determine how to marshal the interface pointer.</span></span> <span data-ttu-id="0a15a-114">這適用于類型為基類參數的介面指標。</span><span class="sxs-lookup"><span data-stu-id="0a15a-114">This is useful for an interface pointer that is typed as a base class parameter.</span></span>

<span data-ttu-id="0a15a-115">使用 iid 的檔案 **\[ \_ 是 \]** 在預設模式下，使用 MIDL 編譯器來編譯的屬性，不是使用 [**/osf**](-osf.md)參數。</span><span class="sxs-lookup"><span data-stu-id="0a15a-115">Files that use the **\[iid\_is\]** attribute must be compiled with the MIDL compiler in default mode, that is not using the [**/osf**](-osf.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="0a15a-116">範例</span><span class="sxs-lookup"><span data-stu-id="0a15a-116">Examples</span></span>

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a><span data-ttu-id="0a15a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a15a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a15a-118">**物件**</span><span class="sxs-lookup"><span data-stu-id="0a15a-118">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="0a15a-119">**uuid**</span><span class="sxs-lookup"><span data-stu-id="0a15a-119">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




