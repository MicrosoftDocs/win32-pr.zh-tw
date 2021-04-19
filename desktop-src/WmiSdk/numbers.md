---
description: 在 MOF 中，數位是描述數值的數位。 MOF 提供各種可轉譯成自動化的資料類型，也可讓這些數位採用不同的格式。 下表列出 MOF 所支援的數位值。
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: " (WMI) 的數位"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992398"
---
# <a name="numbers-wmi"></a><span data-ttu-id="42131-105"> (WMI) 的數位</span><span class="sxs-lookup"><span data-stu-id="42131-105">Numbers (WMI)</span></span>

<span data-ttu-id="42131-106">在 MOF 中，數位是描述數值的數位。</span><span class="sxs-lookup"><span data-stu-id="42131-106">In MOF, numbers are digits that describe numerical values.</span></span> <span data-ttu-id="42131-107">MOF 提供各種可轉譯成自動化的資料類型，也可讓這些數位採用不同的格式。</span><span class="sxs-lookup"><span data-stu-id="42131-107">MOF provides a variety of data types that translate into Automation, and also allows those numbers to be in different formats.</span></span> <span data-ttu-id="42131-108">下表列出 MOF 所支援的數位值。</span><span class="sxs-lookup"><span data-stu-id="42131-108">The following table lists the numeric values that MOF supports.</span></span>



| <span data-ttu-id="42131-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="42131-109">Data type</span></span>  | <span data-ttu-id="42131-110">Automation 類型</span><span class="sxs-lookup"><span data-stu-id="42131-110">Automation type</span></span> | <span data-ttu-id="42131-111">Description</span><span class="sxs-lookup"><span data-stu-id="42131-111">Description</span></span>                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42131-112">**sint8**</span><span class="sxs-lookup"><span data-stu-id="42131-112">**sint8**</span></span>  | <span data-ttu-id="42131-113">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="42131-113">**VT\_I2**</span></span>      | <span data-ttu-id="42131-114">帶正負號的8位整數。</span><span class="sxs-lookup"><span data-stu-id="42131-114">Signed 8-bit integer.</span></span><br/>                                                                                                                                        |
| <span data-ttu-id="42131-115">**sint16**</span><span class="sxs-lookup"><span data-stu-id="42131-115">**sint16**</span></span> | <span data-ttu-id="42131-116">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="42131-116">**VT\_I2**</span></span>      | <span data-ttu-id="42131-117">帶正負號的16位整數。</span><span class="sxs-lookup"><span data-stu-id="42131-117">Signed 16-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="42131-118">**sint32**</span><span class="sxs-lookup"><span data-stu-id="42131-118">**sint32**</span></span> | <span data-ttu-id="42131-119">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="42131-119">VT\_I4</span></span>          | <span data-ttu-id="42131-120">帶正負號的32位整數。</span><span class="sxs-lookup"><span data-stu-id="42131-120">Signed 32-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="42131-121">**sint64**</span><span class="sxs-lookup"><span data-stu-id="42131-121">**sint64**</span></span> | <span data-ttu-id="42131-122">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42131-122">**VT\_BSTR**</span></span>    | <span data-ttu-id="42131-123">字串格式的帶正負號64位整數。</span><span class="sxs-lookup"><span data-stu-id="42131-123">Signed 64-bit integer in string form.</span></span> <span data-ttu-id="42131-124">根據美國國家標準局 (ANSI) C 規則，此類型遵循十六進位或十進位格式。</span><span class="sxs-lookup"><span data-stu-id="42131-124">This type follows hexadecimal or decimal format according to the American National Standards Institute (ANSI) C rules.</span></span><br/> |
| <span data-ttu-id="42131-125">**real32**</span><span class="sxs-lookup"><span data-stu-id="42131-125">**real32**</span></span> | <span data-ttu-id="42131-126">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="42131-126">**VT\_R4**</span></span>      | <span data-ttu-id="42131-127">四位元組浮點數，依照電氣和電子工程師協會，Inc. (IEEE) 標準。</span><span class="sxs-lookup"><span data-stu-id="42131-127">4-byte floating-point value that follows the Institute of Electrical and Electronics Engineers, Inc. (IEEE) standard.</span></span><br/>                                        |
| <span data-ttu-id="42131-128">**real64**</span><span class="sxs-lookup"><span data-stu-id="42131-128">**real64**</span></span> | <span data-ttu-id="42131-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="42131-129">**VT\_R8**</span></span>      | <span data-ttu-id="42131-130">遵循 IEEE 標準的8位元組浮點值。</span><span class="sxs-lookup"><span data-stu-id="42131-130">8-byte floating-point value that follows the IEEE standard.</span></span><br/>                                                                                                  |
| <span data-ttu-id="42131-131">**uint8**</span><span class="sxs-lookup"><span data-stu-id="42131-131">**uint8**</span></span>  | <span data-ttu-id="42131-132">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="42131-132">**VT\_UI1**</span></span>     | <span data-ttu-id="42131-133">不帶正負號的8位整數。</span><span class="sxs-lookup"><span data-stu-id="42131-133">Unsigned 8-bit integer.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="42131-134">**uint16**</span><span class="sxs-lookup"><span data-stu-id="42131-134">**uint16**</span></span> | <span data-ttu-id="42131-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="42131-135">**VT\_I4**</span></span>      | <span data-ttu-id="42131-136">不帶正負號的16位整數。</span><span class="sxs-lookup"><span data-stu-id="42131-136">Unsigned 16-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="42131-137">**uint32**</span><span class="sxs-lookup"><span data-stu-id="42131-137">**uint32**</span></span> | <span data-ttu-id="42131-138">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="42131-138">**VT\_I4**</span></span>      | <span data-ttu-id="42131-139">不帶正負號的32位整數。</span><span class="sxs-lookup"><span data-stu-id="42131-139">Unsigned 32-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="42131-140">**uint64**</span><span class="sxs-lookup"><span data-stu-id="42131-140">**uint64**</span></span> | <span data-ttu-id="42131-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="42131-141">**VT\_BSTR**</span></span>    | <span data-ttu-id="42131-142">字串格式的不帶正負號64位整數。</span><span class="sxs-lookup"><span data-stu-id="42131-142">Unsigned 64-bit integer in string form.</span></span> <span data-ttu-id="42131-143">此類型遵循的是十六進位或十進位格式（根據 ANSI C 規則）。</span><span class="sxs-lookup"><span data-stu-id="42131-143">This type follows hexadecimal or decimal format according to ANSI C rules.</span></span><br/>                                           |



 

