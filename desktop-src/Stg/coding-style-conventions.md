---
title: 編碼樣式慣例
description: 此範例系列使用編碼樣式慣例來協助清楚且一致。
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684273"
---
# <a name="coding-style-conventions"></a><span data-ttu-id="c83e2-103">編碼樣式慣例</span><span class="sxs-lookup"><span data-stu-id="c83e2-103">Coding Style Conventions</span></span>

<span data-ttu-id="c83e2-104">此範例系列使用編碼樣式慣例來協助清楚且一致。</span><span class="sxs-lookup"><span data-stu-id="c83e2-104">Coding style conventions are used in this sample series to aid clarity and consistency.</span></span> <span data-ttu-id="c83e2-105">使用「匈牙利文」標記法慣例。</span><span class="sxs-lookup"><span data-stu-id="c83e2-105">The "Hungarian" notation conventions are used.</span></span> <span data-ttu-id="c83e2-106">這些已成為 Win32 程式設計中常見的編碼作法。</span><span class="sxs-lookup"><span data-stu-id="c83e2-106">These have become a common coding practice in Win32 programming.</span></span> <span data-ttu-id="c83e2-107">其中包括變數前置詞標記法，可為變數名稱提供變數類型的建議。</span><span class="sxs-lookup"><span data-stu-id="c83e2-107">They include variable prefix notations that give to variable names a suggestion of the type of the variable.</span></span>

<span data-ttu-id="c83e2-108">下表列出常見的首碼。</span><span class="sxs-lookup"><span data-stu-id="c83e2-108">The following table lists common prefixes.</span></span>



