---
title: double 屬性
description: Double 關鍵字會指定64位浮點數。
ms.assetid: a235e9c5-90b3-4fa4-9154-06511abcccd0
keywords:
- double 屬性 MIDL
topic_type:
- apiref
api_name:
- double
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f14f4906de9e843c9413411c9d45ba927cc40ee4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507629"
---
# <a name="double-attribute"></a><span data-ttu-id="3c77d-104">double 屬性</span><span class="sxs-lookup"><span data-stu-id="3c77d-104">double attribute</span></span>

<span data-ttu-id="3c77d-105">**Double** 關鍵字會指定64位浮點數。</span><span class="sxs-lookup"><span data-stu-id="3c77d-105">The **double** keyword designates a 64-bit floating-point number.</span></span>

``` syntax
double identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="3c77d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c77d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c77d-107">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="3c77d-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3c77d-108">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c77d-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="3c77d-109">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="3c77d-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c77d-110">備註</span><span class="sxs-lookup"><span data-stu-id="3c77d-110">Remarks</span></span>

<span data-ttu-id="3c77d-111">**Double** 類型是介面定義語言 (IDL) 的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="3c77d-111">The **double** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="3c77d-112">這個型別可以在 [**typedef**](typedef.md) 宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型規範。</span><span class="sxs-lookup"><span data-stu-id="3c77d-112">This type can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="3c77d-113">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="3c77d-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="3c77d-114">**Double** 型別不能出現在 [**const**](const.md)宣告中。</span><span class="sxs-lookup"><span data-stu-id="3c77d-114">The **double** type cannot appear in [**const**](const.md) declarations.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c77d-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c77d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c77d-116">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="3c77d-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="3c77d-117">**const**</span><span class="sxs-lookup"><span data-stu-id="3c77d-117">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="3c77d-118">**浮動**</span><span class="sxs-lookup"><span data-stu-id="3c77d-118">**float**</span></span>](float.md)
</dt> <dt>

[<span data-ttu-id="3c77d-119"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="3c77d-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3c77d-120">**著**</span><span class="sxs-lookup"><span data-stu-id="3c77d-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




