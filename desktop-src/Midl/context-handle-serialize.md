---
title: coNtext_handle_serialize 屬性
description: '\ 內容 \_ 控制碼 \_ 序列化 \ ACF 屬性可保證無論應用程式的預設行為為何，都會永遠序列化內容控制碼。'
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- coNtext_handle_serialize 屬性 MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965012"
---
# <a name="context_handle_serialize-attribute"></a><span data-ttu-id="88666-104">內容 \_ 控制碼 \_ 序列化屬性</span><span class="sxs-lookup"><span data-stu-id="88666-104">context\_handle\_serialize attribute</span></span>

<span data-ttu-id="88666-105">無論應用程式的預設行為為何， **\[ 內容 \_ 控制碼都會 \_ 序列化 \]** ACF 屬性，以保證會一律序列化內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="88666-105">The **\[context\_handle\_serialize\]** ACF attribute guarantees that a context handle will always be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="88666-106">參數</span><span class="sxs-lookup"><span data-stu-id="88666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88666-107">*類型-acf-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="88666-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="88666-108">適用于型別的任何其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="88666-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="88666-109">*內容-控制碼類型*</span><span class="sxs-lookup"><span data-stu-id="88666-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="88666-110">指定內容控制碼類型的識別碼，如 [**typedef**](typedef.md) 宣告中所定義。</span><span class="sxs-lookup"><span data-stu-id="88666-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="88666-111">這是在 IDL 檔案中接收 **\[ 內容 \_ 句 \_ 柄 \] 序列化** 屬性的型別。</span><span class="sxs-lookup"><span data-stu-id="88666-111">This is the type that receives the **\[context\_handle\_serialize\]** attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="88666-112">*函數-acf-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="88666-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="88666-113">適用于函數的任何其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="88666-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="88666-114">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="88666-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="88666-115">IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="88666-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="88666-116">*參數-acf-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="88666-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="88666-117">適用于參數的任何其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="88666-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="88666-118">*參數名稱*</span><span class="sxs-lookup"><span data-stu-id="88666-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="88666-119">在 IDL 檔案中定義之參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="88666-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88666-120">備註</span><span class="sxs-lookup"><span data-stu-id="88666-120">Remarks</span></span>

<span data-ttu-id="88666-121">**\[ 內容 \_ 控制碼 \_ 序列化 \]** 屬性可識別系結控制碼，此控制碼會在遠端程序呼叫之間，維護伺服器上的內容或狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="88666-121">The **\[context\_handle\_serialize\]** attribute identifies a binding handle that maintains context or state information on the server between remote procedure calls.</span></span> <span data-ttu-id="88666-122">屬性可以顯示為 IDL [**typedef**](typedef.md) 型別屬性（attribute）、函數傳回型別屬性（attribute），或做為參數屬性（attribute）。</span><span class="sxs-lookup"><span data-stu-id="88666-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="88666-123">依預設，會序列化對內容控制碼的呼叫，但應用程式可以呼叫 [**RpcSsDontSerializeCoNtext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) 來覆寫此預設行為。</span><span class="sxs-lookup"><span data-stu-id="88666-123">By default, calls on context handles are serialized, but an application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="88666-124">在 ACF 檔中使用 **\[ 內容 \_ 控制碼 \_ 序列化 \]** 屬性可保證將會序列化這個特定內容控制碼上的呼叫，即使呼叫的應用程式已覆寫預設序列化。</span><span class="sxs-lookup"><span data-stu-id="88666-124">Using the **\[context\_handle\_serialize\]** attribute in an ACF file guarantees that calls on this particular context handle will be serialized, even if the calling application has overridden the default serialization.</span></span> <span data-ttu-id="88666-125">內容取消常式是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="88666-125">A context rundown routine is optional.</span></span>

<span data-ttu-id="88666-126">這個屬性可在 MIDL 5.0 版中使用。</span><span class="sxs-lookup"><span data-stu-id="88666-126">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="88666-127">**Windows ServerÂ2003與 WINDOWS XP 或更新版本：** 單一介面可以容納序列化和非序列化的內容控制碼，在介面上啟用一種方法，以獨佔方式存取 (序列化) 的內容控制碼，而其他方法則會在共用模式中存取該內容控制碼 (非序列化) 。</span><span class="sxs-lookup"><span data-stu-id="88666-127">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="88666-128">這些存取功能相當於讀取/寫入鎖定機制;使用序列化內容控制碼的方法是 (寫入器) 的專屬使用者，而使用非序列化內容控制碼的方法則是 (讀取器) 的共用使用者。</span><span class="sxs-lookup"><span data-stu-id="88666-128">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="88666-129">損毀或修改內容控制碼狀態的方法必須序列化。</span><span class="sxs-lookup"><span data-stu-id="88666-129">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="88666-130">未修改內容控制碼狀態的方法（例如直接從內容控制碼讀取的方法）可以是非序列化的。</span><span class="sxs-lookup"><span data-stu-id="88666-130">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="88666-131">請注意，建立方法會以隱含方式序列化。</span><span class="sxs-lookup"><span data-stu-id="88666-131">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="88666-132">範例</span><span class="sxs-lookup"><span data-stu-id="88666-132">Examples</span></span>

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="88666-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88666-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88666-134">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="88666-134">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="88666-135">ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="88666-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="88666-136">**內容 \_ 控制碼 \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="88666-136">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="88666-137">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="88666-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="88666-138">內容控制碼</span><span class="sxs-lookup"><span data-stu-id="88666-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="88666-139">**RpcSsDontSerializeCoNtext**</span><span class="sxs-lookup"><span data-stu-id="88666-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="88666-140">伺服器內容執行例行常式</span><span class="sxs-lookup"><span data-stu-id="88666-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="88666-141">多執行緒用戶端和內容控制碼</span><span class="sxs-lookup"><span data-stu-id="88666-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="88666-142">**著**</span><span class="sxs-lookup"><span data-stu-id="88666-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 