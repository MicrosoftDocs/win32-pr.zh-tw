---
title: 從 c + + 翻譯為 Visual Basic
description: 從 c + + 翻譯為 Visual Basic
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968645"
---
# <a name="translating-to-visual-basic-from-c"></a><span data-ttu-id="5028e-103">從 c + + 翻譯為 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5028e-103">Translating to Visual Basic from C++</span></span>

<span data-ttu-id="5028e-104">使用 c + + 程式設計語言，開發人員可以直接存取儲存特定變數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5028e-104">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="5028e-105">記憶體指標可提供此直接存取。</span><span class="sxs-lookup"><span data-stu-id="5028e-105">Memory pointers provide this direct access.</span></span> <span data-ttu-id="5028e-106">在 Visual Basic 中，系統會為您處理指標。</span><span class="sxs-lookup"><span data-stu-id="5028e-106">In Visual Basic, pointers are handled for you.</span></span> <span data-ttu-id="5028e-107">例如，在 c + + 中宣告為 **int** 之指標的參數，相當於 Visual Basic 中宣告為 **ByRef** **整數** 的參數。</span><span class="sxs-lookup"><span data-stu-id="5028e-107">For example, a parameter declared as a pointer to an **int** in C++ is equivalent to a parameter declared in Visual Basic as a **ByRef** **Integer**.</span></span>

<span data-ttu-id="5028e-108">在 Visual Basic 中宣告 **為字串** 的參數會宣告為 c + + 中的 **BSTR** 指標。</span><span class="sxs-lookup"><span data-stu-id="5028e-108">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="5028e-109">在 c + + 中將字串指標設定為 **Null** ，相當於將字串設定為 Visual Basic 中的 **vbNullString** 常數。</span><span class="sxs-lookup"><span data-stu-id="5028e-109">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="5028e-110">傳入零長度的字串 ( "" ) 至設計用來接收 **Null** 的函式無效，因為這樣會將指標傳遞至長度為零的字串，而不是零指標。</span><span class="sxs-lookup"><span data-stu-id="5028e-110">Passing in a zero-length string ("") to a function designed to receive **NULL** does not work, as this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="5028e-111">C + + 支援在舊版 Visual Basic 中沒有對等的資料容器，亦即結構和等位。</span><span class="sxs-lookup"><span data-stu-id="5028e-111">C++ supports data containers, namely structures and unions, that have no equivalent in early versions of Visual Basic.</span></span> <span data-ttu-id="5028e-112">基於這個理由，COM 物件通常會包裝通常儲存在物件類別結構和等位中的資訊。</span><span class="sxs-lookup"><span data-stu-id="5028e-112">For this reason, COM objects typically wrap information that usually is stored in structures and unions in object classes.</span></span> <span data-ttu-id="5028e-113">不過，某些 COM 物件可能包含結構，而導致物件的部分方法或功能無法 Visual Basic 存取。</span><span class="sxs-lookup"><span data-stu-id="5028e-113">Some COM objects, however, may contain structures, causing portions of the object's methods or functionality to be inaccessible to Visual Basic.</span></span>

<span data-ttu-id="5028e-114">某些 c + + 資料類型在 Visual Basic 中不受支援，例如不帶正負號的類型和 **HWND** 類型。</span><span class="sxs-lookup"><span data-stu-id="5028e-114">Some C++ data types are not supported in Visual Basic, for example unsigned types and **HWND** types.</span></span> <span data-ttu-id="5028e-115">Visual Basic 不提供接受或傳回這些資料類型的方法。</span><span class="sxs-lookup"><span data-stu-id="5028e-115">Methods that accept or return these data types are not available in Visual Basic.</span></span>

<span data-ttu-id="5028e-116">Visual Basic 使用 Automation 相容的資料類型作為其內部資料類型。</span><span class="sxs-lookup"><span data-stu-id="5028e-116">Visual Basic uses Automation-compatible data types as its internal data types.</span></span> <span data-ttu-id="5028e-117">因此，與自動化相容的 c + + 資料類型也會與 Visual Basic 相容。</span><span class="sxs-lookup"><span data-stu-id="5028e-117">Thus, C++ data types that are Automation-compatible are also compatible with Visual Basic.</span></span> <span data-ttu-id="5028e-118">非自動化相容的資料類型可能無法轉換成 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="5028e-118">Data types that are not Automation-compatible may not be able to be converted to Visual Basic.</span></span>

<span data-ttu-id="5028e-119">下表列出 Visual Basic 所支援的資料類型及其 **VARTYPE** 。</span><span class="sxs-lookup"><span data-stu-id="5028e-119">The following table lists the data types are supported by Visual Basic and their **VARTYPE** equivalents.</span></span> <span data-ttu-id="5028e-120">**VARTYPE** 是列出 Automation variant 類型的列舉。</span><span class="sxs-lookup"><span data-stu-id="5028e-120">**VARTYPE** is an enumeration that lists the Automation variant types.</span></span>