| <span data-ttu-id="c83e2-109">前置詞</span><span class="sxs-lookup"><span data-stu-id="c83e2-109">Prefix</span></span> | <span data-ttu-id="c83e2-110">描述</span><span class="sxs-lookup"><span data-stu-id="c83e2-110">Description</span></span>                         |
|--------|-------------------------------------|
| <span data-ttu-id="c83e2-111">a</span><span class="sxs-lookup"><span data-stu-id="c83e2-111">a</span></span>      | <span data-ttu-id="c83e2-112">Array</span><span class="sxs-lookup"><span data-stu-id="c83e2-112">Array</span></span>                               |
| <span data-ttu-id="c83e2-113">b</span><span class="sxs-lookup"><span data-stu-id="c83e2-113">b</span></span>      | <span data-ttu-id="c83e2-114">BOOL (int) </span><span class="sxs-lookup"><span data-stu-id="c83e2-114">BOOL (int)</span></span>                          |
| <span data-ttu-id="c83e2-115">c</span><span class="sxs-lookup"><span data-stu-id="c83e2-115">c</span></span>      | <span data-ttu-id="c83e2-116">Char</span><span class="sxs-lookup"><span data-stu-id="c83e2-116">Char</span></span>                                |
| <span data-ttu-id="c83e2-117">Cb</span><span class="sxs-lookup"><span data-stu-id="c83e2-117">cb</span></span>     | <span data-ttu-id="c83e2-118">位元組計數</span><span class="sxs-lookup"><span data-stu-id="c83e2-118">Count of bytes</span></span>                      |
| <span data-ttu-id="c83e2-119">鉻</span><span class="sxs-lookup"><span data-stu-id="c83e2-119">cr</span></span>     | <span data-ttu-id="c83e2-120">色彩參考值</span><span class="sxs-lookup"><span data-stu-id="c83e2-120">Color reference value</span></span>               |
| <span data-ttu-id="c83e2-121">殘雪</span><span class="sxs-lookup"><span data-stu-id="c83e2-121">cx</span></span>     | <span data-ttu-id="c83e2-122">X (短) 的計數</span><span class="sxs-lookup"><span data-stu-id="c83e2-122">Count of x (short)</span></span>                  |
| <span data-ttu-id="c83e2-123">dw</span><span class="sxs-lookup"><span data-stu-id="c83e2-123">dw</span></span>     | <span data-ttu-id="c83e2-124">DWORD (不帶正負號的 long) </span><span class="sxs-lookup"><span data-stu-id="c83e2-124">DWORD (unsigned long)</span></span>               |
| <span data-ttu-id="c83e2-125">f</span><span class="sxs-lookup"><span data-stu-id="c83e2-125">f</span></span>      | <span data-ttu-id="c83e2-126">旗標 (通常會有多個位值) </span><span class="sxs-lookup"><span data-stu-id="c83e2-126">Flags (usually multiple bit values)</span></span> |
| <span data-ttu-id="c83e2-127">fn</span><span class="sxs-lookup"><span data-stu-id="c83e2-127">fn</span></span>     | <span data-ttu-id="c83e2-128">函式</span><span class="sxs-lookup"><span data-stu-id="c83e2-128">Function</span></span>                            |
| <span data-ttu-id="c83e2-129">G\_</span><span class="sxs-lookup"><span data-stu-id="c83e2-129">g\_</span></span>    | <span data-ttu-id="c83e2-130">全球</span><span class="sxs-lookup"><span data-stu-id="c83e2-130">Global</span></span>                              |
| <span data-ttu-id="c83e2-131">h</span><span class="sxs-lookup"><span data-stu-id="c83e2-131">h</span></span>      | <span data-ttu-id="c83e2-132">Handle</span><span class="sxs-lookup"><span data-stu-id="c83e2-132">Handle</span></span>                              |
| <span data-ttu-id="c83e2-133">i</span><span class="sxs-lookup"><span data-stu-id="c83e2-133">i</span></span>      | <span data-ttu-id="c83e2-134">整數</span><span class="sxs-lookup"><span data-stu-id="c83e2-134">Integer</span></span>                             |
| <span data-ttu-id="c83e2-135">l</span><span class="sxs-lookup"><span data-stu-id="c83e2-135">l</span></span>      | <span data-ttu-id="c83e2-136">long</span><span class="sxs-lookup"><span data-stu-id="c83e2-136">Long</span></span>                                |
| <span data-ttu-id="c83e2-137">lp</span><span class="sxs-lookup"><span data-stu-id="c83e2-137">lp</span></span>     | <span data-ttu-id="c83e2-138">Long 指標</span><span class="sxs-lookup"><span data-stu-id="c83e2-138">Long pointer</span></span>                        |
| <span data-ttu-id="c83e2-139">m\_</span><span class="sxs-lookup"><span data-stu-id="c83e2-139">m\_</span></span>    | <span data-ttu-id="c83e2-140">類別的資料成員</span><span class="sxs-lookup"><span data-stu-id="c83e2-140">Data member of a class</span></span>              |
| <span data-ttu-id="c83e2-141">n</span><span class="sxs-lookup"><span data-stu-id="c83e2-141">n</span></span>      | <span data-ttu-id="c83e2-142">Short 整數</span><span class="sxs-lookup"><span data-stu-id="c83e2-142">Short int</span></span>                           |
| <span data-ttu-id="c83e2-143">p</span><span class="sxs-lookup"><span data-stu-id="c83e2-143">p</span></span>      | <span data-ttu-id="c83e2-144">Pointer</span><span class="sxs-lookup"><span data-stu-id="c83e2-144">Pointer</span></span>                             |
| <span data-ttu-id="c83e2-145">s</span><span class="sxs-lookup"><span data-stu-id="c83e2-145">s</span></span>      | <span data-ttu-id="c83e2-146">String</span><span class="sxs-lookup"><span data-stu-id="c83e2-146">String</span></span>                              |
| <span data-ttu-id="c83e2-147">sz</span><span class="sxs-lookup"><span data-stu-id="c83e2-147">sz</span></span>     | <span data-ttu-id="c83e2-148">以零結尾的字串</span><span class="sxs-lookup"><span data-stu-id="c83e2-148">Zero terminated String</span></span>              |
| <span data-ttu-id="c83e2-149">tm</span><span class="sxs-lookup"><span data-stu-id="c83e2-149">tm</span></span>     | <span data-ttu-id="c83e2-150">文字度量</span><span class="sxs-lookup"><span data-stu-id="c83e2-150">Text metric</span></span>                         |
| <span data-ttu-id="c83e2-151">u</span><span class="sxs-lookup"><span data-stu-id="c83e2-151">u</span></span>      | <span data-ttu-id="c83e2-152">不帶正負號的 int</span><span class="sxs-lookup"><span data-stu-id="c83e2-152">Unsigned int</span></span>                        |
| <span data-ttu-id="c83e2-153">ul</span><span class="sxs-lookup"><span data-stu-id="c83e2-153">ul</span></span>     | <span data-ttu-id="c83e2-154">不帶正負號的 long (ULONG) </span><span class="sxs-lookup"><span data-stu-id="c83e2-154">Unsigned long (ULONG)</span></span>               |
| <span data-ttu-id="c83e2-155">w</span><span class="sxs-lookup"><span data-stu-id="c83e2-155">w</span></span>      | <span data-ttu-id="c83e2-156">WORD (不帶正負號的短) </span><span class="sxs-lookup"><span data-stu-id="c83e2-156">WORD (unsigned short)</span></span>               |
| <span data-ttu-id="c83e2-157">x、y</span><span class="sxs-lookup"><span data-stu-id="c83e2-157">x,y</span></span>    | <span data-ttu-id="c83e2-158">x、y 座標 (短) </span><span class="sxs-lookup"><span data-stu-id="c83e2-158">x, y coordinates (short)</span></span>            |



 

