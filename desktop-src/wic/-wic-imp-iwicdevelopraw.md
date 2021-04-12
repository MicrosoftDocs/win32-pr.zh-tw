---
description: 執行 IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: 執行 IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683dc2baf0496694943b7640d3f3ed521dc477a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195315"
---
# <a name="implementing-iwicdevelopraw"></a>執行 IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)介面會公開原始影像處理的特定處理選項。 所有原始編解碼器都必須支援 **IWICDevelopRaw** 介面。 某些原始編解碼器可能無法支援此介面公開的每個設定，但您應該支援您的編解碼器能夠執行的所有設定。 每個原始編解碼器至少都必須執行 [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) 和 [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) 方法。

此外，針對原始編解碼器，強烈建議您針對其他編解碼器選用一些方法和介面。 這些包括容器層級的解碼器類別上的 [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) 和 [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) 方法，以及框架層級解碼類別上的 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 介面。

使用 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 方法設定的設定應該以與其他中繼資料保存方式一致的方式保存，而您永遠不應該覆寫原始的「以快照」設定。 藉由保存中繼資料並執行 [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) 和 [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)，您可以啟用原始處理應用程式，以抓取並套用跨會話的處理設定。

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)介面的主要目的是讓應用程式開發人員建立使用者介面，以調整可在不同編解碼器之間盡可能一致運作的原始參數。 假設終端使用者將使用滑杆控制項來調整參數，其最小值和最大值會對應至參數的最小和最大範圍。 為了支援這種情況，您應該盡全力將所有參數範圍視為線性。 為了確保滑杆控制項不會過於敏感，您也應該針對每個參數支援盡可能廣泛的範圍，並至少涵蓋最大可能範圍的50%。 例如，如果最大可能的對比範圍是從純灰色到純黑色和白色，且預設值是對應至0.0，則編解碼器所支援的最小範圍是從預設值到低 ( – 1.0) 的預設值與純黑色之間的中間，至少是在高階 (+ 1.0) 的預設值與純黑色和白色之間的中間。


```C++
interface IWICDevelopRaw : IWICBitmapFrameDecode
{
   HRESULT QueryRawCapabilitiesInfo ( WICRawCapabilitiesInfo *pInfo );
   HRESULT LoadParameterSet ( WICRawParameterSet ParameterSet );
   HRESULT GetCurrentParameterSet ( IPropertyBag2 **ppCurrentParameterSet );
   HRESULT SetExposureCompensation ( double ev );
   HRESULT GetExposureCompensation ( double *pEV );
   HRESULT SetWhitePointRGB ( UINT Red, UINT Green, UINT Blue );
   HRESULT GetWhitePointRGB ( UINT *pRed, UINT *pGreen, UINT *pBlue );
   HRESULT SetNamedWhitePoint ( WICNamedWhitePoint WhitePoint );
   HRESULT GetNamedWhitePoint ( WICNamedWhitePoint *pWhitePoint );
   HRESULT SetWhitePointKelvin ( UINT WhitePointKelvin );
   HRESULT GetWhitePointKelvin ( UINT *pWhitePointKelvin );
   HRESULT GetKelvinRangeInfo ( UINT *pMinKelvinTemp,
               UINT *pMaxKelvinTemp,
               UINT *pKelvinTempStepValue );
   HRESULT SetContrast ( double Contrast );
   HRESULT GetContrast ( double *pContrast );
   HRESULT SetGamma ( double Gamma );
   HRESULT GetGamma ( double *pGamma );
   HRESULT SetSharpness ( double Sharpness );
   HRESULT GetSharpness ( double *pSharpness );
   HRESULT SetSaturation ( double Saturation );
   HRESULT GetSaturation ( double *pSaturation );
   HRESULT SetTint ( double Tint );
   HRESULT GetTint ( double *pTint );
   HRESULT SetNoiseReduction ( double NoiseReduction );
   HRESULT GetNoiseReduction ( double *pNoiseReduction );
   HRESULT SetDestinationColorContext (const IWICColorContext *pColorContext );
   HRESULT SetToneCurve ( UINT cbToneCurveSize,
               const WICRawToneCurve *pToneCurve );
   HRESULT GetToneCurve ( UINT cbToneCurveBufferSize,
               WICRawToneCurve *pToneCurve,
               UINT *pcbActualToneCurveBufferSize );
   HRESULT SetRotation ( double Rotation );
   HRESULT GetRotation ( double *pRotation );
   HRESULT SetRenderMode ( WICRawRenderMode RenderMode );
   HRESULT GetRenderMode ( WICRawRenderMode *pRenderMode ); 
   HRESULT SetNotificationCallback ( IWICDevelopRawNotificationCallback 
               *pCallback );
}
```



