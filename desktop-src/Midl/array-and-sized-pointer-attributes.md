---
title: 陣列和 Sized-Pointer 屬性
description: MIDL 提供一組豐富的功能，可傳遞資料的陣列和指向資料的指標。 您可以使用這些屬性來指定陣列的特性以及多個指標層級。
ms.assetid: 482be83f-eb09-40a0-8dd6-a0cbf5dc4485
keywords:
- IDL MIDL、屬性、陣列和大小指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f9ba435d5c413ea152c2bc9b492486ccc1be94
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842191"
---
# <a name="array-and-sized-pointer-attributes"></a><span data-ttu-id="4e42e-105">陣列和 Sized-Pointer 屬性</span><span class="sxs-lookup"><span data-stu-id="4e42e-105">Array and Sized-Pointer Attributes</span></span>

<span data-ttu-id="4e42e-106">MIDL 提供一組豐富的功能，可傳遞資料的陣列和指向資料的指標。</span><span class="sxs-lookup"><span data-stu-id="4e42e-106">MIDL provides a rich set of features for passing arrays of data and pointers to data.</span></span> <span data-ttu-id="4e42e-107">您可以使用這些屬性來指定陣列的特性以及多個指標層級。</span><span class="sxs-lookup"><span data-stu-id="4e42e-107">You can use these attributes to specify characteristics of arrays and multiple levels of pointers.</span></span>



| <span data-ttu-id="4e42e-108">屬性</span><span class="sxs-lookup"><span data-stu-id="4e42e-108">Attribute</span></span>                       | <span data-ttu-id="4e42e-109">使用方式</span><span class="sxs-lookup"><span data-stu-id="4e42e-109">Usage</span></span>                                                                                                                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e42e-110">**大小 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="4e42e-110">**size\_is**</span></span>](size-is.md)     | <span data-ttu-id="4e42e-111">指定要配置給大小指標的記憶體數量、調整大小指標大小的指標，以及單一或多維度陣列。</span><span class="sxs-lookup"><span data-stu-id="4e42e-111">Specifies the amount of memory to be allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.</span></span>                                                         |
| [<span data-ttu-id="4e42e-112">**最大值 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="4e42e-112">**max\_is**</span></span>](max-is.md)       | <span data-ttu-id="4e42e-113">陣列索引的最大值。</span><span class="sxs-lookup"><span data-stu-id="4e42e-113">The maximum value for an array index.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="4e42e-114">**長度 \_ 為**</span><span class="sxs-lookup"><span data-stu-id="4e42e-114">**length\_is**</span></span>](length-is.md) | <span data-ttu-id="4e42e-115">要傳送的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="4e42e-115">The number of array elements to be transmitted.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="4e42e-116">**第一個 \_ 是**</span><span class="sxs-lookup"><span data-stu-id="4e42e-116">**first\_is**</span></span>](first-is.md)   | <span data-ttu-id="4e42e-117">要傳送之第一個陣列元素的索引。</span><span class="sxs-lookup"><span data-stu-id="4e42e-117">The index of the first array element to be transmitted.</span></span>                                                                                                                                              |
| [<span data-ttu-id="4e42e-118">**last \_**</span><span class="sxs-lookup"><span data-stu-id="4e42e-118">**last\_is**</span></span>](last-is.md)     | <span data-ttu-id="4e42e-119">提供要傳送之最後一個陣列元素的索引。</span><span class="sxs-lookup"><span data-stu-id="4e42e-119">Gives the index of the last array element to be transmitted.</span></span>                                                                                                                                         |
| [<span data-ttu-id="4e42e-120">**字串**</span><span class="sxs-lookup"><span data-stu-id="4e42e-120">**string**</span></span>](string.md)        | <span data-ttu-id="4e42e-121">指出一維 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**byte**](byte.md) (或對等的) 陣列，或是這類陣列的指標，會以字串的形式處理。</span><span class="sxs-lookup"><span data-stu-id="4e42e-121">Indicates that the one-dimensional [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**byte**](byte.md) (or equivalent) array, or the pointer to such an array, is to be handled as a string.</span></span> |
| [<span data-ttu-id="4e42e-122">**範圍**</span><span class="sxs-lookup"><span data-stu-id="4e42e-122">**range**</span></span>](range.md)          | <span data-ttu-id="4e42e-123">指定引數或欄位的允許值範圍，其值會在執行時間設定。</span><span class="sxs-lookup"><span data-stu-id="4e42e-123">Specifies a range of allowable values for arguments or fields whose values are set at runtime.</span></span>                                                                                                       |



 

