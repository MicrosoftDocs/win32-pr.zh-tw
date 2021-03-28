---
description: 每個監視器都可以有自己的色彩深度。
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: 多顯示器顯示器上的色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943808"
---
# <a name="colors-on-multiple-display-monitors"></a><span data-ttu-id="0f081-103">多顯示器顯示器上的色彩</span><span class="sxs-lookup"><span data-stu-id="0f081-103">Colors on Multiple Display Monitors</span></span>

<span data-ttu-id="0f081-104">每個監視器都可以有自己的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="0f081-104">Each monitor can have its own color depth.</span></span> <span data-ttu-id="0f081-105">系統會在不同色彩深度的監視器之間，自動調整色彩。</span><span class="sxs-lookup"><span data-stu-id="0f081-105">The system automatically adjusts colors as windows move across monitors with different color depths.</span></span> <span data-ttu-id="0f081-106">一般來說，這會產生良好的結果。</span><span class="sxs-lookup"><span data-stu-id="0f081-106">In general, this produces good results.</span></span> <span data-ttu-id="0f081-107">不過，這不一定是最佳的作法。</span><span class="sxs-lookup"><span data-stu-id="0f081-107">However, this is not always optimal.</span></span> <span data-ttu-id="0f081-108">若要利用不同監視的色彩功能，請參閱下面的「 [在多個顯示監視器上繪製](painting-on-multiple-display-monitors.md) 」一節。</span><span class="sxs-lookup"><span data-stu-id="0f081-108">To take advantage of the color capabilities of different monitors, see the [Painting on Multiple Display Monitors](painting-on-multiple-display-monitors.md) section that follows.</span></span>

<span data-ttu-id="0f081-109">若要判斷所有監視器是否具有相同的色彩格式，請使用 SM SAMEDISPLAYFORMAT 呼叫 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \_ 。</span><span class="sxs-lookup"><span data-stu-id="0f081-109">To determine if all monitors have the same color format, call [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_SAMEDISPLAYFORMAT.</span></span>

<span data-ttu-id="0f081-110">如果主要監視器是調色盤， [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) 和 [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) 的運作方式與之前相同，但會在所有監視器上運作。</span><span class="sxs-lookup"><span data-stu-id="0f081-110">If the primary monitor is palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) and [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) work the same as before, but across all monitors.</span></span> <span data-ttu-id="0f081-111">此外，所有調色盤裝置的調板都會進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="0f081-111">In addition, the palettes of all palettized devices are synchronized.</span></span> <span data-ttu-id="0f081-112">如果主要監視器未調色盤， **SelectPalette** 和 **RealizePalette** 將會在背景中選取選擇區，而調色盤裝置將不會進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="0f081-112">If the primary monitor is not palettized, **SelectPalette** and **RealizePalette** will select the palette into the background and palettized devices will not be synchronized.</span></span>

 

 
