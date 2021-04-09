---
title: coNtext_handle 屬性
description: '\ 內容 \_ 控制碼 \ 屬性會識別在遠端程序呼叫之間，維護伺服器上內容或狀態資訊的系結控制碼。'
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- coNtext_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681772"
---
# <a name="context_handle-attribute"></a><span data-ttu-id="6d840-104">內容 \_ 控制碼屬性</span><span class="sxs-lookup"><span data-stu-id="6d840-104">context\_handle attribute</span></span>

<span data-ttu-id="6d840-105">**\[ 內容 \_ 控制碼 \]** 屬性會識別在遠端程序呼叫之間，維護伺服器上內容或狀態資訊的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d840-105">The **\[context\_handle\]** attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span>

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a><span data-ttu-id="6d840-106">參數</span><span class="sxs-lookup"><span data-stu-id="6d840-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d840-107">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="6d840-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d840-108">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="6d840-108">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="6d840-109">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="6d840-109">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="6d840-110">指定指標類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="6d840-110">Specifies a pointer type or a type identifier.</span></span> <span data-ttu-id="6d840-111">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="6d840-111">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="6d840-112">*宣告子和宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="6d840-112">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d840-113">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="6d840-113">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="6d840-114">內容控制碼的宣告子必須包含至少一個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="6d840-114">The declarator for a context handle must include at least one pointer declarator.</span></span> <span data-ttu-id="6d840-115">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="6d840-115">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="6d840-116">宣告子清單包含一或多個宣告子， *並* 以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="6d840-116">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="6d840-117">函式宣告子中的參數名稱識別碼是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6d840-117">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6d840-118">*函數-attr-list*</span><span class="sxs-lookup"><span data-stu-id="6d840-118">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d840-119">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="6d840-119">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="6d840-120">有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md) **\]** 和 **\[ 內容 \_ 控制碼 \]**。</span><span class="sxs-lookup"><span data-stu-id="6d840-120">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="6d840-121">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="6d840-121">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="6d840-122">指定零個或多個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="6d840-122">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="6d840-123">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 **\*** 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="6d840-123">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d840-124">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="6d840-124">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6d840-125">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d840-125">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="6d840-126">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="6d840-126">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6d840-127">指定適用于指定之參數類型的零或多個方向屬性、欄位屬性、使用方式屬性和指標屬性。</span><span class="sxs-lookup"><span data-stu-id="6d840-127">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="6d840-128">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="6d840-128">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="6d840-129">*內容-控制碼類型*</span><span class="sxs-lookup"><span data-stu-id="6d840-129">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="6d840-130">指定識別碼，此識別碼會指定在採用 **\[ 內容 \_ 句 \] 柄** 屬性的 [**typedef**](typedef.md)宣告中所定義的內容控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="6d840-130">Specifies the identifier that specifies the context handle type as defined in a [**typedef**](typedef.md) declaration that takes the **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="6d840-131">取消常式是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6d840-131">The rundown routine is optional.</span></span>

<span data-ttu-id="6d840-132">**Windows ServerÂ2003與 WINDOWS XP：** 單一介面可以容納序列化和非序列化的內容控制碼，在介面上啟用一種方法，以獨佔方式存取 (序列化) 的內容控制碼，而其他方法則會在共用模式中存取該內容控制碼 (非序列化) 。</span><span class="sxs-lookup"><span data-stu-id="6d840-132">**Windows ServerÂ 2003 and WindowsÂ XP:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="6d840-133">這些存取功能相當於讀取/寫入鎖定機制;使用序列化內容控制碼的方法是 (寫入器) 的專屬使用者，而使用非序列化內容控制碼的方法則是 (讀取器) 的共用使用者。</span><span class="sxs-lookup"><span data-stu-id="6d840-133">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="6d840-134">損毀或修改內容控制碼狀態的方法必須序列化。</span><span class="sxs-lookup"><span data-stu-id="6d840-134">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="6d840-135">未修改內容控制碼狀態的方法（例如直接從內容控制碼讀取的方法）可以是非序列化的。</span><span class="sxs-lookup"><span data-stu-id="6d840-135">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="6d840-136">請注意，建立方法會以隱含方式序列化。</span><span class="sxs-lookup"><span data-stu-id="6d840-136">Note that creation methods are implicitly serialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d840-137">備註</span><span class="sxs-lookup"><span data-stu-id="6d840-137">Remarks</span></span>

