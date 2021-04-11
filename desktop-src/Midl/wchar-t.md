---
title: wchar_t 屬性
description: Wchar \_ t 關鍵字會指定寬字元類型。
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t 屬性 MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2020
ms.locfileid: "104023134"
---
# <a name="wchar_t-attribute"></a><span data-ttu-id="b1a88-104">wchar \_ t 屬性</span><span class="sxs-lookup"><span data-stu-id="b1a88-104">wchar\_t attribute</span></span>

<span data-ttu-id="b1a88-105">**Wchar \_ t** 關鍵字會指定寬字元類型。</span><span class="sxs-lookup"><span data-stu-id="b1a88-105">The **wchar\_t** keyword designates a wide-character type.</span></span>

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="b1a88-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1a88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a88-107">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="b1a88-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b1a88-108">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1a88-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="b1a88-109">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="b1a88-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1a88-110">備註</span><span class="sxs-lookup"><span data-stu-id="b1a88-110">Remarks</span></span>

<span data-ttu-id="b1a88-111">**Wchar \_ t 型別** 是由 MIDL 定義為不 [**帶正負**](unsigned.md)號的 [**短**](short.md) (16 位) 資料物件。</span><span class="sxs-lookup"><span data-stu-id="b1a88-111">The **wchar\_t** type is defined by MIDL as an [**unsigned**](unsigned.md) [**short**](short.md) (16-bit) data object.</span></span>

<span data-ttu-id="b1a88-112">MIDL 編譯器允許重新定義 **wchar \_ t**，但只有在它與先前的定義一致時才允許。</span><span class="sxs-lookup"><span data-stu-id="b1a88-112">The MIDL compiler allows redefinition of **wchar\_t**, but only if it is consistent with the preceding definition.</span></span>

<span data-ttu-id="b1a88-113">寬字元類型是其中一種預先定義的 MIDL 類型。</span><span class="sxs-lookup"><span data-stu-id="b1a88-113">The wide-character type is one of the predefined types of MIDL.</span></span> <span data-ttu-id="b1a88-114">寬字元類型可顯示為 [**const**](const.md) 宣告、 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="b1a88-114">The wide-character type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="b1a88-115">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a88-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="b1a88-116">**\[ 字串 \]** 屬性可以套用至 **wchar \_ t** 類型的指標或陣列。</span><span class="sxs-lookup"><span data-stu-id="b1a88-116">The **\[string\]** attribute can be applied to a pointer or array of type **wchar\_t**.</span></span>

<span data-ttu-id="b1a88-117">在字元或字串常數之前使用 **L** 字元，以指定寬字元類型常數。</span><span class="sxs-lookup"><span data-stu-id="b1a88-117">Use the **L** character before a character or a string constant to designate the wide character type constant.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1a88-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1a88-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a88-119">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="b1a88-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="b1a88-120">**字元**</span><span class="sxs-lookup"><span data-stu-id="b1a88-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="b1a88-121">**const**</span><span class="sxs-lookup"><span data-stu-id="b1a88-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="b1a88-122"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="b1a88-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b1a88-123">**short**</span><span class="sxs-lookup"><span data-stu-id="b1a88-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="b1a88-124">**著**</span><span class="sxs-lookup"><span data-stu-id="b1a88-124">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="b1a88-125">**符號**</span><span class="sxs-lookup"><span data-stu-id="b1a88-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




