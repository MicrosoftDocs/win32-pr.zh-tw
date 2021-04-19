---
description: Uniscribe 使用多個成形引擎，其中包含特定腳本的版面配置知識。
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: 使用成形引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a106e993aba515af38edd2b809ef60454a186cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971655"
---
# <a name="using-shaping-engines"></a><span data-ttu-id="4ea30-103">使用成形引擎</span><span class="sxs-lookup"><span data-stu-id="4ea30-103">Using Shaping Engines</span></span>

<span data-ttu-id="4ea30-104">Uniscribe 使用多個成形引擎，其中包含特定腳本的版面配置知識。</span><span class="sxs-lookup"><span data-stu-id="4ea30-104">Uniscribe uses multiple shaping engines that contain the layout knowledge for particular scripts.</span></span> <span data-ttu-id="4ea30-105">它也會利用 OpenType 版面配置成形引擎來處理字型特定的腳本功能，例如圖像產生、範圍測量和斷詞支援。</span><span class="sxs-lookup"><span data-stu-id="4ea30-105">It also takes advantage of the OpenType layout shaping engine for handling font-specific script features, such as glyph generation, extent measurement, and word-breaking support.</span></span> <span data-ttu-id="4ea30-106">Uniscribe 會使用 Unicode 雙向演算法來管理雙向字元重新排列，並瞭解阿拉伯文、希伯來文和泰文成形的非 OpenType 版面配置字型格式。</span><span class="sxs-lookup"><span data-stu-id="4ea30-106">Uniscribe manages bidirectional character reordering using the Unicode bidirectional algorithm, and understands non-OpenType layout font formats for Arabic, Hebrew, and Thai shaping.</span></span>

<span data-ttu-id="4ea30-107">由於指派給每個成形引擎的確切程式碼點範圍可能不同，因此不會發行腳本編號，但不會有腳本 \_ 定義例外。</span><span class="sxs-lookup"><span data-stu-id="4ea30-107">Since the exact code point ranges assigned to each shaping engine might vary, script numbers are not published, with the exception of SCRIPT\_UNDEFINED.</span></span> <span data-ttu-id="4ea30-108">不過，您的應用程式可以藉由呼叫 [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) 函式來測試腳本的屬性，該函數會存取全域腳本屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="4ea30-108">However, your application can test the attributes of scripts by calling the [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) function, which accesses the global script properties table.</span></span> <span data-ttu-id="4ea30-109">應用程式可以使用全域腳本屬性，以協助將本身的版面配置規則與所需的成形引擎片段結合在一起。</span><span class="sxs-lookup"><span data-stu-id="4ea30-109">The application can use the global script properties to help combine its own layout rules with the required shaping engine divisions.</span></span>

<span data-ttu-id="4ea30-110">應用程式會透過呼叫 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) 函數來存取成形引擎。</span><span class="sxs-lookup"><span data-stu-id="4ea30-110">The application accesses a shaping engine with a call to the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) function.</span></span> <span data-ttu-id="4ea30-111">在成形之前，所有複雜的腳本成形引擎、數位成形引擎和 ASCII 成形引擎都會驗證裝置內容控制碼中指出的字型。</span><span class="sxs-lookup"><span data-stu-id="4ea30-111">All the complex script shaping engines, the digit shaping engines, and the ASCII shaping engines validate the font indicated in the device context handle before shaping.</span></span> <span data-ttu-id="4ea30-112">複雜字集必須使用 [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) 函式所傳回的腳本來塑造，才能使其更清晰。</span><span class="sxs-lookup"><span data-stu-id="4ea30-112">Complex scripts must be shaped using the script returned by the [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) function in order to be legible.</span></span> <span data-ttu-id="4ea30-113">如果 \_ [**腳本 \_ 分析**](/windows/win32/api/usp10/ns-usp10-script_analysis)結構的 **eScript** 成員中指定了未定義的腳本，則其他執行會保持可讀性，雖然它們可能會遺失印刷品質。</span><span class="sxs-lookup"><span data-stu-id="4ea30-113">Other runs remain legible if shaped with SCRIPT\_UNDEFINED specified in the **eScript** member of the [**SCRIPT\_ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) structure, although they might lose typographic quality.</span></span>

<span data-ttu-id="4ea30-114">如果成功， [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)會傳回 0; \_ \_ \_ \_ \_ 如果應用程式所提供的字型未包含足夠的圖像或成形資料表，則會傳回不含字型的 USP E 腳本。</span><span class="sxs-lookup"><span data-stu-id="4ea30-114">[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) returns 0 if successful, or USP\_E\_SCRIPT\_NOT\_IN\_FONT if the font supplied by the application does not contain sufficient glyphs or shaping tables.</span></span> <span data-ttu-id="4ea30-115">如果應用程式指定腳本未 \_ 定義，且字型不支援某些字元，則函式仍然會成功。</span><span class="sxs-lookup"><span data-stu-id="4ea30-115">If the application specifies SCRIPT\_UNDEFINED and some characters are not supported by the font, the function still succeeds.</span></span> <span data-ttu-id="4ea30-116">在此情況下，應用程式應該掃描圖像輸出緩衝區是否有遺漏的圖像。</span><span class="sxs-lookup"><span data-stu-id="4ea30-116">In this case, the application should scan the glyph output buffer for the presence of missing glyphs.</span></span> <span data-ttu-id="4ea30-117">如需處理遺漏圖像的策略，請參閱 [使用字型](using-font-fallback.md)回復。</span><span class="sxs-lookup"><span data-stu-id="4ea30-117">For strategies to deal with missing glyphs, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ea30-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ea30-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ea30-119">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="4ea30-119">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



