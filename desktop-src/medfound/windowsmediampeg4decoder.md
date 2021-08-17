---
description: Windows Media MPEG4 V1/v2 解碼器會解碼 MPEG4 V1/v2 影片串流。
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: 'WindowsMedia MPEG4 V1/V2 解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c55d5c64cec2a0ad08978064d40c26267d7729adeee9a9f148c8e682ba168509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100930"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>WindowsMedia MPEG4 V1/V2 解碼器

Windows Media MPEG4 V1/v2 解碼器會解碼 MPEG4 V1/v2 影片串流。

## <a name="class-identifier"></a>類別識別碼

Windows Media MPEG4 V1/V2 解碼器 (clsid) 的類別識別碼是以常數 **CLSID \_ CMpeg4DecMediaObject** 表示。 您可以藉由呼叫 **CoCreateInstance** 來建立 MPEG4 V1/V2 解碼器的實例。

## <a name="formats"></a>格式

Windows Media MPEG4 V1/V2 解碼器支援下列輸入媒體類型。

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ mpg4
-   MEDIASUBTYPE \_ MP42
-   MEDIASUBTYPE \_ mp42

當 Windows Media MPEG4 V1/V2 解碼器作為 DirectX 媒體物件 (DMO) 時，支援下列輸出媒體子類型。

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

當 Windows Media MPEG4 V1/V2 解碼器作為媒體基礎轉換 (MFT) 時，支援下列輸出媒體子類型。

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>備註

Windows Media MPEG4 V1/V2 解碼器物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)介面，讓物件可以作為 DirectX 媒體物件 (DMO) ，它會公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面，讓物件可以作為媒體基礎轉換 (MFT) 。 物件具有相同的類別識別碼 (CLSID) ，不論它是否作為 DMO 或 MFT。

MPEG4 V1/V2 解碼器會根據您所取得的介面以及正在執行的 Windows 版本，以 DMO 或 MFT 的形式運作。 下表顯示 MPEG4 V1/V2 解碼器作為 DMO 或 MFT 運作的條件。



| 作業系統            | 解碼器行為                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | MPEG4 V1/V2 解碼器一律會以 DMO 的方式運作。                                                                                                                                 |
| WindowsVista 和 Windows 7 | 根據預設，MPEG4 V1/V2 解碼器會以 DMO 的方式運作。 如果您在 MPEG4 V1/V2 解碼器上取得 [影片子類型 guid](video-subtype-guids.md) 介面，它會以 MFT 的形式運作。 |



 

針對 RGB 媒體子類型 (guid) 的全域唯一識別碼，會隨著解碼器是否做為 DMO 或 MFT 而有所不同。 非 RGB 媒體子類型的 guid 是相同的，不論解碼器是否做為 DMO 或 MFT。 如需表示影片子類型之 Guid 的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器物件](codecobjects.md)
</dt> </dl>

 

 
