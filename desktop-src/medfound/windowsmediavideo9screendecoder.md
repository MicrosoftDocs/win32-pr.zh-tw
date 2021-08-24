---
description: Windows Media 視訊9螢幕編碼程式會將 Windows Media 視訊9螢幕編碼器編碼的資料流程解碼。
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: 'WindowsMedia Video 9 螢幕解碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2e081423c4c5efc2d44fdf78c7c6a94a00dae86d40d761a06ab0de07fa5d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462388"
---
# <a name="windows-media-video-9-screen-decoder"></a>WindowsMedia Video 9 螢幕解碼

Windows Media 視訊9螢幕編碼程式會將 [**Windows Media 視訊9螢幕編碼器**](windowsmediavideo9screenencoder.md)編碼的資料流程解碼。

## <a name="class-identifier"></a>類別識別碼

Windows Media 視訊9螢幕解碼 (clsid) 的類別識別碼是以常數 **CLSID \_ CMSSCDecMediaObject** 表示。 您可以藉由呼叫 **CoCreateInstance** 來建立此解碼器的實例。

## <a name="input-types"></a>輸入類型

適用于 Windows Media 視訊螢幕第9版編碼內容的四個字元的程式碼 (FOURCC) 為 "MSS2"。

第9版螢幕解碼支援下列輸入類型。

-   MEDIASUBTYPE \_ MSS2

## <a name="output-types"></a>輸出型別

當第9版螢幕解碼用作為 DirectX 媒體物件 (DMO) 時，支援下列輸出類型。

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

當第9版的螢幕解碼作為媒體基礎轉換 (MFT) 時，支援下列輸出類型。

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="remarks"></a>備註

螢幕解碼物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)介面，讓物件可以作為 DirectX 媒體物件 (DMO) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面，以便將物件當做媒體基礎轉換 (MFT) 使用。

螢幕解碼會根據您所取得的介面以及正在執行的 Windows 版本，以 DMO 或 MFT 的形式來運作。 下表顯示幕幕解碼器作為 DMO 或 MFT 運作的條件。



| 作業系統            | 解碼器行為                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Windows 媒體畫面的解碼器一律會以 DMO 的方式運作。                                                                                                                 |
| WindowsVista 和 Windows 7 | Windows 媒體螢幕解碼預設會以 DMO 的方式運作。 如果您在螢幕解碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。 |



 

您可以使用相同的 CLSID (CLSID \_ CMSSCDecMediaObject) 來建立第7版的螢幕解碼和第9版的螢幕解碼器。 Windows Media 視訊螢幕第7版編碼內容的 FOURCC 為 "MSS1"。 第7版螢幕解碼支援 MEDIASUBTYPE \_ MSS1 輸入類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | WindowsXP、Windows Vista 或 Windows 7<br/>                                       |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> <dt>

[編解碼器實行](codecimplementation.md)
</dt> <dt>

[使用 Windows Media 視訊9螢幕編解碼器](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[WindowsMedia Video 9 螢幕編碼器](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
