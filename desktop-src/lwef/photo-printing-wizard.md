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
# <a name="photo-printing-wizard"></a>相片列印嚮導

相片列印嚮導可提供簡單易用的 Wizard 介面，協助使用者列印相片。 此嚮導可讓使用者指定相片列印大小及其他列印選項，然後將相片傳送至印表機。 此 wizard 的設計目的是要讓任何應用程式以程式設計方式叫用它，該應用程式想要讓使用者能夠列印相片，以及指定調整大小及其他列印選項。 您可以在 Windows XP 和 Windows Vista 上使用相片列印嚮導。

-   [相片 Print Wizard 提供的功能](#features-provided-by-the-photo-print-wizard)
-   [支援的相片檔案格式](#supported-photo-file-formats)
-   [以程式設計方式啟動相片列印嚮導](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>相片 Print Wizard 提供的功能

「相片列印嚮導」提供數個可能無法在一般印表機對話方塊上使用的選項，例如具有精確維度的多重版面配置範本。 版面配置範本可讓使用者以最有效率的方式使用照片列印紙張上的可用空間。 可以透過 [相片列印嚮導] 指定或存取的其他選項包括：

-   從可用印表機或虛擬列印目的地清單中選取印表機 (例如，[Microsoft XPS Document Writer]) 。 在 Windows Vista 上，視印表機或虛擬列印目的地的功能而定，可能可以使用下列選項：
    -   紙張大小。 例如，"Letter"、"法律聲明"、"A3"。
    -   列印品質（以每英寸支援的點為單位） (DPI) 解析度。
    -   紙張類型。 例如，「純文字」或「光澤」。
-   啟動特定印表機的列印喜好設定和屬性。
-   在 Windows Vista 上將 **每個圖片** (的複本設定) 或在 windows XP) 微調方塊值上 **使用每個 (圖片的次數** 。
-   指定列印版面配置範本。 例如， **整頁相片** 或 **錢包印**。
-   選取 [ **符合圖片大小** ] 選項 (僅適用于 Windows Vista) 。
-   使用目前指定的選項來預覽列印的相片。
-   Accesssing 先進的列印選項，例如，只) Windows Vista 上提供 **的列印** 和 **色彩管理** (。

任何應用程式都可以受益于相片列印嚮導所提供的功能和相片列印功能。 應用程式可以傳入要列印的檔案。 然後，相片列印嚮導會根據使用者指定的選項，負責準備要列印的檔案，並將準備好的檔案傳送至印表機。

下圖顯示 Windows Vista 上的相片列印 Wizard 介面

![windows vista 上的相片列印嚮導](images/ppw-vista.png)

下圖顯示 Windows XP 上的相片列印 Wizard 介面

![windows xp 上的相片列印嚮導](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>支援的相片檔案格式

在 Windows XP 上，「相片列印嚮導」支援 Windows GDI + 支援的所有圖形檔案格式。 目前，這些檔案格式包括：

-   點陣圖 (BMP)
-   圖形交換格式 (GIF)
-   JPEG 格式 (JPEG)
-    (EXIF) 的交換影像檔
-   可攜式網路圖形 (PNG)
-   標記的影像檔案格式 (TIFF)

如需 GDI + 所支援之圖形檔案格式的詳細資訊，請參閱 [點陣圖類型](../gdiplus/-gdiplus-types-of-bitmaps-about.md)。

在 Windows Vista 上，「相片列印嚮導」支援任何已安裝 Windows 影像處理元件 (WIC) 編解碼器的影像檔案格式。 WIC 提供數個標準編解碼器，包括：

-   點陣圖 (BMP)
-   GIF
-    (.ICO) 的圖示格式
-   JPEG
-   PNG
-   TIFF
-   Windows Media 相片格式

如需 WIC 和 WIC 編解碼器的詳細資訊，請參閱 [Windows 影像處理元件](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>以程式設計方式啟動相片列印嚮導

若要叫用相片列印嚮導，請使用下列類別識別碼呼叫 [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面 (CLSID) ：


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



相片列印嚮導所要處理的檔案是在 [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) 物件中指定的。

下列程式碼範例示範如何叫用相片列印嚮導。


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



 

 