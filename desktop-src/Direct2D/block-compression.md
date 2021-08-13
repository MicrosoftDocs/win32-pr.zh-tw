---
title: 區塊壓縮
description: 描述區塊壓縮的運作方式，以及如何在 WIC 和 Direct2D 中使用它。
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8ee83911cc7be1ab6e611a735a7a5b3a7397c472b78e3192468d2e323ed0c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331737"
---
# <a name="block-compression"></a>區塊壓縮

從 Windows 8.1 開始，Direct2D 支援數個區塊壓縮的像素格式。 此外，Windows 8.1 包含新的 Windows 影像處理元件 (WIC) DDS 編解碼器，以啟用以 DDS 檔案格式載入和儲存區塊壓縮的影像。 「封鎖壓縮」是一種技術，可減少點陣圖內容所耗用的圖形記憶體量。 使用區塊壓縮時，您的應用程式可以減少相同解析度影像的記憶體耗用量和載入時間。 或者，您的應用程式可以使用更多或更高的解析度影像，同時仍然耗用相同的 GPU 記憶體使用量。

由於 Direct3D 應用程式已有一段很長的時間可以使用區塊壓縮，而 Windows 8.1 也提供給主流和 Direct2D 的應用程式開發人員使用。

本主題說明 block 壓縮的運作方式，以及如何在 WIC 和 Direct2D 中使用它。

## <a name="about-block-compression"></a>關於區塊壓縮

[區塊壓縮](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) 指的是減少材質大小的一種壓縮技術。 根據功能等級，Direct3D 11 最多可支援7種不同的 BC 格式。 在 Windows 8.1 Direct2D 引進 BC1、BC2 和 BC3 格式的支援，這些格式可在所有功能層級中使用。

### <a name="how-block-compression-works"></a>區塊壓縮的運作方式

區塊壓縮格式全都使用相同的基本技術來減少色彩資料所耗用的空間。 本節摘要說明最簡單的演算法 BC1。 如需更詳細的說明，請參閱 [區塊壓縮](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11)。

首先，映射會分成4個圖元的區塊。 每個區塊會分開壓縮。

> [!Note]  
> 這表示影像的寬度和高度必須是4圖元的倍數，以封鎖壓縮。

 

此範例影像顯示影像內的4x4 圖元區塊。

![範例影像顯示影像內的4x4 圖元區塊。](images/dds1.png)

接下來，在 4 x 4 區塊中，選取兩個「參考」色彩，並將其編碼為 2 16 位值 (5 位紅色、6位綠色、5位藍色) 。 這些色彩的選擇會大幅影響影像品質，而且重要。 兩個中繼色彩的計算方式是在 RGB 色彩空間中兩個參考色彩之間的線性插即用。 這總共會產生四個不同的可能色彩：每個色彩都會指派兩個位的索引值。 不過，請注意，只有兩個端點色彩需要儲存，因為插補是固定的。

在此圖中，會選取色彩0和3作為區塊的「參考」色彩，而色彩1和2則是使用線性插補來計算。

![顯示代表區塊的4個色彩值計算的圖表。](images/dds2.png)

最後，區塊中的每個圖元都會對應到其中四個先前計算的色彩之一，而且每個圖元都會使用兩個位索引值進行編碼。

用來代表這些16圖元的資料總量如下：

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

這會產生每圖元4個位的平均密度。 相較之下，common DXGI \_ format \_ B8G8R8A8 \_ UNORM 像素格式耗用每圖元32位。

下圖顯示每個圖元都會編碼為2位索引。 整個區塊會以64位編碼。

![計算4個色彩值以表示區塊。](images/dds3.png)

有各種不同的支援 Alpha 資料和不同的色彩通道數目。 BC6H 和 BC7 會使用明顯不同的演算法，以支援高動態範圍 (HDR) 內容，並分別增加影像品質。

### <a name="directdraw-surface-dds-file-format"></a>DirectDraw 介面 (DDS) 檔案格式

