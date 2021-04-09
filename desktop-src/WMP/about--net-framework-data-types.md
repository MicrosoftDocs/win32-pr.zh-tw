---
title: 關於 .NET Framework 資料類型
description: 關於 .NET Framework 資料類型
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player，.NET Framework
- Windows Media Player 物件模型，.NET Framework
- 物件模型、.NET Framework
- Windows Media Player Mobile、.NET Framework
- Windows Media Player ActiveX 控制項，.NET Framework
- Windows Media Player 的行動 ActiveX 控制項，.NET Framework
- ActiveX 控制項，.NET Framework
- .NET Framework，資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021948"
---
# <a name="about-net-framework-data-types"></a><span data-ttu-id="541a0-111">關於 .NET Framework 資料類型</span><span class="sxs-lookup"><span data-stu-id="541a0-111">About .NET Framework Data Types</span></span>

<span data-ttu-id="541a0-112">本節包含將腳本導向的物件模型參考轉譯成 Microsoft .NET Framework 基底資料類型所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="541a0-112">This section contains the information you need to translate the script-oriented Object Model Reference into Microsoft .NET Framework base data types.</span></span> <span data-ttu-id="541a0-113">Windows Media Player 的腳本參考幾乎擁有在 .NET Framework 型程式中使用 Windows Media Player 控制項所需的所有資訊，在大部分情況下，語法會與其他指令碼語言（例如 Microsoft JScript）的語法類似。</span><span class="sxs-lookup"><span data-stu-id="541a0-113">The Windows Media Player script reference has almost all the information you need to use the Windows Media Player control in a .NET Framework-based program, and in most cases, the syntax will be similar to that of other scripting languages such as Microsoft JScript.</span></span>

<span data-ttu-id="541a0-114">Windows Media Player 參考會提供 JScript 資料類型，如有必要，則會提供 c + + 轉換。</span><span class="sxs-lookup"><span data-stu-id="541a0-114">The Windows Media Player reference provides the JScript data type and, if necessary, the C++ conversion.</span></span> <span data-ttu-id="541a0-115">例如，方法可能會傳回 **數位** 。</span><span class="sxs-lookup"><span data-stu-id="541a0-115">For example, a **Number** might be returned by a method.</span></span> <span data-ttu-id="541a0-116">JScript 會以相同方式來處理所有數位，但其他語言會區分不同類型的數位 (整數、浮點數等) 。</span><span class="sxs-lookup"><span data-stu-id="541a0-116">JScript treats all numbers in the same way, but other languages distinguish between different types of numbers (integer, floating point, and so on).</span></span> <span data-ttu-id="541a0-117">參考提供數位資料類型的 c + + 轉換，因為 c + + 可以使用不同的方式來處理數位。</span><span class="sxs-lookup"><span data-stu-id="541a0-117">The reference gives the C++ conversion for number data types because numbers can be processed differently by C++.</span></span> <span data-ttu-id="541a0-118">例如，c + + 使用 **int** 資料型別作為浮點數的整數算術和 **浮** 點數。</span><span class="sxs-lookup"><span data-stu-id="541a0-118">For example, C++ uses the **int** data type for integer arithmetic and **float** for floating point.</span></span>

<span data-ttu-id="541a0-119">.NET Framework 會使用稍微不同的基底資料類型系統。</span><span class="sxs-lookup"><span data-stu-id="541a0-119">The .NET Framework uses a slightly different system of base data types.</span></span> <span data-ttu-id="541a0-120">下表顯示您可能使用之一般資料類型的差異。</span><span class="sxs-lookup"><span data-stu-id="541a0-120">The following table shows the differences in the common data types you are likely to use.</span></span> <span data-ttu-id="541a0-121">如需有關 .NET Framework 基底資料類型以及轉換成其他資料類型系統的詳細資訊，請參閱 .NET Framework 《開發人員指南》中的系統命名空間基底資料類型的相關討論。</span><span class="sxs-lookup"><span data-stu-id="541a0-121">For more information on .NET Framework base data types and the conversion to other data type systems, see the .NET Framework Developer's Guide discussion of System Namespace base data types.</span></span>