<span data-ttu-id="42131-144">雖然有彈性，但 MOF 程式碼會在處理自動化時遇到一些變更：</span><span class="sxs-lookup"><span data-stu-id="42131-144">Although flexible, MOF code does encounter some changes when dealing with Automation:</span></span>

-   <span data-ttu-id="42131-145">您必須將64位整數編碼為字串。</span><span class="sxs-lookup"><span data-stu-id="42131-145">You must encode 64-bit integers as strings.</span></span>

    <span data-ttu-id="42131-146">Automation 不支援64位整數類型。</span><span class="sxs-lookup"><span data-stu-id="42131-146">Automation does not support a 64-bit integral type.</span></span>

-   <span data-ttu-id="42131-147">Automation 型別不一定會對應到 MOF 資料類型的位大小。</span><span class="sxs-lookup"><span data-stu-id="42131-147">Automation types do not always correspond in bit size to MOF data types.</span></span>

    <span data-ttu-id="42131-148">例如，Automation 使用 VT \_ I4 傳回不帶正負號的16位值。</span><span class="sxs-lookup"><span data-stu-id="42131-148">For example, Automation uses VT\_I4 to return an unsigned 16-bit value.</span></span> <span data-ttu-id="42131-149">因為有正負號延伸的問題，所以這項差異存在。</span><span class="sxs-lookup"><span data-stu-id="42131-149">This discrepancy exists because of sign-extension problems.</span></span> <span data-ttu-id="42131-150">如果自動化使用 VT （ \_ 而非 vt \_ I4），65536會顯示為值1，導致類型和範圍問題。</span><span class="sxs-lookup"><span data-stu-id="42131-150">If Automation used VT\_I2 instead of VT\_I4, 65,536 would appear to be the value  1, causing type and range problems.</span></span> <span data-ttu-id="42131-151">同樣地，Automation 將 **uint32** 類型表示為 VT \_ I4，因為沒有較大的整數類型可包含 **uint32**。</span><span class="sxs-lookup"><span data-stu-id="42131-151">Similarly, Automation represents the **uint32** type as VT\_I4 because there exists no larger integer type to contain **uint32**.</span></span>

-   <span data-ttu-id="42131-152">您不需要變更8位數位類型的任何標記法。</span><span class="sxs-lookup"><span data-stu-id="42131-152">You do not need to change any representation for 8-bit numeral types.</span></span>

    <span data-ttu-id="42131-153">Automation 支援 VT \_ UI1，這是一個不帶正負號的8位類型。</span><span class="sxs-lookup"><span data-stu-id="42131-153">Automation supports VT\_UI1, an unsigned 8-bit type.</span></span>

