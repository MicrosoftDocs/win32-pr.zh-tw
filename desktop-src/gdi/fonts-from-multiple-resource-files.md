---
description: 多個資源檔中的字型
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: 多個資源檔中的字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/17/2021
ms.locfileid: "104992447"
---
# <a name="fonts-from-multiple-resource-files"></a><span data-ttu-id="d229a-103">多個資源檔中的字型</span><span class="sxs-lookup"><span data-stu-id="d229a-103">Fonts from Multiple Resource Files</span></span>

<span data-ttu-id="d229a-104">一般而言，字型會包含在單一字型資源檔中。</span><span class="sxs-lookup"><span data-stu-id="d229a-104">Typically, a font is contained in a single font resource file.</span></span> <span data-ttu-id="d229a-105">不過，某些字型的資訊會散佈在多個檔案中。</span><span class="sxs-lookup"><span data-stu-id="d229a-105">However, the information for some fonts is spread among several files.</span></span> <span data-ttu-id="d229a-106">例如，輸入1多個主要字型需要兩個檔案：</span><span class="sxs-lookup"><span data-stu-id="d229a-106">For example, Type 1 multiple master fonts require two files:</span></span>

-   <span data-ttu-id="d229a-107">pfm 適用于字型計量</span><span class="sxs-lookup"><span data-stu-id="d229a-107">.pfm for the font metrics</span></span>
-   <span data-ttu-id="d229a-108">pfb 適用于字型位</span><span class="sxs-lookup"><span data-stu-id="d229a-108">.pfb for the font bits</span></span>

<span data-ttu-id="d229a-109">若要從多個檔案將字型新增至系統，請使用 [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) 或 [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) 函數。</span><span class="sxs-lookup"><span data-stu-id="d229a-109">To add a font from multiple files to the system, use the [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) or [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) functions.</span></span> <span data-ttu-id="d229a-110">這些函式中的 *lpszFilename* 參數必須指向字串，其中包含以分隔號分隔的檔案名或 ( ) 的管道 \| 。</span><span class="sxs-lookup"><span data-stu-id="d229a-110">The *lpszFilename* parameter in these functions must point to a string that contains the file names separated by the vertical bar or pipe ( \| ).</span></span> <span data-ttu-id="d229a-111">例如，若要指定類型1字型的 abcxxxxx. pfm 和 abcxxxxx，請使用 "abcxxxxx. pfm \| abcxxxxx. pfb" 字串。</span><span class="sxs-lookup"><span data-stu-id="d229a-111">For example, to specify abcxxxxx.pfm and abcxxxxx.pfb for a Type 1 font, use the string "abcxxxxx.pfm \| abcxxxxx.pfb."</span></span>

<span data-ttu-id="d229a-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) 與 [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) 的不同之處在于，呼叫 **AddFontResourceEx** 的應用程式可以將字型指定為私用或不可列舉。</span><span class="sxs-lookup"><span data-stu-id="d229a-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differs from [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in that the application calling **AddFontResourceEx** can specify the font as private to itself or non-enumerable.</span></span>

<span data-ttu-id="d229a-113">若要從記憶體影像新增字型，請使用 [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex)。</span><span class="sxs-lookup"><span data-stu-id="d229a-113">To add a font from a memory image, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span></span> <span data-ttu-id="d229a-114">這可讓應用程式使用內嵌在檔或網頁中的字型。</span><span class="sxs-lookup"><span data-stu-id="d229a-114">This allows an application to use a font that is embedded in a document or a webpage.</span></span>

<span data-ttu-id="d229a-115">若要移除來自多個資源檔的字型，請呼叫 [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) 或 [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)，視用來新增字型的函式而定。</span><span class="sxs-lookup"><span data-stu-id="d229a-115">To remove a font that came from multiple resource files, call [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) or [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), depending on the function used to add the font.</span></span> <span data-ttu-id="d229a-116">您必須指定用來新增字型的相同旗標。</span><span class="sxs-lookup"><span data-stu-id="d229a-116">You must specify the same flags that were used to add the font.</span></span> <span data-ttu-id="d229a-117">若要移除從記憶體影像新增的字型，請使用 [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex)。</span><span class="sxs-lookup"><span data-stu-id="d229a-117">To remove a font that was added from a memory image, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span></span>

<span data-ttu-id="d229a-118">使用來自多個字型資源檔的字型，與使用單一資源檔中的字型相同。</span><span class="sxs-lookup"><span data-stu-id="d229a-118">Using a font that comes from multiple font-resource files is identical to using a font from a single resource file.</span></span>

 

 