| <span data-ttu-id="5028e-121">Visual Basic 資料類型</span><span class="sxs-lookup"><span data-stu-id="5028e-121">Visual Basic data type</span></span>  | <span data-ttu-id="5028e-122">VARTYPE 相等</span><span class="sxs-lookup"><span data-stu-id="5028e-122">VARTYPE equivalent</span></span>                |
|-------------------------|-----------------------------------|
| <span data-ttu-id="5028e-123">**整數**</span><span class="sxs-lookup"><span data-stu-id="5028e-123">**Integer**</span></span><br/>  | <span data-ttu-id="5028e-124">16位、帶正負號、VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="5028e-124">16 bit, signed, VT\_I2</span></span><br/> |
| <span data-ttu-id="5028e-125">**Long**</span><span class="sxs-lookup"><span data-stu-id="5028e-125">**Long**</span></span><br/>     | <span data-ttu-id="5028e-126">32位、帶正負號、VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5028e-126">32 bit, signed, VT\_I4</span></span><br/> |
| <span data-ttu-id="5028e-127">**日期**</span><span class="sxs-lookup"><span data-stu-id="5028e-127">**Date**</span></span><br/>     | <span data-ttu-id="5028e-128">VT \_ 日期</span><span class="sxs-lookup"><span data-stu-id="5028e-128">VT\_DATE</span></span><br/>               |
| <span data-ttu-id="5028e-129">**貨幣**</span><span class="sxs-lookup"><span data-stu-id="5028e-129">**Currency**</span></span><br/> | <span data-ttu-id="5028e-130">VT \_ CY</span><span class="sxs-lookup"><span data-stu-id="5028e-130">VT\_CY</span></span><br/>                 |
| <span data-ttu-id="5028e-131">**Object**</span><span class="sxs-lookup"><span data-stu-id="5028e-131">**Object**</span></span><br/>   | <span data-ttu-id="5028e-132">\*VT \_ 分派</span><span class="sxs-lookup"><span data-stu-id="5028e-132">\*VT\_DISPATCH</span></span><br/>         |
| <span data-ttu-id="5028e-133">**String**</span><span class="sxs-lookup"><span data-stu-id="5028e-133">**String**</span></span><br/>   | <span data-ttu-id="5028e-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="5028e-134">VT\_BSTR</span></span><br/>               |
| <span data-ttu-id="5028e-135">**布林值**</span><span class="sxs-lookup"><span data-stu-id="5028e-135">**Boolean**</span></span><br/>  | <span data-ttu-id="5028e-136">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="5028e-136">VT\_BOOL</span></span><br/>               |
| <span data-ttu-id="5028e-137">**貨幣**</span><span class="sxs-lookup"><span data-stu-id="5028e-137">**Currency**</span></span><br/> | <span data-ttu-id="5028e-138">VT \_ DECIMAL</span><span class="sxs-lookup"><span data-stu-id="5028e-138">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="5028e-139">**Single**</span><span class="sxs-lookup"><span data-stu-id="5028e-139">**Single**</span></span><br/>   | <span data-ttu-id="5028e-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="5028e-140">VT\_R4</span></span><br/>                 |
| <span data-ttu-id="5028e-141">**Double**</span><span class="sxs-lookup"><span data-stu-id="5028e-141">**Double**</span></span><br/>   | <span data-ttu-id="5028e-142">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="5028e-142">VT\_R8</span></span><br/>                 |
| <span data-ttu-id="5028e-143">**十進位**</span><span class="sxs-lookup"><span data-stu-id="5028e-143">**Decimal**</span></span><br/>  | <span data-ttu-id="5028e-144">VT \_ DECIMAL</span><span class="sxs-lookup"><span data-stu-id="5028e-144">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="5028e-145">**位元組**</span><span class="sxs-lookup"><span data-stu-id="5028e-145">**Byte**</span></span><br/>     | <span data-ttu-id="5028e-146">VT \_ DECIMAL</span><span class="sxs-lookup"><span data-stu-id="5028e-146">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="5028e-147">**變異**</span><span class="sxs-lookup"><span data-stu-id="5028e-147">**Variant**</span></span><br/>  | <span data-ttu-id="5028e-148">VT \_ 變異</span><span class="sxs-lookup"><span data-stu-id="5028e-148">VT\_VARIANT</span></span><br/>            |



 

<span data-ttu-id="5028e-149">除非以關鍵字 **ByVal** 標記，否則 Visual Basic 中的所有參數會以傳址方式傳遞 (做為指標) ，而不是以傳值方式傳遞。</span><span class="sxs-lookup"><span data-stu-id="5028e-149">All parameters in Visual Basic, unless labeled with the keyword **ByVal**, are passed by reference (as pointers) instead of by value.</span></span>

<span data-ttu-id="5028e-150">C + + 和 Visual Basic 在其代表屬性的方式上稍有不同。</span><span class="sxs-lookup"><span data-stu-id="5028e-150">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="5028e-151">在 c + + 中，屬性是以一組存取子函式來表示，其中一個設定屬性值，另一個則會抓取屬性值。</span><span class="sxs-lookup"><span data-stu-id="5028e-151">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="5028e-152">在 Visual Basic 中，屬性會以單一專案的形式表示，可用於抓取或設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="5028e-152">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5028e-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="5028e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5028e-154">翻譯為 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5028e-154">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 





