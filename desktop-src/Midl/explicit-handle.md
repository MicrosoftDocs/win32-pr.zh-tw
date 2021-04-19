---
title: explicit_handle 屬性
description: '\ Explicit \_ 控制碼 \ ACF 屬性指定每個程式都有一個基本控制碼，例如控制碼 t 型別，做為第一個參數 \_ 。'
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965202"
---
# <a name="explicit_handle-attribute"></a><span data-ttu-id="b48c1-104">明確 \_ 控制碼屬性</span><span class="sxs-lookup"><span data-stu-id="b48c1-104">explicit\_handle attribute</span></span>

<span data-ttu-id="b48c1-105">\[**明確的 \_ 控制碼** \] ACF 屬性指定每個程式都有一個基本控制碼，例如 [**控制碼 \_ t 型別**](handle-t.md)，做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="b48c1-105">The \[**explicit\_handle**\] ACF attribute specifies that each procedure has, as its first parameter, a primitive handle, such as a [**handle\_t**](handle-t.md) type.</span></span>

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="b48c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="b48c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b48c1-107">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="b48c1-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b48c1-108">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="b48c1-108">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b48c1-109">備註</span><span class="sxs-lookup"><span data-stu-id="b48c1-109">Remarks</span></span>

<span data-ttu-id="b48c1-110">當您使用 **\[ 明確 \_ 控制碼 \]** 屬性時，每個程式都有一個基本控制碼做為第一個參數，即使 IDL 檔案未在其參數清單中包含這個控制碼也是一樣。</span><span class="sxs-lookup"><span data-stu-id="b48c1-110">When you use the **\[explicit\_handle\]** attribute, each procedure has a primitive handle as its first parameter even if the IDL file does not contain this handle in its parameter list.</span></span> <span data-ttu-id="b48c1-111">發出至標頭檔和存根常式的原型包含額外的參數，並使用該參數做為導向遠端呼叫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b48c1-111">The prototypes emitted to the header file and stub routines contain the additional parameter, and that parameter is used as the handle for directing the remote call.</span></span>

<span data-ttu-id="b48c1-112">**\[ 明確的 \_ 句 \] 柄** 屬性會同時影響遠端程式和序列化程式。</span><span class="sxs-lookup"><span data-stu-id="b48c1-112">The **\[explicit\_handle\]** attribute affects both remote procedures and serialization procedures.</span></span> <span data-ttu-id="b48c1-113">針對型別序列化，會使用初始參數做為明確 (序列化) 控制碼來產生支援常式。</span><span class="sxs-lookup"><span data-stu-id="b48c1-113">For type serialization, the support routines are generated with the initial parameter as an explicit (serialization) handle.</span></span> <span data-ttu-id="b48c1-114">如果未使用 **\[ 明確的 \_ 句 \] 柄** 屬性，應用程式仍然可以指定作業具有明確的控制碼 (系結或序列化) 導向呼叫。</span><span class="sxs-lookup"><span data-stu-id="b48c1-114">If the **\[explicit\_handle\]** attribute is not used, the application can still specify that an operation have an explicit handle (binding or serialization) directing the call.</span></span> <span data-ttu-id="b48c1-115">若要這樣做，具有包含控制碼類型之引數的原型會提供給 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="b48c1-115">To do this, a prototype with an argument containing a handle type is supplied to the IDL file.</span></span> <span data-ttu-id="b48c1-116">請注意，在預設模式下，未先出現的引數也可以做為控制碼來導向呼叫。</span><span class="sxs-lookup"><span data-stu-id="b48c1-116">Note that in default mode, an argument that does not appear first can also be used as a handle directing the call.</span></span>

<span data-ttu-id="b48c1-117">因此，雖然 **\[ 明確的 \_ 句 \] 柄** 屬性是一種提供 idl 原型的基本 **\[ 明確 \_ 控制碼 \]** 屬性的方式，但不一定需要變更 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="b48c1-117">Therefore, while the **\[explicit\_handle\]** attribute is a way of giving the IDL prototype a primitive **\[explicit\_handle\]** attribute, it does not necessarily require a change to the IDL file.</span></span> <span data-ttu-id="b48c1-118">在 [**/osf**](-osf.md) 模式中，只有第一個引數可以當做明確的控制碼類型使用。</span><span class="sxs-lookup"><span data-stu-id="b48c1-118">In [**/osf**](-osf.md) mode only the first argument can be used as an explicit handle type.</span></span>

<span data-ttu-id="b48c1-119">**\[ 明確 \_ 控制碼 \]** 屬性可以當做介面屬性或作業屬性使用。</span><span class="sxs-lookup"><span data-stu-id="b48c1-119">The **\[explicit\_handle\]** attribute can be used as either an interface attribute or an operation attribute.</span></span> <span data-ttu-id="b48c1-120">作為介面屬性，它會影響介面中的所有作業，以及需要序列化支援的所有類型。</span><span class="sxs-lookup"><span data-stu-id="b48c1-120">As an interface attribute, it affects all the operations in the interface and all the types that require serialization support.</span></span> <span data-ttu-id="b48c1-121">但是，如果使用它做為作業屬性，它只會影響該特定的作業。</span><span class="sxs-lookup"><span data-stu-id="b48c1-121">If, however, it is used as an operation attribute, it affects only that particular operation.</span></span> <span data-ttu-id="b48c1-122">如果方法 \[ 在內容控制碼中包含一或多個 \] ，則 \[ 會使用最左邊的 \] 內容控制碼作為系結控制碼，而不會建立其他明確的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b48c1-122">If a method contains one or more \[in\] context handles, the left most \[in\] context handle is used as the binding handle, and no additional explicit handle is created.</span></span>

## <a name="examples"></a><span data-ttu-id="b48c1-123">範例</span><span class="sxs-lookup"><span data-stu-id="b48c1-123">Examples</span></span>

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="b48c1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b48c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48c1-125">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="b48c1-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="b48c1-126">**自動 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="b48c1-126">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="b48c1-127">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="b48c1-127">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="b48c1-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="b48c1-128">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




