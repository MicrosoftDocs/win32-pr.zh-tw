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
# <a name="implementing-iwicdevelopraw"></a><span data-ttu-id="0fe89-103">執行 IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="0fe89-103">Implementing IWICDevelopRaw</span></span>

## <a name="iwicdevelopraw"></a><span data-ttu-id="0fe89-104">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="0fe89-104">IWICDevelopRaw</span></span>

<span data-ttu-id="0fe89-105">[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)介面會公開原始影像處理的特定處理選項。</span><span class="sxs-lookup"><span data-stu-id="0fe89-105">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface exposes processing options specific to raw image processing.</span></span> <span data-ttu-id="0fe89-106">所有原始編解碼器都必須支援 **IWICDevelopRaw** 介面。</span><span class="sxs-lookup"><span data-stu-id="0fe89-106">All raw codecs must support the **IWICDevelopRaw** interface.</span></span> <span data-ttu-id="0fe89-107">某些原始編解碼器可能無法支援此介面公開的每個設定，但您應該支援您的編解碼器能夠執行的所有設定。</span><span class="sxs-lookup"><span data-stu-id="0fe89-107">Some raw codecs may not be able to support every setting exposed by this interface, but you should support all the settings that your codec is capable of performing.</span></span> <span data-ttu-id="0fe89-108">每個原始編解碼器至少都必須執行 [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) 和 [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) 方法。</span><span class="sxs-lookup"><span data-stu-id="0fe89-108">At minimum, every raw codec must implement the [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) methods.</span></span>

<span data-ttu-id="0fe89-109">此外，針對原始編解碼器，強烈建議您針對其他編解碼器選用一些方法和介面。</span><span class="sxs-lookup"><span data-stu-id="0fe89-109">Additionally, some methods and interfaces that are optional for other codecs are strongly recommended for raw codecs.</span></span> <span data-ttu-id="0fe89-110">這些包括容器層級的解碼器類別上的 [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) 和 [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) 方法，以及框架層級解碼類別上的 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 介面。</span><span class="sxs-lookup"><span data-stu-id="0fe89-110">These include the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) and [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) methods on the container-level decoder class, and the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface on the frame-level decode class.</span></span>

<span data-ttu-id="0fe89-111">使用 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 方法設定的設定應該以與其他中繼資料保存方式一致的方式保存，而您永遠不應該覆寫原始的「以快照」設定。</span><span class="sxs-lookup"><span data-stu-id="0fe89-111">Settings set by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) methods should be persisted by the codec in a way that’s consistent with the way other metadata is persisted, but you should never overwrite the original "As Shot" settings.</span></span> <span data-ttu-id="0fe89-112">藉由保存中繼資料並執行 [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) 和 [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)，您可以啟用原始處理應用程式，以抓取並套用跨會話的處理設定。</span><span class="sxs-lookup"><span data-stu-id="0fe89-112">By persisting the metadata and implementing [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) and [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), you enable raw processing applications to retrieve and apply processing settings across sessions.</span></span>

<span data-ttu-id="0fe89-113">[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)介面的主要目的是讓應用程式開發人員建立使用者介面，以調整可在不同編解碼器之間盡可能一致運作的原始參數。</span><span class="sxs-lookup"><span data-stu-id="0fe89-113">A main purpose of the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface is to enable application developers to build a user interface for adjusting raw parameters that will work as consistently as possible across different codecs.</span></span> <span data-ttu-id="0fe89-114">假設終端使用者將使用滑杆控制項來調整參數，其最小值和最大值會對應至參數的最小和最大範圍。</span><span class="sxs-lookup"><span data-stu-id="0fe89-114">Assume that an end user will adjust the parameters by using a slider control, with its minimum and maximum values mapped to the minimum and maximum ranges for the parameter.</span></span> <span data-ttu-id="0fe89-115">為了支援這種情況，您應該盡全力將所有參數範圍視為線性。</span><span class="sxs-lookup"><span data-stu-id="0fe89-115">To support this, you should make every effort to treat all parameter ranges as linear.</span></span> <span data-ttu-id="0fe89-116">為了確保滑杆控制項不會過於敏感，您也應該針對每個參數支援盡可能廣泛的範圍，並至少涵蓋最大可能範圍的50%。</span><span class="sxs-lookup"><span data-stu-id="0fe89-116">To ensure that the slider controls aren’t overly sensitive, you should also support as broad a range as possible for each parameter, covering at least 50 percent of the maximum possible range.</span></span> <span data-ttu-id="0fe89-117">例如，如果最大可能的對比範圍是從純灰色到純黑色和白色，且預設值是對應至0.0，則編解碼器所支援的最小範圍是從預設值到低 ( – 1.0) 的預設值與純黑色之間的中間，至少是在高階 (+ 1.0) 的預設值與純黑色和白色之間的中間。</span><span class="sxs-lookup"><span data-stu-id="0fe89-117">For example, if the maximum possible range of contrast is from pure gray to pure black and white, with the default value being mapped to 0.0, the minimum range supported by a codec would be from at least halfway between the default value and pure gray on the low end (–1.0), to at least halfway between the default value and pure black and white on the high end (+1.0).</span></span>


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



