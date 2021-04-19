---
description: 筆墨轉譯器 Api 可將筆墨筆劃轉譯至通用 Windows 應用程式的指定 Direct2D 裝置內容，而不是預設的 InkCanvas 控制項。
ms.assetid: 8E532066-19EB-4FA6-823D-21823591742F
title: 筆墨轉譯器
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: f9e1e654859dd8d777855bc2bffaf953feb8ba8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989353"
---
# <a name="ink-renderer"></a><span data-ttu-id="a847c-103">筆墨轉譯器</span><span class="sxs-lookup"><span data-stu-id="a847c-103">Ink renderer</span></span>

<span data-ttu-id="a847c-104">筆墨轉譯器 Api 可將筆墨筆劃轉譯至通用 Windows 應用程式的指定 Direct2D 裝置內容，而不是預設的 [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) 控制項。</span><span class="sxs-lookup"><span data-stu-id="a847c-104">The Ink renderer APIs enable the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

<span data-ttu-id="a847c-105">筆墨轉譯器的設計目的是要讓通用 Windows 應用程式開發人員有興趣自訂筆跡筆劃的呈現方式「幹」，以及與 [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) 控制項的相同品質。</span><span class="sxs-lookup"><span data-stu-id="a847c-105">Ink renderer is designed for use by Universal Windows app developers interested in customizing how ink strokes are rendered "dry", and of identical quality to the [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a847c-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="a847c-106">In this section</span></span>

| <span data-ttu-id="a847c-107">主題</span><span class="sxs-lookup"><span data-stu-id="a847c-107">Topic</span></span>                                                             | <span data-ttu-id="a847c-108">描述</span><span class="sxs-lookup"><span data-stu-id="a847c-108">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a847c-109">筆墨轉譯器類別</span><span class="sxs-lookup"><span data-stu-id="a847c-109">Ink renderer classes</span></span>](ink-renderer-classes.md)<br/>       | <span data-ttu-id="a847c-110">本節所包含的主題會提供筆跡轉譯器類別的參考規格。</span><span class="sxs-lookup"><span data-stu-id="a847c-110">The topics contained in this section provide the reference specifications for Ink renderer classes.</span></span> <br/>    |
| [<span data-ttu-id="a847c-111">筆墨轉譯器介面</span><span class="sxs-lookup"><span data-stu-id="a847c-111">Ink renderer interfaces</span></span>](ink-renderer-interfaces.md)<br/> | <span data-ttu-id="a847c-112">本節所包含的主題會提供筆跡轉譯器介面的參考規格。</span><span class="sxs-lookup"><span data-stu-id="a847c-112">The topics contained in this section provide the reference specifications for Ink renderer interfaces.</span></span> <br/> |

## <a name="related-topics"></a><span data-ttu-id="a847c-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="a847c-113">Related topics</span></span>

<span data-ttu-id="a847c-114">[筆跡輸入](input-ink-portal.md)、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例</span><span class="sxs-lookup"><span data-stu-id="a847c-114">[Ink input](input-ink-portal.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
