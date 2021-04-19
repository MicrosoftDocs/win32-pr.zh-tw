---
description: 如果您在程式碼中使用泛型資料類型，則可以使用預處理器指示詞來定義 &0034，以針對 Unicode 進行編譯： \#UNICODE&\# 0034; 在 \# 標頭檔的 include 語句之前。
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: 使用泛型資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976592"
---
# <a name="using-generic-data-types"></a><span data-ttu-id="83d00-103">使用泛型資料類型</span><span class="sxs-lookup"><span data-stu-id="83d00-103">Using Generic Data Types</span></span>

<span data-ttu-id="83d00-104">如果您在程式碼中使用泛型資料類型，則可以使用預處理器指示詞，在標頭檔的 **\# include** 語句之前定義 "unicode"，以編譯 [Unicode](unicode.md) 。</span><span class="sxs-lookup"><span data-stu-id="83d00-104">If you use generic data types in your code, it can be compiled for [Unicode](unicode.md) simply by using a preprocessor directive to define "UNICODE" before the **\#include** statements for the header files.</span></span> <span data-ttu-id="83d00-105">若要編譯 [Windows (ANSI) 字碼頁](code-pages.md)的程式碼，請省略 "UNICODE" 定義。</span><span class="sxs-lookup"><span data-stu-id="83d00-105">To compile the code for [Windows (ANSI) code pages](code-pages.md), omit the "UNICODE" definition.</span></span> <span data-ttu-id="83d00-106">新的 Windows 應用程式應該使用 Unicode 來避免不同字碼頁的不一致，並簡化當地語系化。</span><span class="sxs-lookup"><span data-stu-id="83d00-106">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and simplify localization.</span></span>

<span data-ttu-id="83d00-107">若要建立可編譯成使用 Unicode 字元和字串，或從 Windows 字碼頁使用字元和字串的原始程式碼：</span><span class="sxs-lookup"><span data-stu-id="83d00-107">To create source code that can be compiled either to use Unicode characters and strings or to use characters and strings from Windows code pages:</span></span>

