---
description: 應用程式可以藉由呼叫 PathToRegion 函數，將路徑轉換成區域。
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: 將路徑轉換成區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691915"
---
# <a name="conversion-of-paths-to-regions"></a><span data-ttu-id="eb5ae-103">將路徑轉換成區域</span><span class="sxs-lookup"><span data-stu-id="eb5ae-103">Conversion of Paths to Regions</span></span>

<span data-ttu-id="eb5ae-104">應用程式可以藉由呼叫 [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) 函數，將路徑轉換成區域。</span><span class="sxs-lookup"><span data-stu-id="eb5ae-104">An application can convert a path into a region by calling the [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) function.</span></span> <span data-ttu-id="eb5ae-105">如同 [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)， **PathToRegion** 在建立特殊圖形效果方面很有用。</span><span class="sxs-lookup"><span data-stu-id="eb5ae-105">Like [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** is useful in the creation of special graphics effects.</span></span> <span data-ttu-id="eb5ae-106">例如，沒有可允許應用程式位移路徑的函式;不過，有一個函式可讓應用程式 ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)) 來位移區域。</span><span class="sxs-lookup"><span data-stu-id="eb5ae-106">For example, there are no functions that allow an application to offset a path; however, there is a function that enables an application to offset a region ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span></span> <span data-ttu-id="eb5ae-107">使用 **PathToRegion** ，應用程式可以藉由建立定義圖形的路徑、將路徑轉換成區域 (藉由呼叫 **PathToRegion**) ，然後重複繪製、移動和清除區域 (（例如 [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn)、 **OffsetRgn** 和 **FillRgn**) ），來建立複雜圖形的動畫效果。</span><span class="sxs-lookup"><span data-stu-id="eb5ae-107">Using **PathToRegion** , an application can create the effect of animating a complex shape by creating a path that defines the shape, converting the path into a region (by calling **PathToRegion**), and then repeatedly painting, moving, and erasing the region (by calling functions in a sequence, such as [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** , and **FillRgn**).</span></span>

 

 



