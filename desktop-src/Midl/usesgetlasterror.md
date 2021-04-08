---
title: usesgetlasterror 屬性
description: '\ Usesgetlasterror \ 屬性工作表示呼叫端可以呼叫 GetLastError 來取得錯誤碼。'
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- usesgetlasterror 屬性 MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681817"
---
# <a name="usesgetlasterror-attribute"></a><span data-ttu-id="2c443-104">usesgetlasterror 屬性</span><span class="sxs-lookup"><span data-stu-id="2c443-104">usesgetlasterror attribute</span></span>

<span data-ttu-id="2c443-105">**\[ Usesgetlasterror \]** 屬性會向呼叫端發出信號，告知呼叫端可以呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)來取得錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c443-105">The **\[usesgetlasterror\]** attribute signals the caller that it can call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a><span data-ttu-id="2c443-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c443-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c443-107">*模組屬性*</span><span class="sxs-lookup"><span data-stu-id="2c443-107">*module-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="2c443-108">將套用至 [**模組**](module.md)的零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="2c443-108">Zero or more MIDL attributes that will be applied to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c443-109">*模組名稱*</span><span class="sxs-lookup"><span data-stu-id="2c443-109">*module-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2c443-110">[**模組**](module.md)的識別碼名稱。</span><span class="sxs-lookup"><span data-stu-id="2c443-110">The identifier name of the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c443-111">*專案識別碼*</span><span class="sxs-lookup"><span data-stu-id="2c443-111">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="2c443-112">指定模組進入點–函數名稱或整數識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c443-112">Specifies the module entry point–function name or integer-identification number.</span></span>

</dd> <dt>

<span data-ttu-id="2c443-113">*其他屬性*</span><span class="sxs-lookup"><span data-stu-id="2c443-113">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="2c443-114">將套用至遠端程式的零或多個 MIDL 屬性。</span><span class="sxs-lookup"><span data-stu-id="2c443-114">Zero or more MIDL attributes that will be applied to the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="2c443-115">*傳回類型*</span><span class="sxs-lookup"><span data-stu-id="2c443-115">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2c443-116">完成時，遠端程式將會傳回的資料類型。</span><span class="sxs-lookup"><span data-stu-id="2c443-116">The type of the data that the remote procedure will return upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="2c443-117">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="2c443-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2c443-118">在 IDL 檔案中定義之遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c443-118">The name of the remote procedure as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="2c443-119">*param 清單*</span><span class="sxs-lookup"><span data-stu-id="2c443-119">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2c443-120">遠端程式的零或多個參數。</span><span class="sxs-lookup"><span data-stu-id="2c443-120">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c443-121">備註</span><span class="sxs-lookup"><span data-stu-id="2c443-121">Remarks</span></span>

<span data-ttu-id="2c443-122">**\[ Usesgetlasterror \]** 屬性可以在模組進入點上設定，如果該進入點使用 Windows 函數 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c443-122">The **\[usesgetlasterror\]** attribute can be set on a module entry point, if that entry point uses the Windows function [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return error codes.</span></span> <span data-ttu-id="2c443-123">屬性會告知呼叫端，如果呼叫該函式時發生錯誤，呼叫端可以呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 來取得錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c443-123">The attribute tells the caller that, if there is an error when calling that function, the caller can then call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

## <a name="examples"></a><span data-ttu-id="2c443-124">範例</span><span class="sxs-lookup"><span data-stu-id="2c443-124">Examples</span></span>

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="2c443-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c443-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c443-126">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2c443-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="2c443-127">ODL 檔案範例</span><span class="sxs-lookup"><span data-stu-id="2c443-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="2c443-128">ODL 檔語法</span><span class="sxs-lookup"><span data-stu-id="2c443-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 