<span data-ttu-id="4e42e-124">MIDL 支援三種指標：參考指標、唯一指標和完整指標。</span><span class="sxs-lookup"><span data-stu-id="4e42e-124">MIDL supports three kinds of pointers: reference pointers, unique pointers, and full pointers.</span></span> <span data-ttu-id="4e42e-125">這些指標是由指標屬性 [**ref**](ref.md)、 [**unique**](unique.md)和 [**ptr**](ptr.md)所指定。</span><span class="sxs-lookup"><span data-stu-id="4e42e-125">These pointers are specified by the pointer attributes [**ref**](ref.md), [**unique**](unique.md), and [**ptr**](ptr.md).</span></span>

<span data-ttu-id="4e42e-126">指標屬性可以套用為型別屬性;作為套用至結構成員、等位成員或參數的欄位屬性;或作為套用至函式傳回型別的函式屬性。</span><span class="sxs-lookup"><span data-stu-id="4e42e-126">A pointer attribute can be applied as a type attribute; as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="4e42e-127">指標屬性也可以與 [**指標 \_ default**](pointer-default.md) 關鍵字一起出現。</span><span class="sxs-lookup"><span data-stu-id="4e42e-127">The pointer attribute can also appear with the [**pointer\_default**](pointer-default.md) keyword.</span></span>

<span data-ttu-id="4e42e-128">若要允許指標參數在遠端函式期間變更值，您必須提供多個指標宣告子，以提供另一個間接取值層級。</span><span class="sxs-lookup"><span data-stu-id="4e42e-128">To allow a pointer parameter to change in value during a remote function, you must provide another level of indirection by supplying multiple pointer declarators.</span></span> <span data-ttu-id="4e42e-129">套用至參數的明確指標屬性只會影響參數最右邊的指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="4e42e-129">The explicit pointer attribute applied to the parameter affects only the rightmost pointer declarator for the parameter.</span></span> <span data-ttu-id="4e42e-130">如果在參數宣告中有多個指標宣告子，則其他宣告子會預設為 [**指標 \_ 預設**](pointer-default.md) 屬性所指定的指標屬性。</span><span class="sxs-lookup"><span data-stu-id="4e42e-130">When there are multiple pointer declarators in a parameter declaration, the other declarators default to the pointer attribute specified by the [**pointer\_default**](pointer-default.md) attribute.</span></span> <span data-ttu-id="4e42e-131">若要將不同的指標屬性套用至多個指標宣告子，您必須定義指定明確指標屬性的中繼類型。</span><span class="sxs-lookup"><span data-stu-id="4e42e-131">To apply different pointer attributes to multiple pointer declarators, you must define intermediate types that specify the explicit pointer attributes.</span></span>

## <a name="default-pointer-attribute-values"></a><span data-ttu-id="4e42e-132">預設 Pointer-Attribute 值</span><span class="sxs-lookup"><span data-stu-id="4e42e-132">Default Pointer-Attribute Values</span></span>

