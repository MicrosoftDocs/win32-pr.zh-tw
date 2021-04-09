---
title: 使用 Rebar 控制項
description: 本章節包含的主題會示範如何建立和使用 Rebar 控制項。
ms.assetid: b821216f-609e-41a4-8d45-69609f3572bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9174a4ee05b966037bb30be3e796bcc2c3e00da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683159"
---
# <a name="using-rebar-controls"></a><span data-ttu-id="4e28f-103">使用 Rebar 控制項</span><span class="sxs-lookup"><span data-stu-id="4e28f-103">Using Rebar Controls</span></span>

<span data-ttu-id="4e28f-104">本章節包含的主題會示範如何建立和使用 Rebar 控制項。</span><span class="sxs-lookup"><span data-stu-id="4e28f-104">This section contains topics that demonstrate how to create and use rebar controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4e28f-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="4e28f-105">In this section</span></span>



| <span data-ttu-id="4e28f-106">主題</span><span class="sxs-lookup"><span data-stu-id="4e28f-106">Topic</span></span>                                                                | <span data-ttu-id="4e28f-107">描述</span><span class="sxs-lookup"><span data-stu-id="4e28f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e28f-108">如何建立 Rebar 控制項</span><span class="sxs-lookup"><span data-stu-id="4e28f-108">How to Create Rebar Controls</span></span>](create-rebar-controls.md)<br/> | <span data-ttu-id="4e28f-109">應用程式會藉由呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立 Rebar 控制項，並將 [**REBARCLASSNAME**](common-control-window-classes.md) 指定為 window 類別。</span><span class="sxs-lookup"><span data-stu-id="4e28f-109">An application creates a rebar control by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**REBARCLASSNAME**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="4e28f-110">應用程式必須先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來註冊視窗類別，並 \_ \_ 在伴隨的 [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 結構中指定「ICC 非經常性存取類別」位。</span><span class="sxs-lookup"><span data-stu-id="4e28f-110">The application must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_COOL\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span> <br/> |



 

 

