---
description: Tablet PC 平臺會產生數種保存格式，可作為先前所列格式的建立區塊。 以下是使用 Ink 物件的 Load 和 Save 方法產生和取用的格式。
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: 建置組塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32e6121ddfaabfc860239019ce62df65bdc36c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971979"
---
# <a name="building-blocks"></a><span data-ttu-id="3841a-104">建置組塊</span><span class="sxs-lookup"><span data-stu-id="3841a-104">Building Blocks</span></span>

<span data-ttu-id="3841a-105">Tablet PC 平臺會產生數種保存格式，可作為先前所列格式的建立區塊。</span><span class="sxs-lookup"><span data-stu-id="3841a-105">There are several persistence formats the Tablet PC platform generates that are useful as building blocks for the formats listed previously.</span></span> <span data-ttu-id="3841a-106">以下是使用 [**Ink**](/previous-versions/ms583670(v=vs.100)) 物件的 [**Load**](/previous-versions/ms569609(v=vs.100)) 和 [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) 方法產生和取用的格式。</span><span class="sxs-lookup"><span data-stu-id="3841a-106">The following formats are all generated and consumed by using the [**Ink**](/previous-versions/ms583670(v=vs.100)) object's [**Load**](/previous-versions/ms569609(v=vs.100)) and [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) methods.</span></span>

-   <span data-ttu-id="3841a-107">筆墨序列化格式 (ISF) ：筆跡序列化格式 (ISF) 是最精簡的筆墨持續性標記法。</span><span class="sxs-lookup"><span data-stu-id="3841a-107">Ink serialized format (ISF): Ink Serialized Format (ISF) is the most compact persistent representation of ink.</span></span> <span data-ttu-id="3841a-108">您可以將 ISF 內嵌在二進位檔案格式中，或直接將它移到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="3841a-108">You can embed ISF within a binary document format or move it directly to the Clipboard.</span></span> <span data-ttu-id="3841a-109">以 ISF 儲存的筆墨應該使用預設的座標系統，也就是 HIMETRIC，垂直軸反轉。</span><span class="sxs-lookup"><span data-stu-id="3841a-109">Ink stored in ISF should use the default coordinate system, which is HIMETRIC, with the vertical axis inverted.</span></span>
-   <span data-ttu-id="3841a-110">Base-64 編碼的 ISF：您可以使用 base-64 編碼的 ISF，直接將筆墨編碼成可延伸標記語言 (XML) 的 (XML) 或 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="3841a-110">Base-64 Encoded ISF: You can use base-64 encoded ISF to encode ink directly into an Extensible Markup Language (XML) or HTML file.</span></span>
-   <span data-ttu-id="3841a-111">嚴加防禦圖形交換格式 (GIF) ：嚴加防禦 GIF 是一個 GIF 檔案，其中包含在檔案中內嵌的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3841a-111">Fortified Graphics Interchange Format (GIF): Fortified GIF is a GIF file that contains ISF as metadata embedded within the file.</span></span> <span data-ttu-id="3841a-112">以嚴加防禦 GIF 形式產生的筆墨可在無法辨識筆墨的應用程式中查看，如果筆墨傳回的應用程式可辨識筆墨，則會保留所有筆墨資料。</span><span class="sxs-lookup"><span data-stu-id="3841a-112">Ink generated as a fortified GIF can be viewed in applications that do not recognize ink, and all ink data is maintained if the ink returns to an application that does recognize ink.</span></span> <span data-ttu-id="3841a-113">此格式適合用來在 HTML 檔案中傳輸筆墨內容。</span><span class="sxs-lookup"><span data-stu-id="3841a-113">This format is ideal for transporting ink content within an HTML file.</span></span> <span data-ttu-id="3841a-114">無論應用程式是否辨識筆墨，任何應用程式都可以使用筆墨。</span><span class="sxs-lookup"><span data-stu-id="3841a-114">The ink is available to any application, regardless of whether the application recognizes ink.</span></span>
-   <span data-ttu-id="3841a-115">以64編碼的嚴加防禦 GIF：此格式適用于想要直接將筆跡編碼成 XML 或 HTML 檔案，然後稍後再將檔案轉換成影像的開發人員。</span><span class="sxs-lookup"><span data-stu-id="3841a-115">Base-64 Encoded Fortified GIF: This format is provided for developers who want to encode ink directly into an XML or HTML file and then convert the file into an image at a later time.</span></span> <span data-ttu-id="3841a-116">當您想要產生的 XML 檔案包含所有筆墨資訊，以及使用可延伸樣式單語言轉換 (XSLT) 來產生 HTML 時，可以使用此方法。</span><span class="sxs-lookup"><span data-stu-id="3841a-116">You can use this when you want an XML file that is generated to contain all ink information and to be used as a way to generate HTML by using Extensible Stylesheet Language Transformations (XSLT).</span></span>
    > [!Note]  
    > <span data-ttu-id="3841a-117">這項 LZW 壓縮和解壓縮技術藉由美國專利條款所涵蓋。</span><span class="sxs-lookup"><span data-stu-id="3841a-117">The LZW compression and decompression technology is allegedly covered by US Patent No.</span></span> <span data-ttu-id="3841a-118">4558302與其相關和外國互相對應的專利 (統稱為 Unisys Corporation 所擁有的 LZW 專利) 。</span><span class="sxs-lookup"><span data-stu-id="3841a-118">4,558,302 and its related and foreign counterpart patents (collectively, the LZW Patents) owned by Unisys Corporation.</span></span> <span data-ttu-id="3841a-119">Microsoft Corporation 已從 Unisys 的專利專利取得授權，以在特定 Microsoft 產品中使用 GIF 和 LZW 技術。</span><span class="sxs-lookup"><span data-stu-id="3841a-119">Microsoft Corporation has obtained a license from Unisys under the LZW Patents to use the GIF and the LZW technology in certain Microsoft products.</span></span> <span data-ttu-id="3841a-120">但是，這項授權並不會延伸到使用 Microsoft 開發產品（例如 Microsoft 工具組和語言開發產品）的協力廠商開發人員，以在自己的產品中提供 GIF 讀取/寫入或任何其他的 LZW 功能。</span><span class="sxs-lookup"><span data-stu-id="3841a-120">This license, however, does not extend to third-party developers using Microsoft development products, such as Microsoft toolkit and language development products, to provide GIF read/write or any other LZW capabilities in their own products.</span></span> <span data-ttu-id="3841a-121">協力廠商開發人員必須自行決定是否需要來自 Unisys 的產品授權。</span><span class="sxs-lookup"><span data-stu-id="3841a-121">Third-party developers need to make their own determination as to whether they need a license from Unisys for their products.</span></span>

     

