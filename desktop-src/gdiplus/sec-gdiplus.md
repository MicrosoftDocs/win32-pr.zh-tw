---
description: 本主題提供與 Windows GDI + 程式設計相關之安全性考慮的資訊。
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 安全性考慮： GDI +
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8c9d50393708e58651566ee90adcb4339cb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991306"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="a8b31-103">安全性考慮： GDI +</span><span class="sxs-lookup"><span data-stu-id="a8b31-103">Security Considerations: GDI+</span></span>

<span data-ttu-id="a8b31-104">本主題提供與 Windows GDI + 程式設計相關之安全性考慮的資訊。</span><span class="sxs-lookup"><span data-stu-id="a8b31-104">This topic provides information about security considerations related to programming with Windows GDI+.</span></span> <span data-ttu-id="a8b31-105">本主題並未提供安全性問題的相關資訊，而是將其作為此技術領域的起點和參考。</span><span class="sxs-lookup"><span data-stu-id="a8b31-105">This topic doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="a8b31-106">驗證函式是否成功</span><span class="sxs-lookup"><span data-stu-id="a8b31-106">Verifying the Success of Constructors</span></span>](#verifying-the-success-of-constructors)
-   [<span data-ttu-id="a8b31-107">配置緩衝區</span><span class="sxs-lookup"><span data-stu-id="a8b31-107">Allocating Buffers</span></span>](#allocating-buffers)
-   [<span data-ttu-id="a8b31-108">錯誤檢查</span><span class="sxs-lookup"><span data-stu-id="a8b31-108">Error Checking</span></span>](#error-checking)
-   [<span data-ttu-id="a8b31-109">執行緒同步處理</span><span class="sxs-lookup"><span data-stu-id="a8b31-109">Thread Synchronization</span></span>](#thread-synchronization)
-   [<span data-ttu-id="a8b31-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8b31-110">Related topics</span></span>](#related-topics)

## <a name="verifying-the-success-of-constructors"></a><span data-ttu-id="a8b31-111">驗證函式是否成功</span><span class="sxs-lookup"><span data-stu-id="a8b31-111">Verifying the Success of Constructors</span></span>

<span data-ttu-id="a8b31-112">許多 GDI + 類別都提供 [**Image：： GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) 方法，您可以呼叫這個方法來判斷在物件上叫用的方法是否成功。</span><span class="sxs-lookup"><span data-stu-id="a8b31-112">Many of the GDI+ classes provide a [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method that you can call to determine whether methods invoked on an object are successful.</span></span> <span data-ttu-id="a8b31-113">您也可以呼叫 **Image：： GetLastStatus** 來判斷是否成功。</span><span class="sxs-lookup"><span data-stu-id="a8b31-113">You can also call **Image::GetLastStatus** to determine whether a constructor is successful.</span></span>

<span data-ttu-id="a8b31-114">下列範例示範如何建立 [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，並呼叫 [**Image：： GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) 方法來判斷是否成功。</span><span class="sxs-lookup"><span data-stu-id="a8b31-114">The following example shows how to construct an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and call the [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method to determine whether the constructor was successful.</span></span> <span data-ttu-id="a8b31-115">**Ok** 和 **InvalidParameter** 值是 [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status)列舉的元素。</span><span class="sxs-lookup"><span data-stu-id="a8b31-115">The values **Ok** and **InvalidParameter** are elements of the [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) enumeration.</span></span>


```C++
Image myImage(L"Climber.jpg");
Status st = myImage.GetLastStatus();

if(Ok == st)
   // The constructor was successful. Use myImage.
else if(InvalidParameter == st)
   // The constructor failed because of an invalid parameter.
else
   // Compare st to other elements of the Status 
   // enumeration or do general error processing.
```



## <a name="allocating-buffers"></a><span data-ttu-id="a8b31-116">配置緩衝區</span><span class="sxs-lookup"><span data-stu-id="a8b31-116">Allocating Buffers</span></span>

<span data-ttu-id="a8b31-117">有幾個 GDI + 方法會傳回由呼叫端配置的緩衝區中的數值或字元資料。</span><span class="sxs-lookup"><span data-stu-id="a8b31-117">Several GDI+ methods return numeric or character data in a buffer that is allocated by the caller.</span></span> <span data-ttu-id="a8b31-118">這兩種方法都有提供所需緩衝區大小的伴隨方法。</span><span class="sxs-lookup"><span data-stu-id="a8b31-118">For each of those methods, there is a companion method that gives the size of the required buffer.</span></span> <span data-ttu-id="a8b31-119">例如， [**GraphicsPath：： GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) 方法會傳回 [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b31-119">For example, the [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) method returns an array of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="a8b31-120">在呼叫 **GraphicsPath：： GetPathPoints** 之前，您必須配置夠大的緩衝區來保存該陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b31-120">Before you call **GraphicsPath::GetPathPoints**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="a8b31-121">您可以藉由呼叫 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)物件的 [**GraphicsPath：： GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount)方法，來判斷所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="a8b31-121">You can determine the size of the required buffer by calling the [**GraphicsPath::GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span>

<span data-ttu-id="a8b31-122">下列範例示範如何判斷 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) 物件中的點數目、配置夠大的緩衝區以容納多個點，然後呼叫 [**GraphicsPath：： GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) 來填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a8b31-122">The following example shows how to determine the number of points in a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object, allocate a buffer large enough to hold that many points, and then call [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) to fill the buffer.</span></span> <span data-ttu-id="a8b31-123">在程式碼呼叫 **GraphicsPath：： GetPathPoints** 之前，它會先確認緩衝區指標不是 **Null**，藉以驗證緩衝區配置是否成功。</span><span class="sxs-lookup"><span data-stu-id="a8b31-123">Before the code calls **GraphicsPath::GetPathPoints**, it verifies that the buffer allocation was successful by making sure that the buffer pointer is not **NULL**.</span></span>


```C++
GraphicsPath path;
path.AddEllipse(10, 10, 200, 100);

INT count = path.GetPointCount();          // get the size
Point* pointArray = new Point[count];      // allocate the buffer

if(pointArray)  // Check for successful allocation.
{
   path.GetPathPoints(pointArray, count);  // get the data
   ...                                     // use pointArray
   delete[] pointArray;                    // release the buffer
   pointArray = NULL;
}
```



<span data-ttu-id="a8b31-124">上述範例使用 new 運算子來配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a8b31-124">The previous example uses the new operator to allocate a buffer.</span></span> <span data-ttu-id="a8b31-125">New 運算子很方便，因為緩衝區已填滿已知數目的 [**點**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) 物件。</span><span class="sxs-lookup"><span data-stu-id="a8b31-125">The new operator was convenient because the buffer was filled with a known number of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="a8b31-126">在某些情況下，GDI + 會將更多寫入緩衝區，而不是 GDI + 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b31-126">In some cases, GDI+ writes more into buffer than an array of GDI+ objects.</span></span> <span data-ttu-id="a8b31-127">有時候緩衝區會填入 GDI + 物件的陣列，以及這些物件的成員所指向的其他資料。</span><span class="sxs-lookup"><span data-stu-id="a8b31-127">Sometimes a buffer is filled with an array of GDI+ objects along with additional data that is pointed to by members of those objects.</span></span> <span data-ttu-id="a8b31-128">例如， [**image：： GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) 方法會傳回 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) 物件的陣列，每一個屬性專案 (部分的中繼資料) 儲存在影像中。</span><span class="sxs-lookup"><span data-stu-id="a8b31-128">For example, the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method returns an array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects, one for each property item (piece of metadata) stored in the image.</span></span> <span data-ttu-id="a8b31-129">但 **Image：： GetAllPropertyItems** 傳回的不只是 **PropertyItem** 物件的陣列;它會附加具有其他資料的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8b31-129">But **Image::GetAllPropertyItems** returns more than just the array of **PropertyItem** objects; it appends the array with additional data.</span></span>

<span data-ttu-id="a8b31-130">在您呼叫 [**Image：： GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)之前，您必須配置夠大的緩衝區，以容納 [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) 物件的陣列以及額外的資料。</span><span class="sxs-lookup"><span data-stu-id="a8b31-130">Before you call [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), you must allocate a buffer large enough to hold the array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects along with the additional data.</span></span> <span data-ttu-id="a8b31-131">您可以呼叫影像物件的 [**image：： GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) 方法，以判斷所需緩衝區的總大小。</span><span class="sxs-lookup"><span data-stu-id="a8b31-131">You can call the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method of an Image object to determine the total size of the required buffer.</span></span>

<span data-ttu-id="a8b31-132">下列範例示範如何建立 [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件，並在稍後呼叫該 **Image** 物件的 [**image：： GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)方法，以抓取儲存在影像中 (中繼資料) 的所有屬性專案。</span><span class="sxs-lookup"><span data-stu-id="a8b31-132">The following example shows how to create an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and later call the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method of that **Image** object to retrieve all the property items (metadata) stored in the image.</span></span> <span data-ttu-id="a8b31-133">程式碼會根據 [**Image：： GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) 方法所傳回的大小值配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a8b31-133">The code allocates a buffer based on a size value returned by the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method.</span></span> <span data-ttu-id="a8b31-134">**Image：： GetPropertySize** 也會傳回 count 值，以提供影像中屬性專案的數目。</span><span class="sxs-lookup"><span data-stu-id="a8b31-134">**Image::GetPropertySize** also returns a count value that gives the number of property items in the image.</span></span> <span data-ttu-id="a8b31-135">請注意，程式碼不會將緩衝區大小計算為 `count*sizeof(PropertyItem)` 。</span><span class="sxs-lookup"><span data-stu-id="a8b31-135">Notice that the code does not calculate the buffer size as `count*sizeof(PropertyItem)`.</span></span> <span data-ttu-id="a8b31-136">以該方式計算的緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="a8b31-136">A buffer calculated that way would be too small.</span></span>


```C++
UINT count = 0;
UINT size = 0;
Image myImage(L"FakePhoto.jpg");
myImage.GetPropertySize(&size, &count);

// GetAllPropertyItems returns an array of PropertyItem objects
// along with additional data. Allocate a buffer large enough to 
// receive the array and the additional data.
PropertyItem* propBuffer =(PropertyItem*)malloc(size);

if(propBuffer)
{
   myImage.GetAllPropertyItems(size, count, propBuffer);
   ...
   free(propBuffer);
   propBuffer = NULL;
}
```



## <a name="error-checking"></a><span data-ttu-id="a8b31-137">錯誤檢查</span><span class="sxs-lookup"><span data-stu-id="a8b31-137">Error Checking</span></span>

<span data-ttu-id="a8b31-138">GDI + 檔中的大部分程式碼範例都不會顯示錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="a8b31-138">Most of the code examples in the GDI+ documentation do not show error checking.</span></span> <span data-ttu-id="a8b31-139">完成錯誤檢查會讓程式碼範例變得更久，而且可能會遮蔽範例所說明的點。</span><span class="sxs-lookup"><span data-stu-id="a8b31-139">Complete error checking makes a code example much longer and can obscure the point being illustrated by the example.</span></span> <span data-ttu-id="a8b31-140">您不應該將範例直接從檔貼入生產程式碼;相反地，您應該新增自己的錯誤檢查來增強範例。</span><span class="sxs-lookup"><span data-stu-id="a8b31-140">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

<span data-ttu-id="a8b31-141">下列範例示範使用 GDI + 來執行錯誤檢查的一種方式。</span><span class="sxs-lookup"><span data-stu-id="a8b31-141">The following example shows one way of implementing error checking with GDI+.</span></span> <span data-ttu-id="a8b31-142">每次建立 GDI + 物件時，程式碼都會檢查是否成功。</span><span class="sxs-lookup"><span data-stu-id="a8b31-142">Each time a GDI+ object is constructed, the code checks to see whether the constructor was successful.</span></span> <span data-ttu-id="a8b31-143">這項檢查對於需要讀取檔案的 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 檢查點而言特別重要。</span><span class="sxs-lookup"><span data-stu-id="a8b31-143">That check is especially important for the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) constructor, which relies on reading a file.</span></span> <span data-ttu-id="a8b31-144">如果所有四個 GDI + 物件 ([**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)、 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)、 **影像** 和 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) 都已成功建立，則程式碼會在這些物件上呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="a8b31-144">If all four of the GDI+ objects ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image**, and [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) are constructed successfully, the code calls methods on those objects.</span></span> <span data-ttu-id="a8b31-145">系統會檢查每個方法呼叫是否成功，如果發生失敗，則會略過其餘的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="a8b31-145">Each method call is checked for success, and in the event of failure, the remaining method calls are skipped.</span></span>


```C++
Status GdipExample(HDC hdc)
{
   Status status = GenericError;
   INT count = 0;
   Point* points = NULL;

   Graphics graphics(hdc);
   status = graphics.GetLastStatus();
   if(Ok != status)
      return status;

   GraphicsPath path;
   status = path.GetLastStatus();
   if(Ok != status)
      return status;

   Image image(L"MyTexture.bmp");
   status = image.GetLastStatus();
   if(Ok != status)
      return status;

   TextureBrush brush(&image);
   status = brush.GetLastStatus();
   if(Ok != status)
      return status;

   status = path.AddEllipse(10, 10, 200, 100);

   if(Ok == status)
   {
      status = path.AddBezier(40, 130, 200, 130, 200, 200, 60, 200);
   }
  
   if(Ok == status)
   {
      count = path.GetPointCount();
      status = path.GetLastStatus();
   }

   if(Ok == status)
   {
      points = new Point[count];

      if(NULL == points)
         status = OutOfMemory;
   }

   if(Ok == status)
   {
      status = path.GetPathPoints(points, count);  
   }
  
   if(Ok == status)
   {
      status = graphics.FillPath(&brush, &path);
   }
   
   if(Ok == status)
   {
      for(int j = 0; j < count; ++j)
      {
         status = graphics.FillEllipse(
         &brush, points[j].X - 5, points[j].Y - 5, 10, 10);
      }
   }

   if(points)
   {
      delete[] points;
      points = NULL;
   }

   return status;
}
```



## <a name="thread-synchronization"></a><span data-ttu-id="a8b31-146">執行緒同步處理</span><span class="sxs-lookup"><span data-stu-id="a8b31-146">Thread Synchronization</span></span>

<span data-ttu-id="a8b31-147">有一個以上的執行緒可以存取單一 GDI + 物件。</span><span class="sxs-lookup"><span data-stu-id="a8b31-147">It is possible for more than one thread to have access to a single GDI+ object.</span></span> <span data-ttu-id="a8b31-148">不過，GDI + 並不提供任何自動同步處理機制。</span><span class="sxs-lookup"><span data-stu-id="a8b31-148">However, GDI+ does not provide any automatic synchronization mechanism.</span></span> <span data-ttu-id="a8b31-149">因此，如果您的應用程式中有兩個執行緒具有相同 GDI + 物件的指標，則您必須負責同步處理該物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="a8b31-149">So if two threads in your application have a pointer to the same GDI+ object, it is your responsibility to synchronize access to that object.</span></span>

<span data-ttu-id="a8b31-150">如果執行緒嘗試呼叫方法，而另一個執行緒在相同物件上執行方法，則某些 GDI + 方法會傳回 **ObjectBusy** 。</span><span class="sxs-lookup"><span data-stu-id="a8b31-150">Some GDI+ methods return **ObjectBusy** if a thread attempts to call a method while another thread is executing a method on the same object.</span></span> <span data-ttu-id="a8b31-151">請勿嘗試根據 **ObjectBusy** 傳回值來同步處理對物件的存取。</span><span class="sxs-lookup"><span data-stu-id="a8b31-151">Do not try to synchronize access to an object based on the **ObjectBusy** return value.</span></span> <span data-ttu-id="a8b31-152">相反地，每次您存取某個成員或呼叫物件的方法時，請將呼叫放在重要區段內，或使用其他標準同步處理技術。</span><span class="sxs-lookup"><span data-stu-id="a8b31-152">Instead, each time you access a member or call a method of the object, place the call inside a critical section, or use some other standard synchronization technique.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8b31-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8b31-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8b31-154">MSDN Security Developer Center</span><span class="sxs-lookup"><span data-stu-id="a8b31-154">MSDN Security Developer Center</span></span>](https://msdn.microsoft.com/security/)
</dt> <dt>

<span data-ttu-id="a8b31-155">[安全性 How-To 資源](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="a8b31-155">[Security How-To Resources](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span></span>
</dt> <dt>

[<span data-ttu-id="a8b31-156">TechNet 安全性中心</span><span class="sxs-lookup"><span data-stu-id="a8b31-156">TechNet Security Center</span></span>](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
