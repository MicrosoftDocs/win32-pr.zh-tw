---
description: 16位 Windows 所提供的印表機轉義允許存取特殊裝置功能。
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: 印表機轉義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193375"
---
# <a name="printer-escapes"></a><span data-ttu-id="a2b60-103">印表機轉義</span><span class="sxs-lookup"><span data-stu-id="a2b60-103">Printer Escapes</span></span>

<span data-ttu-id="a2b60-104">16位 Windows 所提供的印表機轉義允許存取特殊裝置功能。</span><span class="sxs-lookup"><span data-stu-id="a2b60-104">The printer escapes provided by 16-bit Windows allowed access special device features.</span></span> <span data-ttu-id="a2b60-105">這些轉義大部分都已過時，但有幾個是為了簡化16位 Windows 應用程式的移植而提供。</span><span class="sxs-lookup"><span data-stu-id="a2b60-105">Most of these escapes are obsolete, but a few are provided to simplify the porting of 16-bit Windows-based applications.</span></span> <span data-ttu-id="a2b60-106">GDI 支援一組完整的路徑函式，可讓應用程式使用，而不是使用 esc 鍵在任何裝置上繪製路徑。</span><span class="sxs-lookup"><span data-stu-id="a2b60-106">GDI supports a complete set of path functions that applications can use instead of the escapes to draw paths on any device.</span></span> <span data-ttu-id="a2b60-107">如需取代部分轉義的函式清單，請參閱 [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) 函數。</span><span class="sxs-lookup"><span data-stu-id="a2b60-107">For a list of functions that replace some of the escapes, see the [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) function.</span></span>

<span data-ttu-id="a2b60-108">在64原始印表機的轉義中，只能使用 **QUERYESCSUPPORT** 和 **傳遞** 。</span><span class="sxs-lookup"><span data-stu-id="a2b60-108">Of the 64 original printer escapes, only **QUERYESCSUPPORT** and **PASSTHROUGH** can be used.</span></span>

<span data-ttu-id="a2b60-109">另外還有一個稱為 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的延伸 escape 函數。</span><span class="sxs-lookup"><span data-stu-id="a2b60-109">There is also an extended escape function called [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="a2b60-110">此函式可讓應用程式存取特定裝置的功能，而不是透過 GDI 直接提供。</span><span class="sxs-lookup"><span data-stu-id="a2b60-110">This function allows applications to access capabilities of a particular device not directly available through GDI.</span></span>

 

 



