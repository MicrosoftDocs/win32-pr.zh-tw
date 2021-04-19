---
description: 顯示輸入面板的總覽。
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: 顯示輸入面板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982103"
---
# <a name="displaying-the-input-panel"></a><span data-ttu-id="67ce3-103">顯示輸入面板</span><span class="sxs-lookup"><span data-stu-id="67ce3-103">Displaying the Input Panel</span></span>

<span data-ttu-id="67ce3-104">\[針對 managed 程式碼) ， [**PenInputPanel**](peninputpanel-class.md)已被 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([>textinput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) 。</span><span class="sxs-lookup"><span data-stu-id="67ce3-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) for managed code).</span></span> <span data-ttu-id="67ce3-105">請參閱 [文字輸入面板](programming-the-text-input-panel.md)的程式設計。\]</span><span class="sxs-lookup"><span data-stu-id="67ce3-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="67ce3-106">控制項的各種焦點事件順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="67ce3-106">The order of the various focus events for a control is as follows:</span></span>

-   [<span data-ttu-id="67ce3-107">控制項。輸入</span><span class="sxs-lookup"><span data-stu-id="67ce3-107">Control.Enter</span></span>](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [<span data-ttu-id="67ce3-108">控制項. GotFocus</span><span class="sxs-lookup"><span data-stu-id="67ce3-108">Control.GotFocus</span></span>](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [<span data-ttu-id="67ce3-109">控制項。離開</span><span class="sxs-lookup"><span data-stu-id="67ce3-109">Control.Leave</span></span>](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [<span data-ttu-id="67ce3-110">控制。正在驗證</span><span class="sxs-lookup"><span data-stu-id="67ce3-110">Control.Validating</span></span>](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [<span data-ttu-id="67ce3-111">控制項。已驗證</span><span class="sxs-lookup"><span data-stu-id="67ce3-111">Control.Validated</span></span>](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [<span data-ttu-id="67ce3-112">控制項. LostFocus</span><span class="sxs-lookup"><span data-stu-id="67ce3-112">Control.LostFocus</span></span>](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

<span data-ttu-id="67ce3-113">控制項中設定控制項時，並不保證控制項的焦點是由 [控制項所](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) 撰寫。 [請輸入](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="67ce3-113">There is no guarantee that the control actually has focus by the time the [Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) property is written when it is set in the [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="67ce3-114">控制項。輸入事件是將 [PenInputPanel](/previous-versions/ms583923(v=vs.100)) 物件附加至控制項的最佳位置，但 [control。 GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) 事件是變更 [PenInputPanel Visible](/previous-versions/ms571984(v=vs.100)) 屬性的最佳位置。</span><span class="sxs-lookup"><span data-stu-id="67ce3-114">The Control.Enter event is the best place to attach the [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control, but the [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) event is the best place to change the [PenInputPanel.Visible](/previous-versions/ms571984(v=vs.100)) property.</span></span>

 

 
