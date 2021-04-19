---
title: float 屬性
description: Float 關鍵字會指定32位浮點數。
ms.assetid: dfc94378-13a4-4d34-a254-7ff68f4f9d40
keywords:
- float 屬性 MIDL
topic_type:
- apiref
api_name:
- float
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82d298506c5117c0643df8ecea841832d5f923
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106976330"
---
# <a name="float-attribute"></a><span data-ttu-id="db4ab-104">float 屬性</span><span class="sxs-lookup"><span data-stu-id="db4ab-104">float attribute</span></span>

<span data-ttu-id="db4ab-105">**Float** 關鍵字會指定32位浮點數。</span><span class="sxs-lookup"><span data-stu-id="db4ab-105">The **float** keyword designates a 32-bit floating-point number.</span></span>

``` syntax
float identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="db4ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="db4ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db4ab-107">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="db4ab-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="db4ab-108">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="db4ab-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="db4ab-109">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="db4ab-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db4ab-110">備註</span><span class="sxs-lookup"><span data-stu-id="db4ab-110">Remarks</span></span>

<span data-ttu-id="db4ab-111">**Float** 類型是介面定義語言 (IDL) 的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="db4ab-111">The **float** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="db4ab-112">**Float** 型別可以在 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範和參數類型指定名稱) 。</span><span class="sxs-lookup"><span data-stu-id="db4ab-112">The **float** type can appear as a type specifier in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="db4ab-113">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="db4ab-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="db4ab-114">**Float** 型別不能出現在 [**const**](const.md)宣告中。</span><span class="sxs-lookup"><span data-stu-id="db4ab-114">The **float** type cannot appear in [**const**](const.md) declarations.</span></span>

## <a name="see-also"></a><span data-ttu-id="db4ab-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db4ab-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4ab-116">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="db4ab-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="db4ab-117">**double**</span><span class="sxs-lookup"><span data-stu-id="db4ab-117">**double**</span></span>](double.md)
</dt> <dt>

[<span data-ttu-id="db4ab-118"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="db4ab-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="db4ab-119">**著**</span><span class="sxs-lookup"><span data-stu-id="db4ab-119">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




