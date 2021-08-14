---
description: 序列化 IWICDevelopRaw 設定的實指導方針
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: 序列化 IWICDevelopRaw 設定的實指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119b6377fc8b75aa9763e8141e17ef79832a2aef5f010c2783a412cef0133788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709828"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>序列化 IWICDevelopRaw 設定的實指導方針

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)介面會公開設定，讓應用程式用來修改原始影像的處理。 這些設定應該能夠序列化，以便跨會話保存。 雖然這可以透過數種方式來完成，但建議您以與其他中繼資料一致的方式來編碼此資料。

以下是一些一般的執行指導方針：

-   透過 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 所做的任何設定 (例如旋轉或白色餘額) 應該避免覆寫相機設定或「以快照」的資料，除非此標記通常用來做為「目前的設定」。 例如，您可以使用 EXIF 方向標記來保存旋轉。
-   最好不要將整個檔案儲存 (包括每次要求序列化 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 設定時的馬賽克圖元資料) 。
-   序列化 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 設定的程式通常會遵循此事件順序。 應用程式：

    1.  具現化原始檔案上的 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。
    2.  呼叫 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)：：[**GETFRAME**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) 來取得原始框架的 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。
    3.  在 IWICBitmapFrameDecode 介面上呼叫 IWICDevelopRaw 介面的 QueryInterface。
    4.  呼叫 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)，它會傳回 IPropertyBag2 介面，其中包含所有目前儲存在其中的屬性。

        在這個過程中，目標是要將 IPropertyBag2 介面中的設定序列化為原始檔案。 若要這樣做，需要啟動編碼器，依此類推，在下列步驟中會有詳細的說明。

    5.  建立原始檔案的 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 。
    6.  呼叫 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)：：[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)，傳入新的 (空白) 資料流程以進行編碼。
    7.  呼叫 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)：：[**CREATENEWFRAME**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) 來建立原始框架的新 IWICBitmapFrameEncode。
    8.  呼叫 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)：：[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)，然後在步驟4的 IPropertyBag2 介面中傳遞。
    9.  從解碼器的原始影像框架呼叫 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)：：[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) 與 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。
    10. 呼叫 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)：：[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)。 然後，編解碼器會將步驟8中 IPropertyBag2 的屬性序列化為檔案。 將屬性序列化的最常見方法是在檔案中將其寫出為中繼資料。
    11. 呼叫 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)：：[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)。
    12. 在步驟6中的資料流程上呼叫 IStream：： Commit。

    這些設定會在檔案中進行序列化。

    這種方法會在每次序列化設定時，產生重寫整個原始檔案的成本。 如果您執行 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) ，或您的圖像檔案格式支援 XMP 或 EXIF，則可以避免這種情況，因為 WIC 提供這兩種格式的 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) 。 此外，如果您的編解碼器將變更寫入影像檔案的結尾，您就不會最後重寫整個影像檔案。

-   當應用程式在 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset)方法上設定 [**WICRawParameterSet WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset)列舉時，會從序列化狀態載入參數集。 [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset)旗標指的是最後儲存的參數集，因此使用此旗標的負載應該會導致將參數還原到最後儲存的狀態。
-   初始載入時，應該載入最後儲存的參數集（如果有的話）。 如果沒有，則應該使用「快照」設定做為 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 介面變數上的預設值。 您也可以使用 [**WICRawParameterSet. WICAsShotParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) 旗標來載入這些進行中的設定。
-   識別碼 [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) 是用來表示「自動」設定。 編解碼器設計工具可以選擇下列任一方法，以瞭解如何在進行此設定時設定 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 參數：

    -   執行某些參數的演算法優化，例如曝光或色彩。 這是典型影像編輯器中的自動函式，而且主要是以圖元資料分析為基礎。
    -   設定攝影機設定，類似于自動設定的行為。 如果影像是以手動設定為快照，並允許使用者覆寫手動設定，這就很有用。
    -   不執行任何動作。 當選取 [自動] 時，並非所有控制項都需要設定，而且不會讓設定保持不變。

當使用者針對所有一般編解碼器控制項調整（例如色彩和曝光）選取自動校正時，Windows Vista 影像中心和 Windows Live 影像中心編輯工具和其他編輯應用程式會使用 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)自動參數載入來取得最佳結果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



