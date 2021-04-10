---
title: 元件感知
description: 您的應用程式必須回應 WM \_ PALETTECHANGED、wm \_ QUERYNEWPALETTE 和 wm \_ 啟動訊息，才能察覺並使用調色板。 將您的應用程式設計為選取並實現調色板以回應這些訊息。
ms.assetid: 0670e929-dfdb-44d2-bda2-c532d1739d8e
keywords:
- Windows 上的 OpenGL、元件感知
- 調色板感知 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ceab4c27f63c12977d072f84e789d1800b6557
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842675"
---
# <a name="palette-awareness"></a><span data-ttu-id="5ead9-106">元件感知</span><span class="sxs-lookup"><span data-stu-id="5ead9-106">Palette Awareness</span></span>

<span data-ttu-id="5ead9-107">您的應用程式必須回應 [wm \_ PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged)、 [wm \_ QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette)和 [wm \_ 啟動](../inputdev/wm-activate.md) 訊息，才能察覺並使用調色板。</span><span class="sxs-lookup"><span data-stu-id="5ead9-107">Your application must respond to the [WM\_PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged), [WM\_QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette), and [WM\_ACTIVATE](../inputdev/wm-activate.md) messages to be aware of and use palettes.</span></span> <span data-ttu-id="5ead9-108">將您的應用程式設計為選取並實現調色板以回應這些訊息。</span><span class="sxs-lookup"><span data-stu-id="5ead9-108">Design your application to select and realize palettes in response to these messages.</span></span>

<span data-ttu-id="5ead9-109">如需調色板和調色板感知的詳細資訊，請參閱 Microsoft 開發人員網路開發程式庫 compact 光碟上的「調色板感知」和「元件管理員：如何與原因」文章。</span><span class="sxs-lookup"><span data-stu-id="5ead9-109">For more information on palettes and palette awareness, see the articles "Palette Awareness," and "The Palette Manager: How and Why" on the Microsoft Developer Network Development Library compact discs.</span></span>

 

 