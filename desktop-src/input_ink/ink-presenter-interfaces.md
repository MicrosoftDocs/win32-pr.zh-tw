---
description: 本節所包含的主題會提供筆跡呈現介面的參考規格。
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: 筆跡展示者介面
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 1839c8ebc0a7597ab7c5becaf7c7492128b4d6af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981166"
---
# <a name="ink-presenter-interfaces"></a><span data-ttu-id="f73af-103">筆跡展示者介面</span><span class="sxs-lookup"><span data-stu-id="f73af-103">Ink presenter interfaces</span></span>

<span data-ttu-id="f73af-104">本節所包含的主題會提供 [筆跡呈現](ink-presenter.md) 介面的參考規格。</span><span class="sxs-lookup"><span data-stu-id="f73af-104">The topics contained in this section provide the reference specifications for [Ink presenter](ink-presenter.md) interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f73af-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f73af-105">In this section</span></span>

| <span data-ttu-id="f73af-106">主題</span><span class="sxs-lookup"><span data-stu-id="f73af-106">Topic</span></span> | <span data-ttu-id="f73af-107">描述</span><span class="sxs-lookup"><span data-stu-id="f73af-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="f73af-108">**IInkCommitRequestHandler**</span><span class="sxs-lookup"><span data-stu-id="f73af-108">**IInkCommitRequestHandler**</span></span>](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | <span data-ttu-id="f73af-109">啟用您的應用程式 (而不是 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件) ，以將所有暫止的 Microsoft DirectComposition 命令認可到應用程式的 [DirectComposition](../directcomp/directcomposition-portal.md) 視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="f73af-109">Enables your app (instead of an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object) to commit all pending Microsoft DirectComposition commands to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span><br/>   |
| [<span data-ttu-id="f73af-110">**IInkDesktopHost**</span><span class="sxs-lookup"><span data-stu-id="f73af-110">**IInkDesktopHost**</span></span>](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | <span data-ttu-id="f73af-111">透過建立應用程式執行緒來啟用筆跡輸入、處理和轉譯，以裝載 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件，並將它插入應用程式的 [DirectComposition](../directcomp/directcomposition-portal.md) 視覺化樹狀結構中。</span><span class="sxs-lookup"><span data-stu-id="f73af-111">Enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span> <br/> |
| [<span data-ttu-id="f73af-112">**IInkHostWorkItem**</span><span class="sxs-lookup"><span data-stu-id="f73af-112">**IInkHostWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | <span data-ttu-id="f73af-113">表示要在 [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件執行緒上執行的筆墨運算。</span><span class="sxs-lookup"><span data-stu-id="f73af-113">Represents an ink operation to be executed on an [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object thread.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="f73af-114">**IInkPresenterDesktop**</span><span class="sxs-lookup"><span data-stu-id="f73af-114">**IInkPresenterDesktop**</span></span>](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | <span data-ttu-id="f73af-115">代表可以設定並插入至傳統 Windows 應用程式之 [DirectComposition](../directcomp/directcomposition-portal.md)視覺化樹狀結構的 [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) 。</span><span class="sxs-lookup"><span data-stu-id="f73af-115">Represents an [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) that can be configured and inserted into the [DirectComposition](../directcomp/directcomposition-portal.md) visual tree of the Classic Windows app.</span></span> <br/>                                        |

## <a name="related-topics"></a><span data-ttu-id="f73af-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="f73af-116">Related topics</span></span>

<span data-ttu-id="f73af-117">[筆跡展示者](ink-presenter.md)、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例</span><span class="sxs-lookup"><span data-stu-id="f73af-117">[Ink presenter](ink-presenter.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
