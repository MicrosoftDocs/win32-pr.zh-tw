---
description: '&\# 0034; 字元集&\# 0034; 是字元與其識別程式碼值的對應。'
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: 字元集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971384"
---
# <a name="character-sets"></a><span data-ttu-id="625c8-103">字元集</span><span class="sxs-lookup"><span data-stu-id="625c8-103">Character Sets</span></span>

<span data-ttu-id="625c8-104">「字元集」是字元與其識別程式碼值的對應。</span><span class="sxs-lookup"><span data-stu-id="625c8-104">A "character set" is a mapping of characters to their identifying code values.</span></span> <span data-ttu-id="625c8-105">現今電腦最常使用的字元集是 [Unicode](unicode.md)，也是字元編碼的通用標準。</span><span class="sxs-lookup"><span data-stu-id="625c8-105">The character set most commonly used in computers today is [Unicode](unicode.md), a global standard for character encoding.</span></span> <span data-ttu-id="625c8-106">Windows 應用程式會在內部使用 UTF-16 的 Unicode 實作為。</span><span class="sxs-lookup"><span data-stu-id="625c8-106">Internally, Windows applications use the UTF-16 implementation of Unicode.</span></span> <span data-ttu-id="625c8-107">在 UTF-16 中，大部分的字元都是由兩個位元組的代碼所識別。</span><span class="sxs-lookup"><span data-stu-id="625c8-107">In UTF-16, most characters are identified by two-byte codes.</span></span> <span data-ttu-id="625c8-108">較不常用的補充字元分別是由一組成對的雙位元組代碼來表示。</span><span class="sxs-lookup"><span data-stu-id="625c8-108">The less commonly used supplementary characters are each represented by a surrogate pair, which is a pair of two-byte codes.</span></span> <span data-ttu-id="625c8-109">如需詳細資訊，請參閱 [代理程式和補充字元](surrogates-and-supplementary-characters.md)。</span><span class="sxs-lookup"><span data-stu-id="625c8-109">For more information, see [Surrogates and Supplementary Characters](surrogates-and-supplementary-characters.md).</span></span>

<span data-ttu-id="625c8-110">某些 Windows 應用程式必須使用 Windows Me/98/95 原生的舊版字元集。</span><span class="sxs-lookup"><span data-stu-id="625c8-110">Some Windows applications must work with the older character sets that are native to Windows Me/98/95.</span></span> <span data-ttu-id="625c8-111">[Windows 字碼頁](code-pages.md) 可讓您的應用程式使用這些字元集。</span><span class="sxs-lookup"><span data-stu-id="625c8-111">[Windows code pages](code-pages.md) allow your application to work with these character sets.</span></span> <span data-ttu-id="625c8-112">這些字元集可以分為：</span><span class="sxs-lookup"><span data-stu-id="625c8-112">These character sets can be divided into:</span></span>

-   <span data-ttu-id="625c8-113">[單一位元組字元集](single-byte-character-sets.md) (SBCS) 。</span><span class="sxs-lookup"><span data-stu-id="625c8-113">[Single-byte character sets](single-byte-character-sets.md) (SBCS).</span></span> <span data-ttu-id="625c8-114">在 SBCS 中，每個字元都是以一個位元組寬的值來識別。</span><span class="sxs-lookup"><span data-stu-id="625c8-114">In an SBCS, each character is identified by a value one byte wide.</span></span>
-   <span data-ttu-id="625c8-115">多位元組字元集，特別是 [雙位元組](double-byte-character-sets.md) 字集 (DBCS) 。</span><span class="sxs-lookup"><span data-stu-id="625c8-115">Multibyte character sets, in particular the [double-byte character sets](double-byte-character-sets.md) (DBCS).</span></span> <span data-ttu-id="625c8-116">多位元組字元集提供表示許多亞洲語言的大量字元。</span><span class="sxs-lookup"><span data-stu-id="625c8-116">Multibyte character sets provide a means to represent the large number of characters in many Asian languages.</span></span>

<span data-ttu-id="625c8-117">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="625c8-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="625c8-118">字碼頁</span><span class="sxs-lookup"><span data-stu-id="625c8-118">Code Pages</span></span>](code-pages.md)
-   [<span data-ttu-id="625c8-119">雙位元組字集</span><span class="sxs-lookup"><span data-stu-id="625c8-119">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
-   [<span data-ttu-id="625c8-120">單一位元組字元集</span><span class="sxs-lookup"><span data-stu-id="625c8-120">Single-byte Character Sets</span></span>](single-byte-character-sets.md)
-   [<span data-ttu-id="625c8-121">代理和補充字元</span><span class="sxs-lookup"><span data-stu-id="625c8-121">Surrogates and Supplementary Characters</span></span>](surrogates-and-supplementary-characters.md)
-   [<span data-ttu-id="625c8-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="625c8-122">Unicode</span></span>](unicode.md)

## <a name="related-topics"></a><span data-ttu-id="625c8-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="625c8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="625c8-124">關於 Unicode 和字元集</span><span class="sxs-lookup"><span data-stu-id="625c8-124">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