<span data-ttu-id="3841a-122">應用程式可以使用 [system.windows.media.visualtreehelper.hittest](/previous-versions/ms828460(v=msdn.10)) 或 [system.windows.media.visualtreehelper.hittest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) 方法來產生筆觸集合，以產生這些持續格式的其中一種，也可以：</span><span class="sxs-lookup"><span data-stu-id="3841a-122">An application can generate one of these persistent formats by using the [Microsoft.Ink.Stroke.HitTest](/previous-versions/ms828460(v=msdn.10)) or the [Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to generate a strokes collection and either:</span></span>

-   <span data-ttu-id="3841a-123">使用 [AddStrokesAtRectangle](/previous-versions/ms569548(v=vs.100))方法，將這些筆觸新增至新的 [**筆墨**](/previous-versions/ms583670(v=vs.100))物件。</span><span class="sxs-lookup"><span data-stu-id="3841a-123">Adding these strokes to a new [**Ink**](/previous-versions/ms583670(v=vs.100)) object by using the [AddStrokesAtRectangle](/previous-versions/ms569548(v=vs.100)) method.</span></span>
-   <span data-ttu-id="3841a-124">使用 [ExtractStrokes](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90))方法產生新的 [**筆墨**](/previous-versions/ms583670(v=vs.100))物件。</span><span class="sxs-lookup"><span data-stu-id="3841a-124">Generating a new [**Ink**](/previous-versions/ms583670(v=vs.100)) object by using the [ExtractStrokes](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90)) method.</span></span>

<span data-ttu-id="3841a-125">第一個會將選取矩形轉譯成原點，而第二個則不會。</span><span class="sxs-lookup"><span data-stu-id="3841a-125">The first translates the selection rectangle to the origin, while the second does not.</span></span> <span data-ttu-id="3841a-126">然後，應用程式會使用 [**Ink**](/previous-versions/ms583670(v=vs.100))物件的 [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90))方法。</span><span class="sxs-lookup"><span data-stu-id="3841a-126">The application then uses the [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method of the [**Ink**](/previous-versions/ms583670(v=vs.100)) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3841a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="3841a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3841a-128">sInk 和 tInk 物件</span><span class="sxs-lookup"><span data-stu-id="3841a-128">sInk and tInk Objects</span></span>](sink-and-tink-objects.md)
</dt> </dl>

 

 
