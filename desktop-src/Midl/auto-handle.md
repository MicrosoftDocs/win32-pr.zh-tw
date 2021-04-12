---
title: auto_handle 屬性
description: '\ Auto \_ handle \ ACF 屬性會指示存根自動為沒有明確系結控制碼參數的函式建立系結。請注意，此屬性已淘汰，不再支援。'
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle 屬性 MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462541"
---
# <a name="auto_handle-attribute"></a><span data-ttu-id="d0fb4-104">自動 \_ 處理屬性</span><span class="sxs-lookup"><span data-stu-id="d0fb4-104">auto\_handle attribute</span></span>

<span data-ttu-id="d0fb4-105">**\[ Auto \_ handle \]** ACF 屬性會指示存根自動建立沒有明確系結控制碼參數之函式的系結。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-105">The **\[auto\_handle\]** ACF attribute directs the stub to automatically establish the binding for a function that does not have an explicit binding-handle parameter.</span></span>

> [!Note]  
> <span data-ttu-id="d0fb4-106">這個屬性已淘汰，不再支援。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-106">This attribute is obsolete and no longer supported.</span></span> <span data-ttu-id="d0fb4-107">建議使用 [**/robust**](-robust.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-107">Use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="d0fb4-108">參數</span><span class="sxs-lookup"><span data-stu-id="d0fb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0fb4-109">*介面屬性清單*</span><span class="sxs-lookup"><span data-stu-id="d0fb4-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d0fb4-110">指定套用至整個介面的零或多個屬性，例如程式 [**代碼**](code.md) 或 [**了 nocode**](nocode.md)。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-110">Specifies zero or more attributes that apply to the interface as a whole, such as [**code**](code.md) or [**nocode**](nocode.md).</span></span> <span data-ttu-id="d0fb4-111">以逗號分隔介面屬性。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-111">Separate interface attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d0fb4-112">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="d0fb4-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d0fb4-113">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d0fb4-114">*介面定義*</span><span class="sxs-lookup"><span data-stu-id="d0fb4-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="d0fb4-115">指定組成介面定義的 IDL 語句。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-115">Specifies IDL statements that form the definition of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0fb4-116">備註</span><span class="sxs-lookup"><span data-stu-id="d0fb4-116">Remarks</span></span>

<span data-ttu-id="d0fb4-117">**\[ Auto \_ 控制碼 \]** 屬性會出現在 ACF 的介面標頭中。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-117">The **\[auto\_handle\]** attribute appears in the interface header of the ACF.</span></span> <span data-ttu-id="d0fb4-118">當您指定 MIDL 編譯器參數 [**/app \_**](-app-config.md)設定時，它也會出現在 IDL 檔案的介面標頭中。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-118">It also appears in the interface header of the IDL file when you specify the MIDL compiler switch [**/app\_config**](-app-config.md).</span></span>

<span data-ttu-id="d0fb4-119">當用戶端呼叫使用自動系結的函式，但不存在任何伺服器系結時，存根會自動建立系結。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-119">When the client calls a function that uses automatic binding and no binding to a server exists, the stub automatically establishes the binding.</span></span> <span data-ttu-id="d0fb4-120">系結會在使用自動系結之介面中的其他函式的後續呼叫中重複使用。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-120">The binding is reused for subsequent calls to other functions in the interface that use automatic binding.</span></span> <span data-ttu-id="d0fb4-121">用戶端應用程式不需要宣告或執行任何與系結控制碼相關的處理。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-121">The client application program does not have to declare or perform any processing relating to the binding handle.</span></span>

<span data-ttu-id="d0fb4-122">當 ACF 不存在或未包含 [**\[ 隱含 \_ 控制碼 \]**](implicit-handle.md)屬性時，MIDL 編譯器會使用 **\[ 自動 \_ 處理 \]** ，併發出參考用訊息。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-122">When the ACF is not present or does not include the [**\[implicit\_handle\]**](implicit-handle.md) attribute, the MIDL compiler uses **\[auto\_handle\]** and issues an informational message.</span></span> <span data-ttu-id="d0fb4-123">如果有需要，MIDL 編譯器也會使用 **\[ auto \_ 控制碼 \]** 來建立 [**\[ 內容 \_ 控制碼 \]**](context-handle.md)的初始系結。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-123">The MIDL compiler also uses **\[auto\_handle\]**, if needed, to establish the initial binding for a [**\[context\_handle\]**](context-handle.md).</span></span>

<span data-ttu-id="d0fb4-124">只有在未發生 [**\[ 隱含 \_ 控制碼 \]**](implicit-handle.md)或 [**\[ 明確 \_ 控制碼 \]**](explicit-handle.md)屬性時，才會發生 **\[ auto \_ 控制碼 \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-124">The **\[auto\_handle\]** attribute can occur only if the [**\[implicit\_handle\]**](implicit-handle.md) or [**\[explicit\_handle\]**](explicit-handle.md) attribute does not occur.</span></span> <span data-ttu-id="d0fb4-125">**\[ 自動 \_ 控制碼 \]** 屬性可以出現在 ACF 或 IDL 介面標頭中最多一次。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-125">The **\[auto\_handle\]** attribute can occur in the ACF or IDL interface header at most once.</span></span>

> [!Note]  
> <span data-ttu-id="d0fb4-126">您無法使用自動系結 (搭配 **\[ auto \_ handle \]** 屬性，或根據預設) （如果您是透過管道處理資料）。</span><span class="sxs-lookup"><span data-stu-id="d0fb4-126">You cannot use automatic binding (either with the **\[auto\_handle\]** attribute, or by default) if you are processing data through pipes.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d0fb4-127">範例</span><span class="sxs-lookup"><span data-stu-id="d0fb4-127">Examples</span></span>

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a><span data-ttu-id="d0fb4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0fb4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fb4-129">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="d0fb4-129">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d0fb4-130">**/app \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="d0fb4-130">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="d0fb4-131">**代碼**</span><span class="sxs-lookup"><span data-stu-id="d0fb4-131">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="d0fb4-132">**明確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="d0fb4-132">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="d0fb4-133">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="d0fb4-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="d0fb4-134">**隱含 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="d0fb4-134">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="d0fb4-135">**了 nocode**</span><span class="sxs-lookup"><span data-stu-id="d0fb4-135">**nocode**</span></span>](nocode.md)
</dt> </dl>

 

 