<span data-ttu-id="c83e2-159">這些通常會結合，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c83e2-159">These are often combined, as in the following.</span></span>



| <span data-ttu-id="c83e2-160">前置片語合</span><span class="sxs-lookup"><span data-stu-id="c83e2-160">Prefix combination</span></span> | <span data-ttu-id="c83e2-161">Description</span><span class="sxs-lookup"><span data-stu-id="c83e2-161">Description</span></span>                                             |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="c83e2-162">pszMyString</span><span class="sxs-lookup"><span data-stu-id="c83e2-162">pszMyString</span></span>        | <span data-ttu-id="c83e2-163">字串的指標。</span><span class="sxs-lookup"><span data-stu-id="c83e2-163">A pointer to a string.</span></span>                                  |
| <span data-ttu-id="c83e2-164">m \_ pszMyString</span><span class="sxs-lookup"><span data-stu-id="c83e2-164">m\_pszMyString</span></span>     | <span data-ttu-id="c83e2-165">字串的指標，該字串為類別的資料成員。</span><span class="sxs-lookup"><span data-stu-id="c83e2-165">A pointer to a string that is a data member of a class.</span></span> |



 

<span data-ttu-id="c83e2-166">下表列出其他慣例。</span><span class="sxs-lookup"><span data-stu-id="c83e2-166">Other conventions are listed in the following table.</span></span>



| <span data-ttu-id="c83e2-167">慣例</span><span class="sxs-lookup"><span data-stu-id="c83e2-167">Convention</span></span>       | <span data-ttu-id="c83e2-168">Description</span><span class="sxs-lookup"><span data-stu-id="c83e2-168">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="c83e2-169">CMyClass</span><span class="sxs-lookup"><span data-stu-id="c83e2-169">CMyClass</span></span>         | <span data-ttu-id="c83e2-170">C + + 類別名稱的前置詞 ' C '。</span><span class="sxs-lookup"><span data-stu-id="c83e2-170">Prefix 'C' for C++ class names.</span></span>                          |
| <span data-ttu-id="c83e2-171">COMyObjectClass</span><span class="sxs-lookup"><span data-stu-id="c83e2-171">COMyObjectClass</span></span>  | <span data-ttu-id="c83e2-172">COM 物件類別名稱的前置詞 ' CO '。</span><span class="sxs-lookup"><span data-stu-id="c83e2-172">Prefix 'CO' for COM object class names.</span></span>                  |
| <span data-ttu-id="c83e2-173">CFMyClassFactory</span><span class="sxs-lookup"><span data-stu-id="c83e2-173">CFMyClassFactory</span></span> | <span data-ttu-id="c83e2-174">COM class factory 名稱的前置詞 ' CF '。</span><span class="sxs-lookup"><span data-stu-id="c83e2-174">Prefix 'CF' for COM class factory names.</span></span>                 |
| <span data-ttu-id="c83e2-175">IMyInterface</span><span class="sxs-lookup"><span data-stu-id="c83e2-175">IMyInterface</span></span>     | <span data-ttu-id="c83e2-176">COM 介面類別別名稱的前置詞 ' I '。</span><span class="sxs-lookup"><span data-stu-id="c83e2-176">Prefix 'I' for COM interface class names.</span></span>                |
| <span data-ttu-id="c83e2-177">CImpIMyInterface</span><span class="sxs-lookup"><span data-stu-id="c83e2-177">CImpIMyInterface</span></span> | <span data-ttu-id="c83e2-178">COM 介面實類別的前置詞 ' CImpI '。</span><span class="sxs-lookup"><span data-stu-id="c83e2-178">Prefix 'CImpI' for COM interface implementation classes.</span></span> |



 

