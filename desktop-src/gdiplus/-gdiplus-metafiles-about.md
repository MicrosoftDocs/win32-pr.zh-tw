---
description: Windows GDI + 提供了中繼檔類別，讓您可以記錄和顯示中繼檔。
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: " (GDI +) 的中繼檔"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318339"
---
# <a name="metafiles-gdi"></a><span data-ttu-id="5974b-103"> (GDI +) 的中繼檔</span><span class="sxs-lookup"><span data-stu-id="5974b-103">Metafiles (GDI+)</span></span>

<span data-ttu-id="5974b-104">Windows GDI + 提供了 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 類別，讓您可以記錄和顯示中繼檔。</span><span class="sxs-lookup"><span data-stu-id="5974b-104">Windows GDI+ provides the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class so that you can record and display metafiles.</span></span> <span data-ttu-id="5974b-105">中繼檔（也稱為向量影像）是儲存為一系列繪製命令和設定的影像。</span><span class="sxs-lookup"><span data-stu-id="5974b-105">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="5974b-106">在 **中繼檔** 物件中記錄的命令和設定可以儲存在記憶體中，或儲存至檔案或資料流程。</span><span class="sxs-lookup"><span data-stu-id="5974b-106">The commands and settings recorded in a **Metafile** object can be stored in memory or saved to a file or stream.</span></span>

<span data-ttu-id="5974b-107">GDI + 可以顯示以下列格式儲存的中繼檔：</span><span class="sxs-lookup"><span data-stu-id="5974b-107">GDI+ can display metafiles that have been stored in the following formats:</span></span>

-   <span data-ttu-id="5974b-108">Windows 中繼檔格式 (WMF) </span><span class="sxs-lookup"><span data-stu-id="5974b-108">Windows Metafile Format (WMF)</span></span>
-   <span data-ttu-id="5974b-109">加強型中繼檔 (EMF) </span><span class="sxs-lookup"><span data-stu-id="5974b-109">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="5974b-110">EMF +</span><span class="sxs-lookup"><span data-stu-id="5974b-110">EMF+</span></span>

<span data-ttu-id="5974b-111">GDI + 可以記錄 EMF 和 EMF + 格式的中繼檔，但不能以 WMF 格式記錄。</span><span class="sxs-lookup"><span data-stu-id="5974b-111">GDI+ can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>

<span data-ttu-id="5974b-112">EMF + 是 EMF 的延伸模組，可讓您儲存 GDI + 記錄。</span><span class="sxs-lookup"><span data-stu-id="5974b-112">EMF+ is an extension to EMF that allows GDI+ records to be stored.</span></span> <span data-ttu-id="5974b-113">EMF + 格式有兩種變化： [僅限 EMF +] 和 [EMF + 雙重]。</span><span class="sxs-lookup"><span data-stu-id="5974b-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="5974b-114">僅限 EMF + 的中繼檔只包含 GDI + 記錄。</span><span class="sxs-lookup"><span data-stu-id="5974b-114">EMF+ Only metafiles contain only GDI+ records.</span></span> <span data-ttu-id="5974b-115">GDI + 可能會顯示這類中繼檔，但 Windows 圖形裝置介面 (GDI) 。</span><span class="sxs-lookup"><span data-stu-id="5974b-115">Such metafiles can be displayed by GDI+ but not by Windows Graphics Device Interface (GDI).</span></span> <span data-ttu-id="5974b-116">EMF + 雙重中繼檔包含 GDI + 和 GDI 記錄。</span><span class="sxs-lookup"><span data-stu-id="5974b-116">EMF+ Dual metafiles contain GDI+ and GDI records.</span></span> <span data-ttu-id="5974b-117">EMF + 雙重中繼檔中的每個 GDI + 記錄都會與替代的 GDI 記錄配對。</span><span class="sxs-lookup"><span data-stu-id="5974b-117">Each GDI+ record in an EMF+ Dual metafile is paired with an alternate GDI record.</span></span> <span data-ttu-id="5974b-118">GDI + 或 GDI 可以顯示這類中繼檔。</span><span class="sxs-lookup"><span data-stu-id="5974b-118">Such metafiles can be displayed by GDI+ or by GDI.</span></span>

<span data-ttu-id="5974b-119">下列範例會在磁片檔案中記錄一個設定和一個繪圖命令。</span><span class="sxs-lookup"><span data-stu-id="5974b-119">The following example records one setting and one drawing command in a disk file.</span></span> <span data-ttu-id="5974b-120">請注意，此範例會建立 [**graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，而 **graphics** 物件的函式會接收 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 物件的位址做為引數。</span><span class="sxs-lookup"><span data-stu-id="5974b-120">Note that the example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and that the constructor for the **Graphics** object receives the address of a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object as an argument.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



<span data-ttu-id="5974b-121">如上一個範例所示， [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別是在 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 物件中記錄指令和設定的關鍵。</span><span class="sxs-lookup"><span data-stu-id="5974b-121">As the preceding example shows, the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the key to recording instructions and settings in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="5974b-122">對 **圖形** 物件的方法所做的任何呼叫都可以記錄在 **中繼檔** 物件中。</span><span class="sxs-lookup"><span data-stu-id="5974b-122">Any call made to a method of a **Graphics** object can be recorded in a **Metafile** object.</span></span> <span data-ttu-id="5974b-123">同樣地，您可以設定 **圖形** 物件的任何屬性，並將該設定記錄在 **中繼檔** 物件中。</span><span class="sxs-lookup"><span data-stu-id="5974b-123">Likewise, you can set any property of a **Graphics** object and record that setting in a **Metafile** object.</span></span> <span data-ttu-id="5974b-124">當 **圖形** 物件被刪除或超出範圍時，就會結束錄製。</span><span class="sxs-lookup"><span data-stu-id="5974b-124">The recording ends when the **Graphics** object is deleted or goes out of scope.</span></span>

<span data-ttu-id="5974b-125">下列範例會顯示先前範例中所建立的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="5974b-125">The following example displays the metafile created in the preceding example.</span></span> <span data-ttu-id="5974b-126">中繼檔的左上角會顯示 (100，100) 。</span><span class="sxs-lookup"><span data-stu-id="5974b-126">The metafile is displayed with its upper-left corner at (100, 100).</span></span>


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



<span data-ttu-id="5974b-127">下列範例會記錄 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 物件中 (裁剪區域、世界轉換和平滑模式) 的數個屬性設定。</span><span class="sxs-lookup"><span data-stu-id="5974b-127">The following example records several property settings (clipping region, world transformation, and smoothing mode) in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="5974b-128">然後，程式碼會記錄數個繪圖指令。</span><span class="sxs-lookup"><span data-stu-id="5974b-128">Then the code records several drawing instructions.</span></span> <span data-ttu-id="5974b-129">指示和設定會儲存在磁片檔案中。</span><span class="sxs-lookup"><span data-stu-id="5974b-129">The instructions and settings are saved in a disk file.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



<span data-ttu-id="5974b-130">下列範例會顯示先前範例中所建立的中繼檔映射。</span><span class="sxs-lookup"><span data-stu-id="5974b-130">The following example displays the metafile image created in the preceding example.</span></span>


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



<span data-ttu-id="5974b-131">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="5974b-131">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="5974b-132">請注意消除鋸齒、橢圓形裁剪區域和30度旋轉。</span><span class="sxs-lookup"><span data-stu-id="5974b-132">Note the antialiasing, the elliptical clipping region, and the 30-degree rotation.</span></span>

![視窗的螢幕擷取畫面，其中包含填滿繪製于橢圓形外面某個點之線條的橢圓形](images/aboutgdip05-art00.png)

 

 