<span data-ttu-id="42131-154">MOF 支援長常數。</span><span class="sxs-lookup"><span data-stu-id="42131-154">MOF supports long constants.</span></span> <span data-ttu-id="42131-155">您可以使用具有選擇性負號的簡單數位系列來宣告長常數。</span><span class="sxs-lookup"><span data-stu-id="42131-155">You declare a long constant using a simple series of digits with an optional negative sign.</span></span> <span data-ttu-id="42131-156">長常數不能超過宣告用來保存它之變數的大小。</span><span class="sxs-lookup"><span data-stu-id="42131-156">A long constant cannot exceed the size of the variable that is declared to hold it.</span></span> <span data-ttu-id="42131-157">長常數的一些範例是1000和12310。</span><span class="sxs-lookup"><span data-stu-id="42131-157">Some examples of long constants are 1000 and  12310.</span></span>

<span data-ttu-id="42131-158">MOF 也支援替代的數位格式。</span><span class="sxs-lookup"><span data-stu-id="42131-158">MOF also supports alternate numerical formats.</span></span> <span data-ttu-id="42131-159">下表列出您必須用來描述十六進位、二進位和八進位常數的特殊字元。</span><span class="sxs-lookup"><span data-stu-id="42131-159">The following table lists the special characters you must use to describe hexadecimal, binary, and octal constants.</span></span>



| <span data-ttu-id="42131-160">常數</span><span class="sxs-lookup"><span data-stu-id="42131-160">Constant</span></span>               | <span data-ttu-id="42131-161">特殊字元</span><span class="sxs-lookup"><span data-stu-id="42131-161">Special character</span></span>     | <span data-ttu-id="42131-162">範例</span><span class="sxs-lookup"><span data-stu-id="42131-162">Example</span></span>                   |
|------------------------|-----------------------|---------------------------|
| <span data-ttu-id="42131-163">Decimal</span><span class="sxs-lookup"><span data-stu-id="42131-163">Decimal</span></span><br/>     | <span data-ttu-id="42131-164">無</span><span class="sxs-lookup"><span data-stu-id="42131-164">None</span></span><br/>       | <span data-ttu-id="42131-165">val = 65</span><span class="sxs-lookup"><span data-stu-id="42131-165">val = 65</span></span><br/>       |
| <span data-ttu-id="42131-166">十六進位</span><span class="sxs-lookup"><span data-stu-id="42131-166">Hexadecimal</span></span><br/> | <span data-ttu-id="42131-167">0x 前置詞</span><span class="sxs-lookup"><span data-stu-id="42131-167">0x prefix</span></span><br/>  | <span data-ttu-id="42131-168">val = 0x41 向</span><span class="sxs-lookup"><span data-stu-id="42131-168">val = 0x41</span></span><br/>     |
| <span data-ttu-id="42131-169">八進位</span><span class="sxs-lookup"><span data-stu-id="42131-169">Octal</span></span><br/>       | <span data-ttu-id="42131-170">前置0</span><span class="sxs-lookup"><span data-stu-id="42131-170">Leading 0</span></span><br/>  | <span data-ttu-id="42131-171">val = 0101</span><span class="sxs-lookup"><span data-stu-id="42131-171">val = 0101</span></span><br/>     |
| <span data-ttu-id="42131-172">Binary</span><span class="sxs-lookup"><span data-stu-id="42131-172">Binary</span></span><br/>      | <span data-ttu-id="42131-173">尾端 B</span><span class="sxs-lookup"><span data-stu-id="42131-173">Trailing B</span></span><br/> | <span data-ttu-id="42131-174">val = 1000001B</span><span class="sxs-lookup"><span data-stu-id="42131-174">val = 1000001B</span></span><br/> |



 

<span data-ttu-id="42131-175">您可以使用浮點常數來表示科學記號和分數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="42131-175">You can use a floating-point constant to represent scientific notation as well as fractions, as shown next:</span></span>

``` syntax
3.14
-3.14
-1.2778E+02
```

<span data-ttu-id="42131-176">WMI 會將浮點常數視為自動化的 **VT \_ R8** 類型。</span><span class="sxs-lookup"><span data-stu-id="42131-176">WMI considers floating-point constants as **VT\_R8** types for Automation.</span></span>

<span data-ttu-id="42131-177">下列範例描述的類別和實例宣告，說明如何使用每個數值資料類型來設定屬性：</span><span class="sxs-lookup"><span data-stu-id="42131-177">The following example describes class and instance declarations that illustrate how to use each of the numeric data types to set properties:</span></span>

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




