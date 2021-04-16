---
title: 'DirectWrite (DWrite) '
description: 現今的應用程式必須支援高品質的文字轉譯、解析度無關的大綱字型，以及完整的 Unicode 文字和版面配置支援。 DirectWrite 是 [DirectX](../directx.md) API，可提供這些功能和其他功能。
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2020
ms.locfileid: "104464173"
---
# <a name="directwrite-dwrite"></a><span data-ttu-id="f2dbd-104">DirectWrite (DWrite) </span><span class="sxs-lookup"><span data-stu-id="f2dbd-104">DirectWrite (DWrite)</span></span>

## <a name="purpose"></a><span data-ttu-id="f2dbd-105">目的</span><span class="sxs-lookup"><span data-stu-id="f2dbd-105">Purpose</span></span>

<span data-ttu-id="f2dbd-106">現今的應用程式必須支援高品質的文字轉譯、解析度無關的大綱字型，以及完整的 Unicode 文字和版面配置支援。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-106">Today's applications must support high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support.</span></span> <span data-ttu-id="f2dbd-107">DirectWrite 是 [DirectX](../directx.md) API，可提供這些功能和其他功能。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-107">DirectWrite, a [DirectX](../directx.md) API, provides these features and more.</span></span>

- <span data-ttu-id="f2dbd-108">與裝置無關的文字版面配置系統，可改善檔和 UI 中的文字可讀性。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-108">A device-independent text layout system that improves text readability in documents and in UI.</span></span>
- <span data-ttu-id="f2dbd-109">可使用[GDI](interoperating-with-gdi.md)、 [Direct2D](rendering-by-using-direct2d.md)或應用程式特定轉譯技術的高品質、子圖元、 [Microsoft ClearType](/typography/cleartype/)文字轉譯。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-109">High-quality, sub-pixel, [Microsoft ClearType](/typography/cleartype/) text rendering that can use [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md), or application-specific rendering technology.</span></span>
- <span data-ttu-id="f2dbd-110">與 [Direct2D](rendering-by-using-direct2d.md)搭配使用時，硬體加速文字。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-110">Hardware-accelerated text, when used with [Direct2D](rendering-by-using-direct2d.md).</span></span>
- <span data-ttu-id="f2dbd-111">支援多重格式的文字。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-111">Support for multi-format text.</span></span>
- <span data-ttu-id="f2dbd-112">支援 OpenType 字型的先進印刷樣式功能。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-112">Support for the advanced typography features of OpenType fonts.</span></span>
- <span data-ttu-id="f2dbd-113">支援所有支援語言的文字版面配置和轉譯。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-113">Support for the layout and rendering of text in all supported languages.</span></span>
- <span data-ttu-id="f2dbd-114">[GDI](interoperating-with-gdi.md)相容的版面配置和轉譯。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-114">[GDI](interoperating-with-gdi.md)-compatible layout and rendering.</span></span>

<span data-ttu-id="f2dbd-115">API 支援測量、繪製和點擊測試多重格式的文字。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-115">The API supports measuring, drawing, and hit-testing of multi-format text.</span></span> <span data-ttu-id="f2dbd-116">DirectWrite 會以 Windows 7 中的主要語言基礎結構為基礎，處理全球和當地語系化應用程式的所有支援語言文字。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-116">DirectWrite handles text in all supported languages for global and localized applications, building on the key language infrastructure found in Windows 7.</span></span> <span data-ttu-id="f2dbd-117">DirectWrite 也提供低階字符轉譯 API，適用於想要執行自己的版面配置和 Unicode 對字符處理的開發人員。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-117">DirectWrite also provides a low-level glyph rendering API for developers who want to perform their own layout and Unicode-to-glyph processing.</span></span>

> [!NOTE]
> <span data-ttu-id="f2dbd-118">[Project 留尼旺島](/windows/apps/project-reunion/) 導入了新版本的 DirectWrite， &mdash; 稱為 DWriteCore &mdash; ，可在 Windows 版本下執行以 Windows 8，並開啟您在跨平臺使用的大門。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-118">[Project Reunion](/windows/apps/project-reunion/) introduces a new version of DirectWrite&mdash;called DWriteCore&mdash;that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="f2dbd-119">如需詳細資訊，請參閱 [DWriteCore 總覽](dwritecore-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-119">For more details, see [DWriteCore overview](dwritecore-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f2dbd-120">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="f2dbd-120">Run-time requirements</span></span>

- <span data-ttu-id="f2dbd-121">Windows 7 或 Windows Vista Service Pack 2 (SP2) 和 Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="f2dbd-121">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>
- <span data-ttu-id="f2dbd-122">Windows Server 2008 R2 或 Windows Server 2008 Service Pack 2 (SP2) 和 Windows Server 2008 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="f2dbd-122">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f2dbd-123">本節內容</span><span class="sxs-lookup"><span data-stu-id="f2dbd-123">In this section</span></span>

| <span data-ttu-id="f2dbd-124">主題</span><span class="sxs-lookup"><span data-stu-id="f2dbd-124">Topic</span></span> | <span data-ttu-id="f2dbd-125">描述</span><span class="sxs-lookup"><span data-stu-id="f2dbd-125">Description</span></span> |
|-|-|
| [<span data-ttu-id="f2dbd-126">DirectWrite 的新功能</span><span class="sxs-lookup"><span data-stu-id="f2dbd-126">What's new in DirectWrite</span></span>](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | <span data-ttu-id="f2dbd-127">以下是一些 DirectWrite 新增專案。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-127">Here are some of the new additions to DirectWrite.</span></span> <br/> |
| [<span data-ttu-id="f2dbd-128">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="f2dbd-128">Programming Guide</span></span>](programming-guide.md)<br/> | <span data-ttu-id="f2dbd-129">下列主題提供 DirectWrite API 的總覽。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-129">The following topics provide an overview of the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="f2dbd-130">API 參考</span><span class="sxs-lookup"><span data-stu-id="f2dbd-130">API Reference</span></span>](reference.md)<br/> | <span data-ttu-id="f2dbd-131">描述 DirectWrite API。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-131">Describes the DirectWrite API.</span></span><br/> |
| [<span data-ttu-id="f2dbd-132">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="f2dbd-132">Sample Code</span></span>](samples.md)<br/> | <span data-ttu-id="f2dbd-133">本節包含 DirectWrite 範例程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f2dbd-133">This section contains information about sample programs for DirectWrite.</span></span><br/> |
