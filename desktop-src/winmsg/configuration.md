---
description: 組態
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: 'Configuration (Windows 和訊息) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194566"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="58649-103">Configuration (Windows 和訊息) </span><span class="sxs-lookup"><span data-stu-id="58649-103">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="58649-104">*顯示元素* 是視窗的元件，以及顯示在系統顯示畫面上的顯示。</span><span class="sxs-lookup"><span data-stu-id="58649-104">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="58649-105">*系統計量* 是各種顯示元素的維度。</span><span class="sxs-lookup"><span data-stu-id="58649-105">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="58649-106">一般系統計量包括視窗框線寬度、圖示高度等等。</span><span class="sxs-lookup"><span data-stu-id="58649-106">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="58649-107">系統計量也會描述系統的其他層面，例如是否已安裝滑鼠、支援雙位元組字元，或是已安裝作業系統的偵錯工具版本。</span><span class="sxs-lookup"><span data-stu-id="58649-107">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="58649-108">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)函式會捕獲指定的系統計量。</span><span class="sxs-lookup"><span data-stu-id="58649-108">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="58649-109">應用程式也可以分別使用 [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) 和 [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) 函式，來抓取和設定視窗元素（例如功能表、捲軸和按鈕）的色彩。</span><span class="sxs-lookup"><span data-stu-id="58649-109">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="58649-110">[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)函式會捕獲或設定各種系統屬性，例如按兩下時間、螢幕保護裝置超時時間、視窗框線寬度和桌面圖案。</span><span class="sxs-lookup"><span data-stu-id="58649-110">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="58649-111">當應用程式使用 **SystemParametersInfo** 來設定參數時，會立即進行變更。</span><span class="sxs-lookup"><span data-stu-id="58649-111">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="58649-112">此功能也可讓應用程式更新使用者設定檔，因此系統重新開機時，系統將會保留系統的變更。</span><span class="sxs-lookup"><span data-stu-id="58649-112">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
