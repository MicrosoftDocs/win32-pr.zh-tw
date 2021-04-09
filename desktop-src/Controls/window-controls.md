---
title: Windows 控制項
description: 控制項是應用程式用來與另一個視窗結合以啟用使用者互動的子視窗。
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021053"
---
# <a name="windows-controls"></a><span data-ttu-id="41a51-103">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="41a51-103">Windows Controls</span></span>

## <a name="purpose"></a><span data-ttu-id="41a51-104">目的</span><span class="sxs-lookup"><span data-stu-id="41a51-104">Purpose</span></span>

<span data-ttu-id="41a51-105">控制項是應用程式用來與另一個視窗結合以啟用使用者互動的子視窗。</span><span class="sxs-lookup"><span data-stu-id="41a51-105">A control is a child window that an application uses in conjunction with another window to enable user interaction.</span></span> <span data-ttu-id="41a51-106">控制項最常用於對話方塊內，但也可以在其他視窗中使用。</span><span class="sxs-lookup"><span data-stu-id="41a51-106">Controls are most often used within dialog boxes, but they can also be used in other windows.</span></span> <span data-ttu-id="41a51-107">對話方塊內的控制項可讓使用者輸入文字、選擇選項，以及起始動作。</span><span class="sxs-lookup"><span data-stu-id="41a51-107">Controls within dialog boxes provide the user with a way to type text, choose options, and initiate actions.</span></span> <span data-ttu-id="41a51-108">其他視窗中的控制項提供各種不同的服務，例如讓使用者選擇命令、查看狀態，以及查看和編輯文字。</span><span class="sxs-lookup"><span data-stu-id="41a51-108">Controls in other windows provide a variety of services, such as letting the user choose commands, view status, and view and edit text.</span></span> <span data-ttu-id="41a51-109">本檔說明 Windows 所提供的控制項，以及用來建立和操作這些控制項的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="41a51-109">This documentation describes the controls provided by Windows and the programming elements used to create and manipulate them.</span></span>

