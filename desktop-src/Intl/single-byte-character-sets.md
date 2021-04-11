---
description: 單一位元組字元集 (SBCS) 是將256個個別字符對應到它們的識別程式碼值（實作為字碼頁）。
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: 單一位元組字元集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945337"
---
# <a name="single-byte-character-sets"></a><span data-ttu-id="5f5ad-103">單一位元組字元集</span><span class="sxs-lookup"><span data-stu-id="5f5ad-103">Single-byte Character Sets</span></span>

<span data-ttu-id="5f5ad-104">單一位元組字元集 (SBCS) 是將256個個別字符對應到它們的識別程式碼值（實作為字碼頁）。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-104">A single-byte character set (SBCS) is a mapping of 256 individual characters to their identifying code values, implemented as a code page.</span></span> <span data-ttu-id="5f5ad-105">SBCS 可以對應至 Windows 字碼頁或 OEM 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-105">An SBCS can correspond either to a Windows code page or an OEM code page.</span></span> <span data-ttu-id="5f5ad-106">SBCS 字碼頁也可以包含非原生字碼頁，例如，EBCDIC 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-106">An SBCS code page can also include a non-native code page, for example, an EBCDIC code page.</span></span> <span data-ttu-id="5f5ad-107">如需這些字碼頁的定義，請參閱 [字碼頁](code-pages.md)。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-107">For definitions of these code pages, see [Code Pages](code-pages.md).</span></span>

> [!Note]  
> <span data-ttu-id="5f5ad-108">新的 Windows 應用程式應該使用 [Unicode](unicode.md) 來避免不同的程式字碼頁不一致，並方便當地語系化。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-108">New Windows applications should use [Unicode](unicode.md) to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="5f5ad-109">不過，某些舊版通訊協定需要使用 SBCS。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-109">However, some legacy protocols require the use of an SBCS.</span></span> <span data-ttu-id="5f5ad-110">每個 SBCS 字碼頁支援不同的字元，但沒有任何頁面支援 Unicode 提供的完整字元範圍。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-110">Each SBCS code page supports different characters, but no page supports the full breadth of characters provided by Unicode.</span></span> <span data-ttu-id="5f5ad-111">每個 SBCS 字碼頁支援不同的子集，並以不同方式編碼。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-111">Each SBCS code page supports a different subset, differently encoded.</span></span> <span data-ttu-id="5f5ad-112">從一個 SBCS 字碼頁轉換成另一個字碼頁的資料可能會損毀，因為不同字碼頁上的相同資料值可以編碼不同的字元。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-112">Data converted from one SBCS code page to another is subject to corruption, because the same data value on different code pages can encode a different character.</span></span> <span data-ttu-id="5f5ad-113">從 Unicode 轉換成 SBCS 的資料會受到資料遺失的影響，因為指定的字碼頁可能無法表示該特定 Unicode 資料中使用的每個字元。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-113">Data converted from Unicode to SBCS is subject to data loss because a given code page might not be able to represent every character used in that particular Unicode data.</span></span>

 

<span data-ttu-id="5f5ad-114">您的應用程式會搭配 Windows 函式的 "A" 版本使用 SBCS Windows 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-114">Your applications use SBCS Windows code pages with the "A" versions of Windows functions.</span></span> <span data-ttu-id="5f5ad-115">請參閱函數原型和[字碼頁](code-pages.md)[的慣例](conventions-for-function-prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-115">See [Conventions for Function Prototypes](conventions-for-function-prototypes.md) and [Code Pages](code-pages.md).</span></span> <span data-ttu-id="5f5ad-116">為了協助識別 SBCS 字碼頁，應用程式可以使用 [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) 或 [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-116">To help identify an SBCS code page, an application can use the [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) or [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) function.</span></span> <span data-ttu-id="5f5ad-117">此外，應用程式可以使用 [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 函式，在 Unicode 和 SBCS 字串之間進行對應。</span><span class="sxs-lookup"><span data-stu-id="5f5ad-117">In addition, an application can use the [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) functions to map between Unicode and SBCS strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f5ad-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f5ad-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f5ad-119">字元集</span><span class="sxs-lookup"><span data-stu-id="5f5ad-119">Character Sets</span></span>](character-sets.md)
</dt> <dt>

[<span data-ttu-id="5f5ad-120">雙位元組字集</span><span class="sxs-lookup"><span data-stu-id="5f5ad-120">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
</dt> </dl>

 

 



