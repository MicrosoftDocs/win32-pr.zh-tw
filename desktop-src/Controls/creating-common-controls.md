---
title: 建立通用控制項
description: 本主題說明如何建立屬於通用控制項程式庫中所定義之視窗類別的視窗 Comctl32.dll。
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933723"
---
# <a name="creating-common-controls"></a><span data-ttu-id="40f21-103">建立通用控制項</span><span class="sxs-lookup"><span data-stu-id="40f21-103">Creating Common Controls</span></span>

<span data-ttu-id="40f21-104">本主題說明如何建立屬於通用控制項程式庫中所定義之視窗類別的視窗 Comctl32.dll。</span><span class="sxs-lookup"><span data-stu-id="40f21-104">This topic describes how to create a window that belongs to a window class defined in the common control library, Comctl32.dll.</span></span>


<span data-ttu-id="40f21-105">最常見的控制項屬於通用控制項 DLL 中定義的視窗類別。</span><span class="sxs-lookup"><span data-stu-id="40f21-105">Most common controls belong to a window class defined in the common control DLL.</span></span> <span data-ttu-id="40f21-106">視窗類別和對應的視窗程式會定義控制項的屬性、外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="40f21-106">The window class and the corresponding window procedure define the properties, appearance, and behavior of the control.</span></span> <span data-ttu-id="40f21-107">若要確定已載入通用控制項 DLL，請在您的應用程式中包含 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式。</span><span class="sxs-lookup"><span data-stu-id="40f21-107">To ensure that the common control DLL is loaded, include the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function in your application.</span></span> <span data-ttu-id="40f21-108">您可以在呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式時指定視窗類別的名稱，或在對話方塊範本中指定適當的類別名稱，藉以建立通用控制項。</span><span class="sxs-lookup"><span data-stu-id="40f21-108">You create a common control by specifying the name of the window class when calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or by specifying the appropriate class name in a dialog box template.</span></span>


<span data-ttu-id="40f21-109">每種類型的通用控制項都有一組控制項樣式，可用來改變控制項的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="40f21-109">Each type of common control has a set of control styles that you can use to vary the appearance and behavior of the control.</span></span> <span data-ttu-id="40f21-110">通用控制項程式庫也包含一組控制項樣式，適用于兩種或多種類型的通用控制項。</span><span class="sxs-lookup"><span data-stu-id="40f21-110">The common control library also includes a set of control styles that apply to two or more types of common controls.</span></span> <span data-ttu-id="40f21-111">[ [樣式](common-control-styles.md) ] 區段中描述的通用控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="40f21-111">The common control styles are described in the [Styles](common-control-styles.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40f21-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="40f21-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40f21-113">關於通用控制項</span><span class="sxs-lookup"><span data-stu-id="40f21-113">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 