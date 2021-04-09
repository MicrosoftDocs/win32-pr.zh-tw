---
title: 略過屬性
description: '\ 忽略 \ 屬性會指定包含在結構或等位中的指標，以及指標所指出的物件不會傳送。 \ 忽略 \ 屬性僅限於結構或等位的指標成員。'
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- 忽略屬性 MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e82b9525dd6de316087db8fdfd55181118d3adc6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842163"
---
# <a name="ignore-attribute"></a><span data-ttu-id="2b65b-105">略過屬性</span><span class="sxs-lookup"><span data-stu-id="2b65b-105">ignore attribute</span></span>

<span data-ttu-id="2b65b-106">**\[ Ignore \]** 屬性會指定包含在結構或等位中的指標，以及指標所指出的物件不會傳送。</span><span class="sxs-lookup"><span data-stu-id="2b65b-106">The **\[ignore\]** attribute designates that a pointer contained in a structure or union and the object indicated by the pointer is not transmitted.</span></span> <span data-ttu-id="2b65b-107">**\[ Ignore \]** 屬性僅限於結構或等位的指標成員。</span><span class="sxs-lookup"><span data-stu-id="2b65b-107">The **\[ignore\]** attribute is restricted to pointer members of structures or unions.</span></span>

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a><span data-ttu-id="2b65b-108">參數</span><span class="sxs-lookup"><span data-stu-id="2b65b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b65b-109">*指標成員類型*</span><span class="sxs-lookup"><span data-stu-id="2b65b-109">*pointer-member-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2b65b-110">指定結構或等位之指標成員的類型。</span><span class="sxs-lookup"><span data-stu-id="2b65b-110">Specifies the type of the pointer member of the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="2b65b-111">*指標名稱*</span><span class="sxs-lookup"><span data-stu-id="2b65b-111">*pointer-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2b65b-112">指定在封送處理期間要忽略之指標成員的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b65b-112">Specifies the name of the pointer member that is to be ignored during marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b65b-113">備註</span><span class="sxs-lookup"><span data-stu-id="2b65b-113">Remarks</span></span>

<span data-ttu-id="2b65b-114">目的地端未定義具有 **\[ ignore \]** 屬性之結構成員的值。</span><span class="sxs-lookup"><span data-stu-id="2b65b-114">The value of a structure member with the **\[ignore\]** attribute is undefined at the destination.</span></span> <span data-ttu-id="2b65b-115">**\[**[**在**](in.md) **\]** 遠端電腦上未定義 in 參數。</span><span class="sxs-lookup"><span data-stu-id="2b65b-115">An **\[**[**in**](in.md)**\]** parameter is not defined at the remote computer.</span></span> <span data-ttu-id="2b65b-116">**\[** [](out-idl.md) **\]** 在本機電腦上未定義 out 參數。</span><span class="sxs-lookup"><span data-stu-id="2b65b-116">An **\[**[**out**](out-idl.md)**\]** parameter is not defined at the local computer.</span></span>

<span data-ttu-id="2b65b-117">**\[ Ignore \]** 屬性可讓您防止資料的傳輸。</span><span class="sxs-lookup"><span data-stu-id="2b65b-117">The **\[ignore\]** attribute allows you to prevent transmission of data.</span></span> <span data-ttu-id="2b65b-118">這在類似于雙重連結清單的情況下很有用。</span><span class="sxs-lookup"><span data-stu-id="2b65b-118">This is useful in situations such as a double-linked list.</span></span> <span data-ttu-id="2b65b-119">下列範例包含會導入資料別名的雙重連結清單：</span><span class="sxs-lookup"><span data-stu-id="2b65b-119">The following example includes a double-linked list that introduces data aliasing:</span></span>

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

<span data-ttu-id="2b65b-120">在上述範例中會發生別名，因為在函式 **p** 和 **p >下一個 >** 的兩個不同指標中，可以使用相同的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="2b65b-120">Aliasing occurs in the preceding example because the same memory area is available from two different pointers in the function **p** and **p->next->previous**.</span></span>

<span data-ttu-id="2b65b-121">請注意，[ **\[ 忽略 \]** ] 不能用來做為類型屬性。</span><span class="sxs-lookup"><span data-stu-id="2b65b-121">Note that **\[ignore\]** cannot be used as a type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="2b65b-122">範例</span><span class="sxs-lookup"><span data-stu-id="2b65b-122">Examples</span></span>

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="2b65b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b65b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b65b-124">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="2b65b-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b65b-125">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="2b65b-125">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="2b65b-126">陣列和指標</span><span class="sxs-lookup"><span data-stu-id="2b65b-126">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="2b65b-127">**在**</span><span class="sxs-lookup"><span data-stu-id="2b65b-127">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="2b65b-128">**擴展**</span><span class="sxs-lookup"><span data-stu-id="2b65b-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="2b65b-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="2b65b-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="2b65b-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="2b65b-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="2b65b-131">**獨特**</span><span class="sxs-lookup"><span data-stu-id="2b65b-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 