<span data-ttu-id="6d840-138">**\[ 內容 \_ 控制碼 \]** 屬性可以顯示為 IDL [**typedef**](typedef.md)型別屬性（attribute），做為函式傳回型別屬性（attribute），或做為參數屬性（attribute）。</span><span class="sxs-lookup"><span data-stu-id="6d840-138">The **\[context\_handle\]** attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span> <span data-ttu-id="6d840-139">當您將 **\[ 內容 \_ 控制碼 \]** 屬性套用至類型定義時，您也必須提供內容取消常式。</span><span class="sxs-lookup"><span data-stu-id="6d840-139">When you apply the **\[context\_handle\]** attribute to a type definition, you must also provide a context rundown routine.</span></span> <span data-ttu-id="6d840-140">如需詳細資訊，請參閱 [伺服器內容執行常式](/windows/desktop/Rpc/server-context-run-down-routine) 。</span><span class="sxs-lookup"><span data-stu-id="6d840-140">See [Server Context Run-down Routine](/windows/desktop/Rpc/server-context-run-down-routine) for details.</span></span>

<span data-ttu-id="6d840-141">當您在預設情況下使用 MIDL 編譯器 ([**/ms \_ Ext**](-ms-ext.md)) 模式時，只要符合此處所述的內容控制碼需求，內容控制碼就可以是使用者選取的任何指標類型。</span><span class="sxs-lookup"><span data-stu-id="6d840-141">When you use the MIDL compiler in default ([**/ms\_ext**](-ms-ext.md)) mode, a context handle can be any pointer type selected by the user, as long as it complies with the requirements for context handles described here.</span></span> <span data-ttu-id="6d840-142">與這類內容控制碼類型相關聯的資料，不會在網路上傳輸，因此應該只由伺服器應用程式操作。</span><span class="sxs-lookup"><span data-stu-id="6d840-142">The data associated with such a context handle type is not transmitted on the network and should only be manipulated by the server application.</span></span> <span data-ttu-id="6d840-143">DCE IDL 編譯器會將內容控制碼限制為 [**void**](void.md)類型的指標 **\*** 。</span><span class="sxs-lookup"><span data-stu-id="6d840-143">DCE IDL compilers restrict context handles to pointers of type [**void**](void.md) **\***.</span></span> <span data-ttu-id="6d840-144">因此，當您使用 MIDL 編譯器 [**/osf**](-osf.md) 參數時，就無法使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="6d840-144">Therefore this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="6d840-145">如同其他控制碼類型，內容控制碼對用戶端應用程式而言是不透明的，而且不會傳送任何與其相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="6d840-145">As with other handle types, the context handle is opaque to the client application, and any data associated with it is not transmitted.</span></span> <span data-ttu-id="6d840-146">在伺服器上，內容控制碼可作為作用中內容上的控制碼，並可存取與內容控制碼類型相關聯的所有資料。</span><span class="sxs-lookup"><span data-stu-id="6d840-146">On the server, the context handle serves as a handle on active context, and all data associated with the context handle type is accessible.</span></span>

<span data-ttu-id="6d840-147">若要建立內容控制碼，用戶端會將 **\[** [](out-idl.md) **\]** 內容控制碼的 out、 **\[** [**ref**](ref.md) **\]** 指標傳遞給伺服器。</span><span class="sxs-lookup"><span data-stu-id="6d840-147">To create a context handle, the client passes to the server an **\[**[**out**](out-idl.md)**\]**, **\[**[**ref**](ref.md)**\]** pointer to a context handle.</span></span> <span data-ttu-id="6d840-148"> (內容控制碼本身可以有 **null** 或非 **null** 的值，只要其值與指標屬性一致。</span><span class="sxs-lookup"><span data-stu-id="6d840-148">(The context handle itself can have a **NULL** or non-**NULL** value—as long as its value is consistent with its pointer attributes.</span></span> <span data-ttu-id="6d840-149">例如，當內容控制碼類型套用 **\[** [**ref**](ref.md) **\]** 屬性時，它不能有 **Null** 值。 ) 必須提供另一個系結控制碼才能完成系結，直到建立內容控制碼為止。</span><span class="sxs-lookup"><span data-stu-id="6d840-149">For example, when the context handle type has the **\[**[**ref**](ref.md)**\]** attribute applied to it, it cannot have a **NULL** value.) Another binding handle must be supplied to accomplish the binding until the context handle is created.</span></span> <span data-ttu-id="6d840-150">如果未指定明確的控制碼，則會使用隱含系結。</span><span class="sxs-lookup"><span data-stu-id="6d840-150">When no explicit handle is specified, implicit binding is used.</span></span> <span data-ttu-id="6d840-151">當沒有 **\[** [**隱含 \_ 控制碼**](implicit-handle.md) **\]** 屬性存在時，就會使用自動控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d840-151">When no **\[**[**implicit\_handle**](implicit-handle.md)**\]** attribute is present, an auto handle is used.</span></span>