<span data-ttu-id="c83e2-179">此範例系列中會使用批註標頭區塊的一些一致慣例，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c83e2-179">Some consistent conventions for comment header blocks are used in this sample series as follows.</span></span>

## <a name="file-header"></a><span data-ttu-id="c83e2-180">檔案標頭</span><span class="sxs-lookup"><span data-stu-id="c83e2-180">File Header</span></span>

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a><span data-ttu-id="c83e2-181">純文字批註區塊</span><span class="sxs-lookup"><span data-stu-id="c83e2-181">Plain Comment Block</span></span>

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a><span data-ttu-id="c83e2-182">類別宣告標頭</span><span class="sxs-lookup"><span data-stu-id="c83e2-182">Class Declaration Header</span></span>

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a><span data-ttu-id="c83e2-183">類別方法定義標頭</span><span class="sxs-lookup"><span data-stu-id="c83e2-183">Class Method Definition Header</span></span>

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a><span data-ttu-id="c83e2-184">Unexported 或區域函數</span><span class="sxs-lookup"><span data-stu-id="c83e2-184">Unexported or Local Function</span></span>

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a><span data-ttu-id="c83e2-185">匯出的函式定義標頭</span><span class="sxs-lookup"><span data-stu-id="c83e2-185">Exported Function Definition Header</span></span>

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a><span data-ttu-id="c83e2-186">COM 介面聲明標頭</span><span class="sxs-lookup"><span data-stu-id="c83e2-186">COM Interface Declaration Header</span></span>

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a><span data-ttu-id="c83e2-187">COM 物件類別宣告標頭</span><span class="sxs-lookup"><span data-stu-id="c83e2-187">COM Object Class Declaration Header</span></span>

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

<span data-ttu-id="c83e2-188">所有這些批註區塊慣例都有一致的開始和結束權杖字串。</span><span class="sxs-lookup"><span data-stu-id="c83e2-188">All of these comment block conventions have consistent beginning and ending token strings.</span></span> <span data-ttu-id="c83e2-189">這項一致性支援以某種方式自動處理標頭。</span><span class="sxs-lookup"><span data-stu-id="c83e2-189">This consistency supports automatic processing of the headers in some fashion.</span></span> <span data-ttu-id="c83e2-190">例如，您可以撰寫 AWK 腳本，將函式標頭篩選成個別的文字檔，然後做為規格檔的基礎。</span><span class="sxs-lookup"><span data-stu-id="c83e2-190">For example, AWK scripts can be written to filter the function headers into a separate text file that can then serve as the basis for a specification document.</span></span> <span data-ttu-id="c83e2-191">同樣地，Microsoft 開發人員網路開發程式庫 CD-ROM (目前提供的工具，就像是不支援的 AUTODUCK 公用程式一樣) 可以用來處理這些標頭中的批註區塊。</span><span class="sxs-lookup"><span data-stu-id="c83e2-191">Similarly, tools like the unsupported AUTODUCK utility (currently available on the Microsoft Developer Network Development Library CD-ROM) can be used to process the comment blocks in these headers.</span></span>

<span data-ttu-id="c83e2-192">下表列出範例教學課程中所使用的開始和結束權杖字串。</span><span class="sxs-lookup"><span data-stu-id="c83e2-192">The following table lists beginning and ending token strings used in sample tutorials.</span></span>