1.  <span data-ttu-id="83d00-108">針對文字所使用的所有字元和字串類型使用泛型資料類型，例如 TCHAR、LPTSTR 和 LPTCH。</span><span class="sxs-lookup"><span data-stu-id="83d00-108">Use generic data types, such as TCHAR, LPTSTR, and LPTCH, for all character and string types used for text.</span></span> <span data-ttu-id="83d00-109">如需泛型型別的詳細資訊，請參閱 [Windows 資料類型的字串](windows-data-types-for-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="83d00-109">For more about generic types, see [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span>
2.  <span data-ttu-id="83d00-110">請確定非文字資料緩衝區或二進位位元組陣列的指標會以資料類型（例如 LPBYTE 或 LPWORD）進行編碼，而不是使用 LPTSTR 或 LPTCH 類型。</span><span class="sxs-lookup"><span data-stu-id="83d00-110">Be sure that pointers to non-text data buffers or binary byte arrays are coded with data types such as LPBYTE or LPWORD, instead of the LPTSTR or LPTCH type.</span></span>
3.  <span data-ttu-id="83d00-111">適當地使用 LPVOID，將不定類型的指標明確宣告為 void 指標。</span><span class="sxs-lookup"><span data-stu-id="83d00-111">Declare pointers of indeterminate type explicitly as void pointers by using LPVOID as appropriate.</span></span>
4.  <span data-ttu-id="83d00-112">將指標算術類型設為獨立。</span><span class="sxs-lookup"><span data-stu-id="83d00-112">Make pointer arithmetic type-independent.</span></span> <span data-ttu-id="83d00-113">如果已定義 UNICODE，則使用 TCHAR 大小的單位會產生2個位元組的變數，而如果未定義 UNICODE，則會產生1個位元組。</span><span class="sxs-lookup"><span data-stu-id="83d00-113">Using units of TCHAR size yields variables that are 2 bytes if UNICODE is defined, and 1 byte if UNICODE is not defined.</span></span> <span data-ttu-id="83d00-114">如果元素的大小為1或2個位元組，使用指標算術一律會傳回指標所指出的元素數目。</span><span class="sxs-lookup"><span data-stu-id="83d00-114">Using pointer arithmetic always returns the number of elements indicated by the pointer, whether the elements are 1 or 2 bytes in size.</span></span> <span data-ttu-id="83d00-115">下列運算式一律會抓取專案數目，而不論是否已定義 UNICODE。</span><span class="sxs-lookup"><span data-stu-id="83d00-115">The following expression always retrieves the number of elements, regardless of whether UNICODE is defined.</span></span>

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    <span data-ttu-id="83d00-116">下列運算式會決定所使用的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="83d00-116">The following expression determines the number of bytes used.</span></span>

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    <span data-ttu-id="83d00-117">不需要變更如下的語句，因為指標遞增指向下一個字元元素。</span><span class="sxs-lookup"><span data-stu-id="83d00-117">There is no need to change a statement like the following one, because the pointer increment points to the next character element.</span></span>

    ```C++
    chNext = *++lpText;
    ```

    

5.  <span data-ttu-id="83d00-118">使用宏取代常值字串和資訊清單字元常數。</span><span class="sxs-lookup"><span data-stu-id="83d00-118">Replace literal strings and manifest character constants with macros.</span></span> <span data-ttu-id="83d00-119">變更運算式，如下所示。</span><span class="sxs-lookup"><span data-stu-id="83d00-119">Change expressions like the following one.</span></span>

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    <span data-ttu-id="83d00-120">在此運算式中使用 [**文字**](/windows/desktop/api/Winnt/nf-winnt-text) 宏，如下所示。</span><span class="sxs-lookup"><span data-stu-id="83d00-120">Use the [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro as follows in this expression.</span></span>

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    <span data-ttu-id="83d00-121">在定義 UNICODE 時， [**文字**](/windows/desktop/api/Winnt/nf-winnt-text) 宏會將字串評估為 L "string"，否則會是 "string"。</span><span class="sxs-lookup"><span data-stu-id="83d00-121">The [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro causes strings to be evaluated as L"string" when UNICODE is defined, and as "string" otherwise.</span></span> <span data-ttu-id="83d00-122">為了更容易管理，請將常值字串移至資源，特別是如果它們包含 ASCII 範圍以外的字元 (0x00 到 0x7F) 或在使用者介面公開。</span><span class="sxs-lookup"><span data-stu-id="83d00-122">For easier management, move literal strings into resources, especially if they contain characters outside the ASCII range (0x00 through 0x7F) or are exposed at the user interface.</span></span> <span data-ttu-id="83d00-123">為了針對不同國語言支援您應用程式的當地語系化，所有使用者介面字串都必須在可當地語系化的資源中，這點非常重要。</span><span class="sxs-lookup"><span data-stu-id="83d00-123">To support localization of your application for different national languages, it is very important for all user interface strings to be in localizable resources.</span></span>

6.  <span data-ttu-id="83d00-124">使用 Windows 函數的一般版本。</span><span class="sxs-lookup"><span data-stu-id="83d00-124">Use the generic versions of the Windows functions.</span></span> <span data-ttu-id="83d00-125">如需詳細資訊，請參閱 [函數原型的慣例](conventions-for-function-prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="83d00-125">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>
7.  <span data-ttu-id="83d00-126">使用標準 C 程式庫字串函式的泛型版本，並記得定義 " \_ unicode" 和 "unicode"，如 [標準 c](standard-c-functions.md)函式中所述。</span><span class="sxs-lookup"><span data-stu-id="83d00-126">Use the generic versions of the standard C library string functions, and remember to define "\_UNICODE" as well as "UNICODE", as discussed in [Standard C Functions](standard-c-functions.md).</span></span>
8.  <span data-ttu-id="83d00-127">如果您要調整原本針對 Windows 字碼頁所撰寫的應用程式，請記得將任何依賴255的程式碼變更為最大的字元值。</span><span class="sxs-lookup"><span data-stu-id="83d00-127">If you are adapting an application originally written for Windows code pages, remember to change any code that relies on 255 as the largest value for a character.</span></span>

<span data-ttu-id="83d00-128">當您編譯如上面所述撰寫的程式碼時，編譯器可以從相同來源同時建立 Unicode 和 Windows 字碼頁版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="83d00-128">When you compile code that you have written as outlined above, the compiler can create both Unicode and Windows code page versions of your application from the same source.</span></span> <span data-ttu-id="83d00-129">根據 UNICODE 的定義，會解析泛型函式來產生相同的二進位檔案，就像您針對 Unicode 或專門針對 Windows 字碼頁撰寫程式碼一樣。</span><span class="sxs-lookup"><span data-stu-id="83d00-129">Depending on the definitions for UNICODE, the generic functions are resolved to produce the same binary files as if you wrote code exclusively for Unicode or exclusively for Windows code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83d00-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="83d00-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83d00-131">使用 Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="83d00-131">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