<span data-ttu-id="4e42e-133">當沒有指標屬性與參數的指標相關聯時，會假設指標是 [**ref**](ref.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="4e42e-133">When no pointer attribute is associated with a pointer that is a parameter, the pointer is assumed to be a [**ref**](ref.md) pointer.</span></span>

<span data-ttu-id="4e42e-134">當沒有指標屬性與結構或等位成員的指標相關聯時，MIDL 編譯器會使用下列優先順序規則指派指標屬性 (1 為最高) ：</span><span class="sxs-lookup"><span data-stu-id="4e42e-134">When no pointer attribute is associated with a pointer that is a member of a structure or union, the MIDL compiler assigns pointer attributes using the following priority rules (1 is highest):</span></span>

1.  <span data-ttu-id="4e42e-135">明確套用至指標類型的屬性</span><span class="sxs-lookup"><span data-stu-id="4e42e-135">Attributes explicitly applied to the pointer type</span></span>
2.  <span data-ttu-id="4e42e-136">明確套用至指標參數或成員的屬性</span><span class="sxs-lookup"><span data-stu-id="4e42e-136">Attributes explicitly applied to the pointer parameter or member</span></span>
3.  <span data-ttu-id="4e42e-137">IDL 檔案中定義類型的 [**指標 \_ default**](pointer-default.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="4e42e-137">The [**pointer\_default**](pointer-default.md) attribute in the IDL file that defines the type</span></span>
4.  <span data-ttu-id="4e42e-138">匯入類型之 IDL 檔案中的 [**指標 \_ 預設**](pointer-default.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="4e42e-138">The [**pointer\_default**](pointer-default.md) attribute in the IDL file that imports the type</span></span>
5.  <span data-ttu-id="4e42e-139">[**ptr**](ptr.md) (憑證模式) ; [**唯一**](unique.md) (Microsoft RPC 預設模式) </span><span class="sxs-lookup"><span data-stu-id="4e42e-139">[**ptr**](ptr.md) (osf mode); [**unique**](unique.md) (Microsoft RPC default mode)</span></span>

<span data-ttu-id="4e42e-140">在預設模式下編譯 IDL 檔案時，匯入的檔案可以從匯入檔案繼承指標屬性。</span><span class="sxs-lookup"><span data-stu-id="4e42e-140">When the IDL file is compiled in default mode, imported files can inherit pointer attributes from importing files.</span></span> <span data-ttu-id="4e42e-141">當您使用/[**憑證**](-osf.md) 參數進行編譯時，無法使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="4e42e-141">This feature is not available when you compile using the /[**osf**](-osf.md) switch.</span></span> <span data-ttu-id="4e42e-142">如需詳細資訊，請參閱匯 [**入**](import.md)。</span><span class="sxs-lookup"><span data-stu-id="4e42e-142">For more information, see [**import**](import.md).</span></span>

## <a name="function-return-types"></a><span data-ttu-id="4e42e-143">函數傳回類型</span><span class="sxs-lookup"><span data-stu-id="4e42e-143">Function Return Types</span></span>

<span data-ttu-id="4e42e-144">函數所傳回的指標必須是 [**唯一**](unique.md) 指標或完整指標。</span><span class="sxs-lookup"><span data-stu-id="4e42e-144">A pointer returned by a function must be a [**unique**](unique.md) pointer or a full pointer.</span></span> <span data-ttu-id="4e42e-145">如果函式結果是參考指標（明確地或預設值），MIDL 編譯器會回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e42e-145">The MIDL compiler reports an error if a function result is a reference pointer, either explicitly or by default.</span></span> <span data-ttu-id="4e42e-146">傳回的指標一律表示新的儲存體。</span><span class="sxs-lookup"><span data-stu-id="4e42e-146">The returned pointer always indicates new storage.</span></span>

<span data-ttu-id="4e42e-147">傳回指標值的函式可以將指標屬性指定為函數屬性。</span><span class="sxs-lookup"><span data-stu-id="4e42e-147">Functions that return a pointer value can specify a pointer attribute as a function attribute.</span></span> <span data-ttu-id="4e42e-148">如果指標屬性不存在，則函式結果指標會使用提供的值做為 [**指標 \_ 預設**](pointer-default.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4e42e-148">If a pointer attribute is not present, the function-result pointer uses the value provided as the [**pointer\_default**](pointer-default.md) attribute.</span></span>

## <a name="pointer-attributes-in-type-definitions"></a><span data-ttu-id="4e42e-149">類型定義中的指標屬性</span><span class="sxs-lookup"><span data-stu-id="4e42e-149">Pointer Attributes in Type Definitions</span></span>

<span data-ttu-id="4e42e-150">當您在 [**typedef**](typedef.md) 語句的最上層指定指標屬性時，會如預期般將指定的屬性套用至指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="4e42e-150">When you specify a pointer attribute at the top level of a [**typedef**](typedef.md) statement, the specified attribute is applied to the pointer declarator, as expected.</span></span> <span data-ttu-id="4e42e-151">如果未指定指標屬性，在使用時，typedef 語句最上層的指標宣告子會繼承指標屬性型別。</span><span class="sxs-lookup"><span data-stu-id="4e42e-151">When no pointer attribute is specified, pointer declarators at the top level of a typedef statement inherit the pointer attribute type when used.</span></span>

<span data-ttu-id="4e42e-152">DCE IDL 不允許明確地套用相同的指標屬性，例如在 [**typedef**](typedef.md) 宣告和參數屬性清單中都有兩次。</span><span class="sxs-lookup"><span data-stu-id="4e42e-152">DCE IDL does not allow the same pointer attribute to be explicitly applied twice—for example, in both the [**typedef**](typedef.md) declaration and the parameter attribute list.</span></span> <span data-ttu-id="4e42e-153">當您使用 MIDL 編譯器的預設 (Microsoft 擴充功能) 模式時，會放寬此條件約束。</span><span class="sxs-lookup"><span data-stu-id="4e42e-153">When you use the default (Microsoft extensions) mode of the MIDL compiler, this constraint is relaxed.</span></span>

<span data-ttu-id="4e42e-154">如需在遠端程序呼叫中使用 MIDL 陣列和指標的討論，請參閱 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="4e42e-154">For a discussion of using MIDL arrays and pointers in remote procedure calls, see [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

 

 