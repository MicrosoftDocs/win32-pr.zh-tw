---
title: implicit_handle 屬性
description: '\ 隱含 \_ 控制碼 \ ACF 屬性會指定用於不包含明確控制碼做為程式參數之函數的控制碼。'
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841112"
---
# <a name="implicit_handle-attribute"></a><span data-ttu-id="6b3a5-104">隱含 \_ 控制碼屬性</span><span class="sxs-lookup"><span data-stu-id="6b3a5-104">implicit\_handle attribute</span></span>

<span data-ttu-id="6b3a5-105">**\[ 隱含 \_ 控制碼 \]** ACF 屬性會指定用於不包含明確控制碼做為程式參數之函數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-105">The **\[implicit\_handle\]** ACF attribute specifies the handle used for functions that do not include an explicit handle as a procedure parameter.</span></span>

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a><span data-ttu-id="6b3a5-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b3a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b3a5-107">*控制碼類型*</span><span class="sxs-lookup"><span data-stu-id="6b3a5-107">*handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="6b3a5-108">指定控制碼資料類型，例如基底類型 [**控制碼 \_ t**](handle-t.md) 或使用者定義的控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-108">Specifies the handle data type, such as the base type [**handle\_t**](handle-t.md) or a user-defined handle type.</span></span>

</dd> <dt>

<span data-ttu-id="6b3a5-109">*控制碼名稱*</span><span class="sxs-lookup"><span data-stu-id="6b3a5-109">*handle-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6b3a5-110">指定控制碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-110">Specifies the name of the handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b3a5-111">備註</span><span class="sxs-lookup"><span data-stu-id="6b3a5-111">Remarks</span></span>

<span data-ttu-id="6b3a5-112">視程式的本質而定， **\[ 隱含 \_ 控制碼 \]** 屬性指定的控制碼會以不同的方式使用。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-112">The handle specified by the **\[implicit\_handle\]** attribute is used in different ways depending on the nature of the procedure.</span></span> <span data-ttu-id="6b3a5-113">如果程式是遠端的，則會使用控制碼做為遠端呼叫的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-113">If the procedure is remote, the handle will be used as the binding handle for the remote call.</span></span> <span data-ttu-id="6b3a5-114">隱含控制碼也可以用來建立使用內容控制碼之函式的初始系結。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-114">The implicit handle may also be used to establish an initial binding for a function that uses a context handle.</span></span> <span data-ttu-id="6b3a5-115">如果程式是序列化程式，則會使用控制碼做為控制作業的序列化控制碼。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-115">If the procedure is a serializing procedure, the handle is used as a serializing handle controlling the operation.</span></span> <span data-ttu-id="6b3a5-116">在序列化類型的情況下，會使用控制碼作為所有序列化類型的序列化控制碼。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-116">In the case of type serialization, the handle is used as the serialization handle for all the serialized types.</span></span>

<span data-ttu-id="6b3a5-117">**\[ 隱含 \_ 控制碼 \]** 屬性指定的全域變數包含任何需要隱含控制碼的函式所使用的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-117">The **\[implicit\_handle\]** attribute specifies a global variable that contains a handle used by any function needing implicit handles.</span></span>

<span data-ttu-id="6b3a5-118">隱含系結控制碼類型必須是 [**處理 \_ t**](handle-t.md) (或以 **控制碼 \_ t**) 為基礎的型別，或是以 [**handle**](handle.md) 屬性指定的使用者定義控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-118">The implicit binding handle type must be either [**handle\_t**](handle-t.md) (or a type based on **handle\_t**) or a user-defined handle type specified with the [**handle**](handle.md) attribute.</span></span> <span data-ttu-id="6b3a5-119">隱含序列化控制碼必須是以 **控制碼 \_ t** 為基礎的型別。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-119">The implicit serializing handle must be a type based on **handle\_t**.</span></span>

<span data-ttu-id="6b3a5-120">如果 IDL 檔中未定義隱含控制碼類型，或是在 MIDL 電腦的 IDL 檔案包含和匯入的任何檔案中定義，則當您編譯存根時，必須提供包含控制碼類型定義的檔案。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-120">If the implicit handle type is not defined in the IDL file or in any files included and imported by the IDL file for the MIDL computer, you must supply the file containing the handle-type definition when you compile the stubs.</span></span> <span data-ttu-id="6b3a5-121">您可以使用 ACF [**include**](include.md) 語句來包含包含控制碼類型定義的檔案。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-121">Use the ACF [**include**](include.md) statement to include the file containing the handle-type definition.</span></span>

<span data-ttu-id="6b3a5-122">**\[ 隱含 \_ 控制碼 \]** 屬性最多隻能出現一次。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-122">The **\[implicit\_handle\]** attribute can occur once, at most.</span></span> <span data-ttu-id="6b3a5-123">只有當 [**\[ 自動 \_ 控制碼 \]**](auto-handle.md)和 [**\[ 明確的 \_ 控制碼 \]**](explicit-handle.md)屬性不發生時，才會發生 **\[ 隱含 \_ 句 \]** 柄屬性。</span><span class="sxs-lookup"><span data-stu-id="6b3a5-123">The **\[implicit\_handle\]** attribute can occur only if the [**\[auto\_handle\]**](auto-handle.md) and [**\[explicit\_handle\]**](explicit-handle.md) attributes do not occur.</span></span>

## <a name="examples"></a><span data-ttu-id="6b3a5-124">範例</span><span class="sxs-lookup"><span data-stu-id="6b3a5-124">Examples</span></span>

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a><span data-ttu-id="6b3a5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b3a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b3a5-126">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="6b3a5-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="6b3a5-127">**自動 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="6b3a5-127">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="6b3a5-128">**明確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="6b3a5-128">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="6b3a5-129">**處理 \_ t**</span><span class="sxs-lookup"><span data-stu-id="6b3a5-129">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="6b3a5-130">**包括**</span><span class="sxs-lookup"><span data-stu-id="6b3a5-130">**include**</span></span>](include.md)
</dt> </dl>

 

 