<span data-ttu-id="6d840-152">伺服器上的遠端程式會建立活動內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d840-152">The remote procedure on the server creates an active context handle.</span></span> <span data-ttu-id="6d840-153">用戶端必須在後續呼叫中使用該內容控制碼做為 **\[** [**in**](in.md) **\]** 或 **\[ in**、 **out \]** 參數。</span><span class="sxs-lookup"><span data-stu-id="6d840-153">The client must use that context handle as an **\[**[**in**](in.md)**\]** or **\[in**, **out\]** parameter in subsequent calls.</span></span> <span data-ttu-id="6d840-154">僅供使用的內容控制碼可作為系結控制碼，因此它必須有非 **Null** 的值。 **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="6d840-154">An **\[in\]**-only context handle can be used as a binding handle, so it must have a non-**NULL** value.</span></span> <span data-ttu-id="6d840-155">僅限 **\[ 內 \]** 的內容控制碼不會反映伺服器上的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="6d840-155">An **\[in\]**-only context handle does not reflect state changes on the server.</span></span>

<span data-ttu-id="6d840-156">在伺服器上，呼叫的程式可以視需要解讀內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d840-156">On the server, the called procedure can interpret the context handle as needed.</span></span> <span data-ttu-id="6d840-157">例如，呼叫的程式可以配置堆積儲存體，並使用內容控制碼作為此儲存體的指標。</span><span class="sxs-lookup"><span data-stu-id="6d840-157">For example, the called procedure can allocate heap storage and use the context handle as a pointer to this storage.</span></span>

<span data-ttu-id="6d840-158">為了關閉內容控制碼，用戶端會以 **\[** [**in**](in.md) **\]** 、 **\[** [**out**](out-idl.md) **\]** 引數傳遞內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d840-158">To close a context handle, the client passes the context handle as an **\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]** argument.</span></span> <span data-ttu-id="6d840-159">當伺服器不再代表呼叫端維護內容時，伺服器必須傳回 **Null** 內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d840-159">The server must return a **NULL** context handle when it is no longer maintaining context on behalf of the caller.</span></span> <span data-ttu-id="6d840-160">例如，如果內容控制碼代表開啟的檔案，而呼叫關閉檔案，則伺服器必須將內容控制碼設為 **Null** ，然後將它傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="6d840-160">For example, if the context handle represents an open file and the call closes the file, the server must set the context handle to **NULL** and return it to the client.</span></span> <span data-ttu-id="6d840-161">**Null** 值在後續呼叫上是不正確系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d840-161">A **NULL** value is invalid as a binding handle on subsequent calls.</span></span>

<span data-ttu-id="6d840-162">內容控制碼只對一部伺服器有效。</span><span class="sxs-lookup"><span data-stu-id="6d840-162">A context handle is only valid for one server.</span></span> <span data-ttu-id="6d840-163">當函數有兩個控制碼參數，且內容控制碼不是 **Null** 時，系結控制碼必須參考相同的位址空間。</span><span class="sxs-lookup"><span data-stu-id="6d840-163">When a function has two handle parameters and the context handle is not **NULL**, the binding handles must refer to the same address space.</span></span>

