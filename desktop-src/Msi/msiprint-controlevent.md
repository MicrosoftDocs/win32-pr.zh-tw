---
description: 此事件是由 ScrollableText 控制項所發佈，讓使用者可以列印該控制項的內容。
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852528"
---
# <a name="msiprint-controlevent"></a><span data-ttu-id="3103a-103">MsiPrint ControlEvent</span><span class="sxs-lookup"><span data-stu-id="3103a-103">MsiPrint ControlEvent</span></span>

<span data-ttu-id="3103a-104">此事件是由 [ScrollableText 控制項](scrollabletext-control.md) 所發佈，讓使用者可以列印該控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="3103a-104">This event is published by the [ScrollableText Control](scrollabletext-control.md) to enable the user to print the contents of that control.</span></span>

<span data-ttu-id="3103a-105">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="3103a-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="3103a-106">從 Windows Installer 5.0 開始提供此 ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="3103a-106">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="3103a-107">此事件應由位於與[ScrollableText 控制項](scrollabletext-control.md)相同對話方塊的[按鈕控制項](pushbutton-control.md)訂閱。</span><span class="sxs-lookup"><span data-stu-id="3103a-107">This event should be subscribed to by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the [ScrollableText Control](scrollabletext-control.md).</span></span> <span data-ttu-id="3103a-108">TheMsiPrint ControlEvent 應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。</span><span class="sxs-lookup"><span data-stu-id="3103a-108">TheMsiPrint ControlEvent should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="3103a-109">發佈者</span><span class="sxs-lookup"><span data-stu-id="3103a-109">Published By</span></span>

[<span data-ttu-id="3103a-110">ScrollableText</span><span class="sxs-lookup"><span data-stu-id="3103a-110">ScrollableText</span></span>](scrollabletext-control.md)

## <a name="argument"></a><span data-ttu-id="3103a-111">引數</span><span class="sxs-lookup"><span data-stu-id="3103a-111">Argument</span></span>

<span data-ttu-id="3103a-112">這個 ControlEvent 不會使用引數。</span><span class="sxs-lookup"><span data-stu-id="3103a-112">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="3103a-113">訂閱者的動作</span><span class="sxs-lookup"><span data-stu-id="3103a-113">Action on Subscribers</span></span>

<span data-ttu-id="3103a-114">此 ControlEvent 不會在訂閱者上執行動作。</span><span class="sxs-lookup"><span data-stu-id="3103a-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="3103a-115">一般用法</span><span class="sxs-lookup"><span data-stu-id="3103a-115">Typical Use</span></span>

<span data-ttu-id="3103a-116">與[ScrollableText 控制項](scrollabletext-control.md)相同對話方塊上的[按鈕](pushbutton-control.md)控制項可用來顯示模式對話方塊，讓使用者可以列印 ScrollableText 控制項的內容。</span><span class="sxs-lookup"><span data-stu-id="3103a-116">A [PushButton](pushbutton-control.md) control on the same dialog box as the [ScrollableText Control](scrollabletext-control.md) can be used to display a modal dialog box enabling the user to print the contents of the ScrollableText Control.</span></span>

 

 



