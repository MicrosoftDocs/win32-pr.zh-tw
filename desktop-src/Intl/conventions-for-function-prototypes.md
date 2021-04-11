---
description: Windows SDK 在泛型、Windows 字碼頁和 Unicode 版本中提供函式原型。
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: 函數原型的慣例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849484"
---
# <a name="conventions-for-function-prototypes"></a><span data-ttu-id="f664d-103">函數原型的慣例</span><span class="sxs-lookup"><span data-stu-id="f664d-103">Conventions for Function Prototypes</span></span>

<span data-ttu-id="f664d-104">Windows SDK 在泛型、 [Windows 字碼頁](code-pages.md)和 [Unicode](unicode.md) 版本中提供函式原型。</span><span class="sxs-lookup"><span data-stu-id="f664d-104">The Windows SDK provides function prototypes in generic, [Windows code page](code-pages.md), and [Unicode](unicode.md) versions.</span></span> <span data-ttu-id="f664d-105">您可以編譯原型來產生 Windows 字碼頁原型或 Unicode 原型。</span><span class="sxs-lookup"><span data-stu-id="f664d-105">The prototypes can be compiled to produce either Windows code page prototypes or Unicode prototypes.</span></span> <span data-ttu-id="f664d-106">本主題將討論這三個原型，並使用 [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) 函式的程式碼範例來說明。</span><span class="sxs-lookup"><span data-stu-id="f664d-106">All three prototypes are discussed in this topic and are illustrated by code samples for the [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) function.</span></span>

<span data-ttu-id="f664d-107">以下是泛用原型的範例。</span><span class="sxs-lookup"><span data-stu-id="f664d-107">The following is an example of a generic prototype.</span></span>


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



<span data-ttu-id="f664d-108">標頭檔提供了實作成巨集的泛用函數名稱。</span><span class="sxs-lookup"><span data-stu-id="f664d-108">The header file provides the generic function name implemented as a macro.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



<span data-ttu-id="f664d-109">預處理器會將宏擴充到 Windows 程式字碼頁或 Unicode 函數名稱。</span><span class="sxs-lookup"><span data-stu-id="f664d-109">The preprocessor expands the macro into either the Windows code page or Unicode function name.</span></span> <span data-ttu-id="f664d-110">您可以視需要在泛型函式名稱的結尾加上字母 "A" (ANSI) 或 "W" (Unicode) 。</span><span class="sxs-lookup"><span data-stu-id="f664d-110">The letter "A" (ANSI) or "W" (Unicode) is added at the end of the generic function name, as appropriate.</span></span> <span data-ttu-id="f664d-111">標頭檔會提供兩個特定的原型，一個用於 Windows 字碼頁，另一個用於 Unicode，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="f664d-111">The header file then provides two specific prototypes, one for Windows code pages and one for Unicode, as shown in the following examples.</span></span>


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



<span data-ttu-id="f664d-112">如同適用于 [字串的 Windows 資料類型](windows-data-types-for-strings.md)中所述，泛型函式原型會使用 text 參數的資料類型 LPCTSTR。</span><span class="sxs-lookup"><span data-stu-id="f664d-112">As explained in [Windows Data Types for Strings](windows-data-types-for-strings.md), the generic function prototype uses the data type LPCTSTR for the text parameter.</span></span> <span data-ttu-id="f664d-113">不過，Windows 字碼頁原型是使用 LPCSTR 類型，而 Unicode 原型則使用 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="f664d-113">However, the Windows code page prototype uses the type LPCSTR, and the Unicode prototype uses LPCWSTR.</span></span>

<span data-ttu-id="f664d-114">凡是具有文字引數的任何函數，應用程式通常都應使用泛用函數原型。</span><span class="sxs-lookup"><span data-stu-id="f664d-114">For all functions with text arguments, applications should normally use the generic function prototypes.</span></span> <span data-ttu-id="f664d-115">如果應用程式在標頭檔的 **\# include** 語句之前或編譯期間定義 "UNICODE"，語句將會編譯成 UNICODE 函式。</span><span class="sxs-lookup"><span data-stu-id="f664d-115">If an application defines "UNICODE" either before the **\#include** statements for the header files or during compilation, the statements will be compiled into Unicode functions.</span></span>

