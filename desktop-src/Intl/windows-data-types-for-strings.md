---
description: 大部分的字串作業都可以使用 Unicode 和 Windows 字碼頁的相同邏輯。
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: 適用於字串的 Windows 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027574"
---
# <a name="windows-data-types-for-strings"></a><span data-ttu-id="b3eb5-103">適用於字串的 Windows 資料類型</span><span class="sxs-lookup"><span data-stu-id="b3eb5-103">Windows Data Types for Strings</span></span>

<span data-ttu-id="b3eb5-104">大部分的字串作業都可以使用 [Unicode](unicode.md) 和 [Windows 字碼頁](code-pages.md)的相同邏輯。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-104">Most string operations can use the same logic for [Unicode](unicode.md) and for [Windows code pages](code-pages.md).</span></span> <span data-ttu-id="b3eb5-105">唯一的差別在於，基本的運算單位是16位的字元 (也稱為寬字元) 用於 Unicode，而8位字元則適用于 Windows 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-105">The only difference is that the basic unit of operation is a 16-bit character (also known as a wide character) for Unicode and an 8-bit character for Windows code pages.</span></span> <span data-ttu-id="b3eb5-106">Windows 標頭檔提供數種類型定義，可讓您輕鬆地建立可針對 Unicode 或 Windows 字碼頁編譯的來源。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-106">The Windows header files provide several type definitions that make it easy to create sources that can be compiled for Unicode or for Windows code pages.</span></span>

<span data-ttu-id="b3eb5-107">Windows 支援三組字元和字串資料類型：一組可以針對 Unicode 或 Windows 字碼頁編譯的泛型型別定義，以及兩組特定的類型定義。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-107">Windows supports three sets of character and string data types: a set of generic type definitions that can compile for either Unicode or Windows code pages, and two sets of specific type definitions.</span></span> <span data-ttu-id="b3eb5-108">一組特定的型別定義適用于 Unicode，而另一組則是用來搭配 Windows 字碼頁使用。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-108">One set of specific type definitions is for use with Unicode, and the other is for use with Windows code pages.</span></span>

<span data-ttu-id="b3eb5-109">使用泛型資料類型的應用程式只要在標頭檔的 **\# include** 語句之前定義 "unicode"，或在編譯期間定義 "unicode"，就可以針對 Unicode 編譯。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-109">An application using generic data types can be compiled for Unicode simply by defining "UNICODE" before the **\#include** statements for the header files, or during compilation.</span></span> <span data-ttu-id="b3eb5-110">新的 Windows 應用程式應該使用 Unicode 來避免不同字碼頁的不一致，並簡化當地語系化。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-110">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and to simplify localization.</span></span> <span data-ttu-id="b3eb5-111">它們應該以泛型資料類型撰寫，且應該定義 "UNICODE"，以便將這些類型編譯成 Unicode 類型。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-111">They should be written with generic data types, and should define "UNICODE" in order to compile these types into Unicode types.</span></span> <span data-ttu-id="b3eb5-112">在應用程式必須使用8位字元資料的幾個地方，它可以明確地使用 Windows 字碼頁的類型。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-112">In the few places where an application must work with 8-bit character data, it can make explicit use of the types for Windows code pages.</span></span>

<span data-ttu-id="b3eb5-113">將泛型型別編譯成 Windows 字碼頁類型的能力，主要是為了支援繼承應用程式。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-113">The ability to compile the generic types into types for Windows code pages exists mainly to support legacy applications.</span></span> <span data-ttu-id="b3eb5-114">若要針對 Windows 字碼頁進行編譯，應用程式只會省略 UNICODE 定義。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-114">To compile for Windows code pages, the application just omits the UNICODE definition.</span></span>

<span data-ttu-id="b3eb5-115">下列範例顯示 Windows 標頭檔中用來定義三組資料類型的方法。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-115">The following example shows the method used in the Windows header files to define the three sets of data types.</span></span> <span data-ttu-id="b3eb5-116">若要執行此程式，請參閱 Winnt 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-116">For the implementation, see the Winnt.h header file.</span></span>


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



<span data-ttu-id="b3eb5-117">類型定義中的字母 "T" （例如，TCHAR 或 LPTSTR）會指定可針對 Windows 字碼頁或 Unicode 編譯的泛型型別。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-117">The letter "T" in a type definition, for example, TCHAR or LPTSTR, designates a generic type that can be compiled for either Windows code pages or Unicode.</span></span> <span data-ttu-id="b3eb5-118">型別定義中的字母 "W" （例如，WCHAR 或 LPWSTR）會指定 Unicode 型別。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-118">The letter "W" in a type definition, for example, WCHAR or LPWSTR, designates a Unicode type.</span></span> <span data-ttu-id="b3eb5-119">由於 Windows 字碼頁的格式較舊，因此它們具有簡單的型別定義，例如 CHAR 和 LPSTR。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-119">Because Windows code pages are of the older form, they have simple type definitions, such as CHAR and LPSTR.</span></span> <span data-ttu-id="b3eb5-120">如需 Windows 中資料類型的完整說明，請參閱 [Windows 資料類型](../winprog/windows-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b3eb5-120">For a complete description of data types in Windows, see [Windows Data Types](../winprog/windows-data-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3eb5-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3eb5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3eb5-122">Windows API 中的 Unicode</span><span class="sxs-lookup"><span data-stu-id="b3eb5-122">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