<span data-ttu-id="6d840-164">當函式具有 **\[** [**in**](in.md) **\]** 或 **\[ in**、 **\] out** 內容控制碼時，其內容控制碼可以當做系結控制碼使用。</span><span class="sxs-lookup"><span data-stu-id="6d840-164">When a function has an **\[**[**in**](in.md)**\]** or an **\[in**, **out\]** context handle, its context handle can be used as the binding handle.</span></span> <span data-ttu-id="6d840-165">在此情況下，不會使用隱含系結，而且 **\[** 會忽略 [**隱含 \_ 控制碼**](implicit-handle.md) **\]** 或 **\[** [**自動 \_ 控制碼**](auto-handle.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6d840-165">In this case, implicit binding is not used and the **\[**[**implicit\_handle**](implicit-handle.md)**\]** or **\[**[**auto\_handle**](auto-handle.md)**\]** attribute is ignored.</span></span>

<span data-ttu-id="6d840-166">下列限制適用于內容控制碼：</span><span class="sxs-lookup"><span data-stu-id="6d840-166">The following restrictions apply to context handles:</span></span>

-   <span data-ttu-id="6d840-167">內容控制碼不可以是陣列元素、結構成員或等位成員。</span><span class="sxs-lookup"><span data-stu-id="6d840-167">Context handles cannot be array elements, structure members, or union members.</span></span> <span data-ttu-id="6d840-168">它們只能是參數。</span><span class="sxs-lookup"><span data-stu-id="6d840-168">They can only be parameters.</span></span>
-   <span data-ttu-id="6d840-169">內容控制碼不能將 **\[** [**傳輸 \_ as**](transmit-as.md) **\]** 或 **\[** [**表示 \_ 為**](represent-as.md) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6d840-169">Context handles cannot have the **\[**[**transmit\_as**](transmit-as.md)**\]** or **\[**[**represent\_as**](represent-as.md)**\]** attribute.</span></span>
-   <span data-ttu-id="6d840-170">指向 **\[** [](out-idl.md) **\]** 內容控制碼指標的參數必須是 **\[** [**ref**](ref.md) **\]** 指標。</span><span class="sxs-lookup"><span data-stu-id="6d840-170">Parameters that are pointers to **\[**[**out**](out-idl.md)**\]** context handles must be **\[**[**ref**](ref.md)**\]** pointers.</span></span>
-   <span data-ttu-id="6d840-171">**\[**[**在**](in.md) **\]** 內容控制碼中，可以當做系結控制碼使用，且不能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6d840-171">An **\[**[**in**](in.md)**\]** context handle can be used as the binding handle and cannot be **NULL**.</span></span>
-   <span data-ttu-id="6d840-172">在輸入時， **\[ in**、 [**out**](out-idl.md)內容控制碼可以是 **Null** ，但只有在程式有另一個明確的控制碼參數時。</span><span class="sxs-lookup"><span data-stu-id="6d840-172">An **\[in**, [**out**](out-idl.md) context handle can be **NULL** on input, but only if the procedure has another explicit handle parameter.</span></span> <span data-ttu-id="6d840-173">如果沒有其他明確的非 **Null** 內容控制碼參數， **\[ in**、 **out \]** 內容控制碼不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6d840-173">If there are no other explicit non-**NULL** context handle parameters, the **\[in**, **out\]** context handle cannot be **NULL**.</span></span>
-   <span data-ttu-id="6d840-174">內容控制碼無法與回呼一起使用。</span><span class="sxs-lookup"><span data-stu-id="6d840-174">A context handle cannot be used with callbacks.</span></span>

## <a name="examples"></a><span data-ttu-id="6d840-175">範例</span><span class="sxs-lookup"><span data-stu-id="6d840-175">Examples</span></span>

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a><span data-ttu-id="6d840-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d840-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d840-177">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="6d840-177">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="6d840-178">**自動 \_ 處理**</span><span class="sxs-lookup"><span data-stu-id="6d840-178">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="6d840-179">**回撥**</span><span class="sxs-lookup"><span data-stu-id="6d840-179">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="6d840-180">用戶端內容重設</span><span class="sxs-lookup"><span data-stu-id="6d840-180">Client Context Reset</span></span>](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[<span data-ttu-id="6d840-181">**const**</span><span class="sxs-lookup"><span data-stu-id="6d840-181">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="6d840-182">內容控制碼</span><span class="sxs-lookup"><span data-stu-id="6d840-182">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="6d840-183">**處理**</span><span class="sxs-lookup"><span data-stu-id="6d840-183">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="6d840-184">系結和控制碼</span><span class="sxs-lookup"><span data-stu-id="6d840-184">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="6d840-185">**忽略**</span><span class="sxs-lookup"><span data-stu-id="6d840-185">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="6d840-186">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="6d840-186">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="6d840-187">**在**</span><span class="sxs-lookup"><span data-stu-id="6d840-187">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="6d840-188">**當地**</span><span class="sxs-lookup"><span data-stu-id="6d840-188">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="6d840-189">多執行緒用戶端和內容控制碼</span><span class="sxs-lookup"><span data-stu-id="6d840-189">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="6d840-190">**/ms \_ ext**</span><span class="sxs-lookup"><span data-stu-id="6d840-190">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="6d840-191">**擴展**</span><span class="sxs-lookup"><span data-stu-id="6d840-191">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="6d840-192">**ptr**</span><span class="sxs-lookup"><span data-stu-id="6d840-192">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="6d840-193">**ref**</span><span class="sxs-lookup"><span data-stu-id="6d840-193">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="6d840-194">**表示 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="6d840-194">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="6d840-195">**RpcSsDestroyClientCoNtext**</span><span class="sxs-lookup"><span data-stu-id="6d840-195">**RpcSsDestroyClientContext**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[<span data-ttu-id="6d840-196">伺服器內容執行例行常式</span><span class="sxs-lookup"><span data-stu-id="6d840-196">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="6d840-197">**字串**</span><span class="sxs-lookup"><span data-stu-id="6d840-197">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="6d840-198">**傳輸 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="6d840-198">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="6d840-199">**著**</span><span class="sxs-lookup"><span data-stu-id="6d840-199">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="6d840-200">**獨特**</span><span class="sxs-lookup"><span data-stu-id="6d840-200">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="6d840-201">**void**</span><span class="sxs-lookup"><span data-stu-id="6d840-201">**void**</span></span>](void.md)
</dt> </dl>

 

 