<span data-ttu-id="541a0-122">下表提供 .NET Framework 的類別名稱和 c # 資料型別。</span><span class="sxs-lookup"><span data-stu-id="541a0-122">This table gives the .NET Framework class name and the C# data type.</span></span> <span data-ttu-id="541a0-123">其他語言的資料類型則是針對其各自語言參考中的每種語言所定義。</span><span class="sxs-lookup"><span data-stu-id="541a0-123">Data types for other languages are defined for each language in their respective language references.</span></span>



| <span data-ttu-id="541a0-124">腳本資料類型</span><span class="sxs-lookup"><span data-stu-id="541a0-124">Script data type</span></span> | <span data-ttu-id="541a0-125">C++ 資料型別</span><span class="sxs-lookup"><span data-stu-id="541a0-125">C++ data type</span></span>     | <span data-ttu-id="541a0-126">.NET Framework 類別 (c # 資料類型 ) </span><span class="sxs-lookup"><span data-stu-id="541a0-126">.NET Framework class (C# data type )</span></span> |
|------------------|-------------------|---------------------------------------|
| <span data-ttu-id="541a0-127">**Number**</span><span class="sxs-lookup"><span data-stu-id="541a0-127">**Number**</span></span>       | <span data-ttu-id="541a0-128">**int**</span><span class="sxs-lookup"><span data-stu-id="541a0-128">**int**</span></span>           | <span data-ttu-id="541a0-129">**Int32** (**int**) </span><span class="sxs-lookup"><span data-stu-id="541a0-129">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="541a0-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="541a0-130">**Number**</span></span>       | <span data-ttu-id="541a0-131">**long**</span><span class="sxs-lookup"><span data-stu-id="541a0-131">**long**</span></span>          | <span data-ttu-id="541a0-132">**Int32** (**int**) </span><span class="sxs-lookup"><span data-stu-id="541a0-132">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="541a0-133">**Number**</span><span class="sxs-lookup"><span data-stu-id="541a0-133">**Number**</span></span>       | <span data-ttu-id="541a0-134">**double**</span><span class="sxs-lookup"><span data-stu-id="541a0-134">**double**</span></span>        | <span data-ttu-id="541a0-135">**雙** (**雙精度**) </span><span class="sxs-lookup"><span data-stu-id="541a0-135">**Double** (**double**)</span></span>               |
| <span data-ttu-id="541a0-136">**Number**</span><span class="sxs-lookup"><span data-stu-id="541a0-136">**Number**</span></span>       | <span data-ttu-id="541a0-137">**float**</span><span class="sxs-lookup"><span data-stu-id="541a0-137">**float**</span></span>         | <span data-ttu-id="541a0-138">**Single** (**float**) </span><span class="sxs-lookup"><span data-stu-id="541a0-138">**Single** (**float**)</span></span>                |
| <span data-ttu-id="541a0-139">**String**</span><span class="sxs-lookup"><span data-stu-id="541a0-139">**String**</span></span>       | <span data-ttu-id="541a0-140">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="541a0-140">**BSTR**</span></span>          | <span data-ttu-id="541a0-141">**字串** (**字串**) </span><span class="sxs-lookup"><span data-stu-id="541a0-141">**String** (**string**)</span></span>               |
| <span data-ttu-id="541a0-142">**布林值**</span><span class="sxs-lookup"><span data-stu-id="541a0-142">**Boolean**</span></span>      | <span data-ttu-id="541a0-143">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="541a0-143">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="541a0-144">**布林值** (**bool**) </span><span class="sxs-lookup"><span data-stu-id="541a0-144">**Boolean** (**bool**)</span></span>                |
| <span data-ttu-id="541a0-145">**Object**</span><span class="sxs-lookup"><span data-stu-id="541a0-145">**Object**</span></span>       | <span data-ttu-id="541a0-146">**Object**</span><span class="sxs-lookup"><span data-stu-id="541a0-146">**Object**</span></span>        | <span data-ttu-id="541a0-147">**物件** (**物件**) </span><span class="sxs-lookup"><span data-stu-id="541a0-147">**Object** (**object**)</span></span>               |



 

<span data-ttu-id="541a0-148">如果您使用 Visual Studio，可以使用 Microsoft IntelliSense 技術來判斷特定函數預期的資料類型。</span><span class="sxs-lookup"><span data-stu-id="541a0-148">If you are using Visual Studio, you can use the Microsoft IntelliSense technology to determine what data type is expected for a specific function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="541a0-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="541a0-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541a0-150">**在 .NET Framework 方案中內嵌 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="541a0-150">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="541a0-151">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="541a0-151">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




