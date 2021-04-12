---
title: 鍵盤喜好設定參數
description: 鍵盤喜好設定參數表示使用者依賴鍵盤而非滑鼠，因此應用程式應該會顯示其他隱藏的鍵盤介面。
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375808"
---
# <a name="keyboard-preference-parameter"></a><span data-ttu-id="50057-103">鍵盤喜好設定參數</span><span class="sxs-lookup"><span data-stu-id="50057-103">Keyboard preference parameter</span></span>

<span data-ttu-id="50057-104">鍵盤喜好設定參數表示使用者依賴鍵盤而非滑鼠，因此應用程式應該會顯示其他隱藏的鍵盤介面。</span><span class="sxs-lookup"><span data-stu-id="50057-104">The keyboard preference parameter indicates that the user relies on the keyboard instead of the mouse, so applications should display keyboard interfaces that would otherwise be hidden.</span></span>

<span data-ttu-id="50057-105">使用者可以使用主控台中的輕鬆存取中心來控制鍵盤喜好設定參數的設定，或使用其他應用程式來自訂環境。</span><span class="sxs-lookup"><span data-stu-id="50057-105">The user controls the setting of the keyboard preference parameter by using the Ease of Access Center in Control Panel, or another application for customizing the environment.</span></span> <span data-ttu-id="50057-106">應用程式會使用 **spi \_ GETKEYBOARDPREF** 和 **spi \_ SETKEYBOARDPREF** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定鍵盤喜好設定參數。</span><span class="sxs-lookup"><span data-stu-id="50057-106">Applications use the **SPI\_GETKEYBOARDPREF** and **SPI\_SETKEYBOARDPREF** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the keyboard preference parameter.</span></span>

<span data-ttu-id="50057-107">此外，在 Windows 2000 上，使用者可以設定一個參數，指出功能表便捷鍵是否一律加上底線。</span><span class="sxs-lookup"><span data-stu-id="50057-107">Additionally, on Windows 2000, users can set a parameter that indicates whether menu access keys are always underlined.</span></span> <span data-ttu-id="50057-108">應用程式會使用 **spi \_ GETMENUUNDERLINES** 和 **spi \_ SETMENUUNDERLINES** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定功能表底線參數。</span><span class="sxs-lookup"><span data-stu-id="50057-108">Applications use the **SPI\_GETMENUUNDERLINES** and **SPI\_SETMENUUNDERLINES** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the menu underlines parameter.</span></span>

<span data-ttu-id="50057-109">當應用程式收到鍵盤喜好設定或功能表底線參數的 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) 訊息時，建議應用程式呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 來更新這兩個參數的資訊。</span><span class="sxs-lookup"><span data-stu-id="50057-109">When an application receives a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message for either the keyboard preference or menu underline parameter, it is recommended that the application call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) to update the information for both parameters.</span></span>

<span data-ttu-id="50057-110">請注意 **， \_ spi GETMENUUNDERLINES** 與 **spi \_ GETKEYBOARDCUES** 相同，且 **spi \_ SETMENUUNDERLINES** 與 **spi \_ SETKEYBOARDCUES** 相同。</span><span class="sxs-lookup"><span data-stu-id="50057-110">Note that **SPI\_GETMENUUNDERLINES** is the same as **SPI\_GETKEYBOARDCUES**, and **SPI\_SETMENUUNDERLINES** is the same as **SPI\_SETKEYBOARDCUES**.</span></span>

 

 