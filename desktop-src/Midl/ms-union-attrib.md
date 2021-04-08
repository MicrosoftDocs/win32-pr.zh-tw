---
title: ms_union 屬性
description: 關鍵字 \ ms \_ union \ 用來控制 nonencapsulated 等位的 NDR 對齊。
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union 屬性 MIDL
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022302"
---
# <a name="ms_union-attribute"></a><span data-ttu-id="91765-104">ms 聯 \_ 集屬性</span><span class="sxs-lookup"><span data-stu-id="91765-104">ms\_union attribute</span></span>

<span data-ttu-id="91765-105">關鍵字 \[ **ms 聯 \_ 集** \] 用來控制 nonencapsulated 等位的 NDR 對齊。</span><span class="sxs-lookup"><span data-stu-id="91765-105">The keyword \[**ms\_union**\] is used to control the NDR alignment of nonencapsulated unions.</span></span>

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a><span data-ttu-id="91765-106">參數</span><span class="sxs-lookup"><span data-stu-id="91765-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91765-107">*介面-名稱*</span><span class="sxs-lookup"><span data-stu-id="91765-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91765-108">指定介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="91765-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="91765-109">*procedure 類型*</span><span class="sxs-lookup"><span data-stu-id="91765-109">*procedure-type*</span></span> 
</dt> <dd>

<span data-ttu-id="91765-110">指定要套用屬性之程式的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="91765-110">Specifies the return type of the procedure to which the attribute is being applied.</span></span>

</dd> <dt>

<span data-ttu-id="91765-111">*程式-名稱*</span><span class="sxs-lookup"><span data-stu-id="91765-111">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="91765-112">指定程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="91765-112">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="91765-113">*param 清單*</span><span class="sxs-lookup"><span data-stu-id="91765-113">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="91765-114">指定程式的參數清單，此清單可能是空的。</span><span class="sxs-lookup"><span data-stu-id="91765-114">Specifies the procedure's parameter list, which may be empty.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91765-115">備註</span><span class="sxs-lookup"><span data-stu-id="91765-115">Remarks</span></span>

<span data-ttu-id="91765-116">請勿使用這個參數或具有新介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="91765-116">Never use this switch or attribute with new interfaces.</span></span> <span data-ttu-id="91765-117">這是回溯相容性功能。這一版 Microsoft RPC 中的 MIDL 編譯器會鏡像 nonencapsulated 等位的憑證 DCE IDL 編譯器行為。</span><span class="sxs-lookup"><span data-stu-id="91765-117">This is a backward compatibility feature only.The MIDL compiler in this version of Microsoft RPC mirrors the behavior of the OSF DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="91765-118">不過，因為舊版 MIDL 編譯器沒有這樣做，所以 [**/ms 聯 \_ 集**](-ms-union.md) 參數會提供與舊版 midl 編譯器的介面相容性。</span><span class="sxs-lookup"><span data-stu-id="91765-118">However, because earlier versions of the MIDL compiler did not do so, the [**/ms\_union**](-ms-union.md) switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="91765-119">**Ms 聯 \_ 集** 功能可以當做 idl 介面屬性、idl 型別屬性，或做為命令列參數來 ( [**/ms 聯 \_ 集**](-ms-union.md)) 。</span><span class="sxs-lookup"><span data-stu-id="91765-119">The **ms\_union** feature can be used as an IDL interface attribute, an IDL type attribute, or as a command-line switch ( [**/ms\_union**](-ms-union.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="91765-120">範例</span><span class="sxs-lookup"><span data-stu-id="91765-120">Examples</span></span>

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a><span data-ttu-id="91765-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91765-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91765-122"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="91765-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="91765-123">**/ms 聯 \_ 集**</span><span class="sxs-lookup"><span data-stu-id="91765-123">**/ms\_union**</span></span>](-ms-union.md)
</dt> </dl>

 

 