區塊壓縮資料通常儲存在 [DirectDraw 介面 (DDS) ](/windows/desktop/direct3ddds/dx-graphics-dds-reference) 檔。 如果您是 Direct3D 開發人員，您可能很熟悉 DDS 檔。 請注意，Direct2D 只支援特定的 DDS 功能;如需詳細資訊，請參閱 [DDS 需求](#dds-requirements)。

### <a name="advantages-of-block-compression"></a>區塊壓縮的優點

封鎖壓縮格式與常見的產業影像壓縮格式不同，例如 JPEG，這類的 BC 格式會由新式 Gpu 原生支援。 這表示您可以直接將區塊壓縮的影像載入至 GPU，而不需要任何解碼或解壓縮。 BC 格式平均耗用每圖元4到8位;相較于一般未壓縮的32位的每個圖元 BGRA 點陣圖，這會導致記憶體節省75% 到87.5%。 此外，由於沒有解碼步驟，相較于 JPEG 格式，載入 BC 映射的時間會大幅減少。

### <a name="when-to-use-block-compression"></a>使用區塊壓縮的時機

如果您想要減少點陣圖的記憶體耗用量，或想要減少解碼和載入時間，您應該考慮在應用程式中使用區塊壓縮影像，而不是其他格式，例如 JPEG。

不過，區塊壓縮並非適用于所有情況，而且需要一些取捨。 首先，區塊壓縮演算法會有損量。 區塊壓縮適用于自然的影像內容，但可能會將不需要的視覺效果成品引入具有清晰、高對比界線的影像，例如電腦產生的螢幕擷取畫面。 您應該確定您的區塊壓縮影像資產在使用影像品質之前都具有可接受的影像品質。

其次，封鎖壓縮的 DDS 檔案通常會在磁片上耗用比可比較的 JPEG 影像更多的空間。 這將會增加您應用程式的套件大小和網路頻寬需求。

## <a name="using-block-compression"></a>使用區塊壓縮

本節說明如何在 Direct2D 應用程式中產生和使用封鎖壓縮的資產。

### <a name="overview"></a>概觀

區塊壓縮的 DDS 檔案是執行時間優化的格式，表示它們已特別針對應用程式執行時間的良好效能進行優化。 建議您繼續使用現有的資產建立和編輯管線，並只在您將它們匯入至應用程式專案時或在組建階段時，轉換成區塊壓縮格式。

### <a name="dds-requirements"></a>DDS 需求

DDS 檔案格式的設計目的是要支援 Direct3D 中使用的各種功能。 Direct2D 只會使用這些功能的子集。 因此，當您建立要與 Direct2D 搭配使用的 DDS 映射時，必須記住下列限制：

-   只允許下列 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 值：
    -   DXGI \_ 格式 \_ BC1 \_ UNORM
    -   DXGI \_ 格式 \_ BC2 \_ UNORM
    -   DXGI \_ 格式 \_ BC3 \_ UNORM
-   必須使用預乘的 Alpha 資料。 這包括舊版的 DDS 檔，其使用的格式會明確定義預乘的 Alpha (DXT1、DXT2、DXT4) ，以及使用 dds \_ 標頭 \_ DX10 結構與 dds \_ Alpha \_ 模式不 \_ 透明和 dds \_ ALPHA \_ 模式預先設置值 \_ 的 dds 檔案。
-   X 和 Y 維度必須是4圖元的倍數。
-   不允許使用磁片區紋理、cubemaps、mipmap 或紋理陣列。 您應該只使用單一畫面格來源影像。

### <a name="generating-block-compressed-assets"></a>產生區塊壓縮的資產

有各種不同的 DDS 撰寫工具可用來建立或轉換區塊壓縮的 DDS 檔。 請注意，並非所有工具都支援搭配 Direct2D 使用 DDS 檔案的需求，如上一節中所述。

從 Visual Studio 2013 開始，您可以 Visual Studio 將 JPEG 和 PNG 等現有的視覺效果資產轉換成正確的 DDS 區塊壓縮格式，做為組建程式的自動部分。 這是使用「影像內容工作」自訂群組建步驟來完成的。

如需如何為您的專案設定此專案的詳細資訊，請參閱： [如何：匯出材質以搭配 Direct2D 或 JAVAscipt Apps 使用](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))。

