---
title: /ms_union 參數
description: /Ms 聯 \_ 集參數控制 nonencapsulated 聯集的 NDR 對齊。注意：此屬性是為了回溯相容性而提供。
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union switch MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841432"
---
# <a name="ms_union-switch"></a><span data-ttu-id="9ddea-104">/ms 聯 \_ 集參數</span><span class="sxs-lookup"><span data-stu-id="9ddea-104">/ms\_union switch</span></span>

<span data-ttu-id="9ddea-105">**/Ms 聯 \_ 集** 參數控制 nonencapsulated 聯集的 NDR 對齊。</span><span class="sxs-lookup"><span data-stu-id="9ddea-105">The **/ms\_union** switch controls the NDR alignment of nonencapsulated unions.</span></span>

> [!Note]  
> <span data-ttu-id="9ddea-106">這個屬性是為了回溯相容性而提供。</span><span class="sxs-lookup"><span data-stu-id="9ddea-106">This attribute is provided for backwards compatibility.</span></span> <span data-ttu-id="9ddea-107">不建議在新介面中使用。</span><span class="sxs-lookup"><span data-stu-id="9ddea-107">It is not recommended for use in a new interface.</span></span>

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a><span data-ttu-id="9ddea-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="9ddea-108">Switch Options</span></span>

<span data-ttu-id="9ddea-109">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9ddea-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ddea-110">備註</span><span class="sxs-lookup"><span data-stu-id="9ddea-110">Remarks</span></span>

<span data-ttu-id="9ddea-111">MIDL 編譯器會鏡像 nonencapsulated 聯集的憑證-DCE IDL 編譯器的行為。</span><span class="sxs-lookup"><span data-stu-id="9ddea-111">The MIDL compiler mirrors the behavior of the OSF-DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="9ddea-112">不過，因為舊版 MIDL 編譯器沒有這樣做，所以 **/ms 聯 \_ 集** 參數會提供與舊版 midl 編譯器的介面相容性。</span><span class="sxs-lookup"><span data-stu-id="9ddea-112">However, because earlier versions of the MIDL compiler did not do so, the **/ms\_union** switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="9ddea-113">Ms 聯 \_ 集功能可以用來做為命令列參數 (**/ms 聯 \_ 集**) 、IDL 介面屬性或 idl 型別屬性。</span><span class="sxs-lookup"><span data-stu-id="9ddea-113">The ms\_union feature can be used as a command-line switch (**/ms\_union**), an IDL interface attribute, or as an IDL-type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="9ddea-114">範例</span><span class="sxs-lookup"><span data-stu-id="9ddea-114">Examples</span></span>

<span data-ttu-id="9ddea-115">**midl/ms 聯 \_ 集檔案 .idl**</span><span class="sxs-lookup"><span data-stu-id="9ddea-115">**midl /ms\_union file.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="9ddea-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ddea-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ddea-117">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="9ddea-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="9ddea-118"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="9ddea-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




