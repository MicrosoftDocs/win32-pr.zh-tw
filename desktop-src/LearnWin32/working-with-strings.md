---
title: 處理字串
description: 處理字串
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110966"
---
# <a name="working-with-strings"></a><span data-ttu-id="ec23d-103">處理字串</span><span class="sxs-lookup"><span data-stu-id="ec23d-103">Working with Strings</span></span>

<span data-ttu-id="ec23d-104">Windows 原本就支援 UI 元素、檔案名等等的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="ec23d-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="ec23d-105">Unicode 是慣用的字元編碼，因為它支援所有字元集和語言。</span><span class="sxs-lookup"><span data-stu-id="ec23d-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="ec23d-106">Windows 代表使用 UTF-16 編碼的 Unicode 字元，其中每個字元會編碼為16位值。</span><span class="sxs-lookup"><span data-stu-id="ec23d-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="ec23d-107">UTF-16 字元稱為 *寬* 字元，用來區別8位的 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="ec23d-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="ec23d-108">Visual C++ 編譯器支援內建資料類型 **wchar \_ t** 的寬字元。</span><span class="sxs-lookup"><span data-stu-id="ec23d-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="ec23d-109">標頭檔中的標頭檔也會定義下列 **typedef**。</span><span class="sxs-lookup"><span data-stu-id="ec23d-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="ec23d-110">您會在 MSDN 範例程式碼中看到這兩個版本。</span><span class="sxs-lookup"><span data-stu-id="ec23d-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="ec23d-111">若要宣告寬字元常值或寬字元字串常值，請在常值前面加上 **L** 。</span><span class="sxs-lookup"><span data-stu-id="ec23d-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="ec23d-112">以下是您將會看到的一些其他字串相關 typedef：</span><span class="sxs-lookup"><span data-stu-id="ec23d-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="ec23d-113">Typedef</span><span class="sxs-lookup"><span data-stu-id="ec23d-113">Typedef</span></span>                   | <span data-ttu-id="ec23d-114">定義</span><span class="sxs-lookup"><span data-stu-id="ec23d-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="ec23d-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="ec23d-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="ec23d-116">**PSTR** 或 **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="ec23d-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="ec23d-117">**PCSTR** 或 **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="ec23d-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="ec23d-118">**PWSTR** 或 **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ec23d-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="ec23d-119">**PCWSTR** 或 **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ec23d-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="ec23d-120">Unicode 和 ANSI 函數</span><span class="sxs-lookup"><span data-stu-id="ec23d-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="ec23d-121">當 Microsoft 對 Windows 引進 Unicode 支援時，它會藉由提供兩組平行的 Api （一個用於 ANSI 字串，另一個用於 Unicode 字串）來分階段減緩轉換。</span><span class="sxs-lookup"><span data-stu-id="ec23d-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="ec23d-122">例如，有兩個函數可設定視窗標題列的文字：</span><span class="sxs-lookup"><span data-stu-id="ec23d-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="ec23d-123">**SetWindowTextA** 會採用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="ec23d-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="ec23d-124">**SetWindowTextW** 會採用 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="ec23d-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="ec23d-125">就內部而言，ANSI 版本會將字串轉譯成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="ec23d-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="ec23d-126">在定義預處理器符號或 ANSI 版本時，Windows 標頭也會定義可解析為 Unicode 版本的宏 `UNICODE` 。</span><span class="sxs-lookup"><span data-stu-id="ec23d-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="ec23d-127">在 MSDN 中，此函式會記錄在名稱 [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)底下，雖然這實際上是宏名稱，而不是實際的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="ec23d-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="ec23d-128">新的應用程式應該一律呼叫 Unicode 版本。</span><span class="sxs-lookup"><span data-stu-id="ec23d-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="ec23d-129">許多世界語言都需要 Unicode。</span><span class="sxs-lookup"><span data-stu-id="ec23d-129">Many world languages require Unicode.</span></span> <span data-ttu-id="ec23d-130">如果您使用 ANSI 字串，就不可能將應用程式當地語系化。</span><span class="sxs-lookup"><span data-stu-id="ec23d-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="ec23d-131">ANSI 版本的效率也較低，因為作業系統必須在執行時間將 ANSI 字串轉換為 Unicode。</span><span class="sxs-lookup"><span data-stu-id="ec23d-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="ec23d-132">根據您的喜好設定，您可以明確地呼叫 Unicode 函式（例如 **SetWindowTextW**），或使用宏。</span><span class="sxs-lookup"><span data-stu-id="ec23d-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="ec23d-133">MSDN 上的範例程式碼通常會呼叫宏，但這兩種形式完全相等。</span><span class="sxs-lookup"><span data-stu-id="ec23d-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="ec23d-134">Windows 中最新的 Api 只有 Unicode 版本，沒有對應的 ANSI 版本。</span><span class="sxs-lookup"><span data-stu-id="ec23d-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="ec23d-135">TCHARs</span><span class="sxs-lookup"><span data-stu-id="ec23d-135">TCHARs</span></span>

<span data-ttu-id="ec23d-136">回到需要同時支援 Windows NT 以及 Windows 95、Windows 98 和 Windows Me 的應用程式時，視目標平臺而定，針對 ANSI 或 Unicode 字串編譯相同的程式碼會很有用。</span><span class="sxs-lookup"><span data-stu-id="ec23d-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="ec23d-137">至此，Windows SDK 提供宏將字串對應至 Unicode 或 ANSI （視平臺而定）。</span><span class="sxs-lookup"><span data-stu-id="ec23d-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="ec23d-138">巨集</span><span class="sxs-lookup"><span data-stu-id="ec23d-138">Macro</span></span>     | <span data-ttu-id="ec23d-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="ec23d-139">Unicode</span></span>   | <span data-ttu-id="ec23d-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="ec23d-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="ec23d-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="ec23d-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="ec23d-142">TEXT ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="ec23d-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="ec23d-143">例如，下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="ec23d-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="ec23d-144">解析成下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="ec23d-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="ec23d-145">由於所有應用程式都應該使用 Unicode，因此 **TEXT** 和 **TCHAR** 宏目前較不實用。</span><span class="sxs-lookup"><span data-stu-id="ec23d-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="ec23d-146">不過，您可能會在較舊的程式碼和一些 MSDN 程式碼範例中看到它們。</span><span class="sxs-lookup"><span data-stu-id="ec23d-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="ec23d-147">Microsoft C 執行時間程式庫的標頭會定義一組類似的宏。</span><span class="sxs-lookup"><span data-stu-id="ec23d-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="ec23d-148">例如，如果未定義， **\_ tcslen** 會解析為 **strlen** `_UNICODE` ; 否則會解析為 **wcslen**，也就是寬字元版本的 **strlen**。</span><span class="sxs-lookup"><span data-stu-id="ec23d-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="ec23d-149">請小心：某些標頭會使用預處理器符號，其他標頭則會搭配 `UNICODE` `_UNICODE` 底線前置詞使用。</span><span class="sxs-lookup"><span data-stu-id="ec23d-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="ec23d-150">一律定義這兩個符號。</span><span class="sxs-lookup"><span data-stu-id="ec23d-150">Always define both symbols.</span></span> <span data-ttu-id="ec23d-151">Visual C++ 在建立新專案時，預設會設定這些專案。</span><span class="sxs-lookup"><span data-stu-id="ec23d-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="ec23d-152">下一個</span><span class="sxs-lookup"><span data-stu-id="ec23d-152">Next</span></span>

[<span data-ttu-id="ec23d-153">什麼是視窗？</span><span class="sxs-lookup"><span data-stu-id="ec23d-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 
