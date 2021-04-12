---
title: 相片列印嚮導
description: 相片列印嚮導可提供簡單易用的 Wizard 介面，協助使用者列印相片。
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- 相片列印嚮導
- IDropTarget，相片列印嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375268"
---
# <a name="photo-printing-wizard"></a><span data-ttu-id="507a0-105">相片列印嚮導</span><span class="sxs-lookup"><span data-stu-id="507a0-105">Photo Printing Wizard</span></span>

<span data-ttu-id="507a0-106">相片列印嚮導可提供簡單易用的 Wizard 介面，協助使用者列印相片。</span><span class="sxs-lookup"><span data-stu-id="507a0-106">The Photo Printing Wizard helps users print photos by providing an easy-to-use wizard interface.</span></span> <span data-ttu-id="507a0-107">此嚮導可讓使用者指定相片列印大小及其他列印選項，然後將相片傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="507a0-107">The wizard enables the user to specify photo print sizes and other print options, and then sends the photos to the printer.</span></span> <span data-ttu-id="507a0-108">此 wizard 的設計目的是要讓任何應用程式以程式設計方式叫用它，該應用程式想要讓使用者能夠列印相片，以及指定調整大小及其他列印選項。</span><span class="sxs-lookup"><span data-stu-id="507a0-108">The wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to print photos and specify sizing and other print options.</span></span> <span data-ttu-id="507a0-109">您可以在 Windows XP 和 Windows Vista 上使用相片列印嚮導。</span><span class="sxs-lookup"><span data-stu-id="507a0-109">The Photo Printing Wizard is available on Windows XP and Windows Vista.</span></span>