| <span data-ttu-id="c83e2-193">Token</span><span class="sxs-lookup"><span data-stu-id="c83e2-193">Token</span></span> | <span data-ttu-id="c83e2-194">描述</span><span class="sxs-lookup"><span data-stu-id="c83e2-194">Description</span></span>                      |
|-------|----------------------------------|
| /\*+  | <span data-ttu-id="c83e2-195">檔案標頭開始</span><span class="sxs-lookup"><span data-stu-id="c83e2-195">File Header Begin</span></span>                |
| +\*/  | <span data-ttu-id="c83e2-196">檔案標頭結束</span><span class="sxs-lookup"><span data-stu-id="c83e2-196">File Header End</span></span>                  |
| /\*-  | <span data-ttu-id="c83e2-197">純文字批註區塊標頭開始</span><span class="sxs-lookup"><span data-stu-id="c83e2-197">Plain comment block Header Begin</span></span> |
| -\*/  | <span data-ttu-id="c83e2-198">純文字批註區塊標頭結束</span><span class="sxs-lookup"><span data-stu-id="c83e2-198">Plain comment block Header End</span></span>   |
| <span data-ttu-id="c83e2-199">/\*C</span><span class="sxs-lookup"><span data-stu-id="c83e2-199">/\*C</span></span>  | <span data-ttu-id="c83e2-200">類別標頭開始</span><span class="sxs-lookup"><span data-stu-id="c83e2-200">Class Header Begin</span></span>               |
| <span data-ttu-id="c83e2-201">C\*/</span><span class="sxs-lookup"><span data-stu-id="c83e2-201">C\*/</span></span>  | <span data-ttu-id="c83e2-202">類別標頭結束</span><span class="sxs-lookup"><span data-stu-id="c83e2-202">Class Header End</span></span>                 |
| <span data-ttu-id="c83e2-203">/\*M</span><span class="sxs-lookup"><span data-stu-id="c83e2-203">/\*M</span></span>  | <span data-ttu-id="c83e2-204">方法標頭開始</span><span class="sxs-lookup"><span data-stu-id="c83e2-204">Method Header Begin</span></span>              |
| <span data-ttu-id="c83e2-205">M\*/</span><span class="sxs-lookup"><span data-stu-id="c83e2-205">M\*/</span></span>  | <span data-ttu-id="c83e2-206">方法標頭結束</span><span class="sxs-lookup"><span data-stu-id="c83e2-206">Method Header End</span></span>                |
| <span data-ttu-id="c83e2-207">/\*F</span><span class="sxs-lookup"><span data-stu-id="c83e2-207">/\*F</span></span>  | <span data-ttu-id="c83e2-208">函式標頭開始</span><span class="sxs-lookup"><span data-stu-id="c83e2-208">Function Header Begin</span></span>            |
| <span data-ttu-id="c83e2-209">F\*/</span><span class="sxs-lookup"><span data-stu-id="c83e2-209">F\*/</span></span>  | <span data-ttu-id="c83e2-210">函式標頭結束</span><span class="sxs-lookup"><span data-stu-id="c83e2-210">Function Header End</span></span>              |
| <span data-ttu-id="c83e2-211">/\*我</span><span class="sxs-lookup"><span data-stu-id="c83e2-211">/\*I</span></span>  | <span data-ttu-id="c83e2-212">介面標頭開始</span><span class="sxs-lookup"><span data-stu-id="c83e2-212">Interface Header Begin</span></span>           |
| <span data-ttu-id="c83e2-213">我\*/</span><span class="sxs-lookup"><span data-stu-id="c83e2-213">I\*/</span></span>  | <span data-ttu-id="c83e2-214">介面標頭結束</span><span class="sxs-lookup"><span data-stu-id="c83e2-214">Interface Header End</span></span>             |
| <span data-ttu-id="c83e2-215">/\*輸出</span><span class="sxs-lookup"><span data-stu-id="c83e2-215">/\*O</span></span>  | <span data-ttu-id="c83e2-216">COM 物件類別標頭開始</span><span class="sxs-lookup"><span data-stu-id="c83e2-216">COM Object Class Header Begin</span></span>    |
| <span data-ttu-id="c83e2-217">輸出\*/</span><span class="sxs-lookup"><span data-stu-id="c83e2-217">O\*/</span></span>  | <span data-ttu-id="c83e2-218">COM 物件類別標頭結束</span><span class="sxs-lookup"><span data-stu-id="c83e2-218">COM Object Class Header End</span></span>      |



 

<span data-ttu-id="c83e2-219">這些標頭也可以用來做為快速掃描原始程式檔的視覺提示。</span><span class="sxs-lookup"><span data-stu-id="c83e2-219">These headers can also be used as visual cues for rapid scanning of source files.</span></span> <span data-ttu-id="c83e2-220">如果您在編輯器中設定搜尋字串，然後「重複最後搜尋」來快速找出這些標頭，它們也能方便您快速取得某些來源位置。</span><span class="sxs-lookup"><span data-stu-id="c83e2-220">They also provide convenience for rapidly getting to some source location if you set up search strings in your editor and then 'repeat last search' to quickly locate these headers.</span></span>

<span data-ttu-id="c83e2-221">例如，搜尋字串 "M + M" 會找到方法標頭的開頭，而 "M-M" 將會找出實際方法定義/執行程式碼的開頭。</span><span class="sxs-lookup"><span data-stu-id="c83e2-221">For example, the search string "M+M" will locate the start of method headers, and "M-M" will locate the beginning of the actual method definition/implementation code.</span></span>

 

 




