---
description: 筆跡呈現器 API 可以讓 Microsoft Win32 應用程式透過插入 App 之 DirectComposition 視覺化樹狀結構的 InkPresenter 物件，來管理筆跡輸入 (標準和已修改) 的輸入、處理及轉換。
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: 筆跡展示者
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193782"
---
# <a name="ink-presenter"></a><span data-ttu-id="02c2f-103">筆跡展示者</span><span class="sxs-lookup"><span data-stu-id="02c2f-103">Ink presenter</span></span>

<span data-ttu-id="02c2f-104">筆墨演講者 Api 可讓 Microsoft Win32 應用程式透過插入應用程式 [DirectComposition](../directcomp/directcomposition-portal.md)視覺化樹狀結構的 [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter)物件，來管理筆墨輸入的輸入、處理和轉譯 (標準和修改過的) 。</span><span class="sxs-lookup"><span data-stu-id="02c2f-104">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

> [!Note]
>
> <span data-ttu-id="02c2f-105">標準筆墨輸入 (畫筆提示或橡皮擦提示/按鈕) 不會使用次要 affordance 來修改，例如畫筆圓筒按鈕、滑鼠右鍵或類似的按鈕。</span><span class="sxs-lookup"><span data-stu-id="02c2f-105">Standard ink input (pen tip or eraser tip/button) is not modified with a secondary affordance, such as a pen barrel button, right mouse button, or similar.</span></span>

<span data-ttu-id="02c2f-106">通用 Windows 平臺 (UWP) 使用 Extensible Application Markup Language (XAML 的應用程式) 透過 [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)控制項提供這種功能，以及連接到 XAML [DirectComposition](../directcomp/directcomposition-portal.md)視覺化樹狀結構的 [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter)物件。</span><span class="sxs-lookup"><span data-stu-id="02c2f-106">Universal Windows Platform (UWP) apps using Extensible Application Markup Language (XAML) provide this functionality through an [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control along with an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object that connects to the XAML [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span> <span data-ttu-id="02c2f-107">如需詳細資訊，請參閱 [畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)。</span><span class="sxs-lookup"><span data-stu-id="02c2f-107">For more detail, see [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions).</span></span>

<span data-ttu-id="02c2f-108">[筆墨](ink-renderer.md)轉譯器的設計目的是要讓通用 Windows 應用程式開發人員有興趣 [](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)在 / 原生 Win32 應用程式中提供以 XAML 為基礎的 InkCanvas [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter)功能。</span><span class="sxs-lookup"><span data-stu-id="02c2f-108">[Ink renderer](ink-renderer.md) is designed for use by Universal Windows app developers interested in providing XAML-based [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)/[**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) functionality in native Win32 apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="02c2f-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="02c2f-109">In this section</span></span>



| <span data-ttu-id="02c2f-110">主題</span><span class="sxs-lookup"><span data-stu-id="02c2f-110">Topic</span></span>                                                               | <span data-ttu-id="02c2f-111">描述</span><span class="sxs-lookup"><span data-stu-id="02c2f-111">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02c2f-112">筆跡展示者類別</span><span class="sxs-lookup"><span data-stu-id="02c2f-112">Ink presenter classes</span></span>](ink-presenter-classes.md)<br/>       | <span data-ttu-id="02c2f-113">本節所包含的主題會提供筆跡展示者類別的參考規格。</span><span class="sxs-lookup"><span data-stu-id="02c2f-113">The topics contained in this section provide the reference specifications for Ink presenter classes.</span></span> <br/>    |
| [<span data-ttu-id="02c2f-114">筆跡展示者介面</span><span class="sxs-lookup"><span data-stu-id="02c2f-114">Ink presenter interfaces</span></span>](ink-presenter-interfaces.md)<br/> | <span data-ttu-id="02c2f-115">本節所包含的主題會提供筆跡呈現介面的參考規格。</span><span class="sxs-lookup"><span data-stu-id="02c2f-115">The topics contained in this section provide the reference specifications for Ink presenter interfaces.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="02c2f-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="02c2f-116">Related topics</span></span>

<span data-ttu-id="02c2f-117">[筆跡展示者](ink-presenter.md)、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例</span><span class="sxs-lookup"><span data-stu-id="02c2f-117">[Ink presenter](ink-presenter.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
