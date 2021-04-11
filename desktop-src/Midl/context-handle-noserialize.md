---
title: coNtext_handle_noserialize 屬性
description: '\ 內容 \_ 控制碼 \_ NOSERIALIZE \ ACF 屬性可保證不論應用程式的預設行為為何，都不會序列化內容控制碼。'
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- coNtext_handle_noserialize 屬性 MIDL
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681773"
---
# <a name="context_handle_noserialize-attribute"></a><span data-ttu-id="8564d-104">內容 \_ 控制碼 \_ noserialize 屬性</span><span class="sxs-lookup"><span data-stu-id="8564d-104">context\_handle\_noserialize attribute</span></span>

<span data-ttu-id="8564d-105">無論應用程式的預設行為為何， **\[ 內容 \_ 控制碼 \_ noserialize \]** ACF 屬性都保證永遠不會序列化內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="8564d-105">The **\[context\_handle\_noserialize\]** ACF attribute guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="8564d-106">參數</span><span class="sxs-lookup"><span data-stu-id="8564d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8564d-107">*類型-acf-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="8564d-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8564d-108">適用于型別的任何其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="8564d-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="8564d-109">*內容-控制碼類型*</span><span class="sxs-lookup"><span data-stu-id="8564d-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="8564d-110">指定內容控制碼類型的識別碼，如 [**typedef**](typedef.md) 宣告中所定義。</span><span class="sxs-lookup"><span data-stu-id="8564d-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="8564d-111">這是在 IDL 檔案中接收 [**\[ 內容 \_ 句 \] 柄**](context-handle.md)屬性的型別。</span><span class="sxs-lookup"><span data-stu-id="8564d-111">This is the type that receives the [**\[context\_handle\]**](context-handle.md) attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="8564d-112">*函數-acf-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="8564d-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8564d-113">適用于函數的任何其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="8564d-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="8564d-114">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="8564d-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8564d-115">IDL 檔案中所定義的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="8564d-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="8564d-116">*參數-acf-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="8564d-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8564d-117">適用于參數的任何其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="8564d-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8564d-118">*參數名稱*</span><span class="sxs-lookup"><span data-stu-id="8564d-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8564d-119">在 IDL 檔案中定義之參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="8564d-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8564d-120">備註</span><span class="sxs-lookup"><span data-stu-id="8564d-120">Remarks</span></span>

<span data-ttu-id="8564d-121">[**\[ 內容 \_ 控制碼 \]**](context-handle.md)屬性會識別在遠端程序呼叫之間，維護伺服器上內容或狀態資訊的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="8564d-121">The [**\[context\_handle\]**](context-handle.md) attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span> <span data-ttu-id="8564d-122">屬性可以顯示為 IDL [**typedef**](typedef.md) 型別屬性（attribute）、函數傳回型別屬性（attribute），或做為參數屬性（attribute）。</span><span class="sxs-lookup"><span data-stu-id="8564d-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="8564d-123">依預設，會序列化對內容控制碼的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8564d-123">By default, calls on context handles are serialized.</span></span> <span data-ttu-id="8564d-124">應用程式可以呼叫 [**RpcSsDontSerializeCoNtext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) 來覆寫此預設行為。</span><span class="sxs-lookup"><span data-stu-id="8564d-124">An application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="8564d-125">使用 ACF 檔中的 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)屬性可保證不會序列化這個特定內容控制碼上的呼叫，不論呼叫應用程式的行為為何。</span><span class="sxs-lookup"><span data-stu-id="8564d-125">Using the [**\[context\_handle\]**](context-handle.md) attribute in an ACF file guarantees that calls on this particular context handle will not be serialized, regardless of the calling application's behavior.</span></span> <span data-ttu-id="8564d-126">提供內容取消常式是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8564d-126">Providing a context rundown routine is optional.</span></span>

<span data-ttu-id="8564d-127">這個屬性可在 MIDL 5.0 版中使用。</span><span class="sxs-lookup"><span data-stu-id="8564d-127">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="8564d-128">**Windows ServerÂ2003與 WINDOWS XP 或更新版本：** 單一介面可以容納序列化和非序列化的內容控制碼，在介面上啟用一種方法，以獨佔方式存取 (序列化) 的內容控制碼，而其他方法則會在共用模式中存取該內容控制碼 (非序列化) 。</span><span class="sxs-lookup"><span data-stu-id="8564d-128">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="8564d-129">這些存取功能相當於讀取/寫入鎖定機制;使用序列化內容控制碼的方法是 (寫入器) 的專屬使用者，而使用非序列化內容控制碼的方法則是 (讀取器) 的共用使用者。</span><span class="sxs-lookup"><span data-stu-id="8564d-129">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="8564d-130">損毀或修改內容控制碼狀態的方法必須序列化。</span><span class="sxs-lookup"><span data-stu-id="8564d-130">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="8564d-131">未修改內容控制碼狀態的方法（例如直接從內容控制碼讀取的方法）可以是非序列化的。</span><span class="sxs-lookup"><span data-stu-id="8564d-131">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="8564d-132">請注意，建立方法會以隱含方式序列化。</span><span class="sxs-lookup"><span data-stu-id="8564d-132">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="8564d-133">範例</span><span class="sxs-lookup"><span data-stu-id="8564d-133">Examples</span></span>

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="8564d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8564d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8564d-135">ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="8564d-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="8564d-136">**內容 \_ 控制碼 \_ 序列化**</span><span class="sxs-lookup"><span data-stu-id="8564d-136">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="8564d-137">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="8564d-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="8564d-138">內容控制碼</span><span class="sxs-lookup"><span data-stu-id="8564d-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="8564d-139">**RpcSsDontSerializeCoNtext**</span><span class="sxs-lookup"><span data-stu-id="8564d-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="8564d-140">伺服器內容執行例行常式</span><span class="sxs-lookup"><span data-stu-id="8564d-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="8564d-141">多執行緒用戶端和內容控制碼</span><span class="sxs-lookup"><span data-stu-id="8564d-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="8564d-142">**著**</span><span class="sxs-lookup"><span data-stu-id="8564d-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 