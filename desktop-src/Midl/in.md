---
title: in 屬性
description: '\ In \ 屬性工作表示參數要從呼叫程式傳遞至呼叫的程式。'
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- 在屬性 MIDL 中
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682274"
---
# <a name="in-attribute"></a><span data-ttu-id="1ad93-104">in 屬性</span><span class="sxs-lookup"><span data-stu-id="1ad93-104">in attribute</span></span>

<span data-ttu-id="1ad93-105">**\[ In \]** 屬性工作表示要將參數從呼叫程式傳遞至被呼叫的進程。</span><span class="sxs-lookup"><span data-stu-id="1ad93-105">The **\[in\]** attribute indicates that a parameter is to be passed from the calling procedure to the called procedure.</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="1ad93-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ad93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ad93-107">*函數-屬性清單*</span><span class="sxs-lookup"><span data-stu-id="1ad93-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad93-108">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="1ad93-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="1ad93-109">有效的函式屬性為 **\[ 回呼 \]**、 **\[ local \]**、指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**，以及使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**。</span><span class="sxs-lookup"><span data-stu-id="1ad93-109">Valid function attributes are **\[callback\]**, **\[local\]**, the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**, and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="1ad93-110">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="1ad93-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad93-111">指定 **基底 \_ 類型**、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ad93-111">Specifies a **base\_type**, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="1ad93-112">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="1ad93-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="1ad93-113">*指標宣告子*</span><span class="sxs-lookup"><span data-stu-id="1ad93-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad93-114">指定零個或多個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="1ad93-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="1ad93-115">指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="1ad93-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ad93-116">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="1ad93-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad93-117">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ad93-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="1ad93-118">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="1ad93-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad93-119">指定適用于指定之參數類型的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="1ad93-119">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="1ad93-120">具有 **\[ \] in** 屬性的參數屬性也可以取得 **\[ \] 方向屬性，** **\[ 第一個 \_ \]** **\[ \]** **\[ \]** **\[ \_ \]** 欄位屬性 **\[ \_ \]\*\*\*\*是、 \[ \]** last、length、 **\[ max \_ 、size 是和 switch type、指標屬性 ref、unique 或 ptr，以及 usage 屬性內容控制碼和字串。 \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="1ad93-120">Parameter attributes with the **\[in\]** attribute can also take the directional attribute **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]** and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="1ad93-121">Usage 屬性 **\[ ignore \]** 不能用來做為參數屬性。</span><span class="sxs-lookup"><span data-stu-id="1ad93-121">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="1ad93-122">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="1ad93-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="1ad93-123">*符中*</span><span class="sxs-lookup"><span data-stu-id="1ad93-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="1ad93-124">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="1ad93-124">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="1ad93-125">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="1ad93-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="1ad93-126">函式宣告子中的參數宣告子（例如參數名稱）是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="1ad93-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ad93-127">備註</span><span class="sxs-lookup"><span data-stu-id="1ad93-127">Remarks</span></span>

<span data-ttu-id="1ad93-128">**\[ In \]** 屬性（attribute）具有反向屬性（attribute），表示要從呼叫的程式將 **\[** [](out-idl.md) **\]** 參數傳回給呼叫的進程。</span><span class="sxs-lookup"><span data-stu-id="1ad93-128">The **\[in\]** attribute has a converse attribute, **\[**[**out**](out-idl.md)**\]**, which indicates that a parameter is to be returned from the called procedure to the calling procedure.</span></span> <span data-ttu-id="1ad93-129">**\[ In \]** 和 **\[ out \]** 屬性稱為方向性參數屬性，因為它們會指定傳遞參數的方向。</span><span class="sxs-lookup"><span data-stu-id="1ad93-129">The **\[in\]** and **\[out\]** attributes are known as directional parameter attributes because they specify the direction in which parameters are passed.</span></span> <span data-ttu-id="1ad93-130">參數可以定義為 **\[ in \]**、 **\[ out \]** 或 **\[ in**、 **out \]**。</span><span class="sxs-lookup"><span data-stu-id="1ad93-130">A parameter can be defined as **\[in\]**, **\[out\]**, or **\[in**, **out\]**.</span></span>

<span data-ttu-id="1ad93-131">**\[ In \]** 屬性會識別由用戶端存根封送處理至伺服器的參數。</span><span class="sxs-lookup"><span data-stu-id="1ad93-131">The **\[in\]** attribute identifies parameters that are marshaled by the client stub for transmission to the server.</span></span>

<span data-ttu-id="1ad93-132">當未指定方向參數屬性時，預設會將 **\[ in \]** 屬性套用至參數。</span><span class="sxs-lookup"><span data-stu-id="1ad93-132">The **\[in\]** attribute is applied to a parameter by default when no directional parameter attribute is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="1ad93-133">範例</span><span class="sxs-lookup"><span data-stu-id="1ad93-133">Examples</span></span>

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a><span data-ttu-id="1ad93-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ad93-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad93-135"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="1ad93-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="1ad93-136">**midl \_ 使用者 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="1ad93-136">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="1ad93-137">**擴展**</span><span class="sxs-lookup"><span data-stu-id="1ad93-137">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 