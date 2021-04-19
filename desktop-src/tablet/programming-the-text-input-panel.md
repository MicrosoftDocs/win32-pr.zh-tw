---
description: 從 Windows Vista 開始，TextInputPanel 會取代 PenInputPanel，以控制平板電腦輸入面板的螢幕外觀和行為。下列各節說明使用文字輸入面板應用程式開發介面來設計輸入面板的程式。TextInputPanel for PenInputPanelUsing 輸入面板的使用者 AutoCompleteEnabling 自訂筆墨的文字更正 CollectorsNote 文字輸入面板會在名為 TabTip.exe 的可執行檔中執行。 使用/SeekDesktop 參數執行 TabTip.exe 時，會嘗試在非標準的互動式桌面上執行較精簡的輸入面板功能版本，如同使用 CreateDesktop 所建立。 針對大部分建立的桌面，輸入面板會在此模式中自動執行。 此參數提供在不尋常的應用程式案例中啟動它，否則會導致自動啟動的方法。 如果輸入面板已在桌面上執行，此參數將不會有任何作用，而且 TabTip.exe 的實例將會立即結束。
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: 程式設計文字輸入面板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981678"
---
# <a name="programming-the-text-input-panel"></a><span data-ttu-id="cdd08-107">程式設計文字輸入面板</span><span class="sxs-lookup"><span data-stu-id="cdd08-107">Programming the Text Input Panel</span></span>

<span data-ttu-id="cdd08-108">從 Windows Vista 開始， [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 會取代 [**PenInputPanel**](peninputpanel-class.md) ，以控制平板電腦輸入面板的螢幕外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="cdd08-108">Starting with Windows Vista, the [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) supersedes the [**PenInputPanel**](peninputpanel-class.md) for controlling the onscreen appearance and behavior of the Tablet Input Panel.</span></span>

<span data-ttu-id="cdd08-109">下列各節說明使用文字輸入面板應用程式開發介面來設計輸入面板的程式。</span><span class="sxs-lookup"><span data-stu-id="cdd08-109">The following sections describe programming the Input Panel using the Text Input Panel application programming interfaces.</span></span>

-   [<span data-ttu-id="cdd08-110">適用于 PenInputPanel 使用者的 TextInputPanel</span><span class="sxs-lookup"><span data-stu-id="cdd08-110">TextInputPanel for Users of PenInputPanel</span></span>](textinputpanel-for-users-of-peninputpanel.md)
-   [<span data-ttu-id="cdd08-111">使用輸入面板自動完成</span><span class="sxs-lookup"><span data-stu-id="cdd08-111">Using Input Panel AutoComplete</span></span>](using-input-panel-autocomplete.md)
-   [<span data-ttu-id="cdd08-112">啟用自訂筆墨收集器的文字更正</span><span class="sxs-lookup"><span data-stu-id="cdd08-112">Enabling Text Correction for Custom Ink Collectors</span></span>](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> <span data-ttu-id="cdd08-113">文字輸入面板會實作為稱為 TabTip.exe 的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="cdd08-113">The Text Input Panel is implemented in an executable file called TabTip.exe.</span></span> <span data-ttu-id="cdd08-114">使用 */SeekDesktop* 參數執行 TabTip.exe 時，會嘗試在非標準的互動式桌面上執行較精簡的輸入面板功能版本，如同使用 [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)所建立。</span><span class="sxs-lookup"><span data-stu-id="cdd08-114">Running TabTip.exe with the */SeekDesktop* parameter attempts to run a reduced functionality version of Input Panel on a nonstandard interactive desktop, as created with [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span> <span data-ttu-id="cdd08-115">針對大部分建立的桌面，輸入面板會在此模式中自動執行。</span><span class="sxs-lookup"><span data-stu-id="cdd08-115">For most created desktops, Input Panel will automatically run in this mode already.</span></span> <span data-ttu-id="cdd08-116">此參數提供在不尋常的應用程式案例中啟動它，否則會導致自動啟動的方法。</span><span class="sxs-lookup"><span data-stu-id="cdd08-116">This parameter provides the means for launching it in unusual application scenarios that otherwise prevent the automatic launch.</span></span> <span data-ttu-id="cdd08-117">如果輸入面板已在桌面上執行，此參數將不會有任何作用，而且 TabTip.exe 的實例將會立即結束。</span><span class="sxs-lookup"><span data-stu-id="cdd08-117">If Input Panel is already running on the desktop, this parameter will have no effect and the instance of TabTip.exe will exit immediately.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cdd08-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="cdd08-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdd08-119">使用 PenInputPanel 類別來設計輸入面板</span><span class="sxs-lookup"><span data-stu-id="cdd08-119">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
