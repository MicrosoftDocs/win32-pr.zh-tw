---
description: 中繼檔類別繼承自 Image 類別，可讓您記錄一系列的繪圖命令。
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: 錄製中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972152"
---
# <a name="recording-metafiles"></a><span data-ttu-id="817ae-103">錄製中繼檔</span><span class="sxs-lookup"><span data-stu-id="817ae-103">Recording Metafiles</span></span>

<span data-ttu-id="817ae-104">[**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)類別繼承自 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別，可讓您記錄一系列的繪圖命令。</span><span class="sxs-lookup"><span data-stu-id="817ae-104">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, allows you to record a sequence of drawing commands.</span></span> <span data-ttu-id="817ae-105">錄製的命令可以儲存在記憶體中、儲存至檔案，或儲存至資料流程。</span><span class="sxs-lookup"><span data-stu-id="817ae-105">The recorded commands can be stored in memory, saved to a file, or saved to a stream.</span></span> <span data-ttu-id="817ae-106">中繼檔可以包含向量圖形、點陣影像和文字。</span><span class="sxs-lookup"><span data-stu-id="817ae-106">Metafiles can contain vector graphics, raster images, and text.</span></span>

<span data-ttu-id="817ae-107">下列範例會建立 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 物件。</span><span class="sxs-lookup"><span data-stu-id="817ae-107">The following example creates a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="817ae-108">程式碼會使用 **中繼檔** 物件來記錄圖形命令序列，然後將記錄的命令儲存在名為 SampleMetafile 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="817ae-108">The code uses the **Metafile** object to record a sequence of graphics commands and then saves the recorded commands in a file named SampleMetafile.emf.</span></span> <span data-ttu-id="817ae-109">請注意， **中繼檔** 的函式會接收裝置內容控制碼，而 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 的函式會接收 **中繼檔** 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="817ae-109">Note that the **Metafile** constructor receives a device context handle, and the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor receives the address of the **Metafile** object.</span></span> <span data-ttu-id="817ae-110">當 **圖形** 物件超出範圍時，會停止錄製 (，並將記錄的命令儲存至檔案) 。</span><span class="sxs-lookup"><span data-stu-id="817ae-110">The recording stops (and the recorded commands are saved to the file) when the **Graphics** object goes out of scope.</span></span> <span data-ttu-id="817ae-111">最後兩行程式碼會藉由建立新的 **圖形** 物件，並將 **中繼檔** 物件的位址傳遞給該 **圖形** 物件的 **DrawImage** 方法，來顯示中繼檔。</span><span class="sxs-lookup"><span data-stu-id="817ae-111">The last two lines of code display the metafile by creating a new **Graphics** object and passing the address of the **Metafile** object to the **DrawImage** method of that **Graphics** object.</span></span> <span data-ttu-id="817ae-112">請注意，程式碼會使用相同的 **中繼檔** 物件來記錄，並顯示 (播放中繼檔) 。</span><span class="sxs-lookup"><span data-stu-id="817ae-112">Note that the code uses the same **Metafile** object to record and to display (play back) the metafile.</span></span>


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> <span data-ttu-id="817ae-113">若要記錄中繼檔，您必須根據 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)物件來建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件。</span><span class="sxs-lookup"><span data-stu-id="817ae-113">To record a metafile, you must construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="817ae-114">當 **圖形** 物件被刪除或移出範圍時，中繼檔的錄製便會結束。</span><span class="sxs-lookup"><span data-stu-id="817ae-114">The recording of the metafile ends when that **Graphics** object is deleted or goes out of scope.</span></span>

 

<span data-ttu-id="817ae-115">中繼檔包含自己的圖形狀態，此狀態是由用來記錄中繼檔的 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件所定義。</span><span class="sxs-lookup"><span data-stu-id="817ae-115">A metafile contains its own graphics state, which is defined by the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used to record the metafile.</span></span> <span data-ttu-id="817ae-116">**圖形** 物件的任何屬性 (裁剪區域、世界轉換、平滑模式，以及您在錄製中繼檔時設定的類似) 都會儲存在中繼檔中。</span><span class="sxs-lookup"><span data-stu-id="817ae-116">Any properties of the **Graphics** object (clip region, world transformation, smoothing mode, and the like) that you set while recording the metafile will be stored in the metafile.</span></span> <span data-ttu-id="817ae-117">當您顯示中繼檔時，將會根據這些儲存的屬性來完成繪圖。</span><span class="sxs-lookup"><span data-stu-id="817ae-117">When you display the metafile, the drawing will be done according to those stored properties.</span></span>

<span data-ttu-id="817ae-118">在下列範例中，假設在錄製中繼檔期間已將平滑模式設定為 SmoothingModeNormal。</span><span class="sxs-lookup"><span data-stu-id="817ae-118">In the following example, assume that the smoothing mode was set to SmoothingModeNormal during the recording of the metafile.</span></span> <span data-ttu-id="817ae-119">即使用於播放的 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件平滑模式設定為 SmoothingModeHighQuality，也會根據 SmoothingModeNormal 設定來播放中繼檔。</span><span class="sxs-lookup"><span data-stu-id="817ae-119">Even though the smoothing mode of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used for playback is set to SmoothingModeHighQuality, the metafile will be played according to the SmoothingModeNormal setting.</span></span> <span data-ttu-id="817ae-120">它是在錄製期間設定的平滑模式，而不是在播放之前設定的平滑模式。</span><span class="sxs-lookup"><span data-stu-id="817ae-120">It is the smoothing mode set during the recording that is important, not the smoothing mode set prior to playback.</span></span>


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



