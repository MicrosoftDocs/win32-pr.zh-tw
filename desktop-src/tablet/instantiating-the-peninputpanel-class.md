---
description: 說明如何具現化畫筆輸入面板。
ms.assetid: 185dbed4-8e2c-49a5-a1c8-23a9787ae2f0
title: 具現化 PenInputPanel 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50daf1f7808eb9dc19449ebee396faf90602ea1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978147"
---
# <a name="instantiating-the-peninputpanel-class"></a><span data-ttu-id="2546c-103">具現化 PenInputPanel 類別</span><span class="sxs-lookup"><span data-stu-id="2546c-103">Instantiating the PenInputPanel Class</span></span>

<span data-ttu-id="2546c-104">\[[**PenInputPanel**](peninputpanel-class.md) 已被 [>textinput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90))取代。</span><span class="sxs-lookup"><span data-stu-id="2546c-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span></span> <span data-ttu-id="2546c-105">請參閱 [文字輸入面板](programming-the-text-input-panel.md)的程式設計。\]</span><span class="sxs-lookup"><span data-stu-id="2546c-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="2546c-106">您可以具現化多個 [**PenInputPanel**](peninputpanel-class.md) 物件，並將其附加至表單上的每個控制項，或您可以具現化一個 **PenInputPanel** 物件，並在焦點事件處理常式的控制項之間移動。</span><span class="sxs-lookup"><span data-stu-id="2546c-106">You can instantiate multiple [**PenInputPanel**](peninputpanel-class.md) objects, attaching one to each control on a form, or you can instantiate one **PenInputPanel** object and move it between controls in focus event handlers.</span></span> <span data-ttu-id="2546c-107">因為一次只能有一個編輯控制項，所以第二個方法可以節省記憶體。</span><span class="sxs-lookup"><span data-stu-id="2546c-107">Because only one edit control can have focus at a time, the second method can save memory.</span></span> <span data-ttu-id="2546c-108">稱為 [PenInputPanel 範例](peninputpanel-sample.md) 的自動宣告範例版本已實作為兩種技術的範例。</span><span class="sxs-lookup"><span data-stu-id="2546c-108">A version of the Auto Claims sample called the [PenInputPanel Sample](peninputpanel-sample.md) has been implemented showing both techniques.</span></span>

<span data-ttu-id="2546c-109">下列各節將說明如何建立及顯示 [**PenInputPanel**](peninputpanel-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2546c-109">The following sections describe creating and displaying [**PenInputPanel**](peninputpanel-class.md) objects.</span></span>

-   [<span data-ttu-id="2546c-110">建立 PenInputPanel 物件</span><span class="sxs-lookup"><span data-stu-id="2546c-110">Creating a PenInputPanel Object</span></span>](creating-a-peninputpanel-object.md)
-   [<span data-ttu-id="2546c-111">使用 PenInputPanel 搭配下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="2546c-111">Using the PenInputPanel with Combo Boxes</span></span>](using-the-peninputpanel-with-combo-boxes.md)
-   [<span data-ttu-id="2546c-112">顯示輸入面板</span><span class="sxs-lookup"><span data-stu-id="2546c-112">Displaying the Input Panel</span></span>](displaying-the-input-panel.md)

 

 
