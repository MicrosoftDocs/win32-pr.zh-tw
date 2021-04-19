---
description: 語言識別項是國家或地區中語言的標準國際數值縮寫。
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: 語言識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991760"
---
# <a name="language-identifiers"></a><span data-ttu-id="f0ec0-103">語言識別碼</span><span class="sxs-lookup"><span data-stu-id="f0ec0-103">Language Identifiers</span></span>

<span data-ttu-id="f0ec0-104">語言識別項是國家或地區中 [語言](locales-and-languages.md) 的標準國際數值縮寫。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-104">A language identifier is a standard international numeric abbreviation for the [language](locales-and-languages.md) in a country or geographical region.</span></span> <span data-ttu-id="f0ec0-105">每種語言都有唯一的語言識別項 (資料類型 LANGID) ，它是由主要語言識別項和子語言識別項組成的16位值。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-105">Each language has a unique language identifier (data type LANGID), a 16-bit value that consists of a primary language identifier and a sublanguage identifier.</span></span> <span data-ttu-id="f0ec0-106">如需語言識別項的詳細資訊，請參閱 [語言識別項常數和字串](language-identifier-constants-and-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-106">For details of language identifiers, see [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md).</span></span>

<span data-ttu-id="f0ec0-107">語言識別項是使用 [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) 宏所建立。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-107">A language identifier is constructed using the [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) macro.</span></span> <span data-ttu-id="f0ec0-108">下圖顯示語言識別項中的位格式。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-108">The following illustration shows the format of the bits in a language identifier.</span></span>

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

<span data-ttu-id="f0ec0-109">以下是預先定義的語言識別項：</span><span class="sxs-lookup"><span data-stu-id="f0ec0-109">The following are predefined language identifiers:</span></span>

-   <span data-ttu-id="f0ec0-110">LANG \_ 系統 \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-110">LANG\_SYSTEM\_DEFAULT.</span></span> <span data-ttu-id="f0ec0-111">作業系統的預設語言。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-111">The operating system default language.</span></span>
-   <span data-ttu-id="f0ec0-112">LANG \_ 使用者 \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-112">LANG\_USER\_DEFAULT.</span></span> <span data-ttu-id="f0ec0-113">目前使用者的語言。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-113">The language of the current user.</span></span>

<span data-ttu-id="f0ec0-114">您的應用程式可以使用 [多語系消費者介面](multilingual-user-interface.md) 函式來取得目前的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="f0ec0-114">Your application can retrieve the current language identifiers by using the [Multilingual User Interface](multilingual-user-interface.md) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0ec0-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0ec0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0ec0-116">地區設定和語言</span><span class="sxs-lookup"><span data-stu-id="f0ec0-116">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="f0ec0-117">語言識別項常數和字串</span><span class="sxs-lookup"><span data-stu-id="f0ec0-117">Language Identifier Constants and Strings</span></span>](language-identifier-constants-and-strings.md)
</dt> <dt>

[<span data-ttu-id="f0ec0-118">多語系使用者介面</span><span class="sxs-lookup"><span data-stu-id="f0ec0-118">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="f0ec0-119">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="f0ec0-119">**MAKELANGID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