-   [<span data-ttu-id="0fe89-118">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="0fe89-118">QueryRawCapabilitiesInfo</span></span>](#queryrawcapabilitiesinfo)
-   [<span data-ttu-id="0fe89-119">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe89-119">LoadParameterSet</span></span>](#loadparameterset)
-   [<span data-ttu-id="0fe89-120">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe89-120">GetCurrentParameterSet</span></span>](#getcurrentparameterset)
-   [<span data-ttu-id="0fe89-121">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="0fe89-121">Set/GetExposureCompensation</span></span>](#setgetexposurecompensation)
-   [<span data-ttu-id="0fe89-122">Set/GetCurrentParameterRGB、Set/GetNamedWhitePoint、Set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="0fe89-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [<span data-ttu-id="0fe89-123">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="0fe89-123">Set/GetContrast</span></span>](#setgetcontrast)
-   [<span data-ttu-id="0fe89-124">Set/GetGamma</span><span class="sxs-lookup"><span data-stu-id="0fe89-124">Set/GetGamma</span></span>](#setgetgamma)
-   [<span data-ttu-id="0fe89-125">Set/GetSharpness</span><span class="sxs-lookup"><span data-stu-id="0fe89-125">Set/GetSharpness</span></span>](#setgetsharpness)
-   [<span data-ttu-id="0fe89-126">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="0fe89-126">Set/GetSaturation</span></span>](#setgetsaturation)
-   [<span data-ttu-id="0fe89-127">Set/GetTint</span><span class="sxs-lookup"><span data-stu-id="0fe89-127">Set/GetTint</span></span>](#setgettint)
-   [<span data-ttu-id="0fe89-128">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="0fe89-128">Set/GetNoiseReduction</span></span>](#setgetnoisereduction)
-   [<span data-ttu-id="0fe89-129">SetDestinationColorCoNtext</span><span class="sxs-lookup"><span data-stu-id="0fe89-129">SetDestinationColorContext</span></span>](#setdestinationcolorcontext)
-   [<span data-ttu-id="0fe89-130">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="0fe89-130">Set/GetToneCurve</span></span>](#setgettonecurve)
-   [<span data-ttu-id="0fe89-131">Set/GetRotation</span><span class="sxs-lookup"><span data-stu-id="0fe89-131">Set/GetRotation</span></span>](#setgetrotation)
-   [<span data-ttu-id="0fe89-132">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="0fe89-132">Set/GetRenderMode</span></span>](#setgetrendermode)
-   [<span data-ttu-id="0fe89-133">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="0fe89-133">SetNotificationCallback</span></span>](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a><span data-ttu-id="0fe89-134">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="0fe89-134">QueryRawCapabilitiesInfo</span></span>

<span data-ttu-id="0fe89-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) 會傳回這個原始檔案的一組支援功能。</span><span class="sxs-lookup"><span data-stu-id="0fe89-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) returns the set of supported capabilities for this raw file.</span></span> <span data-ttu-id="0fe89-136">[**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo)結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="0fe89-136">The [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) structure is defined as follows:</span></span>


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



<span data-ttu-id="0fe89-137">此結構中所使用的 [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) 列舉定義如下：</span><span class="sxs-lookup"><span data-stu-id="0fe89-137">The [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) enumeration used in this structure is defined as:</span></span>


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



<span data-ttu-id="0fe89-138">最後一個欄位是 [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) 列舉，定義為：</span><span class="sxs-lookup"><span data-stu-id="0fe89-138">The final field is a [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) enumeration, defined as:</span></span>


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a><span data-ttu-id="0fe89-139">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe89-139">LoadParameterSet</span></span>

<span data-ttu-id="0fe89-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) 可讓使用者指定是否要使用 [進行中] 設定、使用使用者調整的設定，或要求解碼器自動校正影像。</span><span class="sxs-lookup"><span data-stu-id="0fe89-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) enables the user to specify whether to use As Shot settings, use user-adjusted settings, or request the decoder to auto-correct the image.</span></span>


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a><span data-ttu-id="0fe89-141">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe89-141">GetCurrentParameterSet</span></span>

<span data-ttu-id="0fe89-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) 會傳回具有目前參數集的 **IPropertyBag2** 。</span><span class="sxs-lookup"><span data-stu-id="0fe89-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) returns an **IPropertyBag2** with the current parameter set.</span></span> <span data-ttu-id="0fe89-143">然後，呼叫端可以將此參數集傳遞給編碼器，以做為編碼器選項使用。</span><span class="sxs-lookup"><span data-stu-id="0fe89-143">The caller can then pass this parameter set to the encoder to use as the encoder options.</span></span>

### <a name="setgetexposurecompensation"></a><span data-ttu-id="0fe89-144">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="0fe89-144">Set/GetExposureCompensation</span></span>

<span data-ttu-id="0fe89-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) 和 [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) 指出要套用至最終輸出的曝光補償。</span><span class="sxs-lookup"><span data-stu-id="0fe89-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) and [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicate the exposure compensation to apply to the final output.</span></span> <span data-ttu-id="0fe89-146">EV 的有效範圍是–5.0 到 + 5.0 停止。</span><span class="sxs-lookup"><span data-stu-id="0fe89-146">The valid range for EV is –5.0 to +5.0 stops.</span></span>

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a><span data-ttu-id="0fe89-147">Set/GetCurrentParameterRGB、Set/GetNamedWhitePoint、Set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="0fe89-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>

<span data-ttu-id="0fe89-148">這些函式全都提供取得和設定白色點的方式，可為 RGB 值、預設的名稱值或為開氏值。</span><span class="sxs-lookup"><span data-stu-id="0fe89-148">These functions all provide ways to get and set the white point, either as an RGB value, a preset named value, or as a Kelvin value.</span></span> <span data-ttu-id="0fe89-149">可接受的開氏範圍是1500–30000。</span><span class="sxs-lookup"><span data-stu-id="0fe89-149">The acceptable range for Kelvin is 1,500 – 30,000.</span></span>

### <a name="setgetcontrast"></a><span data-ttu-id="0fe89-150">Set/GetContrast</span><span class="sxs-lookup"><span data-stu-id="0fe89-150">Set/GetContrast</span></span>

<span data-ttu-id="0fe89-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) 和 [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) 指出要套用至輸出的對比量。</span><span class="sxs-lookup"><span data-stu-id="0fe89-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) and [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicate the amount of contrast to apply to the output.</span></span> <span data-ttu-id="0fe89-152">指定對比度的有效範圍是–1.0 到 + 1.0，預設對比為0.0。</span><span class="sxs-lookup"><span data-stu-id="0fe89-152">The valid range to specify contrast is –1.0 to +1.0, with the default contrast being 0.0.</span></span>

### <a name="setgetgamma"></a><span data-ttu-id="0fe89-153">Set/GetGamma</span><span class="sxs-lookup"><span data-stu-id="0fe89-153">Set/GetGamma</span></span>

<span data-ttu-id="0fe89-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) 和 [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) 指出要套用的 Gamma。</span><span class="sxs-lookup"><span data-stu-id="0fe89-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) and [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicate the Gamma to apply.</span></span> <span data-ttu-id="0fe89-155">Gamma 的有效範圍是0.2 到5.0，而1.0 是預設值。</span><span class="sxs-lookup"><span data-stu-id="0fe89-155">The valid range for Gamma is 0.2 to 5.0, with 1.0 being the default.</span></span> <span data-ttu-id="0fe89-156">Gamma 通常是使用傳統 Gamma power 函式來執行， (具有 unity 增益) 的線性強大功能。</span><span class="sxs-lookup"><span data-stu-id="0fe89-156">Gamma typically is implemented using the traditional Gamma power function (a linear power function with unity gain).</span></span> <span data-ttu-id="0fe89-157">亮度會隨著 gamma 的遞增而增加，並減少為 Gamma 方法零。</span><span class="sxs-lookup"><span data-stu-id="0fe89-157">Brightness is increased with increasing Gamma and decreased as Gamma approaches zero.</span></span> <span data-ttu-id="0fe89-158"> (請注意，最小值為非零，因為在傳統 Gamma 計算中，零會導致零除的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0fe89-158">(Note that the minimum value is non-zero, because zero would result in a divide-by-zero error in traditional Gamma calculations.</span></span> <span data-ttu-id="0fe89-159">邏輯最小限制為 1/最大值，這是最小值為0.2 的原因。 ) </span><span class="sxs-lookup"><span data-stu-id="0fe89-159">The logical minimum limit is 1/max, which is why the minimum is 0.2.)</span></span>

### <a name="setgetsharpness"></a><span data-ttu-id="0fe89-160">Set/GetSharpness</span><span class="sxs-lookup"><span data-stu-id="0fe89-160">Set/GetSharpness</span></span>

<span data-ttu-id="0fe89-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) 和 [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) 指出要套用的銳化量。</span><span class="sxs-lookup"><span data-stu-id="0fe89-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) and [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicate the amount of sharpening to apply.</span></span> <span data-ttu-id="0fe89-162">有效範圍是–1.0 到 + 1.0，0.0 是預設的銳化量，而–1.0 表示完全沒有任何銳化。</span><span class="sxs-lookup"><span data-stu-id="0fe89-162">The valid range is –1.0 to +1.0, with 0.0 being the default amount of sharpening, and –1.0 indicating no sharpening at all.</span></span>

### <a name="setgetsaturation"></a><span data-ttu-id="0fe89-163">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="0fe89-163">Set/GetSaturation</span></span>

<span data-ttu-id="0fe89-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) 和 [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) 指出要套用的飽和度量。</span><span class="sxs-lookup"><span data-stu-id="0fe89-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) and [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicate the amount of saturation to apply.</span></span> <span data-ttu-id="0fe89-165">指定飽和度的有效範圍為–1.0 到 + 1.0、0.0 為一般飽和度、-1.0 代表完整 desaturation，而 + 1.0 代表完整的飽和度。</span><span class="sxs-lookup"><span data-stu-id="0fe89-165">The valid range to specify saturation is –1.0 to +1.0, with 0.0 being normal saturation, –1.0 representing complete desaturation, and +1.0 representing full saturation.</span></span>

### <a name="setgettint"></a><span data-ttu-id="0fe89-166">Set/GetTint</span><span class="sxs-lookup"><span data-stu-id="0fe89-166">Set/GetTint</span></span>

<span data-ttu-id="0fe89-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) 和 [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) 指出要套用的色調（以綠色/洋紅偏差為依據）。</span><span class="sxs-lookup"><span data-stu-id="0fe89-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) and [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicate the tint to apply, on a green/magenta bias.</span></span> <span data-ttu-id="0fe89-168">有效範圍是–1.0 到 + 1.0，綠色位於尺規的負角，而紅色則為正數。</span><span class="sxs-lookup"><span data-stu-id="0fe89-168">The valid range is –1.0 to +1.0, with green being on the negative side of the scale and magenta on the positive.</span></span> <span data-ttu-id="0fe89-169">色調尺規會定義為與彩色溫度的正向。</span><span class="sxs-lookup"><span data-stu-id="0fe89-169">The tint scale is defined as orthogonal to color temperature.</span></span>

### <a name="setgetnoisereduction"></a><span data-ttu-id="0fe89-170">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="0fe89-170">Set/GetNoiseReduction</span></span>

<span data-ttu-id="0fe89-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) 和 [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) 指出減少要套用的雜訊量。</span><span class="sxs-lookup"><span data-stu-id="0fe89-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) and [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicate the amount of noise reduction to apply.</span></span> <span data-ttu-id="0fe89-172">有效範圍為–1.0 到 + 1.0，0.0 指出預設的雜訊減少量，-1.0 表示無雜訊降低，而 + 1.0 表示減少雜訊上限。</span><span class="sxs-lookup"><span data-stu-id="0fe89-172">The valid range to is –1.0 to +1.0, with 0.0 indicating the default amount of noise reduction, –1.0 indicating no noise reduction and +1.0 indicating maximum noise reduction.</span></span>

### <a name="setdestinationcolorcontext"></a><span data-ttu-id="0fe89-173">SetDestinationColorCoNtext</span><span class="sxs-lookup"><span data-stu-id="0fe89-173">SetDestinationColorContext</span></span>

<span data-ttu-id="0fe89-174">[**SetDestinationColorCoNtext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) 指定要套用至映射的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="0fe89-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifies the color profile to apply to the image.</span></span> <span data-ttu-id="0fe89-175">您可以呼叫 [**GetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) 來取出目前的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="0fe89-175">You can call [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) to retrieve the current color profile.</span></span>

### <a name="setgettonecurve"></a><span data-ttu-id="0fe89-176">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="0fe89-176">Set/GetToneCurve</span></span>

<span data-ttu-id="0fe89-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) 和 [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) 指定要套用的音調曲線。</span><span class="sxs-lookup"><span data-stu-id="0fe89-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) and [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specify the tone curve to apply.</span></span> <span data-ttu-id="0fe89-178">假設點之間的線性插補。</span><span class="sxs-lookup"><span data-stu-id="0fe89-178">Assume linear interpolation between points.</span></span> <span data-ttu-id="0fe89-179">**PToneCurve** 是 [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve)結構，其中包含 [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint)結構的陣列，以及陣列中的點數目計數。</span><span class="sxs-lookup"><span data-stu-id="0fe89-179">The **pToneCurve** is a [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) structure, which contains an array of [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) structures, and a count of the number of points in the array.</span></span>


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



<span data-ttu-id="0fe89-180">[**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint)包含輸入值和輸出值。</span><span class="sxs-lookup"><span data-stu-id="0fe89-180">A [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contains an input value and an output value.</span></span>


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



<span data-ttu-id="0fe89-181">當呼叫端在 *pToneCurve* 參數中傳遞 **Null** 時，您應該在 *pcbActualToneCurveBufferSize* 參數中傳回 [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve)的必要大小。</span><span class="sxs-lookup"><span data-stu-id="0fe89-181">When the caller passes **NULL** in the *pToneCurve* parameter, you should pass back the required size for the [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) in the *pcbActualToneCurveBufferSize* parameter.</span></span>

### <a name="setgetrotation"></a><span data-ttu-id="0fe89-182">Set/GetRotation</span><span class="sxs-lookup"><span data-stu-id="0fe89-182">Set/GetRotation</span></span>

<span data-ttu-id="0fe89-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) 和 [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) 指出要套用的旋轉程度。</span><span class="sxs-lookup"><span data-stu-id="0fe89-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) and [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicate the degree of rotation to apply.</span></span> <span data-ttu-id="0fe89-184">旋轉90.0 會順時針指定90度的旋轉。</span><span class="sxs-lookup"><span data-stu-id="0fe89-184">A rotation of 90.0 would specify a rotation of 90 degrees clockwise.</span></span> <span data-ttu-id="0fe89-185"> (使用 **SetRotation** 與使用 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 方法設定旋轉之間的差異在於，使用 **SetRotation** 所設定的旋轉角度應該由編解碼器保存，而透過 **CopyPixels** 設定旋轉只會在記憶體中旋轉影像。</span><span class="sxs-lookup"><span data-stu-id="0fe89-185">(The difference between using **SetRotation** and setting rotation using the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method is that the rotation angle set using **SetRotation** should be persisted by the codec, while setting rotation through **CopyPixels** only rotates the image in memory.</span></span>

### <a name="setgetrendermode"></a><span data-ttu-id="0fe89-186">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="0fe89-186">Set/GetRenderMode</span></span>

<span data-ttu-id="0fe89-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) 和 [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) 指出呼叫端需要的輸出品質層級。</span><span class="sxs-lookup"><span data-stu-id="0fe89-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicate the quality level of output the caller requires.</span></span> <span data-ttu-id="0fe89-188">當使用者調整參數時，如果套用變更，應用程式應該會顯示實際影像看起來非常快速的近似值。</span><span class="sxs-lookup"><span data-stu-id="0fe89-188">When a user is adjusting parameters, the application should display a very fast approximation of what the actual image will look like if the changes are applied.</span></span> <span data-ttu-id="0fe89-189">基於這個目的，影像通常會顯示在螢幕解析度或較小的位置，而不是實際的影像解析度，以提供立即的意見反應給使用者。</span><span class="sxs-lookup"><span data-stu-id="0fe89-189">For this purpose, the image is usually displayed at screen resolution or less, rather than the actual image resolution, to provide immediate feedback to the user.</span></span> <span data-ttu-id="0fe89-190">這是因為應用程式會要求草稿模式品質，因此這應該非常快速。</span><span class="sxs-lookup"><span data-stu-id="0fe89-190">This is when an application would request Draft Mode quality, so this should be very fast.</span></span> <span data-ttu-id="0fe89-191">當使用者進行所有變更時，在草稿模式中進行預覽，並決定使用目前的設定來解碼完整影像，應用程式會要求最佳品質的解碼。</span><span class="sxs-lookup"><span data-stu-id="0fe89-191">When the user has made all changes, previewed them in draft mode, and decided to decode the full image with the current settings, the application requests a Best Quality decode.</span></span> <span data-ttu-id="0fe89-192">這通常也會要求列印。</span><span class="sxs-lookup"><span data-stu-id="0fe89-192">This is usually also requested for printing.</span></span> <span data-ttu-id="0fe89-193">如果需要在速度之間進行合理的取捨，則應用程式會要求正常品質。</span><span class="sxs-lookup"><span data-stu-id="0fe89-193">Where a reasonable tradeoff between speed an quality is required, the application requests Normal Quality.</span></span>


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a><span data-ttu-id="0fe89-194">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="0fe89-194">SetNotificationCallback</span></span>

<span data-ttu-id="0fe89-195">當任何原始處理參數變更時， [**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback)會為要呼叫的解碼器註冊回呼函數。</span><span class="sxs-lookup"><span data-stu-id="0fe89-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registers a callback function for the decoder to call when any of the Raw processing parameters change.</span></span> <span data-ttu-id="0fe89-196">[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)的簽章只有一個方法，稱為「[**通知**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify)」。</span><span class="sxs-lookup"><span data-stu-id="0fe89-196">The signature for the [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) has only one method, called [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span></span> <span data-ttu-id="0fe89-197">**Notify** 具有單一參數，這是一個遮罩，指出哪些原始處理參數已變更。</span><span class="sxs-lookup"><span data-stu-id="0fe89-197">**Notify** has a single parameter, which is a mask that indicates which of the raw processing parameters have changed.</span></span>


```C++
HRESULT Notify ( UINT NotificationMask );
```



<span data-ttu-id="0fe89-198">在 NotificationMask 的下列值上，會執行或運算。</span><span class="sxs-lookup"><span data-stu-id="0fe89-198">An OR operation is performed on the following values for the NotificationMask.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0fe89-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="0fe89-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0fe89-200">**參考**</span><span class="sxs-lookup"><span data-stu-id="0fe89-200">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0fe89-201">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="0fe89-201">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

<span data-ttu-id="0fe89-202">**概念**</span><span class="sxs-lookup"><span data-stu-id="0fe89-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0fe89-203">執行 IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="0fe89-203">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="0fe89-204">執行 WIC-Enabled 編碼器</span><span class="sxs-lookup"><span data-stu-id="0fe89-204">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="0fe89-205">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="0fe89-205">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="0fe89-206">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="0fe89-206">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



