---
title: WIC 常數、列舉和旗標
description: 本節包含 Windows 影像處理元件 (WIC) 常數、列舉和旗標的相關資訊。
ms.assetid: a3f44919-bd55-48cf-9dc6-37de0059a639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee9718641dd0e0e9159a6da9998e0109e4ec97fa366b1e9cba35f9d5f1065ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549628"
---
# <a name="wic-constants-enumerations-and-flags"></a>WIC 常數、列舉和旗標

本節包含 Windows 影像處理元件 (WIC) 常數、列舉和旗標的相關資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                              | 描述                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WIC Guid 和 Clsid](-wic-guids-clsids.md)<br/>                                                           |                                                                                                                                                                 |
| [編解碼器錯誤碼](-wic-codec-error-codes.md)<br/>                                                         |                                                                                                                                                                 |
| [原生像素格式](-wic-codec-native-pixel-formats.md)<br/>                                             | 本主題介紹 WIC 提供的像素格式<br/>                                                                                          |
| [**IWICDevelopRawNotificationCallback 常數**](-wic-codec-iwicdeveloprawnotification-constants.md)<br/> | [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)用來指出哪些成員已變更的旗標。<br/> |
| [**IWICJpegFrameDecode 常數**](iwicjpegframedecode-constants.md)<br/>                                  | [**WICJpegScanHeader**](/windows/desktop/api/wincodec/ns-wincodec-wicjpegscanheader)和 [**WICJpegFrameHeader**](/windows/desktop/api/wincodec/ns-wincodec-wicjpegframeheader)所使用的旗標。<br/>                               |
| [**WIC8BIMIptcDigestProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wic8bimiptcdigestproperties)<br/>                           | 在8BIM 的 IPTC 摘要中繼資料區塊中指定中繼資料專案的識別碼。<br/>                                                               |
| [**WIC8BIMIptcProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wic8bimiptcproperties)<br/>                                       | 指定 8BIM IPTC 區塊中中繼資料專案的識別碼。<br/>                                                                               |
| [**WIC8BIMResolutionInfoProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wic8bimresolutioninfoproperties)<br/>                   | 在8BIMResolutionInfo 區塊中指定中繼資料專案的識別碼。<br/>                                                                      |
| [**WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)<br/>                           | 指定所需的 Alpha 通道使用方式。<br/>                                                                                                           |
| [**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)<br/>                             | 指定所需的快取使用量。<br/>                                                                                                                   |
| [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities)<br/>                         | 指定此解碼器的功能。<br/>                                                                                                           |
| [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)<br/>                                           | 指定在影像格式之間轉換時要套用的 [遞色](/windows) 演算法類型。<br/>                                               |
| [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)<br/>                           | 指定適用于編碼器的快取選項。<br/>                                                                                                |
| [**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)<br/>                             | 指定調整影像時要使用的取樣或篩選模式。<br/>                                                                               |
| [**WICBitmapLockFlags**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaplockflags)<br/>                                             | 指定 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)的存取權。<br/>                                                                                  |
| [**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)<br/>                                         | 指定用於索引影像格式的元件類型。<br/>                                                                                      |
| [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)<br/>                               | 指定翻轉和旋轉轉換。<br/>                                                                                                          |
| [**WICColorCoNtextType**](/windows/desktop/api/Wincodec/ne-wincodec-wiccolorcontexttype)<br/>                                           | 指定色彩內容類型。<br/>                                                                                                                   |
| [**WICComponentEnumerateOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions)<br/>                         | 指定元件列舉選項。<br/>                                                                                                             |
| [**WICComponentSigning**](/windows/desktop/api/Wincodec/ne-wincodec-wiccomponentsigning)<br/>                                           | 指定元件簽署狀態。<br/>                                                                                                              |
| [**WICComponentType**](/windows/desktop/api/Wincodec/ne-wincodec-wiccomponenttype)<br/>                                                 | 指定 WIC 元件的類型。<br/>                                                                                                                 |
| [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)<br/>                                                 | 指定解碼選項。<br/>                                                                                                                            |
| [**WICDdsDimension**](/windows/desktop/api/Wincodec/ne-wincodec-wicddsdimension)<br/>                                                              | 指定 DDS 影像中所含資料的維度類型。<br/>                                                                                     |
| [**WICDdsAlphaMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicddsalphamode)<br/>                                                              | 指定 DDS 影像中包含的圖元色彩元件值的意義。<br/>                                                                |
| [**WICGifApplicationExtensionProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicgifapplicationextensionproperties)<br/>         | 指定圖形交換格式 (GIF) 影像的應用程式延伸模組中繼資料屬性。<br/>                                               |
| [**WICGifCommentExtensionProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicgifcommentextensionproperties)<br/>                 | 為 GIF 影像指定批註延伸的中繼資料屬性。<br/>                                                                                 |
| [**WICGifGraphicControlExtensionProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicgifgraphiccontrolextensionproperties)<br/>   | 指定圖形控制項延伸的中繼資料屬性，定義 GIF 影像的每個畫面格動畫之間的轉換。<br/>                 |
| [**WICGifImageDescriptorProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicgifimagedescriptorproperties)<br/>                   | 指定 GIF 框架的影像描述元中繼資料屬性。<br/>                                                                                   |
| [**WICGifLogicalScreenDescriptorProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicgiflogicalscreendescriptorproperties)<br/>   | 指定 GIF 中繼資料的邏輯螢幕描述項屬性。<br/>                                                                                 |
| [**WICJpegCommentProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegcommentproperties)<br/>                                 | 指定 JPEG 批註屬性。<br/>                                                                                                               |
| [**WICJpegChrominanceProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegchrominanceproperties)<br/>                         | 指定 JPEG 色度 table 屬性。<br/>                                                                                                       |
| [**WICJpegIndexingOptions**](/windows/desktop/api/wincodec/ne-wincodec-wicjpegindexingoptions)<br/>                                                | 指定用於建立 JPEG 影像索引的選項。 <br/>                                                                                                    |
| [**WICJpegLuminanceProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegluminanceproperties)<br/>                             | 指定 JPEG 亮度資料表屬性。<br/>                                                                                                         |
| [**WICJpegScanType**](/windows/desktop/api/wincodec/ne-wincodec-wicjpegscantype)<br/>                                                              | 指定 JPEG 影像掃描中圖元資料的記憶體配置。 <br/>                                                                                     |
| [**WICJpegTransferMatrix**](/windows/desktop/api/wincodec/ne-wincodec-wicjpegtransfermatrix)<br/>                                                  | 指定從 Y'Cb'Cr 到 R'G'B 的轉換矩陣。 <br/>                                                                                                |
| [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption)<br/>                       | 指定 JPEG YCrCB 次取樣選項。 <br/>                                                                                                       |
| [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)<br/>                             | 指定中繼資料的建立選項。<br/>                                                                                                                 |
| [**WICNamedWhitePoint**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint)<br/>                                             | 指定原始影像的命名白色餘額。<br/>                                                                                                       |
| [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)<br/>                                               | 指定使用資料流程初始化元件時所使用的 WIC 選項。<br/>                                                                     |
| [**WICPixelFormatNumericRepresentation**](/windows/desktop/api/Wincodec/ne-wincodec-wicpixelformatnumericrepresentation)<br/>           |                                                                                                                                                                 |
| [**WICPlanarOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicplanaroptions)<br/>                                                            | 指定 [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) 執行的其他選項。 <br/>                       |
| [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation)<br/>                                         | 指定要接收通知的進度作業。<br/>                                                                                      |
| [**WICPngBkgdProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngbkgdproperties)<br/>                                         | 指定可移植網狀圖形 (PNG) 背景 (bKGD) 區塊中繼資料屬性。<br/>                                                           |
| [**WICPngChrmProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngchrmproperties)<br/>                                         | 指定 CIE XYZ chromaticity 的 PNG cHRM 區塊中繼資料屬性。<br/>                                                                           |
| [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)<br/>                                             | 指定可用於壓縮優化的 PNG 篩選。<br/>                                                                                    |
| [**WICPngGamaProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicpnggamaproperties)<br/>                                         | 指定 PNG gAMA 區塊中繼資料屬性。<br/>                                                                                                    |
| [**WICPngHistProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicpnghistproperties)<br/>                                         | 指定 PNG >hist 區塊中繼資料屬性。<br/>                                                                                                    |
| [**WICPngIccpProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngiccpproperties)<br/>                                         | 指定 PNG iCCP 區塊中繼資料屬性。<br/>                                                                                                    |
| [**WICPngItxtProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngitxtproperties)<br/>                                         | 指定 PNG iTXT 區塊中繼資料屬性。<br/>                                                                                                    |
| [**WICPngSrgbProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngsrgbproperties)<br/>                                         | 指定 PNG sRGB 區塊中繼資料屬性。<br/>                                                                                                    |
| [**WICPngTimeProperties**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngtimeproperties)<br/>                                         | 指定 PNG 時間區塊中繼資料屬性。<br/>                                                                                                    |
| [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification)<br/>                                   | 指定應呼叫進度通知回呼的時間。<br/>                                                                                  |
| [原生 WIC 編解碼器](native-wic-codecs.md)<br/>                                                              | 本節包含 WIC 中可用之原生映射編解碼器的相關資訊。<br/>                                                                  |
| [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities)<br/>                                             | 指定原始影像的功能支援。<br/>                                                                                                     |
| [**WICRawParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset)<br/>                                             | 指定原始編解碼器所使用的參數集。<br/>                                                                                                     |
| [**WICRawRenderMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode)<br/>                                                 | 指定下一個 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) 呼叫的呈現意圖。 <br/>                                          |
| [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities)<br/>                             | 指定編解碼器的旋轉功能。<br/>                                                                                                    |
| [**WICSectionAccessLevel**](/windows/desktop/api/Wincodec/ne-wincodec-wicsectionaccesslevel)<br/>                                       | 指定 Windows 圖形裝置介面 (GDI) 區段的存取層級。<br/>                                                                     |
| [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)<br/>                                 | 指定標記的影像檔案格式 (TIFF) 壓縮選項。<br/>                                                                                   |



 

 

