---
description: 盡可能使用標準的 Windows 控制項，因為它們與 Microsoft Active Accessibility 的指導方針完全相容。 這包括 Windows (User32.dll) 所提供的控制項，以及 (Comctl32.dll) 的 Windows 通用控制項程式庫。
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: 使用標準 Windows 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318291"
---
# <a name="using-standard-windows-controls"></a><span data-ttu-id="8f75f-104">使用標準 Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="8f75f-104">Using Standard Windows Controls</span></span>

<span data-ttu-id="8f75f-105">盡可能使用標準的 Windows 控制項，因為它們與 Microsoft Active Accessibility 的指導方針完全相容。</span><span class="sxs-lookup"><span data-stu-id="8f75f-105">Use standard Windows controls whenever possible, because they are fully compatible with Microsoft Active Accessibility guidelines.</span></span> <span data-ttu-id="8f75f-106">這包括 Windows (User32.dll) 所提供的控制項，以及 (Comctl32.dll) 的 Windows 通用控制項程式庫。</span><span class="sxs-lookup"><span data-stu-id="8f75f-106">This includes controls provided by Windows (User32.dll) and the Windows common controls library (Comctl32.dll).</span></span>

<span data-ttu-id="8f75f-107">每個標準 Windows 控制項都是特定類別的個別視窗，因此當焦點移至新的控制項時，就會通知協助工具輔助。</span><span class="sxs-lookup"><span data-stu-id="8f75f-107">Each standard Windows control is a separate window of a specific class, so the accessibility aid is notified when the focus moves to a new control.</span></span> <span data-ttu-id="8f75f-108">輔助工具可以決定控制項視窗類別，以及它可以傳送來查詢或改變控制項狀態的任何其他訊息。</span><span class="sxs-lookup"><span data-stu-id="8f75f-108">The aid can determine the controls window class, and any additional messages it can send to query or alter the controls state.</span></span> <span data-ttu-id="8f75f-109">輔助工具也可以識別父視窗內包含的所有子控制項，並識別任何控制項的父系。</span><span class="sxs-lookup"><span data-stu-id="8f75f-109">The aid can also identify all of the child controls contained within a parent window and identify the parent of any control.</span></span>

<span data-ttu-id="8f75f-110">某些常見的控制項非常有彈性，而且通常可以替代較不容易存取的自訂控制項和主控描繪的控制項。</span><span class="sxs-lookup"><span data-stu-id="8f75f-110">Some common controls are extremely flexible and can often substitute for less-accessible custom controls and owner-drawn controls.</span></span> <span data-ttu-id="8f75f-111">例如，清單視圖可以取代主控描繪清單方塊，以顯示每個專案旁的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="8f75f-111">For example, a list view can replace an owner-drawn list box to display a check box next to each item.</span></span> <span data-ttu-id="8f75f-112">另一個範例是，增強型按鈕控制項可以顯示影像和文字。</span><span class="sxs-lookup"><span data-stu-id="8f75f-112">As another example, the enhanced button control can display both images and text.</span></span> <span data-ttu-id="8f75f-113">之前，這需要使用自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="8f75f-113">Previously, this required the use of a custom control.</span></span>

 

 