-   [<span data-ttu-id="507a0-110">相片 Print Wizard 提供的功能</span><span class="sxs-lookup"><span data-stu-id="507a0-110">Features Provided by the Photo Print Wizard</span></span>](#features-provided-by-the-photo-print-wizard)
-   [<span data-ttu-id="507a0-111">支援的相片檔案格式</span><span class="sxs-lookup"><span data-stu-id="507a0-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="507a0-112">以程式設計方式啟動相片列印嚮導</span><span class="sxs-lookup"><span data-stu-id="507a0-112">Programmatically Launching the Photo Print Wizard</span></span>](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a><span data-ttu-id="507a0-113">相片 Print Wizard 提供的功能</span><span class="sxs-lookup"><span data-stu-id="507a0-113">Features Provided by the Photo Print Wizard</span></span>

<span data-ttu-id="507a0-114">「相片列印嚮導」提供數個可能無法在一般印表機對話方塊上使用的選項，例如具有精確維度的多重版面配置範本。</span><span class="sxs-lookup"><span data-stu-id="507a0-114">The Photo Printing Wizard offers several options that may not be available on common printer dialogs, such as multi-layout templates with accurate dimensions.</span></span> <span data-ttu-id="507a0-115">版面配置範本可讓使用者以最有效率的方式使用照片列印紙張上的可用空間。</span><span class="sxs-lookup"><span data-stu-id="507a0-115">The layout templates enable users to make the most efficient use of the space available on photographic printing paper.</span></span> <span data-ttu-id="507a0-116">可以透過 [相片列印嚮導] 指定或存取的其他選項包括：</span><span class="sxs-lookup"><span data-stu-id="507a0-116">Other options that can be specified or accessed through the Photo Print Wizard include:</span></span>

-   <span data-ttu-id="507a0-117">從可用印表機或虛擬列印目的地清單中選取印表機 (例如，[Microsoft XPS Document Writer]) 。</span><span class="sxs-lookup"><span data-stu-id="507a0-117">Selecting a printer from a list of available printers or virtual printing destinations (for example, Microsoft XPS Document Writer).</span></span> <span data-ttu-id="507a0-118">在 Windows Vista 上，視印表機或虛擬列印目的地的功能而定，可能可以使用下列選項：</span><span class="sxs-lookup"><span data-stu-id="507a0-118">On Windows Vista, the following options may be available, depending on the capabilities of the printer or virtual printing destination:</span></span>
    -   <span data-ttu-id="507a0-119">紙張大小。</span><span class="sxs-lookup"><span data-stu-id="507a0-119">Paper size.</span></span> <span data-ttu-id="507a0-120">例如，"Letter"、"法律聲明"、"A3"。</span><span class="sxs-lookup"><span data-stu-id="507a0-120">For example, "Letter", "Legal", "A3".</span></span>
    -   <span data-ttu-id="507a0-121">列印品質（以每英寸支援的點為單位） (DPI) 解析度。</span><span class="sxs-lookup"><span data-stu-id="507a0-121">Print quality, in terms of supported dots per inch (dpi) resolutions.</span></span>
    -   <span data-ttu-id="507a0-122">紙張類型。</span><span class="sxs-lookup"><span data-stu-id="507a0-122">Paper type.</span></span> <span data-ttu-id="507a0-123">例如，「純文字」或「光澤」。</span><span class="sxs-lookup"><span data-stu-id="507a0-123">For example, "Plain" or "Glossy".</span></span>
-   <span data-ttu-id="507a0-124">啟動特定印表機的列印喜好設定和屬性。</span><span class="sxs-lookup"><span data-stu-id="507a0-124">Launching the printing preferences and properties for a particular printer.</span></span>
-   <span data-ttu-id="507a0-125">在 Windows Vista 上將 **每個圖片** (的複本設定) 或在 windows XP) 微調方塊值上 **使用每個 (圖片的次數** 。</span><span class="sxs-lookup"><span data-stu-id="507a0-125">Setting the **Copies of each picture** (on Windows Vista) or **Number of times to use each picture** (on Windows XP) spin box values.</span></span>
-   <span data-ttu-id="507a0-126">指定列印版面配置範本。</span><span class="sxs-lookup"><span data-stu-id="507a0-126">Specifying a print layout template.</span></span> <span data-ttu-id="507a0-127">例如， **整頁相片** 或 **錢包印**。</span><span class="sxs-lookup"><span data-stu-id="507a0-127">For example, **Full page photo** or **Wallet prints**.</span></span>
-   <span data-ttu-id="507a0-128">選取 [ **符合圖片大小** ] 選項 (僅適用于 Windows Vista) 。</span><span class="sxs-lookup"><span data-stu-id="507a0-128">Selecting the **Fit picture to frame** option (available on Windows Vista only).</span></span>
-   <span data-ttu-id="507a0-129">使用目前指定的選項來預覽列印的相片。</span><span class="sxs-lookup"><span data-stu-id="507a0-129">Previewing the printed photo with the currently specified options.</span></span>
-   <span data-ttu-id="507a0-130">Accesssing 先進的列印選項，例如，只) Windows Vista 上提供 **的列印** 和 **色彩管理** (。</span><span class="sxs-lookup"><span data-stu-id="507a0-130">Accesssing advanced print options, such as **Sharpen for printing** and **Color management** (available on Windows Vista only).</span></span>

<span data-ttu-id="507a0-131">任何應用程式都可以受益于相片列印嚮導所提供的功能和相片列印功能。</span><span class="sxs-lookup"><span data-stu-id="507a0-131">Any application can benefit from the features and photo printing capability offered by the Photo Printing Wizard.</span></span> <span data-ttu-id="507a0-132">應用程式可以傳入要列印的檔案。</span><span class="sxs-lookup"><span data-stu-id="507a0-132">An application can pass in the files to be printed.</span></span> <span data-ttu-id="507a0-133">然後，相片列印嚮導會根據使用者指定的選項，負責準備要列印的檔案，並將準備好的檔案傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="507a0-133">The Photo Printing Wizard then takes care of preparing the file for printing based on the options specified by the user and sends the prepared files to the printer.</span></span>

<span data-ttu-id="507a0-134">下圖顯示 Windows Vista 上的相片列印 Wizard 介面</span><span class="sxs-lookup"><span data-stu-id="507a0-134">The following figure shows the Photo Printing Wizard interface on Windows Vista</span></span>

![windows vista 上的相片列印嚮導](images/ppw-vista.png)

<span data-ttu-id="507a0-136">下圖顯示 Windows XP 上的相片列印 Wizard 介面</span><span class="sxs-lookup"><span data-stu-id="507a0-136">The following figure shows the Photo Printing Wizard interface on Windows XP</span></span>

![windows xp 上的相片列印嚮導](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="507a0-138">支援的相片檔案格式</span><span class="sxs-lookup"><span data-stu-id="507a0-138">Supported Photo File Formats</span></span>

<span data-ttu-id="507a0-139">在 Windows XP 上，「相片列印嚮導」支援 Windows GDI + 支援的所有圖形檔案格式。</span><span class="sxs-lookup"><span data-stu-id="507a0-139">On Windows XP, the Photo Print Wizard supports all graphics file formats that are supported by Windows GDI+.</span></span> <span data-ttu-id="507a0-140">目前，這些檔案格式包括：</span><span class="sxs-lookup"><span data-stu-id="507a0-140">Currently, these file formats include:</span></span>

-   <span data-ttu-id="507a0-141">點陣圖 (BMP)</span><span class="sxs-lookup"><span data-stu-id="507a0-141">Bitmap (BMP)</span></span>
-   <span data-ttu-id="507a0-142">圖形交換格式 (GIF)</span><span class="sxs-lookup"><span data-stu-id="507a0-142">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="507a0-143">JPEG 格式 (JPEG)</span><span class="sxs-lookup"><span data-stu-id="507a0-143">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="507a0-144"> (EXIF) 的交換影像檔</span><span class="sxs-lookup"><span data-stu-id="507a0-144">Exchangeable Image File (EXIF)</span></span>
-   <span data-ttu-id="507a0-145">可攜式網路圖形 (PNG)</span><span class="sxs-lookup"><span data-stu-id="507a0-145">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="507a0-146">標記的影像檔案格式 (TIFF)</span><span class="sxs-lookup"><span data-stu-id="507a0-146">Tagged Image File Format (TIFF)</span></span>

<span data-ttu-id="507a0-147">如需 GDI + 所支援之圖形檔案格式的詳細資訊，請參閱 [點陣圖類型](../gdiplus/-gdiplus-types-of-bitmaps-about.md)。</span><span class="sxs-lookup"><span data-stu-id="507a0-147">For more information about graphics file formats supported by GDI+, see [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span></span>

<span data-ttu-id="507a0-148">在 Windows Vista 上，「相片列印嚮導」支援任何已安裝 Windows 影像處理元件 (WIC) 編解碼器的影像檔案格式。</span><span class="sxs-lookup"><span data-stu-id="507a0-148">On Windows Vista, the Photo Print Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="507a0-149">WIC 提供數個標準編解碼器，包括：</span><span class="sxs-lookup"><span data-stu-id="507a0-149">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="507a0-150">點陣圖 (BMP)</span><span class="sxs-lookup"><span data-stu-id="507a0-150">Bitmap (BMP)</span></span>
-   <span data-ttu-id="507a0-151">GIF</span><span class="sxs-lookup"><span data-stu-id="507a0-151">GIF</span></span>
-   <span data-ttu-id="507a0-152"> (.ICO) 的圖示格式</span><span class="sxs-lookup"><span data-stu-id="507a0-152">Icon Format (ICO)</span></span>
-   <span data-ttu-id="507a0-153">JPEG</span><span class="sxs-lookup"><span data-stu-id="507a0-153">JPEG</span></span>
-   <span data-ttu-id="507a0-154">PNG</span><span class="sxs-lookup"><span data-stu-id="507a0-154">PNG</span></span>
-   <span data-ttu-id="507a0-155">TIFF</span><span class="sxs-lookup"><span data-stu-id="507a0-155">TIFF</span></span>
-   <span data-ttu-id="507a0-156">Windows Media 相片格式</span><span class="sxs-lookup"><span data-stu-id="507a0-156">Windows Media Photo format</span></span>

<span data-ttu-id="507a0-157">如需 WIC 和 WIC 編解碼器的詳細資訊，請參閱 [Windows 影像處理元件](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="507a0-157">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span></span>

## <a name="programmatically-launching-the-photo-print-wizard"></a><span data-ttu-id="507a0-158">以程式設計方式啟動相片列印嚮導</span><span class="sxs-lookup"><span data-stu-id="507a0-158">Programmatically Launching the Photo Print Wizard</span></span>

<span data-ttu-id="507a0-159">若要叫用相片列印嚮導，請使用下列類別識別碼呼叫 [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面 (CLSID) ：</span><span class="sxs-lookup"><span data-stu-id="507a0-159">To invoke the Photo Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



<span data-ttu-id="507a0-160">相片列印嚮導所要處理的檔案是在 [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) 物件中指定的。</span><span class="sxs-lookup"><span data-stu-id="507a0-160">The files to be processed by the Photo Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="507a0-161">下列程式碼範例示範如何叫用相片列印嚮導。</span><span class="sxs-lookup"><span data-stu-id="507a0-161">The following code example demonstrates how to invoke the Photo Printing Wizard.</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 