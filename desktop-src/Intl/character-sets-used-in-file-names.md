---
description: NTFS 會以 Unicode 儲存檔案名。 相反地，較舊的 FAT12、FAT16 和 FAT32 檔案系統會使用 OEM 字元集。 如需詳細資訊，請參閱字碼頁。
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: 檔案名中使用的字元集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849988"
---
# <a name="character-sets-used-in-file-names"></a><span data-ttu-id="64bc2-105">檔案名中使用的字元集</span><span class="sxs-lookup"><span data-stu-id="64bc2-105">Character Sets Used in File Names</span></span>

<span data-ttu-id="64bc2-106">NTFS 會以 Unicode 儲存檔案名。</span><span class="sxs-lookup"><span data-stu-id="64bc2-106">NTFS stores file names in Unicode.</span></span> <span data-ttu-id="64bc2-107">相反地，較舊的 FAT12、FAT16 和 FAT32 檔案系統會使用 OEM 字元集。</span><span class="sxs-lookup"><span data-stu-id="64bc2-107">In contrast, the older FAT12, FAT16, and FAT32 file systems use the OEM character set.</span></span> <span data-ttu-id="64bc2-108">如需詳細資訊，請參閱[字碼頁](code-pages.md)。</span><span class="sxs-lookup"><span data-stu-id="64bc2-108">For more information, see [Code Pages](code-pages.md).</span></span>

<span data-ttu-id="64bc2-109">建立 FAT 檔案的非 Unicode 應用程式有時必須使用標準的 C 執行時間程式庫轉換函式，在 Windows 字碼頁字元集和 OEM 字碼頁字元集之間轉譯。</span><span class="sxs-lookup"><span data-stu-id="64bc2-109">Non-Unicode applications that create FAT files sometimes have to use the standard C runtime library conversion functions to translate between the Windows code page character set and the OEM code page character set.</span></span> <span data-ttu-id="64bc2-110">使用檔案系統函式的 Unicode 實作為，就不需要執行這類的翻譯。</span><span class="sxs-lookup"><span data-stu-id="64bc2-110">With Unicode implementations of the file system functions, it is not necessary to perform such translations.</span></span>

<span data-ttu-id="64bc2-111">您的應用程式可以使用泛型字串類型，如 [Windows 資料類型中的字串](windows-data-types-for-strings.md)所述。</span><span class="sxs-lookup"><span data-stu-id="64bc2-111">Your application can use generic string types, as described in [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span> <span data-ttu-id="64bc2-112">應用程式也可以使用函式 [原型慣例](conventions-for-function-prototypes.md)中所述的技術來使用泛型函數原型。</span><span class="sxs-lookup"><span data-stu-id="64bc2-112">The application can also use generic function prototypes using techniques described in [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span> <span data-ttu-id="64bc2-113">針對泛型字串類型或泛型函式原型，您的應用程式可以使用單一原始程式檔來編譯 Unicode 或非 Unicode 版本。</span><span class="sxs-lookup"><span data-stu-id="64bc2-113">For either generic string types or generic function prototypes, your application can use a single source file to compile either a Unicode or a non-Unicode version.</span></span> <span data-ttu-id="64bc2-114">為了允許這樣做，應用程式會針對在編譯 Unicode 時未叫用的函式提供宏。</span><span class="sxs-lookup"><span data-stu-id="64bc2-114">To allow for this, the application provides macros for functions that are not invoked when compiling for Unicode.</span></span>

<span data-ttu-id="64bc2-115">在 NTFS 和 FAT 檔案系統中，特殊檔案名字元是： ' \\ '、'/'、'. '、'？ ' 和 ' \* '。</span><span class="sxs-lookup"><span data-stu-id="64bc2-115">In both NTFS and FAT file systems, the special file name characters are: '\\', '/', '.', '?', and '\*'.</span></span> <span data-ttu-id="64bc2-116">在 OEM 字碼頁上，這些特殊字元是在字元的 ASCII 範圍內 (0x00 到 0x7F) 。</span><span class="sxs-lookup"><span data-stu-id="64bc2-116">On OEM code pages, these special characters are in the ASCII range of characters (0x00 through 0x7F).</span></span> <span data-ttu-id="64bc2-117">其 Unicode 對等專案是2位元組形式的相同值，0x0000 至0x007F。</span><span class="sxs-lookup"><span data-stu-id="64bc2-117">Their Unicode equivalents are the same values in a 2-byte form, 0x0000 through 0x007F.</span></span>

> [!Caution]  
> <span data-ttu-id="64bc2-118">在日文版作業系統上使用的 Windows 字碼頁和 OEM 字碼頁字元集，包含日元符號 (¥) ，而不是反斜線 (\\) 。</span><span class="sxs-lookup"><span data-stu-id="64bc2-118">Windows code page and OEM code page character sets used on Japanese-language operating systems contain the Yen symbol (¥) instead of a backslash (\\).</span></span> <span data-ttu-id="64bc2-119">因此，日元符號是 NTFS 和 FAT 檔案系統禁止使用的字元。</span><span class="sxs-lookup"><span data-stu-id="64bc2-119">Thus, the Yen symbol is a prohibited character for NTFS and FAT file systems.</span></span> <span data-ttu-id="64bc2-120">當將 Unicode 對應至日文語言字碼頁時， [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 和其他轉換函式會將反斜線 (U + 005C) 和一般 Unicode 日元符號 (u + 00A5) 轉換成這個相同的字元。</span><span class="sxs-lookup"><span data-stu-id="64bc2-120">When mapping Unicode to a Japanese-language code page, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and other conversion functions map both backslash (U+005C) and the normal Unicode Yen symbol (U+00A5) to this same character.</span></span> <span data-ttu-id="64bc2-121">基於安全性理由，您的應用程式通常不應該在可能轉換的 Unicode 字串中允許字元 U + 00A5，以做為 FAT 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="64bc2-121">For security reasons, your applications should not typically allow the character U+00A5 in a Unicode string that might be converted for use as a FAT file name.</span></span> <span data-ttu-id="64bc2-122">如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="64bc2-122">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="64bc2-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="64bc2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64bc2-124">Windows API 中的 Unicode</span><span class="sxs-lookup"><span data-stu-id="64bc2-124">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> <dt>

[<span data-ttu-id="64bc2-125">安全性考慮：國際功能</span><span class="sxs-lookup"><span data-stu-id="64bc2-125">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> </dl>

 

 