> [!Note]  
> <span data-ttu-id="f664d-116">新的 Windows 應用程式應該使用 Unicode 來避免不同的程式字碼頁不一致，並方便當地語系化。</span><span class="sxs-lookup"><span data-stu-id="f664d-116">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="f664d-117">它們應該以泛型函式撰寫，且應該定義 UNICODE 以將函式編譯成 Unicode 函數。</span><span class="sxs-lookup"><span data-stu-id="f664d-117">They should be written with generic functions, and should define UNICODE to compile the functions into Unicode functions.</span></span> <span data-ttu-id="f664d-118">在應用程式必須使用8位字元資料的幾個地方，它可以明確使用 Windows 字碼頁的函式。</span><span class="sxs-lookup"><span data-stu-id="f664d-118">In the few places where an application must work with 8-bit character data, it can make explicit use of the functions for Windows code pages.</span></span>

 

<span data-ttu-id="f664d-119">您的應用程式應該一律使用泛用函數原型搭配泛用字串和字元類型。</span><span class="sxs-lookup"><span data-stu-id="f664d-119">Your application should always use a generic function prototype with the generic string and character types.</span></span> <span data-ttu-id="f664d-120">名稱以大寫 "W" 結尾的所有函數都是採用 Unicode (即寬字元) 參數。</span><span class="sxs-lookup"><span data-stu-id="f664d-120">All function names that end with an uppercase "W" take Unicode, that is, wide character, parameters.</span></span> <span data-ttu-id="f664d-121">某些函式只存在於 Unicode 版本中，而且只能搭配適當的資料類型使用。</span><span class="sxs-lookup"><span data-stu-id="f664d-121">Some functions exist only in Unicode versions and can be used only with the appropriate data types.</span></span> <span data-ttu-id="f664d-122">例如， [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) 和 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 只有 Unicode 版本。</span><span class="sxs-lookup"><span data-stu-id="f664d-122">For example, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) and [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) have only Unicode versions.</span></span>

<span data-ttu-id="f664d-123">每個 Unicode 和字元集函式的參考檔中的需求一節提供支援的作業系統所執行之函式版本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f664d-123">The Requirements section in the reference documentation for each Unicode and character set function provides information on the function versions implemented by supported operating systems.</span></span> <span data-ttu-id="f664d-124">如果包含開頭為 "Unicode" 的行，則函式會有個別的 Unicode 和 Windows 字碼頁版本。</span><span class="sxs-lookup"><span data-stu-id="f664d-124">If a line beginning with "Unicode" is included, the function has separate Unicode and Windows code page versions.</span></span>

> [!Note]  
> <span data-ttu-id="f664d-125">當函數具有字元字串的長度參數時，長度應該記錄為字串中的 TCHAR 值計數。</span><span class="sxs-lookup"><span data-stu-id="f664d-125">When a function has a length parameter for a character string, the length should be documented as a count of TCHAR values in the string.</span></span> <span data-ttu-id="f664d-126">這種資料類型是指函式的 Windows 字碼頁版本或 Unicode 版本的16位單字的位元組。</span><span class="sxs-lookup"><span data-stu-id="f664d-126">This data type refers to bytes for Windows code page versions of the function or 16-bit words for Unicode versions.</span></span> <span data-ttu-id="f664d-127">不過，需要或傳回非類型記憶體區塊（例如 [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) 函式）之指標的函式通常會以位元組為單位，而不論使用的原型為何。</span><span class="sxs-lookup"><span data-stu-id="f664d-127">However, functions that require or return pointers to untyped memory blocks, such as the [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) function, generally take a size in bytes, regardless of the prototype that is used.</span></span> <span data-ttu-id="f664d-128">如果不具類型的記憶體配置是針對字串，則應用程式必須將字元數乘以 sizeof (TCHAR) 。</span><span class="sxs-lookup"><span data-stu-id="f664d-128">If the allocation of untyped memory is for a string, the application must multiply the number of characters by sizeof(TCHAR).</span></span> <span data-ttu-id="f664d-129">如需詳細資訊，請參閱 [使用泛型資料類型](using-generic-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f664d-129">For additional information, see [Using Generic Data Types](using-generic-data-types.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f664d-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="f664d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f664d-131">Windows API 中的 Unicode</span><span class="sxs-lookup"><span data-stu-id="f664d-131">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
