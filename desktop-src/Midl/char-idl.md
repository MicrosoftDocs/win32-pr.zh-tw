---
title: char 屬性
description: Char 關鍵字會指定8位的資料項目。
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- char 屬性 MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841476"
---
# <a name="char-attribute"></a><span data-ttu-id="be456-104">char 屬性</span><span class="sxs-lookup"><span data-stu-id="be456-104">char attribute</span></span>

<span data-ttu-id="be456-105">**Char** 關鍵字會指定8位的資料項目。</span><span class="sxs-lookup"><span data-stu-id="be456-105">The **char** keyword specifies an 8-bit data item.</span></span>

``` syntax
char identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="be456-106">參數</span><span class="sxs-lookup"><span data-stu-id="be456-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be456-107">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="be456-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="be456-108">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="be456-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="be456-109">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="be456-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be456-110">備註</span><span class="sxs-lookup"><span data-stu-id="be456-110">Remarks</span></span>

<span data-ttu-id="be456-111">關鍵字 **char** 可識別具有8個位的資料項目。</span><span class="sxs-lookup"><span data-stu-id="be456-111">The keyword **char** identifies a data item that has 8 bits.</span></span> <span data-ttu-id="be456-112">對 MIDL 編譯器而言， **char** 預設為不帶正負號，並與不帶 [**正負**](unsigned.md)號的 **char** 同義。</span><span class="sxs-lookup"><span data-stu-id="be456-112">To the MIDL compiler, a **char** is unsigned by default and is synonymous with [**unsigned**](unsigned.md) **char**.</span></span>

<span data-ttu-id="be456-113">在這個版本的 Microsoft RPC 中，ASCII 和 EBCDIC 之間的轉換字元轉譯表內建于執行時間程式庫中，使用者無法變更。</span><span class="sxs-lookup"><span data-stu-id="be456-113">In this version of Microsoft RPC, the character translation tables that convert between ASCII and EBCDIC are built into the run-time libraries and cannot be changed by the user.</span></span>

<span data-ttu-id="be456-114">**Char** 類型是介面定義語言 (IDL) 的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="be456-114">The **char** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="be456-115">**Char** 類型可以做為 [**常數**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範和) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="be456-115">The **char** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="be456-116">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="be456-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="be456-117">DCE IDL 編譯器不接受套用至 **char** 類型的關鍵字 [**簽署**](signed.md)。</span><span class="sxs-lookup"><span data-stu-id="be456-117">DCE IDL compilers do not accept the keyword [**signed**](signed.md) applied to **char** types.</span></span> <span data-ttu-id="be456-118">因此，當您使用 MIDL 編譯器 [**/osf**](-osf.md) 參數時，就無法使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="be456-118">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

## <a name="see-also"></a><span data-ttu-id="be456-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be456-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be456-120">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="be456-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="be456-121">**位元組**</span><span class="sxs-lookup"><span data-stu-id="be456-121">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="be456-122">**/char**</span><span class="sxs-lookup"><span data-stu-id="be456-122">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="be456-123">**const**</span><span class="sxs-lookup"><span data-stu-id="be456-123">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="be456-124"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="be456-124">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="be456-125">**/osf**</span><span class="sxs-lookup"><span data-stu-id="be456-125">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="be456-126">**signed**</span><span class="sxs-lookup"><span data-stu-id="be456-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="be456-127">**字串**</span><span class="sxs-lookup"><span data-stu-id="be456-127">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="be456-128">**著**</span><span class="sxs-lookup"><span data-stu-id="be456-128">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="be456-129">**符號**</span><span class="sxs-lookup"><span data-stu-id="be456-129">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="be456-130">**wchar \_ t**</span><span class="sxs-lookup"><span data-stu-id="be456-130">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




