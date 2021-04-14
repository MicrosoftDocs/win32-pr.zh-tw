---
title: 回呼屬性
description: '\ 回呼 \ 屬性會宣告存在於分散式應用程式的用戶端上的靜態回呼函數。 回呼函數可讓伺服器在用戶端上執行程式碼。'
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- 回呼屬性 MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375188"
---
# <a name="callback-attribute"></a><span data-ttu-id="a6ed8-105">回呼屬性</span><span class="sxs-lookup"><span data-stu-id="a6ed8-105">callback attribute</span></span>

<span data-ttu-id="a6ed8-106">**\[ 回呼 \]** 屬性會宣告存在於分散式應用程式之用戶端的靜態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-106">The **\[callback\]** attribute declares a static callback function that exists on the client side of the distributed application.</span></span> <span data-ttu-id="a6ed8-107">回呼函數可讓伺服器在用戶端上執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-107">Callback functions provide a way for the server to execute code on the client.</span></span>

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="a6ed8-108">參數</span><span class="sxs-lookup"><span data-stu-id="a6ed8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ed8-109">*函數-attr-list*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-109">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ed8-110">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="a6ed8-111">有效的函式屬性為 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及 usage 屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**ignore**](ignore.md)和 **\]** **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-111">Valid function attributes are **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span> <span data-ttu-id="a6ed8-112">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a6ed8-113">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ed8-114">指定 [基底 \_ 類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-114">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="a6ed8-115">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="a6ed8-116">*ptr 宣告子*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-116">*ptr-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ed8-117">指定零個或多個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-117">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="a6ed8-118">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-118">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6ed8-119">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ed8-120">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-120">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a6ed8-121">*屬性清單*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-121">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ed8-122">指定適用于指定之參數類型的零或多個方向屬性、欄位屬性、使用方式屬性和指標屬性。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-122">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="a6ed8-123">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-123">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a6ed8-124">*符中*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-124">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ed8-125">指定標準的 C 宣告子，例如識別碼、指標宣告子和陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-125">Specifies a standard C declarator such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="a6ed8-126">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-126">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="a6ed8-127">參數名稱識別碼是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-127">The parameter-name identifier is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6ed8-128">備註</span><span class="sxs-lookup"><span data-stu-id="a6ed8-128">Remarks</span></span>

<span data-ttu-id="a6ed8-129">當伺服器必須從用戶端取得資訊時， **\[ 回檔 \]** 函式很有用。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-129">The **\[callback\]** function is useful when the server must obtain information from the client.</span></span> <span data-ttu-id="a6ed8-130">如果 Windows 3 支援伺服器應用程式。*x*，伺服器可以呼叫 Windows 3 上的遠端程式。*x* 伺服器以取得所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-130">If server applications were supported on Windows 3.*x*, the server could make a call to a remote procedure on the Windows 3.*x* server to obtain the needed information.</span></span> <span data-ttu-id="a6ed8-131">回呼函式會完成相同的目的，並讓伺服器查詢用戶端以取得原始呼叫內容中的資訊。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-131">The callback function accomplishes the same purpose and lets the server query the client for information in the context of the original call.</span></span>

<span data-ttu-id="a6ed8-132">回呼是在單一線程中執行之遠端呼叫的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-132">Callbacks are special cases of remote calls that execute as part of a single thread.</span></span> <span data-ttu-id="a6ed8-133">回呼是在遠端呼叫的內容中發出。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-133">A callback is issued in the context of a remote call.</span></span> <span data-ttu-id="a6ed8-134">任何定義為與靜態回呼函式相同之介面一部分的遠端程式，都可以呼叫回呼函式。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-134">Any remote procedure defined as part of the same interface as the static callback function can call the callback function.</span></span>

<span data-ttu-id="a6ed8-135">請務必注意， \[ \] 不建議在多執行緒程式設計中使用回呼。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-135">It is important to note that the use of \[callback\] is not recommended in multi-thread programming.</span></span> <span data-ttu-id="a6ed8-136">作為單一執行緒程式設計功能，它並不支援多執行緒環境所提供的安全性需求。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-136">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

<span data-ttu-id="a6ed8-137">**RpcCancelThread** 函數無法用來取消可能分派靜態回呼的呼叫。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-137">The **RpcCancelThread** function cannot be used to cancel a call that may dispatch a static callback.</span></span> <span data-ttu-id="a6ed8-138">如果特定遠端程序呼叫不會產生回呼，則可以取消。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-138">If a particular remote procedure call will never result in a callback, then it can be canceled.</span></span> <span data-ttu-id="a6ed8-139">否則，只有在可以保證呼叫的回呼尚未發出時，才能取消呼叫。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-139">Otherwise, a call can be canceled only if it can be guaranteed that a callback for it has not been issued.</span></span>

<span data-ttu-id="a6ed8-140">只有連接導向和本機通訊協定序列支援回呼屬性。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-140">Only the connection-oriented and local-protocol sequences support the callback attribute.</span></span> <span data-ttu-id="a6ed8-141">\[ \] 本機通訊協定序列的回呼資料大小限制為150個位元組。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-141">The size of the \[out\] data for callbacks over the local-protocol sequence is limited to 150 bytes.</span></span> <span data-ttu-id="a6ed8-142">如果 RPC 介面使用不需連線的 (資料包) 通訊協定順序，則對回呼屬性之程式的呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-142">If an RPC interface uses a connectionless (datagram) protocol sequence, calls to procedures with the callback attribute will fail.</span></span>

<span data-ttu-id="a6ed8-143">控制碼不能當做回呼函數中的參數使用。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-143">Handles cannot be used as parameters in callback functions.</span></span> <span data-ttu-id="a6ed8-144">由於回呼一律是在呼叫的內容中執行，因此用戶端用來對伺服器進行呼叫的系結控制碼也會當做伺服器對用戶端的系結控制碼使用。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-144">Because callbacks always execute in the context of a call, the binding handle used by the client to make the call to the server is also used as the binding handle from the server to the client.</span></span>

<span data-ttu-id="a6ed8-145">回呼可以嵌套到任何深度。</span><span class="sxs-lookup"><span data-stu-id="a6ed8-145">Callbacks can nest to any depth.</span></span>

## <a name="examples"></a><span data-ttu-id="a6ed8-146">範例</span><span class="sxs-lookup"><span data-stu-id="a6ed8-146">Examples</span></span>

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a><span data-ttu-id="a6ed8-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6ed8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ed8-148">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-148">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-149">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="a6ed8-149">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-150">**const**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-150">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-151">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-151">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-152">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-152">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-153"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="a6ed8-153">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-154">**忽略**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-154">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-155">**當地**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-155">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-156">**/osf**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-156">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-157">**ref**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-157">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-158">**ptr**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-158">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-159">**字串**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-159">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-160">**結構**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-160">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-161">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-161">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-162">**獨特**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-162">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="a6ed8-163">**RpcCancelThread**</span><span class="sxs-lookup"><span data-stu-id="a6ed8-163">**RpcCancelThread**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 