---
title: byte 屬性
description: Byte 關鍵字會指定8位的資料項目。
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- byte 屬性 MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965827"
---
# <a name="byte-attribute"></a><span data-ttu-id="185b6-104">byte 屬性</span><span class="sxs-lookup"><span data-stu-id="185b6-104">byte attribute</span></span>

<span data-ttu-id="185b6-105">**Byte** 關鍵字會指定8位的資料項目。</span><span class="sxs-lookup"><span data-stu-id="185b6-105">The **byte** keyword specifies an 8-bit data item.</span></span>

``` syntax
byte identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="185b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="185b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="185b6-107">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="185b6-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="185b6-108">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="185b6-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="185b6-109">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="185b6-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="185b6-110">備註</span><span class="sxs-lookup"><span data-stu-id="185b6-110">Remarks</span></span>

<span data-ttu-id="185b6-111">**位元組** 資料項目不會在網路上進行傳輸，因為可能會有 [**char**](char-idl.md)類型的轉換。</span><span class="sxs-lookup"><span data-stu-id="185b6-111">A **byte** data item does not undergo any conversion for transmission on the network as a [**char**](char-idl.md) type might.</span></span>

<span data-ttu-id="185b6-112">**位元組** 類型是介面定義語言 (IDL) 的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="185b6-112">The **byte** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="185b6-113">**Byte** 類型可以做為 [**常數**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中的類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="185b6-113">The **byte** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="185b6-114">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="185b6-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="185b6-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="185b6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185b6-116">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="185b6-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="185b6-117">**字元**</span><span class="sxs-lookup"><span data-stu-id="185b6-117">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="185b6-118">**const**</span><span class="sxs-lookup"><span data-stu-id="185b6-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="185b6-119"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="185b6-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="185b6-120">**著**</span><span class="sxs-lookup"><span data-stu-id="185b6-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




