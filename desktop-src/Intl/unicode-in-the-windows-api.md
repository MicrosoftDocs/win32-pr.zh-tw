---
description: 管理字元的 Windows API 函式通常會以下列三種格式的其中一種來執行：
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Windows API 中的 Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979921"
---
# <a name="unicode-in-the-windows-api"></a><span data-ttu-id="af494-103">Windows API 中的 Unicode</span><span class="sxs-lookup"><span data-stu-id="af494-103">Unicode in the Windows API</span></span>

<span data-ttu-id="af494-104">管理字元的 Windows API 函式通常會以下列三種格式的其中一種來執行：</span><span class="sxs-lookup"><span data-stu-id="af494-104">Windows API functions that manipulate characters are generally implemented in one of three formats:</span></span>

-   <span data-ttu-id="af494-105">可以針對 Windows 字碼頁或 Unicode 編譯的泛型版本</span><span class="sxs-lookup"><span data-stu-id="af494-105">A generic version that can be compiled for either Windows code pages or Unicode</span></span>
-   <span data-ttu-id="af494-106">具有字母 "A" 的 [Windows 字碼頁](code-pages.md) 版本，用來表示 "ANSI"</span><span class="sxs-lookup"><span data-stu-id="af494-106">A [Windows code page](code-pages.md) version with the letter "A" used to indicate "ANSI"</span></span>
-   <span data-ttu-id="af494-107">[Unicode](unicode.md)版本，其字母 "W" 用來表示「寬」</span><span class="sxs-lookup"><span data-stu-id="af494-107">A [Unicode](unicode.md) version with the letter "W" used to indicate "wide"</span></span>

<span data-ttu-id="af494-108">某些較新的函式只支援 Unicode 版本。</span><span class="sxs-lookup"><span data-stu-id="af494-108">Some newer functions support only Unicode versions.</span></span> <span data-ttu-id="af494-109">如需詳細資訊，請參閱 [函數原型的慣例](conventions-for-function-prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="af494-109">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>

<span data-ttu-id="af494-110">下列主題討論 Unicode 資料類型，以及它們在函式和訊息中的使用方式;使用資源、檔案名和命令列引數;以及在不同類型的字串之間轉譯的方法。</span><span class="sxs-lookup"><span data-stu-id="af494-110">The following topics discuss Unicode data types and how they are used in functions and messages; the use of resources, file names, and command line arguments; and methods of translating between different types of strings.</span></span>

-   [<span data-ttu-id="af494-111">自動訊息轉譯</span><span class="sxs-lookup"><span data-stu-id="af494-111">Automatic Message Translation</span></span>](automatic-message-translation.md)
-   [<span data-ttu-id="af494-112">檔案名中使用的字元集</span><span class="sxs-lookup"><span data-stu-id="af494-112">Character Sets Used in File Names</span></span>](character-sets-used-in-file-names.md)
-   [<span data-ttu-id="af494-113">命令列引數</span><span class="sxs-lookup"><span data-stu-id="af494-113">Command Line Arguments</span></span>](command-line-arguments.md)
-   [<span data-ttu-id="af494-114">函數原型的慣例</span><span class="sxs-lookup"><span data-stu-id="af494-114">Conventions for Function Prototypes</span></span>](conventions-for-function-prototypes.md)
-   [<span data-ttu-id="af494-115">標準 C 函數</span><span class="sxs-lookup"><span data-stu-id="af494-115">Standard C Functions</span></span>](standard-c-functions.md)
-   [<span data-ttu-id="af494-116">字串函數差異</span><span class="sxs-lookup"><span data-stu-id="af494-116">String Function Differences</span></span>](string-function-differences.md)
-   [<span data-ttu-id="af494-117">字串類型之間的轉譯</span><span class="sxs-lookup"><span data-stu-id="af494-117">Translation Between String Types</span></span>](translation-between-string-types.md)
-   [<span data-ttu-id="af494-118">字串的 Windows 資料類型</span><span class="sxs-lookup"><span data-stu-id="af494-118">Windows Data Types for Strings</span></span>](windows-data-types-for-strings.md)

## <a name="related-topics"></a><span data-ttu-id="af494-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="af494-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af494-120">關於 Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="af494-120">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



