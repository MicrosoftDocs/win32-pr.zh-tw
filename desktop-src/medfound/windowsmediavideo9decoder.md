---
description: Windows Media 視訊9解碼器會將 Windows Media 視訊編碼器編碼的影片串流解碼。
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: 'WindowsMedia Video 9 解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df973e78f69e1f1ff0e649b2c4f5637380be9f27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474304"
---
# <a name="windows-media-video-9-decoder"></a>Windows媒體 Video 9 解碼器

Windows Media 視訊9解碼器會將 [**Windows Media 視訊編碼器**](windowsmediavideo9encoder.md)編碼的影片串流解碼。 編碼器和解碼器支援下列四種編碼影片類別。

-   Windows媒體 Video 9 簡單設定檔
-   Windows媒體 Video 9 主要設定檔
-   Windows媒體 Video 9 Advanced Profile
-   WindowsMedia Video 9.1 影像

## <a name="class-identifier"></a>類別識別碼

Windows Media 視訊解碼器 (clsid) 的類別識別碼是以常數 **CLSID \_ CWMVDecMediaObject** 來表示。 您可以藉由呼叫 **CoCreateInstance** 來建立影片解碼的實例。

## <a name="interfaces"></a>介面

影片解碼物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)介面，讓物件可以作為 DirectX 媒體物件 (DMO) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面，以便將物件當做媒體基礎轉換 (MFT) 使用。

根據您取得的介面以及正在執行的 Windows 版本而定，影片解碼會以 DMO 或 MFT 的形式運作。 下表顯示「影片解碼」做為 DMO 或 MFT 運作的條件。



| 作業系統            | 解碼器行為                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Windows 媒體影片解碼一律會以 DMO 的方式運作。                                                                                                                |
| WindowsVista 和 Windows 7 | Windows 媒體影片解碼預設會以 DMO 的形式運作。 如果您在視頻解碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。 |



 

從 Windows 7 開始，Windows Media 視訊解碼器會實行 [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol)介面。

## <a name="input-formats"></a>輸入格式

下表顯示四個字元的代碼 (FOURCCs) ，其對應至 Windows Media 視訊的解碼器所支援的編碼輸入分類。



| 類別                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows媒體 Video 9 簡單設定檔   | "WMV3"                                   |
| Windows媒體 Video 9 主要設定檔     | "WMV3"                                   |
| Windows媒體 Video 9 Advanced Profile | "WVC1"                                   |
| WindowsMedia Video 9.1 影像          | "WMVP" 代表9.1，"WVP2" 代表9.1 第2版 |



 

## <a name="output-formats"></a>輸出格式

當 Windows Media 視訊解碼器作為 DMO 時，支援下列輸出媒體子類型。

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

當 Windows Media 視訊解碼器作為 MFT 時，支援下列輸出媒體子類型。

-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="properties"></a>屬性

Windows Media 視訊的解碼器支援下列屬性。




| 屬性 | 描述 | 
|----------|-------------|
| <a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a> | 指定編解碼器是否將經過壓縮資料流程的交錯式影片框架解碼為漸進式框架。<br /><dl> WindowsXP 和更新版本。<br />簡單設定檔、主要設定檔、Advanced Profile。<br />讀取/寫入<br /></dl> | 
| <a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a> | 指定解碼器是否會使用 DirectX video 加速硬體（如果有的話）。<br /><dl> WindowsXP 和更新版本。<br />簡單設定檔、主要設定檔、Advanced Profile。<br />唯寫。<br /></dl> | 
| <a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a> | 指定此解碼器的電源等級。<br /><dl> Windows 7。<br />簡單設定檔、主要設定檔、Advanced Profile、Image。<br />讀取/寫入<br /></dl> | 
| <a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a> | 指定解碼器是否應使用框架插補。<br /><dl> WindowsXP 和更新版本。<br />簡單設定檔、主要設定檔、Advanced Profile、Image。<br />唯寫。<br /></dl> | 
| <a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a> | 指定此解碼器是否支援框架插補。<br /><dl> WindowsXP 和更新版本。<br />簡單設定檔、主要設定檔、Advanced Profile、Image<br />唯讀。<br /></dl> | 
| <a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a> | 指定此解碼器將使用的執行緒數目。<br /><dl> WindowsVista 和更新版本。<br />簡單設定檔、主要設定檔、Advanced Profile、Image。<br />讀取/寫入<br /></dl> | 
| <a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a> | 指定此解碼器的後置處理模式。<br /><dl> WindowsVista 和更新版本。<br />簡單設定檔、主要設定檔、Advanced Profile、Image。<br />唯寫。<br /></dl> | 
| <strong>g_wszWMVCNeedsDrain</strong> | 指定是否應清空解碼器。<br /><dl> Windows 8<br />唯讀。<br /></dl> Windows 媒體格式執行時間會使用這個屬性。 屬性類型為 <strong>VARIANT_BOOL</strong>。 如果此值為 <strong>VARIANT_TRUE</strong>，則應在不連續的情況下清空此解碼器。 如需有關清空 MFT 的詳細資訊，請參閱 <a href="basic-mft-processing-model.md">基本的 Mft 處理模型</a>。<br /><blockquote>[!Note]<br />若要查詢這個屬性，請使用 <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> 介面。</blockquote><br /> | 




 

## <a name="remarks"></a>備註

Windows Media 視訊9解碼器所允許的最大解析度是4096x4096。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | WindowsXP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[編解碼器實行](codecimplementation.md)
</dt> </dl>

 

 
