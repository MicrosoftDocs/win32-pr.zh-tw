---
title: 布林值屬性
description: 關鍵字布林值表示與識別碼相關聯的運算式或常數運算式只接受值 TRUE 和 FALSE。
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- 布林屬性 MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373165"
---
# <a name="boolean-attribute"></a><span data-ttu-id="8af8d-104">布林值屬性</span><span class="sxs-lookup"><span data-stu-id="8af8d-104">boolean attribute</span></span>

<span data-ttu-id="8af8d-105">關鍵字 **布林值** 表示與識別碼相關聯的運算式或常數運算式只接受值 **TRUE** 和 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8af8d-105">The keyword **boolean** indicates that the expression or constant expression associated with the identifier takes only the values **TRUE** and **FALSE**.</span></span>

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="8af8d-106">參數</span><span class="sxs-lookup"><span data-stu-id="8af8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af8d-107">*識別碼-名稱*</span><span class="sxs-lookup"><span data-stu-id="8af8d-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8af8d-108">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8af8d-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="8af8d-109">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="8af8d-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8af8d-110">備註</span><span class="sxs-lookup"><span data-stu-id="8af8d-110">Remarks</span></span>

<span data-ttu-id="8af8d-111">**布林值** 型別是 IDL 語言的其中一種基底類型。</span><span class="sxs-lookup"><span data-stu-id="8af8d-111">The **boolean** type is one of the base types of the IDL language.</span></span> <span data-ttu-id="8af8d-112">**布林值** 型別可以在 [**const**](const.md)宣告、 [**typedef**](typedef.md)宣告、一般宣告和函式宣告子中顯示為類型指定名稱， (為函式傳回型別規範，以及) 的參數類型指定名稱。</span><span class="sxs-lookup"><span data-stu-id="8af8d-112">The **boolean** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="8af8d-113">如需類型規範出現的內容，請參閱 [ (IDL) 檔案的介面定義](interface-definition-idl-file.md)。</span><span class="sxs-lookup"><span data-stu-id="8af8d-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="8af8d-114">**布林值** 基底類型與 [**oleautomation**](oleautomation.md)屬性不相容。</span><span class="sxs-lookup"><span data-stu-id="8af8d-114">The **boolean** base type is not compatible with the [**oleautomation**](oleautomation.md) attribute.</span></span> <span data-ttu-id="8af8d-115">\_在您的自動化相容介面中使用 VARIANT BOOL。</span><span class="sxs-lookup"><span data-stu-id="8af8d-115">Use VARIANT\_BOOL in your Automation-compatible interfaces.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8af8d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8af8d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af8d-117">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="8af8d-117">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="8af8d-118">**const**</span><span class="sxs-lookup"><span data-stu-id="8af8d-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="8af8d-119"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="8af8d-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8af8d-120">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="8af8d-120">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="8af8d-121">**著**</span><span class="sxs-lookup"><span data-stu-id="8af8d-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




