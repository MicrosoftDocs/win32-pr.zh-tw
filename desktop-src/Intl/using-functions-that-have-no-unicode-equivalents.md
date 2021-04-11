---
description: 尚未使用 Unicode 版本執行的函式，通常是由支援 Unicode 的功能強大或擴充函數所取代。
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: 使用沒有 Unicode 對應項的函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195436"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a><span data-ttu-id="37137-103">使用沒有 Unicode 對應項的函式</span><span class="sxs-lookup"><span data-stu-id="37137-103">Using Functions That Have No Unicode Equivalents</span></span>

<span data-ttu-id="37137-104">尚未使用 [unicode](unicode.md) 版本執行的函式，通常是由支援 unicode 的功能強大或擴充函數所取代。</span><span class="sxs-lookup"><span data-stu-id="37137-104">Functions that have not been implemented with a [Unicode](unicode.md) version have typically been replaced by more powerful or extended functions that do support Unicode.</span></span> <span data-ttu-id="37137-105">例如，如果您正在移植呼叫 [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) 函式的程式碼，則您的應用程式可以改為使用 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數來支援 Unicode。</span><span class="sxs-lookup"><span data-stu-id="37137-105">For example, if you are porting code that calls the [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) function, your application can support Unicode by using the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function instead.</span></span>

<span data-ttu-id="37137-106">如果函式沒有 Unicode 對等專案，應用程式可以在函式呼叫之前和之後，將字元對應到8位字元集。</span><span class="sxs-lookup"><span data-stu-id="37137-106">If a function has no Unicode equivalent, the application can map characters to and from 8-bit character sets before and after the function call.</span></span> <span data-ttu-id="37137-107">例如，數位格式函式 **atoi** 和 **itoa** 只會使用數位0到9。</span><span class="sxs-lookup"><span data-stu-id="37137-107">For example, the number-formatting functions **atoi** and **itoa** use only the digits 0 through 9.</span></span> <span data-ttu-id="37137-108">一般來說，將 Unicode 對應到8位的字元會造成資料遺失，但藉由讓程式碼類型獨立，並讓運算式成為條件式，可避免這種情形。</span><span class="sxs-lookup"><span data-stu-id="37137-108">Normally, mapping Unicode to 8-bit characters causes loss of data, but this can be avoided by making the code type-independent and making the expressions conditional.</span></span> <span data-ttu-id="37137-109">下列範例中，針對8位字元所撰寫的語句會與型別相依，而且應該變更為支援 Unicode。</span><span class="sxs-lookup"><span data-stu-id="37137-109">The statements in the following example, written for 8-bit characters, are type-dependent and should be changed to support Unicode.</span></span>


```C++
char str[4] = "137";

int num = atoi(str);
```



<span data-ttu-id="37137-110">您可以依照下列方式重寫這些語句，使其與型別無關。</span><span class="sxs-lookup"><span data-stu-id="37137-110">These statements can be rewritten as follows to make them type-independent.</span></span>


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



<span data-ttu-id="37137-111">在此範例中，標準 C 程式庫函式 **wcstombs** 會將 Unicode 轉換成 ASCII。</span><span class="sxs-lookup"><span data-stu-id="37137-111">In this example, the standard C library function **wcstombs** translates Unicode to ASCII.</span></span> <span data-ttu-id="37137-112">此範例的事實是，即使某些周圍文字無法使用，數位0到9也可以永遠從 Unicode 轉譯成 ASCII。</span><span class="sxs-lookup"><span data-stu-id="37137-112">The example relies on the fact that the digits 0 through 9 can always be translated from Unicode to ASCII, even if some of the surrounding text cannot.</span></span> <span data-ttu-id="37137-113">**Atoi** 函式會在非數位的任何字元上停止。</span><span class="sxs-lookup"><span data-stu-id="37137-113">The **atoi** function stops at any character that is not a digit.</span></span>

<span data-ttu-id="37137-114">您的應用程式可以使用 (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) 函式的國家語言支援，來處理包含 Unicode 中某些腳本提供之 [原生數位](digit-shapes.md) 的文字。</span><span class="sxs-lookup"><span data-stu-id="37137-114">Your application can use the National Language Support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) function to process text that includes the [native digits](digit-shapes.md) provided for some of the scripts in Unicode.</span></span>

> [!Caution]  
> <span data-ttu-id="37137-115">使用 **wcstombs** 函式不正確，可能會危及應用程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="37137-115">Using the **wcstombs** function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="37137-116">請確定8位字元字串的應用程式緩衝區至少為大小 2 \* (*字元 \_ 長度* + 1) ，其中 *char \_ 長度* 代表 Unicode 字串的長度。</span><span class="sxs-lookup"><span data-stu-id="37137-116">Make sure that the application buffer for the string of 8-bit characters is at least of size 2\*(*char\_length* +1), where *char\_length* represents the length of the Unicode string.</span></span> <span data-ttu-id="37137-117">這項限制的原因是，使用 [雙位元組字元集](double-byte-character-sets.md) (dbcs) ，每個 Unicode 字元都可以對應到兩個連續的8位字元。</span><span class="sxs-lookup"><span data-stu-id="37137-117">This restriction is made because, with [double-byte character sets](double-byte-character-sets.md) (DBCSs), each Unicode character can be mapped to two consecutive 8-bit characters.</span></span> <span data-ttu-id="37137-118">如果緩衝區未保留整個字串，則結果字串不會以 null 結束，因而產生安全性風險。</span><span class="sxs-lookup"><span data-stu-id="37137-118">If the buffer does not hold the entire string, the result string is not null-terminated, posing a security risk.</span></span> <span data-ttu-id="37137-119">如需應用程式安全性的詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="37137-119">For more information about application security, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="37137-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="37137-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37137-121">使用 Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="37137-121">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