<span data-ttu-id="41a51-110">如需所有 Windows 控制項的清單，包括每個控制項的完整總覽和參考資訊的連結，請參閱 [控制項程式庫](individual-control-info.md)。</span><span class="sxs-lookup"><span data-stu-id="41a51-110">For a list of all Windows controls, including a link to comprehensive overview and reference information for each control, see [Control Library](individual-control-info.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="41a51-111">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="41a51-111">Developer audience</span></span>

<span data-ttu-id="41a51-112">控制項是設計來供 C/c + + 開發人員和 UI 設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="41a51-112">Controls are designed for use by C/C++ developers and UI designers.</span></span> <span data-ttu-id="41a51-113">一般情況下，開發人員需要對 UI 程式設計概念、Windows API 程式設計和 Unicode 進行中等程度的瞭解。</span><span class="sxs-lookup"><span data-stu-id="41a51-113">In general, developers need a moderate level of understanding about UI programming concepts, Windows API programming, and Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="41a51-114">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="41a51-114">Run-time requirements</span></span>

<span data-ttu-id="41a51-115">控制項的支援是由 User32.dll 和 Comctl32.dll 所提供。</span><span class="sxs-lookup"><span data-stu-id="41a51-115">Support for controls is provided by User32.dll and Comctl32.dll.</span></span> <span data-ttu-id="41a51-116">如需詳細資訊，請參閱 [通用控制項版本](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="41a51-116">For more information, see [Common Control Versions](common-control-versions.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="41a51-117">本節內容</span><span class="sxs-lookup"><span data-stu-id="41a51-117">In this section</span></span>



| <span data-ttu-id="41a51-118">主題</span><span class="sxs-lookup"><span data-stu-id="41a51-118">Topic</span></span>                                                                             | <span data-ttu-id="41a51-119">描述</span><span class="sxs-lookup"><span data-stu-id="41a51-119">Description</span></span>                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41a51-120">關於通用控制項</span><span class="sxs-lookup"><span data-stu-id="41a51-120">About Common Controls</span></span>](common-controls-intro.md)<br/>                     | <span data-ttu-id="41a51-121">提供 Comctl32.dll 所支援的所有控制項通用的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="41a51-121">Provides general information that is common to all controls that are supported by Comctl32.dll.</span></span><br/>                                      |
| [<span data-ttu-id="41a51-122">控制訊息</span><span class="sxs-lookup"><span data-stu-id="41a51-122">Control Messages</span></span>](control-messages.md)<br/>                               | <span data-ttu-id="41a51-123">說明如何使用 Windows 訊息與控制項通訊。</span><span class="sxs-lookup"><span data-stu-id="41a51-123">Explains how Windows messages are used to communicate with controls.</span></span><br/>                                                                 |
| [<span data-ttu-id="41a51-124">自訂控制項</span><span class="sxs-lookup"><span data-stu-id="41a51-124">Custom Controls</span></span>](user-controls-intro.md)<br/>                             | <span data-ttu-id="41a51-125">描述建立自訂控制項的各種方式。</span><span class="sxs-lookup"><span data-stu-id="41a51-125">Describes various ways of creating custom controls.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="41a51-126">子類別化控制項</span><span class="sxs-lookup"><span data-stu-id="41a51-126">Subclassing Controls</span></span>](subclassing-overview.md)<br/>                       | <span data-ttu-id="41a51-127">描述透過變更或加入新的功能來自訂控制項的方式。</span><span class="sxs-lookup"><span data-stu-id="41a51-127">Describes a way to customize a control by changing its features or adding new ones.</span></span> <br/>                                                 |
| [<span data-ttu-id="41a51-128">自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="41a51-128">Custom Draw</span></span>](custom-draw.md)<br/>                                         | <span data-ttu-id="41a51-129">描述由某些控制項提供的服務，應用程式可以使用這些控制項來自訂控制面板的各種層面。</span><span class="sxs-lookup"><span data-stu-id="41a51-129">Describes a service, provided by some controls, that applications can use to customize various aspects of the control's appearance.</span></span> <br/> |
| [<span data-ttu-id="41a51-130">安全性考慮： Microsoft Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="41a51-130">Security Considerations: Microsoft Windows Controls</span></span>](sec-comctls.md)<br/> | <span data-ttu-id="41a51-131">提供與 Windows 控制項相關之安全性考慮的資訊。</span><span class="sxs-lookup"><span data-stu-id="41a51-131">Provides information about security considerations related to the Windows controls.</span></span> <br/>                                                 |
| [<span data-ttu-id="41a51-132">控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="41a51-132">Control Library</span></span>](individual-control-info.md)<br/>                         | <span data-ttu-id="41a51-133">提供有關 User32.dll 和 Comctl32.dll 所支援之每個控制項的總覽和參考資訊。</span><span class="sxs-lookup"><span data-stu-id="41a51-133">Provides overviews and reference information about each control supported by User32.dll and Comctl32.dll.</span></span><br/>                            |
| [<span data-ttu-id="41a51-134">一般控制項參考</span><span class="sxs-lookup"><span data-stu-id="41a51-134">General Control Reference</span></span>](common-control-reference.md)<br/>              | <span data-ttu-id="41a51-135">提供適用于多個控制項之程式設計專案的參考資訊，而不只是特定的控制項。</span><span class="sxs-lookup"><span data-stu-id="41a51-135">Provides reference information about programming elements that apply to multiple controls, not just to a specific control.</span></span><br/>           |
| [<span data-ttu-id="41a51-136">控制 Spy 2.0 版</span><span class="sxs-lookup"><span data-stu-id="41a51-136">Control Spy v2.0</span></span>](control-spy.md)<br/>                                    | <span data-ttu-id="41a51-137">描述 Control Spy，這是可協助開發人員瞭解通用控制項的工具。</span><span class="sxs-lookup"><span data-stu-id="41a51-137">Describes Control Spy, a tool that helps developers understand common controls.</span></span> <br/>                                                     |
| [<span data-ttu-id="41a51-138">視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="41a51-138">Visual Styles</span></span>](themes-overview.md)<br/>                                   | <span data-ttu-id="41a51-139">說明如何根據使用者選擇的視覺化樣式來變更控制項的外觀。</span><span class="sxs-lookup"><span data-stu-id="41a51-139">Describes how the appearance of controls can change depending on the visual style chosen by the user.</span></span> <br/>                               |
| [<span data-ttu-id="41a51-140">主題檔案格式</span><span class="sxs-lookup"><span data-stu-id="41a51-140">Theme File Format</span></span>](themesfileformat-overview.md)<br/>                     | <span data-ttu-id="41a51-141">討論主題 ( 的格式) Windows 7 和 Windows Vista 中使用的檔。</span><span class="sxs-lookup"><span data-stu-id="41a51-141">Discusses the format of Theme (.theme) files used in Windows 7 and Windows Vista.</span></span><br/>                                                    |



 

 

 





