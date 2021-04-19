---
description: '執行 IWICBitmapCodecProgressNotification (解碼器) '
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: '執行 IWICBitmapCodecProgressNotification (解碼器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977353"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>執行 IWICBitmapCodecProgressNotification (解碼器) 

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

當編解碼器在大型映射上執行 i/o 作業（例如 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) ）時，可能需要數秒鐘或甚至幾分鐘才能完成。 當終端使用者無法中斷長時間執行的作業時，他們可能會認為應用程式已停止運作。 使用者經常會關閉應用程式，或甚至重新開機電腦，以嘗試在應用程式沒有回應時重新取得電腦的控制權。

這個介面可讓應用程式指定一個回呼函式，以供編解碼器在指定的間隔呼叫，以通知呼叫端目前作業的進度。 應用程式可以使用這個回呼函式，在使用者介面中顯示進度的指示，以通知使用者作業的狀態。 如果使用者按一下 [**進度**] 對話方塊中的 [**取消**] 按鈕，應用程式會傳回從回呼函式 **中止的 WINCODEC \_ 錯誤 \_** 。 發生這種情況時，編解碼器必須取消指定的作業，並將此 **HRESULT** 傳播回執行作業之方法的呼叫端。

此介面應該在容器層級的解碼器類別上執行。


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [RegisterProgressNotification](#registerprogressnotification)
-   [PFNProgressNotification](#pfnprogressnotification)

### <a name="registerprogressnotification"></a>RegisterProgressNotification

應用程式會叫用 [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) ，以註冊編解碼器可在指定間隔呼叫的回呼函數。 第一個參數（ *pfnProgressNotification*）是回呼函式的指標，該函式會定期呼叫編解碼器。

*PvData* 參數會指向某些物件，呼叫端想要在每次叫用回呼函式時，將編解碼器傳回到回呼函式。 此物件可能是所有的物件，而且對編解碼器沒有任何特殊意義。

*DwProgressFlags* 參數會指定編解碼器應該呼叫回呼函式的時機。 您可以使用此參數的兩個列舉來執行或函數。 [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation)列舉會指定在解碼 (**WICProgressOperationCopyPixels**) 、編碼 (**WICProgerssOperationWritePixels**) ，或 (**WICProgressOperationAll**) 時，是否要呼叫回呼函式。


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



編解碼器應該在整個作業期間定期呼叫回呼函式，但是呼叫端可能會指定特定需求。 [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification)列舉會指出作業中呼叫回呼函式的位置。 如果呼叫端指定 **WICProgressNotificationBegin**，您必須在作業的開頭呼叫它 (0.0) 。 如果呼叫端未指定此項，則為選擇性。 同樣地，如果呼叫端指定 **WICProgerssNotificationEnd**，您必須在作業完成時呼叫它 (1.0) 。 如果呼叫端指定 **WICProgressNotificationAll**，您必須在開頭和結尾呼叫它，以及在整個作業中定期呼叫它。 呼叫端也可以指定 **WICProgerssNotificationFrequent**，這表示他們想要以頻繁的間隔（也許是在每幾個掃描行之後）來呼叫。  (呼叫端通常只會針對非常大的影像使用此旗標 ) 。否則，您通常應該以大約10% 的間隔來回呼要處理的掃描行總數。


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



一次只能針對特定的解碼器或編碼器實例註冊一個回呼函數。 如果應用程式多次呼叫 [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) ，請將先前註冊的回呼函式取代為新的回呼函數。 若要取消回呼註冊，呼叫端會將 *pfnProgressNotification* 參數設定為 **Null**。

### <a name="pfnprogressnotification"></a>PFNProgressNotification

[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) 是具有下列簽章的回呼函數。


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



當您叫用回呼函式時，請使用 *pvData* 參數傳回應用程式在註冊回呼函式時所指定的相同 *pvData* 。

*UFrameNum* 參數應該指出正在處理之框架的索引。

將 operation 參數設定為在編碼時解碼和 **WICProgressOperationWritePixels** 時的 **WICProgressOperationCopyPixels** 。

*DblProgress* 參數應該是在作業開始 (0.0 之間的數位) 和 1.0 (完成作業) 。 此值應該會反映已處理的掃描行相對於要處理的掃描行總數的比例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**ProgressNotificationCallback**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

**概念**
</dt> <dt>

[執行 IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[執行 IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