-   [QueryRawCapabilitiesInfo](#queryrawcapabilitiesinfo)
-   [LoadParameterSet](#loadparameterset)
-   [GetCurrentParameterSet](#getcurrentparameterset)
-   [Set/GetExposureCompensation](#setgetexposurecompensation)
-   [Set/GetCurrentParameterRGB、Set/GetNamedWhitePoint、Set/GetwhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/GetContrast](#setgetcontrast)
-   [Set/GetGamma](#setgetgamma)
-   [Set/GetSharpness](#setgetsharpness)
-   [Set/GetSaturation](#setgetsaturation)
-   [Set/GetTint](#setgettint)
-   [Set/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorCoNtext](#setdestinationcolorcontext)
-   [Set/GetToneCurve](#setgettonecurve)
-   [Set/GetRotation](#setgetrotation)
-   [Set/GetRenderMode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>QueryRawCapabilitiesInfo

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) 會傳回這個原始檔案的一組支援功能。 [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo)結構的定義如下：


```C++
struct WICRawCapabilitiesInfo
{
   UINT cbSize;
   UINT CodecMajorVersion;
   UINT CodecMinorVersion;
   WICRawCapabilities ExposureCompensationSupport;
   WICRawCapabilities ContrastSupport;
   WICRawCapabilities RGBWhitePointSupport;
   WICRawCapabilities NamedWhitePointSupport;
   UINT NamedWhitePointSupportMask;
   WICRawCapabilities KelvinWhitePointSupport;
   WICRawCapabilities GammaSupport;
   WICRawCapabilities TintSupport;
   WICRawCapabilities SaturationSupport;
   WICRawCapabilities SharpnessSupport;
   WICRawCapabilities NoiseReductionSupport;
   WICRawCapabilities DestinationColorProfileSupport;
   WICRawCapabilities ToneCurveSupport;
   WICRawRotationCapabilities RotationSupport;              
}
```



此結構中所使用的 [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) 列舉定義如下：


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



最後一個欄位是 [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) 列舉，定義為：


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a>LoadParameterSet

[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) 可讓使用者指定是否要使用 [進行中] 設定、使用使用者調整的設定，或要求解碼器自動校正影像。


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) 會傳回具有目前參數集的 **IPropertyBag2** 。 然後，呼叫端可以將此參數集傳遞給編碼器，以做為編碼器選項使用。

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) 和 [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) 指出要套用至最終輸出的曝光補償。 EV 的有效範圍是–5.0 到 + 5.0 停止。

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB、Set/GetNamedWhitePoint、Set/GetwhitePointKelvin

這些函式全都提供取得和設定白色點的方式，可為 RGB 值、預設的名稱值或為開氏值。 可接受的開氏範圍是1500–30000。

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) 和 [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) 指出要套用至輸出的對比量。 指定對比度的有效範圍是–1.0 到 + 1.0，預設對比為0.0。

### <a name="setgetgamma"></a>Set/GetGamma

[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) 和 [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) 指出要套用的 Gamma。 Gamma 的有效範圍是0.2 到5.0，而1.0 是預設值。 Gamma 通常是使用傳統 Gamma power 函式來執行， (具有 unity 增益) 的線性強大功能。 亮度會隨著 gamma 的遞增而增加，並減少為 Gamma 方法零。  (請注意，最小值為非零，因為在傳統 Gamma 計算中，零會導致零除的錯誤。 邏輯最小限制為 1/最大值，這是最小值為0.2 的原因。 ) 

### <a name="setgetsharpness"></a>Set/GetSharpness

[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) 和 [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) 指出要套用的銳化量。 有效範圍是–1.0 到 + 1.0，0.0 是預設的銳化量，而–1.0 表示完全沒有任何銳化。

### <a name="setgetsaturation"></a>Set/GetSaturation

[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) 和 [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) 指出要套用的飽和度量。 指定飽和度的有效範圍為–1.0 到 + 1.0、0.0 為一般飽和度、-1.0 代表完整 desaturation，而 + 1.0 代表完整的飽和度。

### <a name="setgettint"></a>Set/GetTint

[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) 和 [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) 指出要套用的色調（以綠色/洋紅偏差為依據）。 有效範圍是–1.0 到 + 1.0，綠色位於尺規的負角，而紅色則為正數。 色調尺規會定義為與彩色溫度的正向。

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) 和 [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) 指出減少要套用的雜訊量。 有效範圍為–1.0 到 + 1.0，0.0 指出預設的雜訊減少量，-1.0 表示無雜訊降低，而 + 1.0 表示減少雜訊上限。

### <a name="setdestinationcolorcontext"></a>SetDestinationColorCoNtext

[**SetDestinationColorCoNtext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) 指定要套用至映射的色彩設定檔。 您可以呼叫 [**GetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) 來取出目前的色彩設定檔。

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) 和 [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) 指定要套用的音調曲線。 假設點之間的線性插補。 **PToneCurve** 是 [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve)結構，其中包含 [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint)結構的陣列，以及陣列中的點數目計數。


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



[**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint)包含輸入值和輸出值。


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



當呼叫端在 *pToneCurve* 參數中傳遞 **Null** 時，您應該在 *pcbActualToneCurveBufferSize* 參數中傳回 [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve)的必要大小。

### <a name="setgetrotation"></a>Set/GetRotation

[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) 和 [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) 指出要套用的旋轉程度。 旋轉90.0 會順時針指定90度的旋轉。  (使用 **SetRotation** 與使用 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 方法設定旋轉之間的差異在於，使用 **SetRotation** 所設定的旋轉角度應該由編解碼器保存，而透過 **CopyPixels** 設定旋轉只會在記憶體中旋轉影像。

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) 和 [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) 指出呼叫端需要的輸出品質層級。 當使用者調整參數時，如果套用變更，應用程式應該會顯示實際影像看起來非常快速的近似值。 基於這個目的，影像通常會顯示在螢幕解析度或較小的位置，而不是實際的影像解析度，以提供立即的意見反應給使用者。 這是因為應用程式會要求草稿模式品質，因此這應該非常快速。 當使用者進行所有變更時，在草稿模式中進行預覽，並決定使用目前的設定來解碼完整影像，應用程式會要求最佳品質的解碼。 這通常也會要求列印。 如果需要在速度之間進行合理的取捨，則應用程式會要求正常品質。


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

當任何原始處理參數變更時， [**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback)會為要呼叫的解碼器註冊回呼函數。 [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)的簽章只有一個方法，稱為「[**通知**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify)」。 **Notify** 具有單一參數，這是一個遮罩，指出哪些原始處理參數已變更。


```C++
HRESULT Notify ( UINT NotificationMask );
```



在 NotificationMask 的下列值上，會執行或運算。


```C++
WICRawChangeNotification_ExposureCompensation
WICRawChangeNotification_NamedWhitePoint
WICRawChangeNotification_KelvinWhitePoint
WICRawChangeNotification_RGBWhitePoint
WICRawChangeNotification_Contrast
WICRawChangeNotification_Gamma
WICRawChangeNotification_Sharpness
WICRawChangeNotification_Saturation
WICRawChangeNotification_Tint
WICRawChangeNotification_NoiseReduction
WICRawChangeNotification_DestinationColorContext
WICRawChangeNotification_ToneCurve
WICRawChangeNotification_Rotation
WICRawChangeNotification_RenderMode
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

**概念**
</dt> <dt>

[執行 IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[執行 WIC-Enabled 編碼器](-wic-implementingwicencoder.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