### <a name="direct2d-apis"></a>Direct2D Api

Windows 8.1 中的 Direct2D 會更新為支援下列像素格式：

-   DXGI \_ 格式 \_ BC1 \_ UNORM
-   DXGI \_ 格式 \_ BC2 \_ UNORM
-   DXGI \_ 格式 \_ BC3 \_ UNORM

針對上述格式，您必須使用預乘 Alpha。 此外，這些格式只適用于作為來源，而不是目標。 例如，這表示您可以使用 BC1 （而不是裝置內容）來建立 Direct2D 點陣圖。

Windows 8.1 中的下列方法會更新以支援 BC 格式：

-   [**ID2D1DeviceCoNtext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceCoNtext::CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceCoNtext::CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget::CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget::CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap::CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap::CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1::GetSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

請注意， [**CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md)會採用 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource)作為介面;不過，在 Windows 8.1 WIC 不支援從 **IWICBitmapSource** 取得區塊壓縮資料，而且沒有對應至 DXGI \_ 格式 \_ BC1 UNORM 等的 WIC 像素格式 \_ 。相反地， **CreateBitmapFromWicBitmap** 會判斷 **IWICBitmapSource** 是否為有效的 DDS [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) ，並直接載入區塊壓縮的資料。 您可以在 [**D2D1 \_ 點陣圖 \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) 結構中明確指定像素格式，或允許 Direct2D 自動判斷正確的格式。

### <a name="windows-imaging-component-apis"></a>Windows映射處理元件 Api

Windows 影像處理元件 (WIC) 會在 Windows 8.1 中加入新的 DDS 編解碼器。 此外，它還新增了支援存取 DDS 特定資料的新介面，包括區塊壓縮的圖元資料：

-   [**IWICDdsDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>封鎖壓縮的 WIC 像素格式

Windows 8.1 中沒有新的 WIC 區塊壓縮的像素格式。 相反地，如果您從 DDS 解碼器取得 [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) 並呼叫 [**CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels)，您將會收到標準的未壓縮圖元，例如 WICPixelFormat32bppPBGRA。 您可以使用 [**IWICDdsFrameDecode：： CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) ，以來自 DDS 檔案的記憶體緩衝區形式取得原始區塊壓縮的資料。

### <a name="multi-frame-dds-access"></a>多框架 DDS 存取

DDS 檔案格式允許將多個相關的影像儲存在單一檔案中。 例如，DDS 檔案可能包含立方體貼圖、磁片區材質或材質陣列，這些都可以 mipmapped。 在 Direct3D 中，這些多個映射會公開為子資源。 在 WIC 中，會將多個映射公開為框架， ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) 和 [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)) 。

WIC 只支援一維框架陣列的概念，而 DDS 支援三個獨立的維度 (但只有兩個可用於任何一個檔案) 。 WIC 提供便利的方法，協助您在 DDS subresource 和 WIC 框架之間進行對應。 針對解碼， [**IWICDdsDecoder：： GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) 可讓您指定 subresource 的陣列索引、mip 層級和配量索引，並傳回正確的 WIC 框架。

針對編碼， [**IWICDdsEncoder：： CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) 會在您建立新的框架時，計算產生的陣列索引、mip 層級和配量索引。 您必須先呼叫 [**IWICDdsEncoder：： SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) 來定義 DDS 特定的檔案參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何：匯出材質以搭配 Direct2D 或 Javascipt 應用程式使用](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[DDS 的參考](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[區塊壓縮](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 