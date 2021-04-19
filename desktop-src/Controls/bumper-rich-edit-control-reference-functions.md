---
title: Rich Edit 函數
description: Rich Edit 函數
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974808"
---
# <a name="rich-edit-functions"></a><span data-ttu-id="c6fb5-103">Rich Edit 函數</span><span class="sxs-lookup"><span data-stu-id="c6fb5-103">Rich Edit Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6fb5-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="c6fb5-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6fb5-105">主題</span><span class="sxs-lookup"><span data-stu-id="c6fb5-105">Topic</span></span></th>
<th><span data-ttu-id="c6fb5-106">描述</span><span class="sxs-lookup"><span data-stu-id="c6fb5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6fb5-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-108"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a>函式是應用程式定義的回呼函式，可搭配<a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a>訊息使用。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-108">The <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> function is an application-defined callback function that is used with the <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6fb5-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-110"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a>函式是一種應用程式定義的回呼函式，與<a href="em-streamin.md"><strong>EM_STREAMIN</strong></a>和<a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a>的訊息搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-110">The <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> function is an application defined callback function used with the <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> and <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> messages.</span></span> <span data-ttu-id="c6fb5-111">它是用來將資料流程傳入或流出 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-111">It is used to transfer a stream of data into or out of a rich edit control.</span></span> <span data-ttu-id="c6fb5-112"><strong>EDITSTREAMCALLBACK</strong>型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-112">The <strong>EDITSTREAMCALLBACK</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="c6fb5-113"><em>EditStreamCallback</em> 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-113"><em>EditStreamCallback</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6fb5-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-115"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a>函式是搭配<a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a>訊息使用的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-115">The <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> function is an application defined callback function used with the <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> message.</span></span> <span data-ttu-id="c6fb5-116">它會決定文字分隔的字元索引，或字元類別，以及指定文字中字元的字元類別和文字分隔旗標。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-116">It determines the character index of the word break or the character class and word-break flags of the characters in the specified text.</span></span> <span data-ttu-id="c6fb5-117"><strong>EDITWORDBREAKPROCEX</strong>型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-117">The <strong>EDITWORDBREAKPROCEX</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="c6fb5-118"><em>EditWordBreakProcEx</em> 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-118"><em>EditWordBreakProcEx</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6fb5-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-120">抓取 Unicode 轉換格式 (UTF-16) -32 math 英數位元，其對應至指定的基本多語系平面 (BMP) 字元和數學樣式。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-120">Retrieves the Unicode Transformation Format (UTF)-32 math alphanumeric character that corresponds to the specified Basic Multilingual Plane (BMP) character and math style.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6fb5-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-122">抓取數學樣式以及垂直基本多語系平面 (BMP) 字元碼，對應至數學代理配對的指定尾端位元組。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-122">Retrieves the math style and the upright Basic Multilingual Plane (BMP) character code that corresponds to the specified trailing byte of a math surrogate pair.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6fb5-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-124"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a>函式是搭配<a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>訊息使用的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-124">The <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> function is an application defined callback function used with the <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> message.</span></span> <span data-ttu-id="c6fb5-125">它會決定如何在 Microsoft Rich Edit 控制項中完成斷字。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-125">It determines how hyphenation is done in a Microsoft Rich Edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6fb5-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-127">將指定範圍內的內建數學、ruby 和其他内嵌物件轉譯成線性形式。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-127">Translates the built-up math, ruby, and other inline objects in the specified range to linear form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6fb5-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-129">將範圍中的線性格式數學轉換成內建表單，或修改目前的內建表單。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-129">Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6fb5-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-131">轉譯指定範圍內的數學字元。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-131">Translates the math characters in the specified range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6fb5-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6fb5-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span></span><br/></td>
<td><span data-ttu-id="c6fb5-133">註冊兩個類別名稱（REListBox20W 和 RECombobox20W），可用來建立 Rich Edit listbox 或 combobox 視窗。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-133">Registers two class names, REListBox20W and RECombobox20W, that could be used to create Rich Edit listbox or combobox windows.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c6fb5-134">適用于內部用途;不建議在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-134">Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="c6fb5-135">未來的版本可能不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="c6fb5-135">This function may not be supported in future versions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

