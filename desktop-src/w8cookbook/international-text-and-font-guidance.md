---
title: 國際文字與字型指導方針
description: 國際文字與字型指導方針
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375352"
---
# <a name="international-text-and-font-guidance"></a><span data-ttu-id="7a6b4-103">國際文字與字型指導方針</span><span class="sxs-lookup"><span data-stu-id="7a6b4-103">International text and font guidance</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="7a6b4-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="7a6b4-104">Affected Platforms</span></span>

<dl> <span data-ttu-id="7a6b4-105">用戶端-Windows 8 \| Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="7a6b4-105">Clients - Windows 8 \| Windows 8.1</span></span>  
<span data-ttu-id="7a6b4-106">伺服器-Windows Server 2012 \| Windows server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7a6b4-106">Servers - Windows Server 2012 \| Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="7a6b4-107">Description</span><span class="sxs-lookup"><span data-stu-id="7a6b4-107">Description</span></span>

<span data-ttu-id="7a6b4-108">自 Windows 2000 之前起，每個主要版本的 Windows 都已新增新腳本的文字顯示支援。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-108">Since before Windows 2000, text-display support for new scripts has been added in each major release of Windows.</span></span> <span data-ttu-id="7a6b4-109">您可以在「[移至全球開發中心](https://msdn.microsoft.com/goglobal/default)」的[腳本和 Windows 檔的字型支援](https://msdn.microsoft.com/goglobal/bb688099.aspx)中，找到每個主要版本中所做變更的描述。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-109">You can find descriptions of the changes made in each major release in the [Script and Font Support for Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) article at the [Go Global Development Center](https://msdn.microsoft.com/goglobal/default).</span></span>

<span data-ttu-id="7a6b4-110">請注意，對於腳本的支援可能需要對文字堆疊元件進行某些變更，以及變更字型。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-110">Note that support for a script may require certain changes to text stack components as well as changes to fonts.</span></span> <span data-ttu-id="7a6b4-111">Windows 作業系統有許多文字堆疊元件： DirectWrite、GDI、Uniscribe、GDI +、WPF、RichEdit、Comctl32.dll 及其他。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-111">The Windows operating system has many text stack components: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32, and others.</span></span> <span data-ttu-id="7a6b4-112">提供的資訊主要適用于 GDI 和 DirectWrite。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-112">The information provided pertains primarily to GDI and DirectWrite.</span></span> <span data-ttu-id="7a6b4-113">它通常也適用于用於 Windows 8 存放區應用程式和轉譯 web 內容的 UI 架構，例如 RichEdit 或 MSHTML 轉譯代理程式，但這些元件可能會展現某些差異。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-113">It is also generally applicable to UI frameworks such as RichEdit or the MSHTML rendering agent used for Windows 8 Store apps and for rendering web content, though those components may exhibit certain differences.</span></span>

## <a name="best-practices"></a><span data-ttu-id="7a6b4-114">最佳做法</span><span class="sxs-lookup"><span data-stu-id="7a6b4-114">Best Practices</span></span>

<span data-ttu-id="7a6b4-115">**適用于開發人員的印刷樣式指引**</span><span class="sxs-lookup"><span data-stu-id="7a6b4-115">**Typography guidance for developers**</span></span>

<span data-ttu-id="7a6b4-116">印刷樣式是 Microsoft 設計語言的核心。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-116">Typography is at the heart of the Microsoft design language.</span></span> <span data-ttu-id="7a6b4-117">每個 Microsoft 設計原則都強調印刷的重要性。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-117">Each of the Microsoft design principles reinforces the importance of typography.</span></span> <span data-ttu-id="7a6b4-118">第一次，應用程式開發人員有一組支援先進印刷印刷功能的架構。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-118">For the first time, app developers have a set of frameworks that support advanced typographic features.</span></span> <span data-ttu-id="7a6b4-119">如需如何使用 JavaScript 和 HTML 來顯示和編輯 Windows Store 應用程式中文字的詳細資訊，請移至 [顯示和編輯文字](/previous-versions/windows/apps/hh465442(v=win.10)) 。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-119">Go to [Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10)) for information about how to use JavaScript and HTML to display and edit text in Windows Store apps.</span></span>

<span data-ttu-id="7a6b4-120">**字型計量**</span><span class="sxs-lookup"><span data-stu-id="7a6b4-120">**Font metrics**</span></span>

<span data-ttu-id="7a6b4-121">字型計量是應用程式開發人員特定重要性的領域。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-121">Font metrics are an area of particular importance to application developers.</span></span> <span data-ttu-id="7a6b4-122">字型檔案包含與垂直和水準計量相關的各種值。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-122">Font files contain various values related to vertical and horizontal metrics.</span></span> <span data-ttu-id="7a6b4-123">這些值記載于 [OpenType 規格](https://www.microsoft.com/typography/otspec/) 中，而且這些值會透過在 [DWRITE \_ 字型 \_ 計量結構](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) 和 [TEXTMETRIC 結構](/windows/win32/api/wingdi/ns-wingdi-textmetrica)中找到的各種 api 來公開。</span><span class="sxs-lookup"><span data-stu-id="7a6b4-123">These values are documented in the [OpenType specification](https://www.microsoft.com/typography/otspec/) and these are exposed via a variety of APIs found at [DWRITE\_FONT\_METRICS structure](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) and at [TEXTMETRIC Structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span></span>

## <a name="resources"></a><span data-ttu-id="7a6b4-124">資源</span><span class="sxs-lookup"><span data-stu-id="7a6b4-124">Resources</span></span>

-   [<span data-ttu-id="7a6b4-125">Windows 的腳本和字型支援</span><span class="sxs-lookup"><span data-stu-id="7a6b4-125">Script and Font Support for Windows</span></span>](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [<span data-ttu-id="7a6b4-126">前往全球開發中心</span><span class="sxs-lookup"><span data-stu-id="7a6b4-126">Go Global Development Center</span></span>](https://msdn.microsoft.com/goglobal/default)
-   <span data-ttu-id="7a6b4-127">[顯示和編輯文字](/previous-versions/windows/apps/hh465442(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7a6b4-127">[Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10))</span></span>
-   [<span data-ttu-id="7a6b4-128">OpenType 規格</span><span class="sxs-lookup"><span data-stu-id="7a6b4-128">OpenType specification</span></span>](https://www.microsoft.com/typography/otspec/)
-   [<span data-ttu-id="7a6b4-129">DWRITE \_ 字型 \_ 計量結構</span><span class="sxs-lookup"><span data-stu-id="7a6b4-129">DWRITE\_FONT\_METRICS structure</span></span>](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [<span data-ttu-id="7a6b4-130">TEXTMETRIC 結構</span><span class="sxs-lookup"><span data-stu-id="7a6b4-130">TEXTMETRIC Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 