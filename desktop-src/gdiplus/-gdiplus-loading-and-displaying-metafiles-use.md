---
description: Image 類別提供載入和顯示點陣影像和向量影像的基本方法。 中繼檔類別繼承自 Image 類別，可提供更特製化的方法來錄製、顯示和檢查向量影像。
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: 載入和顯示中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026202"
---
# <a name="loading-and-displaying-metafiles"></a><span data-ttu-id="65af7-104">載入和顯示中繼檔</span><span class="sxs-lookup"><span data-stu-id="65af7-104">Loading and Displaying Metafiles</span></span>

<span data-ttu-id="65af7-105">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別提供載入和顯示點陣影像和向量影像的基本方法。</span><span class="sxs-lookup"><span data-stu-id="65af7-105">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="65af7-106">[**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)類別繼承自 **Image** 類別，可提供更特製化的方法來錄製、顯示和檢查向量影像。</span><span class="sxs-lookup"><span data-stu-id="65af7-106">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the **Image** class, provides more specialized methods for recording, displaying, and examining vector images.</span></span>

<span data-ttu-id="65af7-107">若要在螢幕上顯示 (中繼檔) 的向量影像，您需要 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件和 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。</span><span class="sxs-lookup"><span data-stu-id="65af7-107">To display a vector image (metafile) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="65af7-108">將檔案的名稱 (或) 的資料流程指標傳遞至 **影像** 的函式。</span><span class="sxs-lookup"><span data-stu-id="65af7-108">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="65af7-109">建立 **影像** 物件之後，將該 **影像** 物件的位址傳遞給 **圖形** 物件的 **DrawImage** 方法。</span><span class="sxs-lookup"><span data-stu-id="65af7-109">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="65af7-110">下列範例會從 EMF (增強的中繼檔) 檔案建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後在 (60，10) 的左上角繪製影像：</span><span class="sxs-lookup"><span data-stu-id="65af7-110">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from an EMF (enhanced metafile) file and then draws the image with its upper-left corner at (60, 10):</span></span>


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



<span data-ttu-id="65af7-111">下圖顯示在指定位置繪製的影像。</span><span class="sxs-lookup"><span data-stu-id="65af7-111">The following illustration shows the image drawn at the specified location.</span></span>

![視窗的螢幕擷取畫面，其中包含影像並指定原點](images/imageposition2.png)

 

 



